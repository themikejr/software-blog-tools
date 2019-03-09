---
layout: post
title: Linux, Entropy, Random Number Generation, and you
subtitle: "Or 'How I learned to stop worrying and use /dev/urandom'"
layout: post
categories: ["How Things Work"]
description: "Random number generation is important in cryptography. Application developers: make sure you are using a randomness source that provides the needed level of performance."
comments: true
---

Recently while debugging a performance issue with a JRuby application, I learned that the JVM defaults to `/dev/random` as its randomness source. This default resulted in a performance problem in the application. This post will cover the purpose of `/dev/random` and `/dev/urandom` in general, the cause of the performance problem that I experienced, and the solution that I landed on.

## Why Random Number Generation (RNG) is important in computing

In most unix-like operating systems, the files located at the path `/dev/random` and `/dev/urandom` server as random number generators. True randomness is a concept that is very important in computing, especially with regards to cryptography. Cryptography often depends on a key or set of keys that are secret. If an actor was able to identify a pattern used to generate secret keys, they could likely find a way to guess what a secret key is. Inserting *randomness* into the process of generating a secret key makes it harder for an actor to find a pattern in key generation.

Think for a moment about how you might write a program that would generate random values. Perhaps the program could do some math on a seed value that results in integers produced that don't appear to follow any particular pattern. But how does one select a seed? If there is a pattern in the seed used to generate random values then you haven't accomplished much. One might resort to using a date or timestamp and then performing math to generate a seed but in that case the seed could be guessed easily enough.

A source of true randomness would be quite valuable and quite difficult to construe.

## Linux and RNG

To accomplish sufficiently random number generation, the linux operating system keeps an 'entropy pool' which is a collection of random values that one hopes to be unknown by some malevolent actor. The entropy pool then acts as a seed to a process that tries to 'randomly' generate numbers. This results in a stream of random output that is available at `/dev/random` on the filesystem. The entropy pool is populated from a variety of sources like user input activity and other environmental noise that device drivers may observe.

Things get a little complicated when the entropy pool runs low.

When entropy runs low, `/dev/random` stops or blocks. This causes any process requiring data from the random stream to wait until the entropy pool is full enough to continue generating random numbers. There is another randomness stream on most linux system at `/dev/urandom` that does not block when the entropy pool runs low. Choosing not to block when the entropy pool runs low can be considered 'less secure' but one must think about the situations that can cause this to happen and judge accordingly whether or not `/dev/urandom` is safe to use.

## The JVM and /dev/random

By default, many versions of the JVM will default to using `/dev/random`. Depending on the size of your entropy pool and your application's need for random numbers, this can put you in a situation where you are blocked until the entropy pool reaches its required size.

I noticed the performance problem when I modified a JRuby application to use stronger ciphers for TLS. Presumably the strong ciphers required more random input at times and the entropy pool on my servers wasn't always up to the task. After doing some research, (I found [this article](https://www.2uo.de/myths-about-urandom/) to be helpful) I decided to use `/dev/urandom/` for the needs of our application.

## Addendum: Useful commands and config

Here are a few helpful commands and settings related to entropy pools in linux and configuring the JVM accordingly. The commands assume RHEL or another system like it.

- Available entropy: `cat /proc/sys/kernel/random/entropy_avail`
- Does a CPU have a hardware RNG? `cat /proc/cpuinfo | grep -i rdrand | echo $?`
- JVM flag for default randomness source: `-Djava.security.egd=file:/dev/urandom`

---

Have you dealt with problems related to `/dev/random`'s blocking behavior? Did I get something wrong here? Let me know in the comments.

## TL;DR

One-paragraph solution summary.

## Context

You wake up in a dark, damp cell. Your head throbs with pain as memories slowly return...

The last thing you remember is walking through the foggy streets on Halloween night when a monstrous figure attacked you.

Dr. Jekyll's failed experiment, Mr. Hyde, has kidnapped you and thrown you into his cursed castle!

To escape, you must:

Solve three challenging puzzles hidden throughout the castle
Collect three mystical keys through math, cryptography, and esoteric programming
Face Hyde in a final battle of occult knowledge
Can you escape Hyde's Castle before it's too late?

https://raiffeisen-tech.ctfd.io/hyde

## Recon

What you tried first, dead ends, and why.

## Vulnerability / Idea

Root cause and the key insight.

## Exploitation Steps (Reproducible)

A) The Cryptic Manuscript

Alpha: 7x13 = 91
Beta: 1000-666 = 334
Gamma: Difference between two consecutive primes is 2
Delta: 256 - 169 + 6 = 93

"All roads lead to the same number" + "their messages have been scrambled by time" suggests that some on the messages are not correct anymore. The clearest one is Delta's message as it's just a math equation. 
Either using that logic, or brute forcing each of the scholar's answer in, you find out that 93 is the correct answer.

B) The Layered Cipher
Broken - answer was given out "CRYPTIC"

C) The Demonic Script

Using a brainfuck interpreter https://copy.sh/brainfuck/
Script A is "Hello fnehdZ"
Script C is "Hello World!"

Using a befuge compiler on Script B results in "HELLO WORLD"

We know that we're looking for a famous programming phrase "The true script outputs a famous programming phrase"
and
just one of the three scripts is correct "But beware - one script is reversed, another is corrupted"

Script A is the corrupted one.
Script B is initially HELLO WORLD reversed.
Script C is the true one.

After getting past the great hall, answer the questions and get the flag.

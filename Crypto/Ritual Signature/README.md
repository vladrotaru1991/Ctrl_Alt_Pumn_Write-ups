## TL;DR

One-paragraph solution summary.

## Context

The grimoire’s pages are digitally sealed with an old ritual key. The archivist rushed the signing, reusing a fragment of an old exponent — a small one. The seal looks genuine, but the ritual was reckless: shortcuts in the math leave cracks. If you pry one open, the spirit bound inside will be revealed.

Provided files: public.json

Hint 1: The ciphertext was generated using the public key. (raw RSA, no padding)
Hint 2: Check RSA attacks for small private exponents (Wiener).

## Recon

What you tried first, dead ends, and why.

## Vulnerability / Idea

1. "Signing", "Exponent", and in the file the notation n, e, ciphertext all suggest RSA.
2. "rushed the signing, reusing a fragment of an old exponent - a small one" this is the vulnerability and it suggests that wiener's attack will work

## Exploitation Steps (Reproducible)

3. I used a Wiener's attack online tool https://asecuritysite.com/ctf/rsa_ctf05
4. The flag is rtech{THE_RITUALS_HAVE_WEAK_EXPONENTS}

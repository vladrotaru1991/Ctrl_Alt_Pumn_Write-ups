## TL;DR

Base64Decode(Binary to ASCII) -> Profit

## Context

You are met with two guardians. ONE always lies, the other tells the truth. Can you figure out which is which and get the flag?

Provided files: guardians.png

Hint 1: The first digit is misleading

## Recon

The left guardian just tells us the flag. It can't be that easy. Try it anyway
Maybe it's sneaky, make it closer to all previous flags. Try rtech{cake_is_a_lie}
Try both but with cake_is_not_a_lie
But the right guardian's text in a binary to ascii convertor. All good except the first letter. It's a weird symbol
Notice all other values start with 0 so figure that the first one is too high a value for it to be a valid ASCII/UTF character
Replace the first bit with 0.
Decode the result

## Vulnerability / Idea

Left statue is probably lying, so the right one is telling the truth

## Exploitation Steps (Reproducible)

Write out the text of the right statue. Replace the first 1 with a 0. Put this text through a Binary to ASCII/UTF-8 convertor.
Base64 decode the result.
Flag: rtech{guardians}

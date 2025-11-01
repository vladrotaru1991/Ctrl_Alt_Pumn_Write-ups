## TL;DR

Decode -> Reverse -> Profit

## Context

You find yourself trapped inside a mysterious mansion on Halloween night. You discover an exit, but it's locked with an ancient cipher mechanism. While wandering these dark halls, you notice three cryptic messages carved into the mansion's walls - each encoded with a DIFFERENT cipher. The mansion seems to distort reality itself - nothing is quite as it seems, and reflections dance strangely in the dusty mirrors that line the corridors. Decode all three messages and combine them to form the secret passphrase. Only then can you escape and claim your flag!

https://raiffeisen-tech.ctfd.io/mansion

Hint 1: The code must be written with UPPERCASE letters and without spaces
Hint 2: Each decoded word will seem backwards... look for a mirror! 🪞

## Recon

Base64 decode the first code, we get ESUOH. Simple enough. Just reverse that.
Base64 decode the second code. Giberish. Reverse the code first then decode, nothing.
Found out about ROT13 in a different challenge, try that, nothing. Try that + decode, nothing
Try all the cyphers and decodes on https://cryptii.com/ and https://emn178.github.io/online-tools/
Give up, move to the next.
Values stand out as possible Hexadecimal encoded values for letters. Try this and get REHSU. Reverse that to get USHER. Good singer
Take a break.
Think that maybe there's a link between the words. The Rene DESCARTES hint might be specific.
Google Rene Descartes House Usher
Find "The fall of the House of Usher" by Edgar Allan Poe
Try "House of Usher". It fails. Give up again.
Use hints.
Try HOUSEOFUSHER

## Vulnerability / Idea

All values seem to be somehow encoded. We need to figure out how.

## Exploitation Steps (Reproducible)

Base64 decode first value and reverse the result => HOUSE
Use a DES decoder for second value (found about this after getting the answer). Reverse the result => OF
Hexadecimal to UTF-8 convertor for last value. Reverse the result => USHER

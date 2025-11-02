## TL;DR

Inspect Element -> Find Code in a HTML element -> Base64 Decode -> Profit

## Context

Dexter Morgan is a serial killer, but he is always killing respecting a CODE. His father taught him the basics, but he needs to always be cautious and stick to them if he wants to live at least until 64.

https://raiffeisen-tech.ctfd.io/dexter

Hint 1: Sometimes the truth is hidden in plain SIGHT

## Recon

Tried to right click on page, saw it is disabled.
Opened Developer Tools panel using F12.
Searched for the element containing the image.
Found a div with class "encrypted-code" and found a code.

When revisiting the page to write this writeup, found that there was a hidden button in
"Dexter's right eye". Pressed it and the code was revealed. Oh well :D.

## Vulnerability / Idea

There is probably a Base64 base encoded code hidden somewhere.
Use Developer tools to check

## Exploitation Steps (Reproducible)

Use F12 to open Developer tools
Search through the HTML elements
Find a div with class "encrypted-code". It contains a code.
Base64 decoded the code.
Submit the rtech{th3_d4rk_p@$$3ng3r} flag

## TL;DR

We the two pices of information "The flag hides in the shadows — not necessarily where mortal eyes expect it to be" and "robots that can read hundreds of lines of text in a second" hinted at the robots.txt file, accessing the file and the follow-up link (which was b64 encoded) eventually revealved the encoded fag. Used cyberchef for decoding.

## Context

Strange things lurk within this haunted web application.
The flag hides in the shadows — not necessarily where mortal eyes expect it to be.
Can you uncover its ghostly secret before it vanishes forever?

https://raiffeisen-tech.ctfd.io/halloween-web-haunt

Hint 1: The living follow links, but the dead know where to crawl.
Hint 2: Did you know we now have robots that can read hundreds of lines of text in a second ?

## Recon

Basically everything. Press all the buttons
Send all the "emails"
Checked all the HTML
Spent too much time looking into comments,
Looked around the map. Zoomed out, found the pin, searched it on Google Maps didn't get any insight.
Used hints, nothing.
Took a 10 minute break as a team.
Came back. Stefan read the hints, instantly cliked, solved it in 10 seconds.

## Vulnerability / Idea

No initial insight.
Hints + A break + A fresh pair of eyes

## Exploitation Steps (Reproducible)

Go to /robots.txt
Receive a base64 encoded string. Decode it to receive "/text/404spirit.bak"
Go to /text/404spirit.bak
Receive another base64 encoded string. Decode it to receive the flag: rtech{404_boo_not_found}

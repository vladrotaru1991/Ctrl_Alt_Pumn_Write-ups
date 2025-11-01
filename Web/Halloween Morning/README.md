## TL;DR

Set HTTP Request Method to BREW -> Profit

## Context

It’s almost midnight, the horror marathon is about to begin, and you desperately need coffee to stay awake. But the company’s new “smart coffee API” has gone rogue — it refuses to brew anything, no matter how you ask. Every request comes back with the same smug message:

“418: I’m a teapot.”

You can’t survive The Ring, Hereditary, and The Thing without caffeine. Somewhere deep in the server, there’s a way to convince this digital barista to make an exception — if you use the right method and flavor.

Can you persuade the teapot to serve one final cup before the night consumes you?

Note: The server insists it’s a teapot, but maybe… just maybe… it can still /brew.

https://raiffeisen-tech-halloween-morning.chals.io

Hint 1: Are you sure that there is a fixed set of HTTP methods ?

## Recon

The HTTP Code 418 error is a well-known gag.
We need to somehow use brew.
Tried to make the request to /brew => received "I can't post anything? I'm a teapot"
Tried to make the request method to be "BREW" but without the endpoint having /brew => 405 Method Not Allowed

## Vulnerability / Idea

Make the teapot BREW somehow

## Exploitation Steps (Reproducible)

Send a HTTP BREW request to https://raiffeisen-tech-halloween-morning.chals.io/brew
Receive the rtech{brewed_with_love} flag

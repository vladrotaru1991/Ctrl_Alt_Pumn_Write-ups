## TL;DR

SQL Injection to add secret column to response -> Profit

## Context

Hunt through cursed vampire records to uncover the Admin Vampire's blood-soaked secret. Can you exploit the darkness within? 🦇💀

https://raiffeisen-tech.ctfd.io/vampire

Hint 1: The search uses SQL LIKE queries with string concatenation, SQL UNION will help access Admin Vampire hidden columns.

## Recon

Tried to find the Vampire Admin by making searches.
Tried multiple known vampires, couldn't really find anything.
Tried searching for just a letter. Saw that we get responses.
Tried each letter individually and saw that for the letter "r", we get an array with 5 vampires, so we assumed that's all of them.
The "secret" is probably a field of the Database row, but the API is not returning it.
Trying SQL injections to get the "secret" column.
Saw that the array name is "vampires so assumed that the name of the table is vampires
name
Tried "name=' UNION SELECT 1,2,3,4,secret FROM vampires'" => number of columns don't match

## Vulnerability / Idea

Is it hard to find the Vampire admin? No
We need to find the "blood-soaked secret" but there's nothing like that in the response.
We need to receive the secret from the server somehow.

## Exploitation Steps (Reproducible)

Use "name=' UNION SELECT 1,2,3,secret FROM vampires'" as the input
Receive the rtech{sql_inj3ct10n_sucks_bl00d} flag


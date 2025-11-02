## TL;DR

SQL Injection -> Profit

## Context

🎃 The old mansion's login portal is haunted by restless spirits...

Can you find a way past the ghostly authentication?

The ghosts whisper of forgotten SQL queries...

https://raiffeisen-tech.ctfd.io/spooky-login

Hint 1: What happens if you make the SQL query always return true?

## Recon

From the start this looked like it required some SQL injection so we just went for it

## Vulnerability / Idea

Use SQL injection to login as admin.

## Exploitation Steps (Reproducible)

Enter "admin' --" as the username and anything you want as the password.
Login
Receive the rtech{sp00ky_sql_1nj3ct10n_gh0st} flag

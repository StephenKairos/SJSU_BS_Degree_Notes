# Authentication

## Authentication

* Are you who you say you are?
    * Something you: know, have, or are
    * Password, Smartcard, or Fingerprint, respectively
* Something you know: Passwords
    * PIN, Social Security Number, Mother's Maiden Name, Date of Birth, Name of your Pet
* Trouble with Passwords:
    * Dangerous, but cheap, free, no cost
    * Convenience, easy to reset password

## Keys vs Passwords

* Keys are random, hard to crack
* Passwords aren't random, usually predictable
    * Broken by dictionary attack
    * Have pass phrases, convert a sentence to a password

## Attacks on Passwords

* Target one account, any account on system, or any account on any system
* Denial of Service Attack: Large amounts of requests
* Common Attack Path: Outsider > Normal User > Administrator
* May Require only one weak password

## Password Files

* Verify Passwords for authentication
* Need to hash the passwords, verify passwords by hashing
* CAn be broken with forward search

## Salt

* Add salt to password before hashing
* Salt is randomly generated
* Doesn't help every time
* If password is in dictionary, easy to crack, adding salt prevents this

## Issues

* Password reuse
* Don't change default password
* Social Engineering (34% gave their password for chocolate, **CHOCOLATE**)
* Error Logs may contain "almost" passwords
* Bugs, keylogger, spyware
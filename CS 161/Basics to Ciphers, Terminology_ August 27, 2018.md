# Basics to Ciphers, Terminology: August 27, 2018

## How to Speak Crypto

* **Cipher**: the algorithm
* Plaintext, Ciphertext
* **Symmetric Key**: Same key to Encrypt and Decrypt
* **Public/Private Key**: Public Encrypts, Private Decrypts

## **Kerckhoff's Principle**

* Basic Assumptions:
    * System itself is known
    * Key is Secret
* Why it's useful:
    * People can debug easily
    * Easy to add
    * Secret Algorithms are easy to crack when exposed
    * Reverse Engineering
    * Security by Obscurity is not good
* **THE CIPHER MUST BE PUBLIC**

## Types of Ciphers/Algos

* **Simple Substitution**: Shift Cipher, Caesar Cipher is shift by 3
* **"Key Space"**: Larger is better, easy to brute force
* **Affine Cipher**: y = a * x + b mod 26
* *Opinion*: Shift Ciphers are easy to break because you can use frequency graphs, solving for x
* Modular Arithmetic doesn't require parentheses, because the result is always the same
* Simple Substitution shift's key doesn't have to be in order, but permutation of the 26 letters can spawn a key space of 2^88
* **Double Trasposition**: matrix, row/column count is determined, fill with ciphertext, then shift rows/columns
    * Key is Matrix Size, and permutations
    * Padding Spaces with Uncommon Letter is good
![](https://i.imgur.com/oHmDv7V.png)
* One Time Pad: 
    * Unbreakable, but unfeasible in real life

## Exhaustive Key Search

* Probability to try all the keys
* This Average is around 50% of all the possible keys
* Brute force attack can produce false positives
    * This is a Problem, you can't tell whats the actual correct one
    * Fix by **Unicity Distance**

## Terminology

* **secure**: system is secure, if the only attack known is to try all keys
    * computationally secure: if it takes too much time, decades
* **insecure**: if any shortcut attack is known
* *Catch-22*: Insecure Cipher might be harder to break
* *Example*: 
    * Secure Cipher 1: 2^20 Keys
    * Insecure Cipher 2: 2^80, with shortcut, 2^30
    * C2 is still better than C1
* *Self Vocabulary* **Net Key Space**: Final Resulting Key Space after shortcut attacks
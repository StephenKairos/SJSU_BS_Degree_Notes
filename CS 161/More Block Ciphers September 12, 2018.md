# More Block Ciphers September 12, 2018

## Questions

* Why CTR is better than ECB if ECB can do random access already
    * CTR can have different outputs for the same input
    * Ciphertext does not betray the plaintext

## Clock Arithmetic

* Circular
* Always reduced within the boundaries of the modulus
* Modular Inverses:
    * -2 mod 6 = 4 because 2 + 4 - 0 mod 6
    * No negative values, - means additive inverse
    * Same for negative powers
    * Different Notations
    * Additive gives you 0
    * Multiplicative gives you 1
* Not all multiplicaive inverses exist
* The two numbers must be relatively prime, not the same common factor
* x^-1 mod y exists only when x and y are relatively prime
* Totient Function: φ(n), number of numbers less than n that are relatively prime to n
    * φ(p) = p - 1 if p is prime
    * φ(pq) = (p - 1)(q - 1) if p and q are prime

## Public Key Cryptography

* Two Keys, one to encrypt, another to decrypt
* Trap door, one way function
* Easy to compute in one direction, hard to compute in the other direction
* Digital Signature, can be used to verify
    * Use private key to encrypt, can be decrypted by public key, verifies that message was sent by the owner of private key

## Knapsack Problem

* Subset sum problem
* Set true false (0, 1) to weight address to get the solution
* NP-complete problem
* General Knapsack (GK) is hard
* Superincreasing Knapsack (SIK) is easy
* ms to solve SIK

## Knapsack Cryptosystem

* Generate SIK
* Convert SIK to GK
* Public Key: GK
* Private Key: SIK

## Knapsack Weakness

* Lattice Reduction
* Easy to break (don't need to know details)

## RSA

* Within 10 years, could be completely broken
* Gold Standard in Public Key crypto
* Two large prime numbers p and q
* N = pq, the modulus
* Choose e relatively prime to (p - 1)(q - 1) 
* Find d such that ed = 1 mod (p - 1)(q - 1)
* Public Key is (N, e)
* Private Key is d
* M is a number
* encrypt: c = M^e mod N
* decrypt: M = C^d mod N
* Only way to break is to factor modulus
* **Exam** will ask to generate public and private key using RSA
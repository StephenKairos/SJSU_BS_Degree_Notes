# Hash Functions, September 19, 2018

## Review

* If you want a system with authentication and non-repudiation, you have to use public key crypto

## Hashing

* signing messages might be costly to compute and send
* Hashing helps making things more efficient
* One-way crypto
* Hashes can be generated from other hashes, not secure

## Hash Functions

* Compression, Efficiency, One-Way, Weak Collision Resistance, Strong Collision Resistance
* Pre-Birthday Problem, Birthday Problem
* One Case vs. All Possible Cases
* sqrt(number of outputs)
* Hash function should have many outputs similar to size of key
* Collisions aren't too bad for general use, but bad for crypto
* CRC, good for detecting burst errors
    * Easy to construct collisions

## Popular Crypto Hashes

* MD5, broken, don't use
* SHA-2, US Gov standard

## Hash Design

* Avalanche Effect: changing one bit should affect about half of the output bits
* Some number of rounds

## HMAC

* Hashed MAC
* Keyed Hash
* h(K, M) or h(M, K)
* h(M, K) is better, but still has issues, still has collisions
* RFC 2104 method

## Shamir's Secret Sharing

* You can't access the secret by yourself
* You need at least 2 people
* Useful for **Key Escrow** (AKA "fair" cryptosystem): 
    * an arrangement in which the keys needed to decrypt encrypted data are held in escrow so that, under certain circumstances, an authorized third party may gain access to those keys. These third parties may include businesses, who may want access to employees' private communications, or governments, who may wish to be able to view the contents of encrypted communications.
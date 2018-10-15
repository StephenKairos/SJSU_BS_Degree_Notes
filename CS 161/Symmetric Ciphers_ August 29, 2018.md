# Symmetric Ciphers: August 29, 2018

## One Time Pad

* Hard to use IRL
* Randomness is hard to maintain
* One Key used at a time, clunky

## Codebook Cipher

* Break it by checking length of the words
* Zimmermann Telegram

## Claude Shannon

* Common Theory of Secrecy Systems
* Confusion: no clear relationship between plaintext and ciphertext (substitution)
* Diffusion: spread plaintext stats through ciphertext (bit permutation)
* Proved OTP secure
* Only one method is insecure:
    * Shift Cipher (confusion)
    * Transposition (diffusion)
* Concatenation is secure, called **Product Ciphers**
    * Block Ciphers

## Possible Attacks

* Exhaustive Key Search (Brute Force)
* Letter Frequency Analysis
* Implementation Attack (Side-Channel Attacks)
    * Measure electrical power consumption of CPU operating on the key
    * Electromagnetic Radiation
    * Run time, during process
    * **Social Engineering Attacks**: attacking the weakest link
* Using Services like password managers should be open-sourced

## Taxonomy
* Symmetric Key
* Public Key
* Hash Algorithms
* Hybrid

## Example Questions

* Affine Cipher: Would Letter Frequency Analysis work against Affine Cipher? Why? **Yes, same formula, a character is always encrypted to the same character**
* **Affine Cipher is a Confusion Only cipher**
* **Key Space is not increased by affine cipher**
* Explain, if any, a disadvantage of Kerckoffs' Principle. 
* How long is the key in an OTP cipher? **As long as the plaintext**
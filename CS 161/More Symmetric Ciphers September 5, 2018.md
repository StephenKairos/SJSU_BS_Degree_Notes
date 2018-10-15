# More Symmetric Ciphers September 5, 2018

## New Types of Ciphers

* Stream cipher: generalized one-time pad
* Block Ciphers

## Stream Ciphers

* Encrypt bits individually
* Synchronous or Asynchronus, depending on key only or key and ciphertext
* Security relies on keystream
* Encryption: y = x + s mod 2, y is ciphertext bit, x is plaintext bit, s is keystream bit
* Key 011011 converted to keystream: 0111010100101... (some long bit stream)
* XOR is good, because it gives you 50% chance per bit, this multiplies
* longer key makes it harder to guess the key
* Brute force still works on 1/2 average
* It's reversible
* Used to be the king of crypto, but was replaced by block ciphers
* Two Types:
    * A5/1
    * RC4

## A5/1: Shift Registers

* 3 shift registers, x (19 bits), y (22 bits), z (23 bits)
* 64 bit key
* When register steps:
    * 1. Compute new first bit
    * 2. THEN, shifts
* Key is used as initial fill of registers
* Majority vote: 3 bits from the registers, whatever the most apprearing votes, 1 or 0
* Those who won the majority vote, will shift
* Before shifting, compute new first bits, XOR specific bits at specified addresses
* Then shift

## RC4 Initialization

* Always discard the first 256 bytes

## More on Stream Ciphers

* Very fast in hardware
* Popular in the past
* Keeps up with constant ciphers, encoding a call for example
* Shamir declared "the death of stream ciphers"

## Block Ciphers

* A bit different
* **Round Function**: input to function key and output of previous round
* Implemented in software
* Splitting ciphertext/plaintext into blocks

## Feistel Cipher

* Encryption: A type of block cipher
* For each round i = 1, 2, ..., n
    * L(i) = R (i - 1)
    * R(i) = L(i - 1) XOR F(R(i - 1), K(i))
* Decryption, same as encryption, flip left and right

## Data Encryption Standard

* DES developed in 1970s
* Based on IBM's Lucifer cipher
* Controversial
    * NSA secretly involved
    * Secret
    * Made algo less strong, maybe to break the cipher themselves?
* 64 bit block, 56 bit key, 16 rounds, 48 bits of key used each round
* S-Boxes: maps 6 bits to 4 bits
* Expands for diffusion
* S-Boxes are for confusion
* P-box permutates for diffusion
* **Avalanche Effect**
* Expansions position are hard coded
* S-Box: **EXAM**
    * First and last bit to index row, 2-5th bit to index column
    * Non-Linear, trying to reverse will give you different outputs
* Some operations have no security purpose, no shortcuts
* Fast to implement in hardware
* Influenced by limits of tech at the time
* No back-door
* Only attack is exhaustive key search
* Complicated attack in 1990, almost 20-30 years later

## Security of DES

* Differential Cryptanalysis attack
* Linear Cryptanalysis
* Brute Force is still a problem
* Enough funds, you can brute force it
* $20, 000, 000 ish
* COPACOBANA, cracks DES in 7 days 
* Distributed Brute-force, several nodes helped crack  in 22 hours
* Malware can be used to control computers to crack codes
# Block Ciphers September 10, 2018

## Certain Cipher Lis

* RC6
* TEA (Tiny Encryption Algorithm) and it's fixed versions: xTEA and sTEA
* AES

## Block Cipher Modes

* Electronic Codebook (ECB)
    * Each block at a time
* Cipher Block Chaining (CBC) *Not related to blockchain*
    * Chain blocks together
* Counter Mode (CTR)

## ECB 

* Does not work, some attacks
* Cut And Paste, can rearrange blocks, mess up message
* Same plaintext yields same ciphertext **DANGEROUS**

## CBC

* Chains each block, each one depends on the previous one
* Transmission Error is not expanding, issues only focus on the block that was garbled
* Cut and paste is still possible, but more complex, and will cause garbles

## Counter Mode

* Incremental encryption with key

## Integrity

* Confidentiality, making sure only the recipient can read the message
* MAC, Message Authentication Code
* Used for integrity
* If any plaintext block changes, the MAC will change, notifying that the plaintext has been tampered with
* Can use two keys to encrypt the plaintext for integrity, then a second key to encrypt for confidentiality
* Symmetric Crypto is good for confidentiality and integrity
    * Authentication Protocols
    * Anything you can do with hash function
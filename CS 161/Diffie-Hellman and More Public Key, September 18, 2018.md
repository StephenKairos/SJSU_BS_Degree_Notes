# Diffie-Hellman and More Public Key, September 18, 2018

## Diffie-Hellman

* g, p and g^k mod p
* g, p, a, b, and g^ab mod p
* Broken by Man in the Middle Attack

## Non-non-repudiation

* MAC with symmetric key
* Bob can forge the MAC with the key
* Sharing the same key is dangerous

## Non-repudiation

* Use a private key to sign
* Proves that Alice signed the message

## Notation

![](https://i.imgur.com/AJhO6ZU.png)

## Confidentiality and Non-Repudiation

* Can "sign and encrypt" or "encrypt and sign"
* Can forward signed messages to other people
* **Signed means someone made the message, but does not guarantee that the message came from that source**

## Public Key Infrastructure (PKI)

* User ID and User Public Key
* Key Generation and Management
* Certificate Authority (CA)

## PKI Trust Models

* Monopoly Model, not useful if authority is not trusted
* Oligarchy, multiple CAs, browser must store multiple, **currently used**
* Anarchy, web of trust, isn't good
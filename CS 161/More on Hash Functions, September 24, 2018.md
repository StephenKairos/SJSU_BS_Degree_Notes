# More on Hash Functions, September 24, 2018

## Review, Motivation

* If the message is big, signing is expensive to compute and send
* Hash function to change MB or GB sized file to just bits
* Slowly, we are moving to SHA-3, from SHA-2
* Add Key at end of HMAC: h(M, K)
* Key Escrow, AKA Key Sharing

## Visual Cryptography

* Share message in image? Steganography
* Black and White only
* How many white pixels, how many black
* AND operation on colors? White and White returns White, Black and Black returns Black, Black/White returns Black
    * W & W = W
    * B & B = B
    * W & B = B
* Overlay the images over each other
* Will work for colors, as well, would require a larger table
* Impossible to crack
* No exhaustive search possible
* One time pad ish?

## Random Numbers in Cryptography

* Many uses in crypto
* Needs "statistically" random numbers
* Needs an external input
* Needs to be unpredictable

## Problems with Random Numbers

* Pseudorandom is not good in some cases because with enough information, you can predict the next generated numbers
* **Example**: Card Shuffle = 52!
* Failed Software, ASF Software
* Used random 32 bit integer, which is easy to break 2^32
* Easier to break than a basic substitution cipher!

## What is Random?

* Entropy is the measure of randomness
* Software is supposed to be deterministic
* Mouse movements are dynamic, ish
* Good quality of such methods
* Quantity is limited
* Pseudo-random = pseudo-security

## Watermarks

* Invisible/Visible, Robust/Fragile
* Like currency and inner watermark
* Add invisible watermark to photo
* watermarks can be used to rebuild the photo

## Steganography

* Obscuring messages in images
* **Hiding in plain sight, not security by obscurity**
* Low order bits **don't matter for colors**
* Could "clean" an image by setting all low order to 0
* Stirmark: tool to make most watermarks in images unreadable without damaging the image
* Stego/watermarking is currently active research
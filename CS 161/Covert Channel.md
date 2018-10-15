# Covert Channel

## Covert Channel Communications
* hiding idea that there's any communication going on
* File existing on system to show 1, delete to show 0
* Slow but straightforard way to leak TOP SECRET info
* Other Covert Channels: 
    * Print Queue
    * ACK messages
    * Network Traffic
* Requirements:
    * Sender/Receiver have shared resource
    * Sender can change resource, receiver can observe
    * Must be synchronized
* Virtually Impossible to eliminate covert channels
* US Dept. of Defense: **Reduce covert channel capacity to no more than 1 bit/second**
* DoD gave up on eliminating covert channels

## Example

* 100 MB TOP SECRET file
* Plaintext is stored in TOP SECRET
* Ciphertext stored in UNCLASSIFIED (256 bit key)
* Followed guideline, reduce covert channel capacity to 1b/sec
* Would take **25 years** to leak
* But, if you leak the key, you can get it leaked in ~256 seconds

## Real World Covert Channel
* hide data in TCP header reserved field
* covert_TCP
    * sequence number might be wrong
    * ACK number could be used as well

## Inference Control

* query a database

## Quert Set Size Control
* don't return answer when set size is too small
* limits queries though
* N-respondent, k% dominance rule
    * used for real by US Census Bureau

## Other Inference Controls
* randomization
* many other methods, but none are satisfactory for now

## CAPTCHA
* visual/audio
* No Captcha reCAPTCHA from Google (cracked with audio)

## CAPTCHA and AI
* OCR is a challenging AI problem
* segmentation problem
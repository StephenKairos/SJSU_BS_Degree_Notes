# Access Control

## Biometrics
* a way to measure your physical properties
* fingerprints, handwritten signature, facial recognition, etc.
* Not as precise
* More secure replacement?
* Cheap, but not as much as passwords
* Ideal Biometric:
    * Universal, Distinguishing, Permanent, Collectable

## Biometric Modes
* identification: "who goes there?"
    * compare one-to-many
    * fingerprint database
    * does not know who you are
* authenticatio: "Are you who you say you are?"
    * compare one-to-one
* id is much more difficult

## Phases
* enrollment: teach computer who you are, more time
* recogntion: detection of biometric, short

## Problems
* Authentication: uncooperative subjects
* Fraud rate vs. insult rate
    * Fraud: misauthentication, false positive
    * Insult: can't authenticate, false negative
    * Decreasing one increases the other
* Equal error rate: rate where fraud == insult, compares biometrics

## Fingerprints
* Select points on the fingerprint for comparison
* Development as a child will give different prints

## Iris Patterns
* generation is chaotic
* no genetic influence
* stable pattern
* Patent Owned by Iridient Technologies
* Convert eye photo to bits
* Process: 
    * Get hemming distance
    * difference in iris code
    * accept if distance < 0.34
* Photo of eye can be used to fraud/crack such a system

## Equal Error Rates
* Fingerprint: 5%
* Hand Geometry: 0.1%
* Iris Scan: 0.000001

## Something you Have
* Password Generator:
    1. "I'm Alice"
    2. Random value R
    3. Alice sends Pin, R to Pass. Gen.
    4. Pass. Gen. sends h(K, R) to Alice
    5. Alice sends to Bob

## 2-Factor Authentication
* 2 out of the 3: know, have, are
* Can you do 2 of the same one? **No, must be 2 different items**

## Other Auths
* Single Sign On: signed on for all websites
* Cookies, indexes database, maintain state across sessions
    * Easily stolen
    * Better version is "sessions"
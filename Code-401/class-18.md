# Class 18

## Caesar Cipher

One of the simplest and widely known encryption techniques. It is a substitution cipher in which each letter in plaintext is replaced by another letter some fixed number of positions down.

```
Imagine Caesar wants to send this message:
SECRET MEETING AT THE PALACE
Here's what that might look like encrypted:
YKIXKZ SKKZOTM GZ ZNK VGRGIK

Cipher:
A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F
```

## Symmetry

Symmetric encryption is any technique where the same key is used to both encrypt and decrypt the data. Asymmetric encryption is where practice of using pairs of related keys.

| Feature                  | Symmetric Encryption                          | Asymmetric Encryption                          |
|--------------------------|----------------------------------------------|-------------------------------------------------|
| Key Types                | Single key used for both encryption and decryption | Key pair: Public key for encryption, Private key for decryption |
| Key Distribution         | Key must be securely shared between parties  | Public keys can be freely distributed, private keys must be kept secret |
| Key Management           | Requires careful key management and distribution | Easier key management due to separate public and private keys |
| Speed                    | Generally faster compared to asymmetric encryption | Slower compared to symmetric encryption |
| Use Cases                | Suitable for bulk data encryption and fast communication | Used for secure communication, digital signatures, and key exchange |
| Security Concerns        | Key distribution and management are critical security concerns | Private key protection is crucial; potential vulnerabilities in key exchange |
| Examples                 | AES, DES, 3DES                               | RSA, ECC, ElGamal                              |

## RNG

Random number generators are useful for a variety of cases, one of them being cryptography. Cryptography requires numbers that hackers cannot guess. We need numbers that are unpredictable in order to create a securer encryption. 

| Feature                        | True Random Number Generators (TRNG)              | Pseudo-Random Number Generators (PRNG)           |
|--------------------------------|---------------------------------------------------|--------------------------------------------------|
| Source of Randomness           | Derive randomness from physical processes like electronic noise, radioactive decay, or atmospheric noise | Algorithmically generate sequences of seemingly random numbers based on a seed value |
| Predictability                | Completely unpredictable, even with complete knowledge of the past output | Deterministic; the sequence of numbers can be reproduced if the seed is known |
| Initialization                | May require calibration and initialization processes | Initialized with a seed value, which must be kept secret to maintain security |
| Entropy                        | Typically higher entropy, as it relies on unpredictable physical phenomena | Limited by the quality of the seed and the algorithm; potential for patterns in long-term sequences |
| Use Cases                     | Cryptographic applications requiring high-quality random numbers, such as key generation, initialization vectors | Suitable for general-purpose applications like simulations, games, and non-security-critical tasks |
| Security in Cryptography      | Preferred for cryptographic applications due to true randomness, resistant to certain attacks | Used in scenarios where the demand for true randomness is not critical, and predictability is acceptable |
| Speed                          | Generally slower due to reliance on physical processes | Faster as they are algorithmic and can generate numbers on-the-fly |
| Examples                       | Electronic noise-based generators, radioactive decay-based generators | Linear Congruential Generator (LCG), Mersenne Twister, Fortuna |

## Encryption vs Decryption

Encryption is using a lock, decryption is using a key.

## Things I want to know more about

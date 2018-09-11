# cryptopals-resources

### :raised_hand: no spoilers, just pointers :point_left:
when I was going through the [CryptoPals](https://cryptopals.com) challenges, there were quite a few times where I needed a pointer in the right direction, but all I would find online would be coded solutions. this is a curated list of resources that don't give away the solutions, but help you understand what you need to understand to write the solution yourself.

contributions welcome! :relaxed:

## table of contents
- [set 1: basics](#set-1-basics)
  - [challenge 1: convert hex to base64](#challenge-1-convert-hex-to-base64)
  - [challenge 2: fixed xor](#challenge-2-fixed-xor)
  - [challenge 3: single-byte xor cipher](#challenge-3-single-byte-xor-cipher)
  - [challenge 4: detect single-character xor](#challenge-4-detect-single-character-xor)
  - [challenge 5: implement repeating-key xor](#challenge-5-implement-repeating-key-xor)
  - [challenge 6: break repeating-key xor](#challenge-6-break-repeating-key-xor)
  - [challenge 7: aes in ecb mode](#challenge-7-aes-in-ecb-mode)
  - [challenge 8: detect aes in ecb mode](#challenge-8-detect-aes-in-ecb-mode)

## set 1: basics
### __challenge 1__: convert hex to base64
- [Bits and Bytes (Stanford)](https://web.stanford.edu/class/cs101/bits-bytes.html)
- [Hexadecimal (Wikipedia)](https://en.wikipedia.org/wiki/Hexadecimal)
- [Base64 (Wikipedia)](https://en.wikipedia.org/wiki/Base64)

### __challenge 2__: fixed xor
- [Exclusive or (Wikipedia)](https://en.wikipedia.org/wiki/Exclusive_or)

### __challenge 3__: single-byte xor cipher
- [Letter frequency (Wikipedia)](https://en.wikipedia.org/wiki/Letter_frequency)
- _Note: Be prepared to revisit this challenge to fine tune your algorithm as you progress through the other challenges. Your first shot at the algorithm may work for this challenge, but we've found that it usually needs improvement to pass 4, 5, and 6._

### __challenge 4__: detect single-character xor
- _Note: This challenge is really just more testing of your Challenge 3 algorithm to make sure it's shipshape._

### __challenge 5__: implement repeating-key xor
- _Note: The provided plaintext has a line break after `nimble` and no spaces at the end of lines. It is __74 bytes__ long, and the last byte of the plaintext is `0x6C` (ascii letter `l`). Here it is "unrendered":_

```Burning 'em, if you ain't quick and nimble\nI go crazy when I hear a cymbal```

- _Note: The provided hex-encoded ciphertext does not have any line breaks, so when comparing your output to the provided output, strip out any line breaks and spaces. Spaces/line breaks are not part of the Base64 or Hex character set, so those characters ought to be removed before processing. (`/\s/g`). Likewise for other encodings that do not have those characters._

### __challenge 6__: break repeating-key xor
- [Hamming Distance (Wikipedia)](https://en.wikipedia.org/wiki/Hamming_distance)
- _Note: Step 4 of the process allows for a lot of experimentation, so if you aren't getting results play around with that step. Also try breaking something you encrypted yourself with your Challenge 5 code for testing._

### __challenge 7__: aes in ecb mode
- [Advanced Encryption Standard (Wikipedia)](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)
- [ECB Mode (Wikipedia)](https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation#Electronic_Codebook_(ECB))
- _Note: The challenge is not asking you to implement AES from scratch. Find your language's implementation (or a reputable module for your language) and use that._

### __challenge 8__: detect aes in ecb mode
- [ECB Mode (Wikipedia)](https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation#Electronic_Codebook_(ECB))


## set 2: block crypto
### __challenge 9__: implement pkcs#7 padding
### __challenge 10__: implement cbc mode
### __challenge 11__: an ecb/cbc detection oracle
### __challenge 12__: byte-at-a-time ecb decryption (simple)
### __challenge 13__: ecb cut-and-paste
### __challenge 14__: byte-at-a-time ecb decryption (harder)
### __challenge 15__: pkcs#7 padding validation
### __challenge 16__: cbc bitflipping attacks

## set 3: block & stream crypto
### __challenge 17__: the cbc padding oracle
### __challenge 18__: implement ctr, the stream cipher mode
### __challenge 19__: break fixed-nonce ctr mode using substitutions
### __challenge 20__: break fixed-nonce ctr statistically
### __challenge 21__: implement the mt19937 mersenne twister rng
### __challenge 22__: crack an mt19937 seed
### __challenge 23__: clone an mt19937 rng from its output
### __challenge 24__: create the mt19937 stream cipher and break it

## set 4: stream crypto and randomness
### __challenge 25__: break "random access read/write" aes ctr
### __challenge 26__: ctr bitflipping
### __challenge 27__: recover the key from cbc with iv=Key
### __challenge 28__: implement a sha-1 keyed mac
### __challenge 29__: break a sha-1 keyed mac using length extension
### __challenge 30__: break an md4 keyed mac using length extension
### __challenge 31__: implement and break hmac-sha1 with an artificial timing leak
### __challenge 32__: break hmac-sha1 with a slightly less artificial timing leak

## set 5: diffie-hellman and friends
### __challenge 33__: implement diffie-hellman
### __challenge 34__: implement a mitm key-fixing attack on diffie-hellman with parameter injection
### __challenge 35__: implement dh with negotiated groups, and break with malicious "g" parameters
### __challenge 36__: implement secure remote password (srp)
### __challenge 37__: break srp with a zero key
### __challenge 38__: offline dictionary attack on simplified srp
### __challenge 39__: implement rsa
### __challenge 40__: implement an e=3 rsa broadcast attack

## set 6: rsa and dsa
### __challenge 41__: implement unpadded message recovery oracle
### __challenge 42__: bleichenbacher's e=3 rsa attack
### __challenge 43__: dsa key recovery from nonce
### __challenge 44__: dsa nonce recovery from repeated nonce
### __challenge 45__: dsa parameter tampering
### __challenge 46__: rsa parity oracle
### __challenge 47__: bleichenbacher's pkcs 1.5 padding oracle (simple case)
### __challenge 48__: bleichenbacher's pkcs 1.5 padding oracle (complete case)

## set 7: hashes
### __challenge 49__: cbc-mac message forgery
### __challenge 50__: hashing with cbc-mac
### __challenge 51__: compression ratio side-channel attacks
### __challenge 52__: iterated hash function multicollisions
### __challenge 53__: kelsey and schneier's expandable messages
### __challenge 54__: kelsey and kohno's nostradamus attack
### __challenge 55__: md4 collisions
### __challenge 56__: rc4 single-byte biases

## License
MIT

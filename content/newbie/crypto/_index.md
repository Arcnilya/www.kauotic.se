---
title: "Crypto"
date: 2024-06-18T13:49:00+02:00
---

When we say "crypto" we mean cryptography, not Bitcoins (sometimes the 
category "Blockchain" shows up in some CTFs).  The crypto challenges can range
from very simple ciphers to public key signatures. The most common usecase
for cryptography is *confidentiality*, aka hide information from unintended
eyes.

Let us start with something easy, a ceasar cipher. For this cipher you simply
rotate the alphabet a certain number of steps (13 is the most popular).
```
ABCDEFGHIJKLMNOPQRSTUVWXYZ (Normal)
NOPQRSTUVWXYZABCDEFGHIJKLM (rot13)

rot13("FLAG") -> "SYNT"
```

Next we have encodings. Base64 is a way of encoding data into a text format
that can be easily transmitted over text-based protocols like email or included
in URLs without causing issues. Base64 takes binary data and encodes it into a
set of 64 characters that are safe to use in text form. The characters used in
Base64 encoding are: uppercase letters, lowercase letters, numbers as well as
"/" and "+". The "=" is used as padding at the end to make sure that the
encoded data length is a multiple of four.

## Symmetric Key Crypto
Alice wants to send a message to Bob through Eve. But she does not want Eve to
read the message. Alice could write the message backwards or rotate the
alphabet so that A becomes N, and B becomes O, but that might be too simple.
She could instead use a secret key which is shared with Bob! Alice locks the
message with the key (she encrypts it) and give it to Eve. Eve cannot read the
ciphertext because she doesn't have the key.  When Bob receieves the encrypted
message he can unlock it with the same key (he decrypts it). This is called
symmetric cryptography, beacuse the two keys are identical.

```
enc(message, key) -> cipher
dec(cipher, key) -> message
```

## Asymmetric Key Crypto
There is also something called asymmetric cryptography, also known as public
key crypto. Bob will have two keys: a public key and a private key. You can
imagine the public key as a padlock. Bob can publically post this padlock
for people to encrypt messages, but he keeps his private key secret, which
can unlock the padlock.  When Alice wants to send a message to Bob, she uses
his public key (padlock) to encrypt the message and give it to Eve.  Eve
does not have the private key and cannot read the message.  When Bob
receieves the encrypted message, he can decrypt it with his private key.
You can also use crypto to sign things. You can prove that a message is
from you and also verify that it hasn't been tampered with.

```
enc(message, pub_key) -> cipher
dec(cipher, priv_key) -> message
```

Another useful crypto primitive (building block) is the hash function.
It is a one-way function to turn a message (or a file) into a unique
hash. And if you only have the hash, there is no way to know what was hashed.

```
hash(message1) -> hash_digest1
hash(message2) -> hash_digest2
```

### Useful platforms
- https://overthewire.org/wargames/krypton/
- https://cryptohack.org/
- https://tryhackme.com/module/cryptography
- https://academy.hackthebox.com/module/details/20

### Useful tools
- https://rot13.com/
- https://cryptii.com/
- https://www.dcode.fr/en
- [Cipher Identifier and Analyzer](https://www.boxentriq.com/code-breaking/cipher-identifier)
- [CyberChef](https://gchq.github.io/CyberChef/)
- [RsaCtfTool](https://github.com/RsaCtfTool/RsaCtfTool)


### Try your skills
If you feel ready then you can try to solve our [Crypto
challenges](http://intro.kauotic.se) (registration code: 1337). When you have
solved three of them, head over to one of our CTF events and you will get a
sticker!


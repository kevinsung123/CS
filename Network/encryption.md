### cryption (암호화 종류)
- [cryptomatic](https://www.cryptomathic.com/news-events/blog/symmetric-key-encryption-why-where-and-how-its-used-in-banking#:~:text=Symmetric%20encryption%20is%20a%20type,used%20in%20the%20decryption%20process.)
- [classfication of encrpytion](https://www.cryptomathic.com/news-events/blog/classification-of-cryptographic-keys-functions-and-properties)
- [dff 3 kind cryptographic algorithms](https://www.cryptomathic.com/news-events/blog/differences-between-hash-functions-symmetric-asymmetric-algorithms)
- [security service](https://www.cryptomathic.com/news-events/blog/applying-cryptographic-security-services-a-nist-summary)
### Security services
- A lot of security service provied such as 
	- confidentiality
	- integrity
	- authentication
	- non-repudation
---
#### Classfication of Cryptographic algorithm
1. hash functions
2. Symmetric-Key algorithms
3. Asymmetric-Key algorithms
---
#### Hash function
- hash함수는 large random size data를 작은 고정된 size 데이터로 변환하는 알고리즘
- hash함수의 output은 hash-value 또는 digest라고 일컫음
- 일방향, The basic opertation of Hash functions does not nedd any key and operate in one-way manner
- 일방향 작동은 특정 output로부터 input을 계산하기 불가능
-  일반적인 작동 원리
	1.  Generation and verification of digital signatures
	2.  Checksum/Message integrity checks
	3.  Source integrity services via MAC
	4.  Derivation of sub-keys in key-establishment protocols & algorithms
	5.  Generation of pseudorandom numbers
---
#### Symmetric Encryption
- 한개의 secret key로 encrypt/decrypt를 할떄 사용
- 반대가 asymmetric encryption( 한쌍의 key pair를 사용, public/private)
- 2가지 종류가 존재
	1. Blokc algorithm
		- 특정한 secret key를 이용하여 데이터의 블록을 암호화
	2. Stream algorithm
		- system의 메로리를 얻는 대신 stream으로 암호화
##### Symmetric encryption 종류
#### block 
- AES(Advanced Encryption Standard)
- DES(Data Encryption Standard)
- IDEA(International Data Encryption Algorithm)
- RC5
- RC6
##### stream
- RC4(Rivest Cipher 4)
---
#### Asymmetric Encryption
- publick key algorithm 등등.. 2개의 암/복호화 관련 key를 사용
#### key lengths and algorithm
- key의 사이즈가 더 클루록, 더 안전함
- symmetric or asymmetric이든 그것의 절대적인 길이는 algorithm에 의존
- key length should be chosen based on a number factors such as
	- The algorithm being used
	- The strength of security required
	- The amount of data being processed with key
	- The crypto-period of the key

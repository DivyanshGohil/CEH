### In one of the following types of cipher, letters in plaintext are rearranged according to a regular system to produce ciphertext. Which is this type of cipher?


- **Transposition cipher**
- Stream cipher
- Block cipher
- Substitution cipher

Explanation:

    
>**Substitution cipher**: The user replaces units of plaintext with ciphertext according to a regular system. The units may be single letters, pairs of letters, or combinations of them, and so on
    
>**Block cipher**: Deterministic algorithms operating on a block (a group of bits) of fixed size with an unvarying transformation specified by a symmetric key. Most modern ciphers are block ciphers
    
>**Transposition cipher**: Here, letters in the plaintext are rearranged according to a regular system to produce the ciphertext. For example, “CRYPTOGRAPHY” when encrypted becomes “AOYCRGPTYRHP.”
    
>**Stream cipher**: Symmetric-key ciphers are plaintext digits combined with a key stream (pseudorandom cipher digit stream). Here, the user applies the key to each bit, one at a time. Examples include RC4, SEAL, etc.



### Which of the following encryption algorithms is also called Magma and is a symmetric-key block cipher having a 32-round Feistel network working on 64-bit blocks with a key length of 256 bits?


- Serpent
- **GOST**
- TEA
- Camellia

Explanation:

    
>**Camellia**: Camellia is a symmetric-key block cipher having either 18 rounds (for 128-bit keys) or 24 rounds (for 256-bit keys). It is a Feistel cipher with a block size of 128 bits and a key size of 128, 192, and 256 bits. Camellia uses four 8×8-bit S-boxes that perform affine transformations and logical operations. A logical transformation layer FL-function or its inverse is applied every six rounds
    
>**TEA**: The tiny encryption algorithm (TEA) was created by David Wheeler and Roger Needham, and it was publicly presented for the first time in 1994. It is a simple algorithm, easy to implement in code. It is a Feistel cipher that uses 64 rounds
    
>**GOST Block Cipher**: The GOST (Government Standard) block cipher, also called Magma, is a symmetric-key block cipher having a 32-round Feistel network working on 64-bit blocks with a 256-bit key length. It consists of an S-box that can be kept secret and it contains around 354 bits of secret information. GOST is a simple encryption algorithm, where the round function 32-bit subkey modulo 232 is added and put in the layer of S-boxes and the rotate left shift operation is used for shifting 11 bits, thereby providing the output of the round function.
    
>**Serpent**: Serpent is a symmetric-key block cipher that was a finalist in the AES contest. This algorithm was designed by Ross Anderson, Eli Biham, and Lars Knudsen. It uses a 128-bit symmetric block cipher with key sizes of 128, 192, or 256 bits. It can be integrated into software or hardware programs without any restrictions. Serpent involves 32 rounds of computational operations that include substitution and permutation operations on four 32-bit word blocks using 8-variable S-boxes with 4-bit entry and 4-bit exit



### Which of the following types of hardware encryption devices is a crypto-processor or chip present in the motherboard that can securely store encryption keys and perform many cryptographic operations?


- **TPM**
- USB encryption
- HSM
- Hard-drive encryption

Explanation:

    
>**HSM**: Hardware security module (HSM) is an additional external security device that is used in a system for crypto-processing and can be used for managing, generating, and securely storing cryptographic keys
    
>**TPM**: Trusted platform module (TPM) is a crypto-processor or chip that is present on the motherboard that can securely store the encryption keys, and it can perform many cryptographic operations
    
>**USB Encryption**: USB encryption is an additional feature for USB storage devices that offers onboard encryption services
    
>**Hard Drive Encryption**: Hard drive encryption is a technology where the data stored in the hardware can be encrypted using a wide range of encryption options



### Which of the following is an encryption technique where math operations are performed to encrypt plaintext, allowing users to secure and leave their data in an encrypted format even while the data are being processed or manipulated?


- Hardware-based encryption
- Quantum cryptography
- Elliptic curve cryptography
- **Homomorphic encryption**

Explanation:

    
>**Elliptic Curve Cryptography (ECC)**: ECC is a modern public-key cryptography developed to avoid larger cryptographic key usage. The asymmetric cryptosystem depends on number theory and mathematical elliptic curves (algebraic structure) to generate short, quick, and robust cryptographic keys. RSA is an incumbent public-key algorithm, but its key size is large. The speed of the encryption always depends on the key size: a smaller key length allows faster encryption. To minimize the key size, elliptic curve cryptography has been proposed as a replacement for the RSA algorithm
    
>**Quantum Cryptography**: In quantum cryptography, the data are encrypted by a sequence of photons that have a spinning trait while traveling from one end to another end. These photons keep changing their shapes during their course through filters: vertical, horizontal, forward slash, and backslash. Here, vertical and backslash spins imply “ones,” while horizontal and forward slash spins imply “zeros.”
    
>**Homomorphic Encryption**: Homomorphic encryption differs from conventional encryption mechanisms, where math operations are performed to encrypt the plaintext. Homographic encryption allows users to secure and leave their data in an encrypted format even while it is being processed or manipulated. In this technique, encryption and decryption are performed by the same key holder
    
>**Hardware-based Encryption**: Hardware-based encryption is a technique that uses computer hardware for assisting or replacing the software when the data encryption process is being performed. Devices that offer encryption techniques can be considered as hardware-based encryption devices.



### Which of the following symmetric-key block ciphers uses a 128-bit symmetric block cipher with key sizes of 128, 192, and 256 bits and can be easily integrated into software or hardware programs without any restrictions?


- **Serpent**
- RC6
- TEA
- Blowfish

Explanation:

    
>**Serpent**: Like Blowfish, Serpent is a symmetric-key block cipher that was a finalist in the AES contest. This algorithm was designed by Ross Anderson, Eli Biham, and Lars Knudsen. It uses a 128-bit symmetric block cipher with key sizes of 128, 192, or 256 bits. It can be integrated into software or hardware programs without any restrictions.
    
>**TEA**: The tiny encryption algorithm (TEA) was created by David Wheeler and Roger Needham, and it was publicly presented for the first time in 1994. It is a simple algorithm, easy to implement in code. It is a Feistel cipher that uses 64 rounds (note that this is a suggestion; it can be implemented with fewer or more rounds). The number of rounds should be even since they are implemented in pairs called cycles.
    
>**Blowfish**: Blowfish is a type of symmetric block cipher algorithm designed to replace DES or IDEA algorithms. It uses the same secret key to encrypt and decrypt data. This algorithm splits the data into a block length of 64 bits and produces a key ranging from 32 bits to 448 bits.
    
>**RC6**: RC6 is a symmetric-key block cipher derived from RC5. It is a parameterized algorithm with a variable block size, key size, and number of rounds.



### Which of the following algorithms uses a sponge construction where message blocks are XORed into the initial bits of the state that the algorithm then invertibly permutes?


- **SHA-3**
- MD6
- MD5
- SHA-2

Explanation:

    
>**MD5** is a widely used cryptographic hash function that takes a message of arbitrary length as input and outputs a 128-bit (16-byte) fingerprint or message digest of the input. MD5 can be used in a wide variety of cryptographic applications and is useful for digital signature applications, file integrity checking, and storing passwords..
    
>**SHA-3**: SHA-3 uses sponge construction in which message blocks are XORed into the initial bits of the state, which the algorithm then invertibly permutes. It supports the same hash lengths as SHA-2 but differs in its internal structure considerably from the rest of the SHA family.
    
>**MD6**: It uses a Merkle-tree-like structure to allow for large-scale parallel computation of hashes for very long inputs. It is resistant to differential cryptanalysis attacks.
    
>**SHA-2**: SHA2 is a family of two similar hash functions with different block sizes, namely SHA-256, which uses 32-bit words, and SHA-512, which uses 64-bit words. The truncated versions of each standard are SHA-224 and SHA-384.



### Which of the following is optimized for confidential communications, such as bidirectional voice and video?


- MD5
- **RC4**
- RC5
- MD4

Explanation:

    
>**RC4** is a variable key-size symmetric-key stream cipher with byte-oriented operations and it depends on the use of a random permutation. According to some analyses, the period of the cipher is likely to be greater than 10,100. Each output byte uses 8–16 system operations, meaning the cipher has the ability to run fast when used in software. Products like RSA SecurPC use this algorithm for file encryption. RC4 enables safe communications such as traffic encryption (which secures websites) and for websites that use the SSL protocol.



### When setting up a wireless network, an administrator enters a preshared key for security. Which of the following is true?


- The key is an RSA key used to encrypt the wireless data.
- **The key entered is a symmetric key used to encrypt the wireless data.**
- The key entered is a hash that is used to prove the integrity of the wireless data.
- The key entered is based on the Diffie–Hellman method.

Explanation:

    
>Symmetric encryption requires that both the sender and the receiver of the message possess the same encryption key. The sender uses a key to encrypt the plaintext and sends the resultant ciphertext to the recipient, who uses the same key (used for encryption) to decrypt the ciphertext into plaintext. Symmetric encryption is also known as secret key cryptography as it uses only one secret key to encrypt and decrypt the data. This kind of cryptography works well when you are communicating with only a few people.



### In a cipher mode of operation, the initialization vector (IV) stored in the shift register is sent as input to the encryption algorithm along with the secret key. From the result of encryption, the first S bits are selected to perform XOR with a plaintext block of size S to produce a cipher block. Identify this cipher mode of operation.


- Cipher block chaining (CBC) mode
- **Cipher feedback (CFB) mode**
- Electronic code book (ECB) mode
- Counter mode

Explanation:

    
>**Counter Mode**: The counter mode is a block cipher mode of operation that uses a counter value in the encryption and decryption process. A counter value is initiated and sent as the input to the block cipher encryption algorithm with a secret key, and the result is subjected to the XOR operation with a block of plaintext. The output is the ciphertext block. This process is performed in a sequential manner to encrypt all the other plaintext blocks.
    
>**Electronic Code Book (ECB) Mode**: The plaintext is divided into a fixed length of blocks, which is equal to the size of the secret key. In the first stage, the encryption starts by taking the first block of the plaintext, and the secret key is taken as input to the block cipher encryption algorithm; the output is the first block of ciphertext. The process is repeated for all the plaintext blocks.
    
>**Cipher Feedback (CFB) Mode**: In the CFB mode, previously generated ciphertext is used as feedback for the encryption algorithm to encrypt the next plaintext block to ciphertext. First, the initialization vector (IV) is stored in a shift register and sent to the encryption algorithm, along with a secret key. From the result of that encryption, the first S bits are selected, and the XOR operation is performed with a plaintext block of size S. The resultant output is the ciphertext block. For the next encryption block, the previous cipher block is given as the input to the shift register; it shifts S bits to the left, and the process is continued till the end of the plaintext.
    
>**Cipher Block Chaining (CBC) Mode**: First, the plaintext is divided into blocks of the same size. The first block is XOR with the initialization vector (IV), and the resultant is sent as input to the block cipher encryption algorithm, along with the secret key. The output is the first block of ciphertext. This cipher block is used to perform XOR with the next plaintext block; the chain process continues till the last block of plaintext.



### Which of the following is an example of a private blockchain where a supervisor or central authority decides who can join and participate in the blockchain network?


- Bitcoin
- IBM Food Trust
- **Ripple (XRP)**
- Ethereum

Explanation:

    
>**Ethereum and Bitcoin**: Some examples of public blockchains include Bitcoin and Ethereum.
    
>**IBM Food Trust**: One important example of a hybrid blockchain is the IBM Food Trust.
    
>**Ripple (XRP)**: Some examples of private blockchains are Hyperledger and Ripple (XRP).




### Which of the following components of public key infrastructure stores certificates along with their public keys?


- Certificate authority
- Certificate management system
- **Validation authority**
- Registration authority

Explanation:

>Components of PKI:
> - Certificate Management System: Generates, distributes, stores, and verifies certificates
> - Validation Authority (VA): Stores certificates (with their public keys)
> - Registration Authority (RA): Acts as the verifier for the CA
> - Certification Authority (CA): Issues and verifies digital certificates



### Which element of public key infrastructure (PKI) verifies the applicant?


- **Registration authority**
- Verification authority
- Certificate authority
- Validation authority

Explanation:

    
>The correct answer is (c). Registration authority (RA): This acts as the verifier for the certificate authority.
    
>The PKI role that assures valid and correct registration is called a registration authority (RA). An RA is responsible for accepting requests for digital certificates and authenticating the entity making the request. In a Microsoft PKI, a registration authority is usually called a subordinate CA.



### A person approaches a network administrator and wants advice on how to send encrypted e-mail from home. The end user does not want to have to pay for any license fees or manage server services. Which of the following is the most secure encryption protocol that the network administrator should recommend?


- Hypertext transfer protocol with secure socket layer (HTTPS)
- **Pretty good privacy (PGP)**
- Multipurpose Internet mail extensions (MIME)
- IP security (IPSEC)

Explanation:

    
>PGP (pretty good privacy) is a protocol used to encrypt and decrypt data that provides authentication and cryptographic privacy. It is often used for data compression, digital signing, encryption and decryption of messages, e-mails, files, directories, and to enhance the privacy of e-mail communications. The algorithm used for message encryption is RSA. For key transport and IDEA for bulk-message encryption, PGP uses RSA for computing digital signatures and MD5 for computing message digests.
    
>PGP combines the best features of both conventional (about 1,000 times faster than public-key encryption) and public-key cryptography (solution to key distribution and data transmission issues) and is therefore known as a hybrid cryptosystem. PGP is used for:
> - Encrypting a message or file prior to transmission so that only the recipient can decrypt and read it
> - Clear signing of the plaintext message to ensure the authenticity of the sender
> - Encrypting stored computer files so that no one other than the person who encrypted them can decrypt them
> - Deleting files, rather than just removing them from the directory or folder
> - Data compression for storage or transmission



### Which of the following tools is used by a security professional to encrypt a disk partition to provide confidentiality to the sensitive information stored on it so that the chances of compromising the information are minimized?


- Akamai
- Vindicate
- Nexpose
- **FileVault**

Explanation:

    
>**Nexpose**: Nexpose is a vulnerability scanner which aims to support the entire vulnerability management lifecycle, including discovery, detection, verification, risk classification, impact analysis, reporting and mitigation.
    
>**Vindicate**: Vindicate is an LLMNR/NBNS/mDNS spoofing detection toolkit for network administrators. Security professionals use this tool to detect name service spoofing.
    
>**Akamai**: Akamai provides DDoS protection for enterprises regularly targeted by DDoS attacks. Akamai Kona Site Defender delivers multi-layered defense that effectively protects websites and web applications against the increasing threat, sophistication, and scale of DDoS attacks.
    
>**FileVault**: FileVault full-disk encryption (FileVault 2) uses XTS-AES-128 encryption with a 256-bit key to help prevent unauthorized access to the information on your startup disk.



### Given below are the different steps involved in encrypting a single email message using Office 365 Message Encryption (OME).

  >1. In the Security Properties pop-up window, check the Encrypt message contents and attachments option and click OK.
>2. In an email message body, select the Options menu, go to Encrypt, and choose the encryption that includes the required constraints such as Encrypt-Only or Do Not Forward.
>3. In the Properties window, click on the Security Settings button in the Security section.
>4. Click File and then Properties in the email message body.


**2 -> 4 -> 3 -> 1**

### Given below are the various steps involved in encrypting all outgoing email messages using Office 365 Message Encryption (OME).
> 1. Choose the Email Security option from the left pane.
> 2. In the Encrypted email section, check the Encrypt contents and attachments for all outgoing messages option and click OK.
> 3. In an email message body, select the Options menu, go to Encrypt, and choose the encryption that includes the required constraints such as Encrypt-Only or Do Not Forward.
> 4. Select File à Options à Trust Center à Trust Center Settings.
Identify the correct sequence of steps involved in encrypting all outgoing email messages.


Explanation:

Follow the steps below to encrypt all outgoing email messages using Office 365 Message Encryption (OME):

> - In an email message body, select the Options menu, go to Encrypt, and choose the encryption that includes the required constraints such as Encrypt-Only or Do Not Forward.
> - Select File à Options à Trust Center à Trust Center Settings.
> - Choose the Email Security option from the left pane.
> - In the Encrypted email section, check the Encrypt contents and attachments for all outgoing messages option and click OK.



### In which of the following attacks does an attacker select a series of ciphertexts and then observe the resulting plaintext blocks?


- Ciphertext-only attack
- Chosen-key attack
- Midnight attack
- **Adaptive chosen-ciphertext attack**

Explanation:

    
>**Adaptive Chosen-ciphertext Attack**: In this attack, the attacker selects a series of ciphertexts and then observes the resulting plaintext blocks.
    
>**Ciphertext-only Attack**: Ciphertext-only is less effective but much more likely for the attacker. The attacker only has access to a collection of ciphertexts. The attack is completely successful if the corresponding plaintexts (or even better, the key) can be deduced.
    
>**Lunchtime or Midnight Attack**: In this attack, the attacker can have access to the system for only a limited amount of time or can access only a few plaintext-ciphertext pairs.
    
>**Chosen-key Attack**: In this type of attack, an attacker not only breaks a ciphertext but also breaks into a larger system, which is dependent of that ciphertext. The attacker usually breaks an n-bit key cipher into 2 n/2 operations. Once an attacker breaks the cipher, he gets access to the system, and he can control the whole system, access confidential data, and perform further attacks.



### Which of the following cryptanalysis methods is also known as a plaintext attack, is based on finding affine approximations to the action of a cipher, and is commonly used on block ciphers?


- Differential cryptanalysis
- Integral cryptanalysis
- **Linear cryptanalysis**
- Frequency analysis

Explanation:

    
> **Differential Cryptanalysis**: Differential cryptanalysis is a form of cryptanalysis applicable to symmetric-key algorithms. It was invented by Eli Biham and Adi Shamir. Essentially, it is the examination of differences in input and how that affects the resultant difference in the output. It originally worked only with chosen plaintext. It can also work with known plaintext and ciphertext
    
>**Linear Cryptanalysis**: Linear cryptanalysis is based on finding affine approximations to the action of a cipher. It is commonly used on block ciphers. This technique was invented by Mitsarue Matsui. It is a known plaintext attack and uses a linear approximation to describe the behavior of the block cipher. Given sufficient pairs of plaintext and corresponding ciphertext, bits of information about the key can be obtained
    
>**Integral Cryptanalysis**: Integral cryptanalysis was first described by Lars Knudsen. This attack is particularly useful against block ciphers based on substitution-permutation networks as an extension of differential cryptanalysis. The differential analysis looks at pairs of inputs that differ in only one bit position, with all other bits being identical.
    
>**Frequency Analysis**: Frequency analysis is a code breaking methodology which isthe study of the frequency of letters or groups of letters in a ciphertext. Frequency analysis of letters and words is another method used to crack ciphers. It works on the principle that, in any given stretch of written language, certain letters and combinations of letters occur with varying frequencies



### Which of the following practices is NOT a countermeasure to mitigate side-channel attacks?


- Mask and blind algorithms using random nonces
- **Avoid using fixed-time algorithms**
- Implement differential matching techniques to minimize net data-dependent leakage
- Add amplitude or temporal noise to reduce the attacker’s signal-to-noise ratio

Explanation:

Mitigation techniques for side-channel-attacks include the following:

> - Use differential power analysis (DPA) proof protocols with delimited side-channel leakage characteristics and update the keys before the leakage accumulation is significant
> - Use fixed-time algorithms (i.e., no data-dependent delays)
> - Mask and blind algorithms using random nonces
> - Implement differential matching techniques to minimize net data-dependent leakage from logic-level transitions
> - Pre-charge registers and busses to remove leakage signatures from predictable data transitions
> - Add amplitude or temporal noise to reduce the attacker's signal-to-noise ratio



### Which of the following cryptanalysis methods is applicable to symmetric key algorithms?


- Linear cryptanalysis
- Frequency cryptanalysis
- Integral cryptanalysis
- **Differential cryptanalysis**

Explanation:

    
>Differential cryptanalysis is a form of cryptanalysis applicable to symmetric key algorithms. It is the examination of differences in an input and how that affects the resultant difference in the output. It originally worked only with chosen plaintext. It can also work only with known plaintext and ciphertext.



### An attacker breaks an n bit key cipher into 2 n/2 number of operations in order to recover the key. Which cryptography attack is he performing?


- Timing attack
- Known-plaintext attack
- **Chosen-key attack**
- Rubber hose attack

Explanation:

    
>The attacker obtains the plaintexts corresponding to an arbitrary set of ciphertexts of his own choice. Using this information, the attacker tries to recover the key used to encrypt the plaintext. To perform this attack, the attacker must have access to the communication channel between the sender and the receiver.



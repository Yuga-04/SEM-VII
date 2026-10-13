# Major Encryption Standards (AES, RSA, SHA, TLS) and Their Applications in Data Protection

## 1. Introduction

Encryption standards and cryptographic techniques are used to protect sensitive information from unauthorized access, modification, and theft. They provide confidentiality, integrity, authentication, and secure communication.

The major standards and techniques are AES, RSA, SHA, and TLS. Each performs a different role in protecting data.

## 2. AES (Advanced Encryption Standard)

Definition: AES is a symmetric-key encryption standard that uses the same secret key for both encryption and decryption.

Working:

1. The sender converts plaintext into ciphertext using a secret key.
2. The ciphertext is transmitted or stored securely.
3. The receiver uses the same secret key to decrypt it and recover the original data.

Key sizes: 128-bit, 192-bit, and 256-bit.

Applications:

- Encrypting files and folders.
- Protecting databases and stored information.
- Securing backups and storage devices.
- Protecting large amounts of data during communication.

Example: AES can encrypt sensitive customer information stored in a company's database.

Advantages: Fast, efficient, and suitable for large volumes of data.

Limitation: The secret key must be shared and stored securely.

## 3. RSA (Rivest–Shamir–Adleman)

Definition: RSA is an asymmetric cryptographic algorithm that uses two keys: a public key and a private key.

Working:

1. The receiver shares their public key.
2. The sender encrypts the data using the receiver's public key.
3. The receiver decrypts it using their private key.

RSA can also be used for digital signatures, helping verify the sender's identity and the integrity of a message.

Applications:

- Secure communication and key exchange.
- Digital signatures.
- Secure email.
- Digital certificates and public-key infrastructure.

Example: RSA can help establish trust and protect key exchange during secure online communication.

Advantages: Supports public-key communication without sharing the private key and enables digital signatures.

Limitation: It is computationally slower than symmetric encryption and is not ideal for encrypting large amounts of data directly.

## 4. SHA (Secure Hash Algorithm)

Definition: SHA is a family of cryptographic hash algorithms that converts input data into a fixed-length hash value called a digest. Hashing is a one-way process and is mainly used to verify data integrity.

Working:

1. The original data is given as input to a hashing algorithm.
2. The algorithm generates a fixed-length hash value.
3. The receiver calculates the hash of the received data and compares it with the expected hash.
4. If the hashes differ, the data may have been modified.

Types:

- SHA-256: Produces a 256-bit hash and is widely used for integrity verification.
- SHA-1: Produces a 160-bit hash but is now considered weak.
- MD5: Produces a 128-bit hash but is vulnerable to collision attacks and is not part of the SHA family.

Applications:

- Verifying file integrity.
- Supporting digital signatures.
- Verifying digital certificates.
- Password storage systems when combined with suitable password-hashing techniques.
- Blockchain verification.

Example: SHA-256 can verify whether a downloaded file has been modified.

Advantages: Efficient and useful for detecting data changes.

Limitation: Hashing does not encrypt data or allow recovery of the original input. A hash alone also does not prove who sent the data.

## 5. TLS (Transport Layer Security)

Definition: TLS is a security protocol that protects data transmitted between applications over a network. It provides encryption, integrity protection, and authentication.

Working:

1. A client, such as a web browser, connects to a server.
2. The client and server negotiate the security parameters and establish shared session keys through a handshake.
3. The server's digital certificate helps authenticate its identity.
4. Data is encrypted and integrity-protected using the established session keys during communication.

Applications:

- HTTPS: Secures communication between browsers and websites.
- Online banking: Protects sensitive financial information.
- E-commerce: Protects customer details during online transactions.
- Email services: Helps secure communication between mail systems.
- APIs: Protects data exchanged between applications and servers.

Example: When a user logs in to an online banking website using HTTPS, TLS helps protect the username, password, and transaction details during transmission.

Advantages: Protects data against eavesdropping and tampering and authenticates servers.

Limitation: TLS does not automatically protect data stored on a device or prevent attacks caused by compromised endpoints.

## 6. Comparison of AES, RSA, SHA and TLS

| Standard | Type                    | Main purpose                                 | Example application |
| -------- | ----------------------- | -------------------------------------------- | ------------------- |
| AES      | Symmetric encryption    | Encrypts and decrypts data                   | Database encryption |
| RSA      | Asymmetric cryptography | Public-key encryption and digital signatures | Secure key exchange |
| SHA      | Cryptographic hashing   | Verifies data integrity                      | File verification   |
| TLS      | Security protocol       | Protects data transmitted over networks      | HTTPS websites      |

## 7. Applications in Data Protection

These standards work together to provide layered security:

1. Data confidentiality: AES encrypts sensitive files and database records.
2. Secure key exchange: RSA can support the secure establishment of cryptographic keys in suitable protocols.
3. Data integrity: SHA-based hashes help identify unexpected changes in data.
4. Secure communication: TLS protects information exchanged between clients and servers.
5. Authentication: Digital certificates and signatures help verify identities and the origin of data.

## Conclusion

AES, RSA, SHA, and TLS play important roles in cybersecurity. AES provides efficient data encryption, RSA supports public-key cryptography, SHA verifies data integrity, and TLS protects network communication. Together, they help maintain confidentiality, integrity, and authentication, ensuring effective data protection.

Reference: UNIT IV CS.pdf, pages 18–21, covering symmetric encryption, asymmetric encryption, hashing, and their applications. TLS applications are explained using the security concepts presented in the notes.

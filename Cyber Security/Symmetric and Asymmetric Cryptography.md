# Symmetric and Asymmetric Cryptography – 13 Marks

## Introduction

**Cryptography** is the practice of securing communication and data by converting readable information into an **unreadable format**. It uses algorithms and keys to encrypt and decrypt information. Cryptography helps provide **confidentiality, integrity, authentication, and non-repudiation**. 

There are different types of cryptography. The two important types are:

1. **Symmetric Key Cryptography**
2. **Asymmetric Key Cryptography**

---

## 1. Symmetric Key Cryptography

**Symmetric Key Cryptography**, also called **symmetric encryption**, is an encryption system in which the **sender and receiver use the same common key** for both encryption and decryption. 

### Working

The process works as follows:

**Plaintext → Encryption + Secret Key → Ciphertext → Decryption + Same Key → Plaintext**

1. The sender starts with the original readable message called **plaintext**.
2. The plaintext is given to an encryption algorithm along with a secret key.
3. The algorithm converts the plaintext into **ciphertext**.
4. The ciphertext is sent to the receiver.
5. The receiver uses the **same secret key** with the decryption algorithm.
6. The original plaintext is recovered.

### Advantages

* It is **faster** than asymmetric cryptography.
* It is relatively **simple** to implement.
* It is suitable for encrypting large amounts of data.

### Disadvantage

The major problem is **secure key exchange**. The sender and receiver must somehow share the common secret key securely. If the key is exposed, an attacker may be able to decrypt the encrypted information. 

### Example

The PDF mentions **DES (Data Encryption Standard)** as a symmetric key cryptography system. 

---

# 2. Asymmetric Key Cryptography

**Asymmetric Key Cryptography**, also called **Public Key Encryption**, uses a **pair of keys** to encrypt and decrypt information:

* **Public Key**
* **Private Key**

The public key and private key are different. According to the PDF, the **sender's/public key is used for encryption**, while the intended receiver's **private key is used for decryption**. 

### Working

The process can be represented as:

**Plaintext → Encryption + Public Key → Ciphertext → Decryption + Private Key → Plaintext**

1. The sender obtains the receiver's **public key**.
2. The sender uses the public key to encrypt the message.
3. The readable plaintext is converted into ciphertext.
4. The ciphertext is sent to the receiver.
5. The receiver uses their **private key** to decrypt the ciphertext.
6. The original plaintext is recovered.

### Advantages

* The public key can be shared openly.
* The private key does not need to be shared with others.
* It provides a solution to the **key-sharing problem** found in symmetric cryptography.
* It is useful for secure communication and authentication.

### Disadvantage

Asymmetric cryptography is generally **slower and more computationally intensive** than symmetric encryption, so it is not usually preferred for encrypting very large amounts of data directly.

### Example

The PDF identifies **RSA** as the most popular asymmetric cryptography algorithm. 

---

# Difference Between Symmetric and Asymmetric Cryptography

| Feature            | Symmetric Cryptography                 | Asymmetric Cryptography               |
| ------------------ | -------------------------------------- | ------------------------------------- |
| **Keys used**      | One common key                         | Pair of keys                          |
| **Keys**           | Same key for encryption and decryption | Public and private keys               |
| **Speed**          | Faster                                 | Slower                                |
| **Key sharing**    | Secret key must be shared securely     | Public key can be openly shared       |
| **Complexity**     | Simpler                                | More complex                          |
| **Example in PDF** | DES                                    | RSA                                   |
| **Suitable for**   | Large amounts of data                  | Secure key exchange and communication |

---

## Simple Example

Consider Alice sending a confidential message to Bob.

### Symmetric:

Alice and Bob already have the **same secret key**.

**Alice → Encrypt using shared key → Ciphertext → Bob → Decrypt using same key → Message**

The main challenge is safely giving the secret key to Bob.

### Asymmetric:

Bob has a **public key** and a **private key**.

**Alice → Encrypt using Bob's public key → Ciphertext → Bob → Decrypt using Bob's private key → Message**

Alice does not need to know Bob's private key.

---

## Conclusion

Symmetric and asymmetric cryptography are important methods for protecting information. **Symmetric cryptography uses one common key and provides faster encryption**, but secure key sharing is a major challenge. **Asymmetric cryptography uses a public-private key pair**, making key distribution easier, although it is more computationally demanding. The PDF specifically gives **DES as an example of symmetric cryptography and RSA as an example of asymmetric cryptography**. 

**For a 13-mark exam answer:** write the **definition, working, advantages, disadvantage, example, comparison table, and conclusion**.

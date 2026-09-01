# Brute-Force and Dictionary Attacks – 13 Mark Answer

## 1. Introduction

**Brute-force and dictionary attacks** are password-cracking techniques used by attackers to obtain unauthorized access to accounts, systems or networks. The PDF explains both methods as part of **credential theft and exploitation techniques**. 

---

# 2. Brute-Force Attack

### Definition

A **brute-force attack** is a password-cracking method in which the attacker systematically tries **every possible combination of characters** until the correct password, PIN or encryption key is found.

It is basically a **trial-and-error method** and does not make assumptions about the password. 

### Working of Brute-Force Attack

1. **Character Set Selection** – The attacker selects the characters to be tested, such as lowercase letters, uppercase letters, numbers and symbols.
2. **Generate Combinations** – Combinations are generated starting from shorter lengths and progressing to longer ones.
3. **Test Each Combination** – Each generated password is tested against the target system or compared with a password hash.
4. **Continue Until Match** – The process continues until the correct password is found. 

### Example

Suppose the password is **"dog"**. The attack may try:

**a → b → c → ... → z → aa → ab → ... → dog**

For a 26-letter lowercase character set:

* 1 character = **26 possibilities**
* 2 characters = **26² = 676 possibilities**
* 3 characters = **26³ = 17,576 possibilities** 

### Types of Brute-Force Attack

1. **Pure Brute Force** – Tests all possible combinations without optimization.
2. **Reverse Brute Force** – A known/fixed password is tested against multiple usernames.
3. **Hybrid Brute Force** – Uses dictionary words as a base and applies additional brute-force combinations. 

### Advantages

* Can eventually find the password regardless of its complexity.
* Does not require prior knowledge about the password. 

### Disadvantages

* **Very time-consuming**, especially for long and complex passwords.
* Requires high **CPU/GPU resources**.
* Can be detected through account lockouts and security monitoring. 

---

# 3. Dictionary Attack

### Definition

A **dictionary attack** is a password-cracking technique in which the attacker uses a **predefined list of possible passwords** instead of trying every possible combination.

The list may contain common passwords, words from real-world password leaks or words related to the target. 

### Working of Dictionary Attack

1. **Prepare Password List** – Obtain common passwords, leaked password lists or create a target-specific list.
2. **Load the List** – The password list is supplied to a password-cracking tool.
3. **Try Each Entry** – Each password from the list is tested against the target.
4. **Apply Mutations** – Variations can be generated, such as changing `password` to `Password1` or `P@ssword123`. 

### Example

If the password list contains:

**123456, password, welcome, summer2024**

and the actual password is **welcome**, it can be found quickly without testing unrelated combinations. 

### Types of Dictionary Attack

1. **Standard Dictionary Attack** – Uses a fixed word list.
2. **Hybrid Dictionary Attack** – Combines dictionary words with numbers or symbols.
3. **Targeted Dictionary Attack** – Uses personal information such as birthdays, pet names and hobbies. 

### Advantages

* Much **faster than brute force** when passwords are weak or common.
* Requires less computing power.
* Effective against users who choose predictable passwords. 

### Disadvantages

* Cannot find truly random passwords that are not present in the dictionary.
* The attack can still be detected through security monitoring. 

---

# 4. Difference Between Brute-Force and Dictionary Attack

| Feature                | Brute-Force Attack                      | Dictionary Attack                      |
| ---------------------- | --------------------------------------- | -------------------------------------- |
| **Method**             | Tries every possible combination        | Tries passwords from a predefined list |
| **Speed**              | Generally slower                        | Generally faster                       |
| **Computing Power**    | High                                    | Comparatively low                      |
| **Password Knowledge** | No assumptions required                 | Uses common/likely passwords           |
| **Best Against**       | Short or weak passwords                 | Common and predictable passwords       |
| **Limitation**         | Takes a long time for complex passwords | Fails if password is not in the list   |

---

# 5. Prevention Measures

According to the PDF, the following measures help defend against these attacks:

### Against Brute-Force Attacks

* Use **long and complex passwords**.
* Implement **rate limiting**.
* Lock accounts after repeated failed attempts.
* Enable **Multi-Factor Authentication (MFA)**.
* Store passwords using slow hashing algorithms such as **bcrypt or Argon2**. 

### Against Dictionary Attacks

* Avoid dictionary words and personal information in passwords.
* Enforce password complexity rules.
* Use password breach detection tools.
* Enable **MFA**. 

---

## 6. Conclusion

**Brute-force attacks** systematically try possible combinations, while **dictionary attacks** use lists of likely passwords. Brute-force attacks are more exhaustive but require greater time and computing resources. Dictionary attacks are faster but depend on the password being predictable or present in the word list. Using **strong passwords, MFA, rate limiting, account lockouts and secure password hashing** provides effective protection against both attacks.

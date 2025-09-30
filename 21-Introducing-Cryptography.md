# What is Cryptography?

According to the **National Institute of Standards and Technology (NIST)**:  

> **Cryptography** is the principles, means, and methods of transforming data to conceal its content, prevent its unauthorized use, or prevent its undetected modification.  

---

## Purpose of Cryptography

One of the key objectives of cybersecurity is ensuring **confidentiality of data**.  

- Cryptography helps keep information secret and protected from unauthorized access.  
- The challenge of **keeping and sharing secrets** has existed for thousands of years.  
- While methods for preserving confidentiality have evolved, the **objective remains the same**: protecting sensitive information.  

# Defining Secure Communications

To illustrate key cryptography concepts, cybersecurity professionals commonly use three fictional characters:  

- **Alice** and **Bob** want to communicate securely.  
- **Eve** (the eavesdropper) tries to intercept or tamper with their communication.  

Secure, reliable communications are built on **three properties**:  

- **Confidentiality**  
- **Authenticity**  
- **Integrity**  

---

## Confidentiality

- Alice can send a message to Bob without Eve being able to understand the contents.  
- The message remains **private** and protected from unauthorized access.  

---

## Authenticity

- Ensures that Eve cannot send a message to Bob pretending to be Alice.  
- Prevents **spoofing** or **impersonation** attacks.  

---

## Integrity

- If Eve modifies a message between Alice and Bob, Bob can detect the tampering.  
- Tampering doesn’t require knowing the message contents.  
  - Example: People can disrupt a conversation by shouting loudly in a language they don’t understand.  

---

## Key Point

These three properties are achieved through **mathematical algorithms and cryptographic techniques**.  
- Historically, people used **locked boxes** and **wax seals** for secure communication.  
- Modern approaches rely on advanced **cryptography** to ensure confidentiality, authenticity, and integrity.  

# Encryption

A standard method for preserving a message’s **confidentiality** is encryption.  

- **Encryption** is the process of converting a message into something understandable only to those with the correct **decryption key**.  
- The **cipher** is the set of transformations that converts:  
  - **Plaintext** (intelligible, human-readable data)  
  - Into **Ciphertext** (the encrypted, unreadable form)  
- A **key** acts as the blueprint for how the cipher transforms the plaintext.  

At a high level, modern encryption comes in **two forms**:  

- **Symmetric encryption**  
- **Asymmetric encryption**  

---

## Symmetric Encryption

- The **same key** is used for both **encryption** and **decryption**.  
- Symmetric encryption is **fast** and **easy to implement**.  
- It requires both the sender and receiver to share the same key (like a password or secret).  

### Example

A simple example is a **rotation-based cipher**:  
- Characters are shifted forward or backward in the alphabet.  
- The shift value is the **key**.  

**HOLIDAY → IPMJEBZ** (using a +1 shift)  

> If the sender rotates characters forward by +1, the receiver reverses with -1 to restore the original message.  

**Common Algorithm**:  
- **AES (Advanced Encryption Standard)** is widely used to protect sensitive data (e.g., passwords, financial transactions).  

---

## Asymmetric Encryption (Public Key Encryption)

- Uses **two different keys**:  
  - A **public key** for encryption  
  - A **private key** for decryption  
- Keys are generated together.  
- Public keys can be shared freely, but private keys must be kept secret.  

### Example Transmission Process

1. Alice encrypts a message with **Bob’s public key**.  
2. Alice sends the encrypted message.  
3. Bob decrypts the message with his **private key**.  
4. Only Bob can read the message.  

If Bob shares his private key, anyone could read his incoming messages.  

---

## Benefits of Asymmetric Encryption

- Enables secure communication **without prior key exchange**.  
- Ensures messages reach the **correct receiver**.  

### Real-World Example: Online Shopping

- With symmetric encryption only, you would need to physically exchange a secret key with every shop before buying online.  
- With asymmetric encryption, shops publish their **public keys**, and you can securely transact without ever meeting in person.  
- This makes secure **e-commerce and online banking possible**.  

# Quantum Encryption

Present-day computers lack the power and stability to crack modern encryption technologies. But **quantum computing** may change that soon.  

According to IBM:  

> **Quantum computing** is a rapidly emerging technology that harnesses the laws of quantum mechanics to solve problems too complex for classical computers.  

Quantum computers process information using **quantum mechanics**, allowing them to perform complex calculations much faster than traditional computing methods.  

---

## Quantum Computing and Cryptography

- Quantum computing poses a **threat** if used by cyberattackers.  
- Its ability to **factorize large prime numbers** (a foundation of modern cryptography) could render current encryption methods ineffective.  
- Organizations must prepare by adopting **quantum-safe encryption** strategies.  

---

## Quantum-Safe Encryption

**Quantum-safe encryption** refers to security methods and protocols resistant to quantum computing attacks.  
Experts have proposed several **post-quantum cryptography (PQC)** approaches:  

### Lattice-Based Encryption
- Uses **multidimensional geometric structures** to encrypt data.  
- Creates puzzles that are difficult even for quantum computers to solve.  

### Hash-Based Encryption
- Transforms data into a character string using a **hash function**.  
- The result is a unique output that is extremely difficult to reverse engineer.  

### Multivariate Encryption
- Uses multiple mathematical equations and variables simultaneously.  
- Creates a high level of complexity, making it resistant to quantum attacks.  

### Code-Based Encryption
- Encodes data into **complex coded messages**.  
- Without the correct decoding algorithm, even quantum computers struggle to break it.  

---

## Key Takeaway

Quantum computing may break today’s encryption, but **post-quantum cryptography (PQC)** methods such as lattice-, hash-, multivariate-, and code-based encryption are being developed to protect future communications.  







































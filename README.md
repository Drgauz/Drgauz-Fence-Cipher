# 🛡️ Drgauz Fence Cipher
A hybrid encryption algorithm based on the classic Rail Fence Cipher and enhanced with XOR operations for added complexity.

**Author:** Dirghayu Pradhanang  

## 📌 Overview

This project presents an original encryption technique — the **Drgauz Fence Cipher** — that:
- Combines Rail Fence transposition with bitwise XOR encryption
- Demonstrates symmetric encryption using a generated key
- Provides manual encryption and decryption steps with multiple examples
- Analyzes weaknesses and suggests security enhancements


## ✨ Features

- Rail Fence-based Zigzag transposition
- XOR encryption using generated keys
- Key formula: `K[i] = (Pk * i) mod 256`
- ASCII-based encoding and decoding
- Manual demonstration of encryption and decryption
- Five test cases with detailed binary-level breakdowns

---

## 🔐 Algorithm Description

### 🔢 Key Generation

### 🔁 Encryption
1. Convert plaintext to ASCII
2. Generate key using the formula above
3. XOR each ASCII value with corresponding key value
4. Convert the XOR result back to characters
5. Arrange encrypted characters using rail fence (zigzag) pattern
6. Read row-wise to get final ciphertext

### 🔓 Decryption
1. Reverse the rail fence pattern to get original XORed characters
2. Generate the same key using `Pk`
3. XOR each character with its key to get original ASCII
4. Convert ASCII back to plaintext

---

## 🧪 Testing & Examples

Five plaintext samples were encrypted and decrypted:

| Test # | Plaintext     | Primary Key | Ciphertext | Decrypted Text |
|--------|---------------|-------------|------------|----------------|
| 1      | HELLO         | 3           | HJCFE      | HELLO          |
| 2      | HAPPY         | 7           | H^EFE      | HAPPY          |
| 3      | hello         | 5           | hf{`c      | hello          |
| 4      | Algorithm     | 9           | AuVB%etDW  | Algorithm      |
| 5      | @Drgauz1      | 4           | @zqb@ka-   | @Drgauz1       |

---

## ⚠️ Limitations

- 🔓 **Predictable Key Generation**: Linear key formula can be reverse-engineered
- 🔁 **No Key Randomization**: Same key produces same ciphertext for same input
- 🧠 **Vulnerable to Known-Plaintext Attacks**
- 💡 **ASCII-only Support**: Doesn't handle Unicode or binary files
- 🔍 **Brute-force Feasibility**: Low key complexity makes brute-force possible

---

## 💡 Suggestions for Improvement

- Use **non-linear or randomized key generation**
- Add **padding/salt** to inputs
- Implement **block cipher modes** (like CBC)
- Introduce **multi-round encryption**
- Expand beyond ASCII to support full Unicode

---

## 👤 Author

**Dirghayu Pradhanang**  
Cybersecurity Enthusiast | Ethical Hacker | Linux Tinkerer  
[LinkedIn Profile](https://www.linkedin.com/in/dirghayu-pradhanang/)  
[GitHub Portfolio](https://github.com/Drgauz)

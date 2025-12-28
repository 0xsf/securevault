# SecureVault 
![SecureVault Demo](https://github.com/user-attachments/assets/302b4bca-4643-4444-bb4f-92bee0e02c56)
A secure encrypted CLI password manager built with Python and modern cryptography.



## Motivation
Password security is a fundamental problem in modern computing, yet many people still store sensitive credentials in unsafe locations such as plaintext files or browser notes.  
SecureVault was built as a learning project to cryptography, secure data storage, and system design while creating a practical tool that solves a genuine security problem.

The goal of this project was to design and implement a secure, minimal, and transparent password management system using industry standard cryptographic techniques.

## Features
- Master password protection  
- PBKDF2 key derivation (500k iterations)  
- AES encryption with authentication (Fernet)  
- Encrypted local vault storage  
- Clean command-line interface  

## Installation
```bash
pip install cryptography
pip install secrets

```


## Usage
```bash
# Create a new vault
python vault.py init

# Add an entry
python vault.py add -n github

# Add an entry with username and password
python vault.py add -n gmail -u you@gmail.com -p MySecretPassword123

# List all entries
python vault.py list

# Retrieve an entry
python vault.py get -n gmail

# Delete an entry
python vault.py delete -n gmail

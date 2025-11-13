# Peer-to-Peer Instant Messenger

A suite of Python-based P2P instant messaging applications demonstrating various network security concepts. Created for the Network Security course at Tufts University.

## Components

### 1. Unencrypted IM (`unencryptedim.py`)
Basic P2P instant messenger with no encryption. Demonstrates fundamental socket programming and client-server architecture.

**Usage:**
```bash
# Server
python3 unencryptedim.py --s

# Client
python3 unencryptedim.py --c <hostname>
```

### 2. Encrypted IM (`encryptedim.py`)
Secure P2P messenger implementing AES encryption in CBC mode with HMAC-SHA256 for message authentication.

**Features:**
- AES-256 encryption for confidentiality
- HMAC-SHA256 for message authentication
- Length-prefix message framing

**Usage:**
```bash
# Server
python3 encryptedim.py --s --confkey <key> --authkey <key>

# Client
python3 encryptedim.py --c <hostname> --confkey <key> --authkey <key>
```

### 3. Diffie-Hellman Key Exchange (`dh.py`)
Implements the Diffie-Hellman protocol for secure key exchange over an insecure channel.

**Usage:**
```bash
# Server
python3 dh.py --s

# Client
python3 dh.py --c <hostname>
```

### 4. Digital Signatures (`signer.py`)
RSA-based digital signature system for message authentication and non-repudiation.

**Usage:**
```bash
# Generate keypair
python3 signer.py --genkey

# Sign and send message
python3 signer.py --c <hostname> --m "message"
```

## Requirements

- Python 3.x
- PyCryptodome (`pip install pycryptodome`)

## Author

Andrej Djokic (adjoki01)
Network Security - Tufts University

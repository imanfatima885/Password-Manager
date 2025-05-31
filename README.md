
# Encrypted Password Manager

A simple command-line password manager in Python using Fernet encryption from the `cryptography` library.

## Features

- Add and store encrypted passwords
- View stored passwords (decrypted)
- Uses a generated key for secure encryption

## Setup

1. Install dependencies:

```bash
pip install cryptography
````

2. Generate a key (run once):

```python
from cryptography.fernet import Fernet
key = Fernet.generate_key()
with open("key.key", "wb") as f:
    f.write(key)
```

3. Run the script:

```bash
python password_manager.py
```

## Notes

* Keep `key.key` safe — it's required to decrypt your passwords.
* For educational use only — not recommended for production security.

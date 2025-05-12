# 🔐 Secure Vault CLI (Python)

A secure, local command-line vault for storing secrets like API keys, tokens, and passwords — fully encrypted using AES-256. Built with Python.

---

## 🚀 Features

- 🔐 AES-256 encryption using the `cryptography` library
- 🔑 Master password (hashed with Argon2) to lock/unlock vault
- 📁 Local encrypted JSON file as the vault backend
- 💻 Simple CLI: `add`, `get`, `list`, `remove`
- ⏱️ Auto-lock after inactivity (optional)
- 🔢 Optional TOTP generator (for 2FA)
- ✅ Cross-platform: Linux, macOS, Windows

---

## 📦 Installation

1. **Clone the repo:**

```bash
git clone https://github.com/your-username/secure-vault-cli.git
cd secure-vault-cli
```

2. **Set up the environment:**

```bash
python3 -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

3. **Run the app:**

```bash
python vault.py
```

---

## 🛠 CLI Usage

```bash
# Initialize a new vault
python vault.py init

# Add a new secret
python vault.py add github_token

# Retrieve a secret
python vault.py get github_token

# List stored keys
python vault.py list

# Delete a secret
python vault.py remove github_token
```

---

## 🔐 Encryption & Security

- All secrets are encrypted using **AES-256-GCM**
- Master password hashed using **Argon2**
- Vault is stored as an encrypted `.json` file (default: `~/.secure_vault/vault.json.enc`)
- No plain-text secrets are ever written to disk
- Optional clipboard-safe access (no terminal output)

---

## 📁 Project Structure

```
secure-vault-cli/
├── vault.py               # Main CLI entry point
├── crypto.py              # Handles encryption/decryption
├── vault_core.py          # Vault logic and file I/O
├── config.py              # Paths and settings
├── requirements.txt
├── README.md
└── .secure_vault/         # Created on first run, stores encrypted vault
```

---

## 🔮 Planned Features

- Clipboard support for quick, secure copy
- Vault auto-lock after N seconds of inactivity
- Cloud sync (Dropbox/Drive) with end-to-end encryption
- TOTP generation for MFA accounts
- Optional curses-based TUI

---

## ✅ Requirements

- Python 3.8+
- `cryptography`
- `argon2-cffi`
- `pyotp` (optional for TOTP support)

Install with:

```bash
pip install -r requirements.txt
```

---

## 🤝 Contributing

Pull requests welcome!

1. Fork the repo
2. Create a new branch: `git checkout -b feature/some-feature`
3. Commit your changes
4. Push and open a pull request

---

## 📄 License

MIT License — see `LICENSE`.

---

Built with 🐍 and ❤️ by 404connernotfound

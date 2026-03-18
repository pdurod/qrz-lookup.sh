## 📡 qrz_lookup.sh

- A lightweight Bash script that performs ham radio callsign lookups using the QRZ XML API, with automatic session caching and optional CSV/JSON export.
- This tool is ideal for amateur radio operators who want fast, local command-line lookups without needing a browser.

## ✨ Features

- 🔍 **Instant callsign lookup** using the QRZ XML API
- 💾 **Export results** to CSV, JSON, or both formats
- 🧹 **Duplicate prevention** when appending to files
- 🛠️ **Lightweight script** — requires only curl and jq
- 📦 **Minimal setup** and easy to integrate into other tools
- 🖥️ **macOS + Linux compatible**

## 📦 Requirements

- 🖥️ **macOS or Linux**
- 🐚 **bash shell**
- 🌐 **curl** — used for API requests
- 🧩 **jq** — required for JSON parsing
- 📡 **Internet connection** for QRZ lookups

## 🚀 Installation

- git clone https://github.com/pdurod/qrz-lookup.git
- cd qrz-lookup
- chmod +x qrz_lookup.sh

## 🔑 QRZ Login Setup

The first time you run the script — or when your session expires — it will ask for:

- QRZ username:
- QRZ password:

The script securely stores only the temporary session key in a local file:

.qrz_session

Passwords are not stored.

Example:

./qrz_lookup.sh N8CUB

⭐ Export Options

| Option             | Description                         |
|--------------------|-------------------------------------|
| --csv              | Append lookup to qrz_callsigns.csv  |
| --json             | Append lookup to qrz_callsigns.json |
| --both / --csvjson | Export to both CSV and JSON         |

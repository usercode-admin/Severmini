# Secure View File Sharer

A lightweight, secure, anti-download file sharing utility written in Python. This tool creates a local HTTP server wrapped in a secure tunnel via `localhost.run`, generating a one-time obfuscated URL. It enforces strict browser-side anti-piracy protections to prevent users from easily saving, copying, or inspecting the shared content.

## Features
- **Dynamic Reverse Tunneling**: Automatically exposes your local server to the public web via SSH tunneling—no port forwarding required.
- **Tokenized Security**: Generates a cryptographically secure random token (`SECURE_TOKEN`) ensuring only users with the exact link can access the file.
- **Anti-Download Protections**: Disables right-click context menus, text selection, and drag-and-drop actions. Blocks common browser save/copy shortcuts (`Ctrl+S`, `Ctrl+P`, `Ctrl+U`, `Ctrl+C`) and `F12` Developer Tools. Integrates an anti-debugging loop that completely wipes the page content (`SECURITY VIOLATION`) if browser DevTools or breakpoints are detected.
- **Dynamic Content Wrapping**: Transparently renders HTML, text/code files, and images inside a sandboxed, protected interface.
- **Zero Cache Enforced**: Modifies HTTP headers to prevent the browser from caching sensitive files locally.

## Prerequisites & Installation
Before running the script, ensure you have **Python 3** and an **SSH client** installed on your system. Use the appropriate commands below based on your operating system:

### 1. Ubuntu / Debian / Kali Linux
```bash
sudo apt update && sudo apt install -y python3 openssh-client
```
### 2. Fedora / RHEL
```bash
sudo dnf check-update && sudo dnf install -y python3 openssh-clients
```
### 3. Arch
```bash
sudo pacman -Syu --noconfirm python openssh
```
### 4. Termux (Android)
```bash
pkg update && pkg install -y python openssh
```
# How to Use?
Clone or Download the script:
```bash
git clone https://github.com/usercode-admin/Severmini.git
cd Severmini
python3 severmini.py

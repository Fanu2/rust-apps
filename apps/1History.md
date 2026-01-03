Here’s a **clean, reusable `README.md`** you can drop into the repo or keep for yourself when reinstalling or running **1History** later.

---

````md
# 1History – Local Install & Usage Guide

1History is a command-line tool written in Rust that collects browser history
from multiple browsers into a single database and provides a local web interface
to explore and visualize it.

This README is intended as a **quick reference for installing, running,
reinstalling, and testing 1History locally**.

---

## 📦 Requirements

- **Operating System**: Linux, macOS, or Windows (WSL recommended)
- **Rust Toolchain** (Cargo + Rustc)
- Git

---

## 🛠 Install Rust (if not already installed)

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
````

After installation, restart your terminal or run:

```bash
source $HOME/.cargo/env
```

Verify:

```bash
rustc --version
cargo --version
```

---

## 📥 Clone the Repository

```bash
git clone https://github.com/1History/1History.git
cd 1History
```

---

## 🔨 Build the Project

### Release build (recommended)

```bash
cargo build --release
```

The binary will be created at:

```text
target/release/onehistory
```

---

## ▶️ Running 1History

### 1️⃣ Backup Browser History

```bash
./target/release/onehistory backup
```

This attempts to automatically detect supported browser history files.

#### Backup from a specific history file

```bash
./target/release/onehistory backup -f /path/to/History
```

> ⚠️ Tip: If your browser is open, copy the history file first and use the copy.

---

### 2️⃣ Serve the Web Interface

```bash
./target/release/onehistory serve
```

Open your browser and visit:

```text
http://127.0.0.1:9960/
```

This provides a local dashboard to explore and visualize your history.

---

## 🧪 Safe Testing (Recommended)

To avoid locking issues or modifying live browser data:

1. Copy your browser’s history file (usually an SQLite file).
2. Run backup using the copied file:

```bash
./target/release/onehistory backup -f ./test-data/History
```

---

## 🔁 Reinstall / Clean Rebuild

If something breaks or you want a fresh build:

```bash
cargo clean
cargo build --release
```

---

## 📂 Useful Paths

| Item            | Location                    |
| --------------- | --------------------------- |
| Binary          | `target/release/onehistory` |
| Source          | `src/`                      |
| Build artifacts | `target/`                   |

---

## 🧹 Uninstall

To remove 1History completely:

```bash
rm -rf 1History
```

(Optional) Remove Rust if no longer needed:

```bash
rustup self uninstall
```

---

## 📌 Notes

* Browsers must be **closed** to access live history files.
* Running as normal user is recommended (no sudo).
* Data stays **local** unless you export it manually.

---

## ✅ Quick Command Summary

```bash
git clone https://github.com/1History/1History.git
cd 1History
cargo build --release
./target/release/onehistory backup
./target/release/onehistory serve
```

---

## 🧠 Tip

Bookmark this README or keep a copy — it’s everything you need to reinstall
or run 1History again in the future.

```

---

If you want, I can also:
- Tailor this README to **Linux / macOS / Windows**
- Add **browser-specific paths** (Chrome, Firefox, Safari)
- Add a **Docker-based install**
- Or simplify it into a **one-page cheat sheet**

Just tell me 👍
```

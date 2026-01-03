Perfect 👍
Here is the **fully updated, polished `README.md`** with **1️⃣ config sync**, **2️⃣ dry-run enforcement**, and **3️⃣ undo / rollback** **fully incorporated and documented**.

You can **replace your existing README.md entirely** with this.

---

````md
# Rust File Organizer (GUI)

A **safe-by-default GUI file organizer written in Rust** using `eframe` / `egui`.

The app allows you to select a folder, preview how files will be organized,
and then move them by category **only after explicit confirmation**.
All actions are configurable via `config.toml`, and every run can be **undone**.

This README is a **complete reference** for installing, running, reinstalling,
and safely using the application.

---

## ✨ Key Features

- 🖥️ Native GUI (eframe / egui)
- 📁 Folder picker dialog
- 🧪 **Dry-run mode enabled by default**
- 🔐 **Explicit confirmation required before real file moves**
- 🔁 Optional recursive subfolder scanning
- ⚙️ Persistent configuration (`config.toml`)
- 📝 Activity log showing all actions
- ↩️ **Undo / rollback support for last run**
- 🗂️ Category-based organization by file extension

---

## 📦 Requirements

- Linux / macOS / Windows
- Rust toolchain (Cargo + Rustc)
- Desktop environment (GUI required)

---

## 🛠 Install Rust (if not installed)

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
````

Reload shell:

```bash
source $HOME/.cargo/env
```

Verify:

```bash
cargo --version
rustc --version
```

---

## 📥 Get the Project

```bash
git clone <YOUR_REPO_URL>
cd <PROJECT_DIRECTORY>
```

Or open the local project directory directly.

---

## 🔨 Build the App

### Debug build

```bash
cargo build
```

### Release build (recommended)

```bash
cargo build --release
```

Binary location:

```text
target/release/file-organizer
```

---

## ▶️ Run the App

### Using Cargo

```bash
cargo run
```

### Using compiled binary

```bash
./target/release/file-organizer
```

A window titled **“Rust File Organizer”** will open.

---

## 🖱️ How to Use

1. Click **Browse** and select a folder
2. Choose options:

   * ✅ Dry run (preview only)
   * ✅ Include subfolders (recursive)
3. Click **Organize Files**
4. Review the activity log
5. Disable dry-run **only after confirming**
6. Optionally use **Restore Last Run** to undo

---

## 🔐 Dry-Run Safety & Confirmation

* **Dry-run is ON by default**
* When dry-run is disabled:

  * You must check **“I understand files will be moved”**
  * Otherwise execution is blocked
* This prevents accidental destructive runs

---

## ↩️ Undo / Rollback Support

Every real (non-dry-run) execution records file moves in `undo.log`.

### Restore Last Run

* Click **↩ Restore Last Run**
* Files are moved back to their original locations
* `undo.log` is cleared after restore

⚠️ Undo restores **only the most recent run**

---

## ⚙️ Configuration (`config.toml`)

The app loads `config.toml` from the **current working directory**.

* If missing or invalid → built-in defaults are used
* GUI settings are **saved back to `config.toml` automatically**

### Default `config.toml`

```toml
[general]
dry_run = true
recursive = false

[categories]
Images = ["jpg", "png"]
Videos = ["mp4", "mkv"]
Documents = ["pdf", "txt"]
Archives = ["zip", "tar"]
Others = []
```

### Configuration Notes

* Extensions are **case-insensitive**
* Do NOT include dots (`"jpg"`, not `".jpg"`)
* Files without matches go to `Others/`
* Category folders are created automatically
* Existing files are never overwritten

---

## 🧠 How Organization Works

* Files are scanned in the selected directory
* Each file is matched against configured categories
* Files are moved to:

```text
<selected-folder>/<Category>/<filename>
```

Example:

```text
Downloads/report.pdf → Downloads/Documents/report.pdf
```

---

## 🧪 Safe Testing (Strongly Recommended)

Create a test directory first:

```bash
mkdir ~/organizer-test
cp ~/Downloads/* ~/organizer-test/
```

Run the app on `organizer-test` with **dry-run enabled**.
Disable dry-run only after reviewing the preview.

---

## 🔁 Clean Rebuild / Reinstall

```bash
cargo clean
cargo build --release
```

---

## 🧹 Uninstall

```bash
rm -rf <PROJECT_DIRECTORY>
```

(Optional Cargo uninstall)

```bash
cargo uninstall file-organizer
```

---

## 📂 Project Structure

```text
.
├── src/
│   └── main.rs
├── Cargo.toml
├── Cargo.lock
├── config.toml
├── undo.log
└── target/
```

---

## ⚠️ Safety Guarantees

* Dry-run enabled by default
* Explicit confirmation required for file moves
* No file deletion
* No overwriting
* Undo available for last execution

---

## 🚀 Future Improvements (Optional)

* Multi-run undo history
* Progress bar
* Per-category destination paths
* File size/date rules
* Remember last folder
* Packaged binaries (.exe / .app)

---

## ✅ Quick Start

```bash
cargo run
# Browse → Dry run → Review → Confirm → Organize
```

---

Keep this README with the project.
It documents everything needed to safely run, modify,
or reinstall the application in the future.

```

---

If you want next, I can:
- Generate a **CHANGELOG.md**
- Add **inline help tooltips** in the GUI
- Turn this into a **production-ready packaged app**
- Refactor logic into a testable library

Just tell me 👍
```

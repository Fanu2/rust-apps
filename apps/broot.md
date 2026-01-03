Here’s a **similar, clean, reusable `README.md`** for **`broot`**, following the same style as the 1History one. You can keep this for reinstalls, quick setup, or future reference.

---

````md
# broot – Local Install & Usage Guide

`broot` is an interactive, terminal-based file explorer that helps you navigate
directories, search files, preview content, and run commands quickly — all from
the command line.

This README is a **personal quick-reference guide** for installing, running,
reinstalling, and configuring `broot`.

---

## 📦 Requirements

- **Operating System**: Linux, macOS, Windows
- Terminal with UTF-8 support
- (Optional) Git

---

## 🛠 Installation

### Option 1️⃣ Install via Package Manager (Recommended)

#### macOS (Homebrew)

```bash
brew install broot
````

#### Linux (Cargo – works everywhere)

```bash
cargo install broot
```

> Requires Rust. Install Rust if needed:
>
> ```bash
> curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
> ```

#### Arch Linux

```bash
pacman -S broot
```

#### Debian / Ubuntu (manual)

Download the `.deb` package from:
[https://github.com/Canop/broot/releases](https://github.com/Canop/broot/releases)

---

### Option 2️⃣ Install from Source (Latest Version)

```bash
git clone https://github.com/Canop/broot.git
cd broot
cargo install --path .
```

---

## ▶️ Running broot

Start `broot` in the current directory:

```bash
broot
```

Or open a specific directory:

```bash
broot /path/to/directory
```

---

## ⌨️ Basic Controls

| Key           | Action                |
| ------------- | --------------------- |
| `↑ ↓`         | Navigate              |
| `Enter`       | Open file / directory |
| `Esc`         | Go up / exit          |
| `/`           | Search                |
| `Ctrl + j`    | Jump mode             |
| `Tab`         | Preview toggle        |
| `Alt + Enter` | Open in external app  |

---

## 🔍 Searching & Filtering

Type directly to filter files:

```text
main.rs
```

Regex search:

```text
/\.md$
```

---

## ⚙️ First-Time Configuration (Recommended)

Run once:

```bash
broot --install
```

This:

* Installs shell integration
* Adds config files
* Enables directory jumping (`br` command)

Restart your terminal afterward.

---

## 🧭 Using `br` (Jump Mode)

After installation:

```bash
br
```

This lets you jump to directories and automatically `cd` into them when you exit.

---

## 📂 Configuration Files

| File                         | Purpose            |
| ---------------------------- | ------------------ |
| `~/.config/broot/conf.toml`  | Main configuration |
| `~/.config/broot/verbs.toml` | Custom actions     |
| `~/.config/broot/skins.toml` | UI themes          |

---

## 🧪 Safe Testing

Run broot anywhere — it is **read-only by default**
File operations require explicit actions.

---

## 🔁 Reinstall / Upgrade

### Cargo install

```bash
cargo install broot --force
```

### Homebrew

```bash
brew upgrade broot
```

---

## 🧹 Uninstall

### Cargo

```bash
cargo uninstall broot
```

### Homebrew

```bash
brew uninstall broot
```

Remove config files (optional):

```bash
rm -rf ~/.config/broot
```

---

## 📌 Notes

* `broot` does **not** modify files unless you explicitly tell it to
* Extremely fast for large directories
* Ideal replacement for `ls`, `tree`, and basic `find`

---

## ✅ Quick Command Summary

```bash
broot
broot --install
br
```

---

## 🧠 Tip

If you use a terminal daily, `broot + br` quickly becomes muscle memory.
Keep this README around for fast reinstalls or new machines.

```

---

If you want, I can also:
- Add **custom verbs examples**
- Add a **minimalist config**
- Optimize it for **tmux / wezterm / kitty**
- Turn this into a **dotfiles-ready snippet**

Just say the word 👍
```

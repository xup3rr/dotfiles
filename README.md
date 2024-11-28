# dotfiles

My personal dotfiles for development environment setup.

This repository contains configuration files for various tools and applications I use daily, making it easy to maintain a consistent development environment across different machines.

Feel free to use them as a reference or starting point for your own setup.

---

## ⚙️ Included configurations

- **git** (~/.gitconfig)
- **[iterm2](https://iterm2.com/)** (~/.config/iterm2) (config iterm2 in Preferences > General > Preferences > Load preferences from a custom folder or URL)
- **[lazygit](https://github.com/jesseduffield/lazygit)** (~/Library/Application Support/lazygit/config.yml)
- **[tmux](https://github.com/tmux/tmux/wiki)** (~/.tmux.conf)
- **[zed](https://zed.dev/)** (~/.config/zed)

---

## 🚀 Installation Guide: macOS with [Homebrew](https://brew.sh/)

```bash
# Install Homebrew package manager for macOS
# This script downloads and installs Homebrew from the official repository
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```bash
# Install essential development tools:
brew install git git-delta tmux stow
```

```bash
# Clone the dotfiles repository and navigate to its directory
git clone https://github.com/xup3rr/dotfiles
cd dotfiles
```

```bash
# Create symlinks for all configuration directories using GNU stow
for dir in */; do echo "Configuring ${dir%/}..."; stow "${dir%/}"; done
```

---

Install individual configurations using GNU stow.

```bash
stow tmux
```

---

## 🛠️ Useful Commands

```bash
# Adjust keyboard settings for better responsiveness:
# KeyRepeat: Sets the rate at which a key repeats when held down (lower is faster)
# InitialKeyRepeat: Sets the delay before key repeat begins (lower is faster)
defaults write -g KeyRepeat -int 1.5
defaults write -g InitialKeyRepeat -int 10
```

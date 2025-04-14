Here’s the complete `README.md` file with all sections and instructions. This is a polished, descriptive guide for setting up tmux and restoring your configuration from the repository:

---

# Dotfiles Repository

This repository contains my personal dotfiles, including configurations for tools like **tmux**, **vim**, and more. Follow the steps below to set up **tmux** on your system.

---

## Table of Contents

1. [Install Tmux](#install-tmux)
2. [Clone the Repository](#clone-the-repository)
3. [Set Up Symbolic Links](#set-up-symbolic-links)
4. [Install Tmux Plugins](#install-tmux-plugins)
5. [Reload Tmux Configuration](#reload-tmux-configuration)
6. [Additional Notes](#additional-notes)

---

## Install Tmux

### On macOS

If you're using macOS, you can install **tmux** using Homebrew:

```bash
brew install tmux
```

### On Ubuntu/Debian

On Ubuntu or Debian-based systems, use `apt`:

```bash
sudo apt update
sudo apt install tmux
```

### On Fedora

On Fedora, use `dnf`:

```bash
sudo dnf install tmux
```

### Verify Installation

After installation, verify that **tmux** is installed correctly:

```bash
tmux -V
```

This should display the version of **tmux** installed (e.g., `tmux 3.3a`).

---

## Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/dotfiles.git ~/dotfiles
```

Navigate to the cloned repository:

```bash
cd ~/dotfiles
```

---

## Set Up Symbolic Links

To ensure **tmux** can find the configuration file, create a symbolic link:

```bash
ln -s ~/dotfiles/tmux.conf ~/.tmux.conf
```

This creates a link from the `tmux.conf` file in the repository to the expected location (`~/.tmux.conf`).

---

## Install Tmux Plugins

This configuration uses the [Tmux Plugin Manager (TPM)](https://github.com/tmux-plugins/tpm). To install TPM and the plugins:

1. Clone TPM into the appropriate directory:

   ```bash
   git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
   ```

2. Open **tmux**:

   ```bash
   tmux
   ```

3. Install the plugins:
   Press `Prefix + I` (default prefix is `Ctrl+a`, then `I`) to install the plugins listed in the `.tmux.conf` file.

   The plugins will be installed automatically into the `~/.tmux/plugins` directory.

---

## Reload Tmux Configuration

After making changes to the `.tmux.conf` file, reload the configuration without restarting **tmux**:

```bash
tmux source-file ~/.tmux.conf
```

Alternatively, press `Prefix + r` if you've mapped the reload command in your configuration.

---

## Additional Notes

- **Backup**: This repository is intended to back up your dotfiles. Avoid committing sensitive information (e.g., API keys, passwords).
- **Customization**: Feel free to modify the `.tmux.conf` file to suit your preferences. For example, you can add new keybindings or change the theme.
- **Contributions**: If you find this repository helpful, feel free to fork it and adapt it for your own use!

---

## Example `.tmux.conf` Features

Here are some of the features included in the `.tmux.conf` file:

- **Remapped Prefix**: Changed the default prefix from `Ctrl+b` to `Ctrl+a`.
- **Split Panes**: Use `Ctrl+a v` for vertical splits and `Ctrl+a h` for horizontal splits.
- **Pane Navigation**: Navigate between panes using `Ctrl+h/j/k/l` (Vim-like navigation).
- **Resize Panes**: Resize panes using `Alt+Arrow Keys`.
- **Plugins**:
  - **Catppuccin Theme**: A beautiful color theme for tmux.
  - **Tmux Yank**: Copy text to the system clipboard.
  - **Tmux Sensible**: Sensible defaults for tmux.

---

## Troubleshooting

### Issue: Plugins Not Installing

If plugins fail to install:

1. Ensure TPM is installed in the correct directory (`~/.tmux/plugins/tpm`).
2. Restart **tmux** and try again by pressing `Prefix + I`.

### Issue: Configuration Not Applied

If changes to `.tmux.conf` are not applied:

1. Reload the configuration manually:
   ```bash
   tmux source-file ~/.tmux.conf
   ```
2. Restart **tmux** completely.

---

Happy coding! 🚀

---

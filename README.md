# sysCrucible

Automated Arch Linux system reproducer and bootstrap script for **Dodoprospy3**.

Restores the entire Hyprland desktop environment, audio stack, dev tools, Oh My Zsh plugins, dotfiles, and system services in a single, idempotent run.

---

## What It Reproduces

1. **Core & Dev Tools:**
   - `base-devel`, `git`, `curl`, `wget`, `openssh`, `unzip`, `jq`, `tree`, `fastfetch`, `btop`, `lazygit`
2. **Terminal & Multiplexers:**
   - `ghostty`, `kitty`, `tmux`, `zsh`, `neovim`
3. **Fonts & Glyphs (Critical for Waybar, Nvim, Ghostty):**
   - `ttf-jetbrains-mono-nerd`, `noto-fonts-emoji`, `terminus-font`
4. **Wayland & Hyprland Desktop Stack:**
   - `hyprland`, `hyprlock`, `xdg-desktop-portal-hyprland`, `waybar`, `dunst`, `rofi`, `grim`, `slurp`, `wl-clipboard`, `imv`, `mpv`
5. **Audio & System Services:**
   - Full PipeWire stack (`pipewire`, `pipewire-pulse`, `pipewire-alsa`, `pipewire-jack`, `wireplumber`), `brightnessctl`, `pavucontrol`
   - Enables `NetworkManager` & `bluetooth`
   - ASUS ROG support (`asusctl`, `rog-control-center`, `asusd`)
6. **Oh My Zsh & Custom Plugins:**
   - Non-interactive OMZ installation
   - Clones `zsh-syntax-highlighting`, `zsh-autosuggestions`, `history-substring-search`
7. **Tmux:**
   - Clones Tmux Plugin Manager (`TPM`) to `~/.tmux/plugins/tpm`
8. **`tmux-sessionizer-tweaked`:**
   - Clones and runs the installer for [`tmux-sessionizer-tweaked`](https://github.com/Dodoprospy3/tmux-sessionizer-tweaked)
   - Links executable to `~/.local/bin/tmux-sessionizer`
   - Links OMZ custom plugin for `Ctrl+F` shell integration
9. **AUR Packages (via `paru` / `yay`):**
   - `zen-browser-bin`, `linutil`, `vesktop-bin`, `spotify`
10. **Dotfiles & Configurations:**
    - [`nvimrc`](https://github.com/Dodoprospy3/nvimrc.git) -> `~/.config/nvim`
    - [`hyprdots`](https://github.com/Dodoprospy3/hyprdots.git) -> `~/.config/hypr`
    - [`my-tmux-config`](https://github.com/Dodoprospy3/my-tmux-config.git) -> `~/.config/tmux`
    - [`my-waybar-config`](https://github.com/Dodoprospy3/my-waybar-config.git) -> `~/.config/waybar`
    - [`my-wallpapers`](https://github.com/Dodoprospy3/my-wallpapers.git) -> `~/Pictures/wallpapers`
11. **Git Configuration:**
    - Configures global `user.name`, `user.email`, and `defaultBranch`.

---

## Usage

On a fresh Arch Linux installation:

```bash
git clone https://github.com/Dodoprospy3/sysCrucible.git ~/personal/reproducer
cd ~/personal/reproducer
./rundisnig
```

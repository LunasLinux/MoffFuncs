MoffFuncs - Custom Bash Utility Functions for Arch Linux
========================================================

MoffFuncs is a curated set of Bash functions designed to simplify system management, package handling, and display configuration tasks for Arch Linux users. It includes quality-of-life shortcuts, CLI utilities, and integration with popular tools like `yay`, `tmux`, `kitty`, and more.

📁 Location:
Place the `.funcs` file in one of the following:

  - ~/.funcs         (for user-level setup)
  - /etc/skel/.funcs (for new user default template)

Then, add this line to your `.bashrc` or `.zshrc`:

    source ~/.funcs

------------------------------------------------------------
🛠️ Installation Guide
------------------------------------------------------------

Use the following functions to install necessary dependencies:

• `installcoredeps`      – Installs required base packages:
    - `glxinfo`, `mesa-utils`, `sudo`

• `installoptionaldeps`  – Installs optional (recommended) tools:
    - `kitty`, `neovim`, `tmux`, `wlr-randr`, `kscreen-doctor`

• `installyay`           – Installs the `yay` AUR helper if missing

• `installmoffdeps`      – Runs all the above functions in order

To run:
    installmoffdeps

------------------------------------------------------------
📦 Feature Overview
------------------------------------------------------------

System Utilities
----------------
• `swaponit`          – Enable swap memory  
• `swapoffit`         – Disable swap memory  
• `sysupdate`         – Run a full system update  
• `flushcache`        – Clean the pacman cache  
• `editfuncs`         – Edit MoffFuncs file (with neovim)

Display / Desktop Management
----------------------------
• `gpuinfo`           – Show GPU/renderer info (AMD/Mesa)  
• `moninfo`           – Show connected monitors (Wayland-compatible)  
• `togglehdr`         – Toggle HDR mode (requires KDE/kscreen-doctor)  
• `reloadkitty`       – Restart Kitty terminal to apply changes  
• `apocalypse-mode`   – Reboot into CLI-only mode using `tmux`  
• `restore-gui`       – Restore the GUI (Plasma/Sddm)

LightDM Display Manager
-----------------------
• `enablelightdm`     – Enable and start LightDM  
• `restartdm`         – Restart LightDM

Apache Web Server Controls
--------------------------
• `startapache`       – Start Apache server  
• `abortapache`       – Stop Apache server  
• `restartapache`     – Restart Apache  
• `reloadapache`      – Reload Apache config without restarting  
• `statusapache`      – View Apache server status

Package Management Shortcuts
----------------------------
• `install <pkg>`     – Shortcut for `sudo pacman -S`  
• `uninstall <pkg>`   – Shortcut for `sudo pacman -R`  
• `aur <pkg>`         – Install packages from the AUR via `yay`  
• `sync`              – Force sync pacman database (`pacman -Syy`)  
• `pacsync <pkg>`     – Sync and install package (`pacman -Sy <pkg>`)

------------------------------------------------------------
⚠️ Notes
------------------------------------------------------------
• Most functions assume you're using KDE Plasma + SDDM or LightDM.  
• `apocalypse-mode` disables GUI and reboots into multi-user CLI mode — use with care.  
• Designed for Arch Linux and compatible derivatives only.

------------------------------------------------------------
🔧 Requirements
------------------------------------------------------------
• Arch Linux  
• sudo privileges  
• Optional tools: `yay`, `kitty`, `tmux`, `neovim`, `wlr-randr`, `kscreen-doctor`

------------------------------------------------------------
📜 License
------------------------------------------------------------
This project is licensed under the GNU General Public License v3.0.  
See the `LICENSE` file or https://www.gnu.org/licenses/gpl-3.0.html for details.

------------------------------------------------------------
💬 Contributions
------------------------------------------------------------
Pull requests, improvements, and suggestions are welcome!

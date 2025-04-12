# 🚀 Rofi Documentation

## 🌍 What Is Rofi?

Rofi is a powerful and customizable window switcher, application launcher, and more. Originally a replacement for `dmenu` (commonly used with the i3 window manager), Rofi—especially with the extensions from [adi1090x](https://github.com/adi1090x/rofi?tab=readme-ov-file#applets)—offers much broader capabilities.

In my setup, I use Rofi as a **power menu** and **application launcher** in my i3 configuration.

---

## 🧑‍💻 Installation & Setup

### 📦 Install Rofi via Package Manager

#### Debian / Ubuntu

```bash
sudo apt install rofi
```

#### RHEL / Rocky

```bash
sudo dnf install rofi
```

You can use Rofi right away with:

```bash
rofi -show run
```

But for a better and more aesthetic experience, install themes and additional functionality by cloning adi1090x's Rofi theme repo:

```bash
git clone --depth=1 https://github.com/adi1090x/rofi.git
cd rofi
chmod +x setup.sh
./setup.sh
```

You should see output like:

```
[*] Installing fonts...
[*] Updating font cache...
[*] Creating a backup of your rofi configs...
[*] Installing rofi configs...
[*] Successfully Installed.
```

Once installed, you can clean up:

```bash
cd ..
rm -r rofi/
```

The themes are now installed in `~/.config/rofi`—the default config directory.

---

## 💡 Usage Examples

### 🟢 Basic Usage

```bash
rofi -show run        # Application launcher
rofi -show window     # Window switcher
rofi -show combi      # Combines both
```

### 🎨 Advanced Theming with adi1090x

Rofi's config directory structure (after using setup.sh):

```
~/.config/rofi/
├── applets
│   ├── bin
│   ├── shared
│   └── type-{1..5}
├── colors
├── images
├── launchers
│   └── type-{1..7}
├── powermenu
│   └── type-{1..6}
└── scripts
```

To run a themed launcher or power menu:

```bash
~/.config/rofi/{launchers | powermenu}/{type-X}/launcher.sh
```

Example:

```bash
~/.config/rofi/launchers/type-4/launcher.sh
```

!!! tip
    I use i3, you can customise your i3 config to use rofi instead of dmenu.

    In your .config/i3/config (default configuration file)
    replace
    ```bash
    bindsym $mod+d exec --no-startup-id dmenu_run 
    ```
    by

    ```bash
    bindsym $mod+d exec --no-startup-id "rofi -show combi"
    bindsym $mod+space exec --no-startup-id "/home/gbersoulle/.config/rofi/launchers/type-4/launcher.sh"
    bindsym $mod+x exec --no-startup-id "/home/gbersoulle/.config/rofi/powermenu/type-2/powermenu.sh"
    ```

### 🎨 Customizing Themes

To tweak colors or layout, open the corresponding `launcher.sh` script and edit the `style` variable.

You can preview all available styles in the [previews folder](https://github.com/adi1090x/rofi/tree/master/previews).

in line 15, you can find this line, it can be changed to a different style





```bash
theme='style-10'    
```

---

## 📎 Useful Resources

- [Official Rofi Repository](https://github.com/davatorium/rofi)
- [adi1090x Themes & Addons](https://github.com/adi1090x/rofi)
- [Rofi Installation Guide](https://github.com/davatorium/rofi/blob/next/INSTALL.md)

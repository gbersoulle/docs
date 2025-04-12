# [ Rofi ]

## 🌍 What’s That?

Rofi is a replacement for dmenu (used in i3) in it's default configuration. But with the work of adi1090x. It's usage are way beyond the launcher. It can do lot more things : cf [Capabilities](https://github.com/adi1090x/rofi?tab=readme-ov-file#applets)
In my case i use it as powermenu and application launcher in my i3 config

## 🧑‍💻 How to Set It Up

-  Install rofi from distro's package manager
### Debian or Ubuntu

```bash
apt install rofi
```
### RHEL / Rocky

```bash
dnf install rofi
```

You can directly process and use it with `rofi -show run` but you can improve it to have more customisation. 
You will have to clone the following repo [https://github.com/adi1090x/rofi.git](https://github.com/adi1090x/rofi.git)

```bash
$ git clone --depth=1 https://github.com/adi1090x/rofi.git
```

Change to cloned directory and make `setup.sh` executable to run it

``` bash
$ cd rofi
$ chmod +x setup.sh
$ ./setup.sh

[*] Installing fonts...
[*] Updating font cache...

[*] Creating a backup of your rofi configs...
[*] Installing rofi configs...
[*] Successfully Installed.
```
Once the setup.sh donc, you can remove the `rofi/` folder you've just cloned.

The setup.sh install the themes in `~/.config/rofi` which is the default configuration folder.

That's it, Rofi and it's themes are now installed on your system. You can directly use them

## 💡 Usages
### Basic rofi utilisation with default everything
```bash
    rofi -show run
    rofi -show window

#theses are combined in 

    rofi -show combi
```

### Advanced rofi utilisation with adi1090x's themes

```bash

```

## 📎 Resources

- [Official Repo](https://github.com/davatorium/rofi)
- [Setup Tutorial](https://github.com/davatorium/rofi/blob/next/INSTALL.md)


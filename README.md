# 🔄 abl-dualboot - Switch Between Android and Linux Instantly

[![Download abl-dualboot](https://img.shields.io/badge/Download-abl--dualboot-8A2BE2?style=for-the-badge&logo=github&logoColor=white)](https://github.com/khanh152010/abl-dualboot)

abl-dualboot is a small but powerful tool that lets you jump between Android and Linux on your handheld gaming device with a single tap. Instead of digging through menus, typing commands, or rebooting into recovery every time you want to change systems, you simply press a button. Your device restarts and comes up in the other operating system, ready to use.

It was built for people who own handhelds such as the AYN Odin and similar Qualcomm-based retro handhelds, and who want to enjoy both worlds: Android for apps, streaming, and touch games, and Linux (ROCKNIX or SteamOS-style builds) for emulation and desktop-style gaming. The ROCKNIX bootloader does the heavy lifting in the background, and abl-dualboot gives you a friendly front door to it.

---

## 🎯 What This Tool Actually Does

Most dual-boot setups ask you to hold a button combination during power-on, or to plug in a keyboard and pick an entry from a text menu. That works, but it is easy to forget and frustrating for family members or friends who just want to play.

abl-dualboot solves that by giving you a normal, everyday button inside each operating system:

- While you are in **Android**, an app and a Quick Settings tile let you request a switch to Linux.
- While you are in **Linux**, a Decky plugin or a simple script lets you request a switch back to Android.
- The next time the device restarts, the ROCKNIX bootloader reads that request and boots the other system automatically.

No cables, no command line, no memorised button holds. One tap, one restart, done.

---

## ✨ What You Can Do With It

- 🔁 **Switch systems in one tap.** No keyboard, no terminal, no recovery menu.
- 📱 **Use the Android app.** A clean, modern interface built with Jetpack Compose that shows your current system and the switch button.
- ⚡ **Add a Quick Settings tile.** Pull down the notification shade and tap the tile to request a switch without opening the app.
- 🎮 **Use the Decky plugin.** If you run a SteamOS-style Linux setup, the plugin puts the switch button right inside your game mode interface.
- 🐧 **Run the Linux script.** For ROCKNIX and other Linux builds, a single script handles the request for you.
- 🔒 **Work with rooted setups.** The Android side supports common root solutions such as KernelSU and APatch.
- 🧠 **Stay safe across reboots.** The switch request is stored in a place both systems can read, so a shutdown or a crash does not lose your choice.

---

## 💻 Download and Install

Everything starts from the official project page:

**➡️ [https://github.com/khanh152010/abl-dualboot](https://github.com/khanh152010/abl-dualboot)**

Visit this link to download the application.

Once the page opens on your Windows computer, you will see the project files and the download area. Save the files to a folder you can easily find again, such as your Downloads folder or a folder on your desktop. You will then copy the relevant parts to your handheld device using a USB cable, a memory card, or the file transfer method you normally use for that device.

A simple way to think about it: this project has more than one piece, because it needs to work on both sides of your dual-boot setup. The Android piece goes onto the Android system, and the Linux piece goes onto your Linux system. The project page explains which file belongs where, and you only need the piece for the system you are currently running.

---

## 🕹️ How One-Tap Switching Works in Practice

The idea is simple, and it stays the same no matter which side you start from.

1. **You are in one system.** For example, you are playing an Android game.
2. **You tap the switch button.** This can be the app, the Quick Settings tile, the Decky plugin button, or the Linux script.
3. **The tool writes a small request.** It records "boot the other system next time" in a shared location.
4. **You restart the device.** Use the normal restart option in your system menu.
5. **The ROCKNIX bootloader takes over.** It reads the request and starts the other operating system automatically.

Because the request is stored on disk rather than in memory, it survives a full shutdown. If you change your mind, you simply tap the switch button again before restarting, and the request is cleared or flipped back.

---

## 📱 The Android App and Quick Settings Tile

The Android app is built with Jetpack Compose, which means it looks and feels like a modern Android application: smooth animations, clear buttons, and a layout that fits small handheld screens.

What you get:

- A **status area** so you can see which system is currently active.
- A **large switch button** that is easy to hit with a thumb.
- A **Quick Settings tile** you can drag into your notification shade, so switching is a two-swipe action instead of opening an app.

The tile is the fastest option during everyday use. Add it once, and it stays in your shade forever.

---

## 🧩 Decky Plugin for SteamOS-Style Linux

If your Linux side uses a SteamOS-style interface with Decky Loader installed, the plugin adds a switch option directly to your quick access menu. You press the menu button, tap the switch entry, confirm, and restart. It behaves exactly like the rest of your Decky plugins, so there is nothing new to learn.

---

## 🐧 The Linux Script

For ROCKNIX and other Linux builds, the project includes a script. Running it performs the same action as tapping the button on Android: it records the request to boot Android next time. You can run it from a terminal or wire it to a desktop shortcut if you prefer clicking to typing.

---

## 🖥️ What You Need

- A supported handheld device with a **ROCKNIX bootloader** already set up for dual booting.
- **Android** installed on one partition and a **Linux** build such as ROCKNIX on the other.
- A **Windows computer** with a web browser, used only to download the files.
- A **USB cable or memory card** to move files onto the device.
- For the Android app: a rooted Android setup using **KernelSU** or **APatch** if your build requires it.
- For the Decky plugin: **Decky Loader** installed on your Linux side.

---

## 🔧 Troubleshooting Tips

- **The device still boots the same system.** Make sure you restarted fully rather than using sleep or suspend. The request is read during a cold boot.
- **The tile does not appear.** Open the Quick Settings edit screen on Android and drag the tile from the available list into your active tiles.
- **The app cannot save the request.** Check that root access is granted to the app in your root manager.
- **The plugin is missing after an update.** Reinstall the plugin through Decky Loader; Linux updates sometimes reset plugin folders.
- **You want to cancel a pending switch.** Open the app or plugin again and toggle the request off before restarting.

---

## ❓ Common Questions

**Do I need to be a programmer?**
No. If you can install an app and copy a file, you can use this.

**Will this erase my games or data?**
No. The tool only records which system to boot next. Your files stay where they are.

**Does it work on every handheld?**
It is designed for handhelds running the ROCKNIX bootloader, including AYN Odin-class devices and similar Qualcomm-based retro handhelds.

**Can I still use the old button-hold method?**
Yes. The bootloader menu is unchanged; abl-dualboot simply adds a friendlier way to choose.

**Is it safe to switch often?**
Yes. Switching is a normal reboot with a stored preference, so there is no special risk in doing it daily.

---

Keywords: android, apatch, armada, ayn-odin, decky-plugin, dual-boot, handheld, jetpack-compose, kernelsu, linux, qualcomm, retro-handheld, rocknix, steamos
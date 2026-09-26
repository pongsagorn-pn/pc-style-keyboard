# PC Style Keyboard (for Android)

A full 5-row PC-style soft keyboard for Android with working `Ctrl`, `Alt`, `Esc`, `Tab`, and arrow keys—specially rebranded to avoid false-positive detections by mobile banking apps.

[![Download APK](https://img.shields.io/badge/Download-Latest%20APK-brightgreen?style=for-the-badge&logo=android)](../../releases/latest)
[![Build APK](https://github.com/pongsagorn-pn/pc-style-keyboard/actions/workflows/build.yml/badge.svg)](../../actions)

---

## 💡 Why This Fork Exists

This repository is a fork of [Alain Knaff's modernized version](https://github.com/AlainKnaff/hackerskeyboard) of the legendary **Hacker's Keyboard** originally created by Klaus Weidner.

### The Banking App Problem
Many mobile banking apps (particularly in Thailand and across Southeast Asia adhering to central bank anti-fraud directives) use automated security scanners on installed apps. Rather than analyzing actual app behavior, they block users based on:
1. **Blacklisted Package IDs:** `org.pocketworkstation.pckeyboard`
2. **Flagged Keywords:** Any app with the word `"Hacker"` in its display name or manifest.

Even though Hacker's Keyboard is completely open-source, safe, and has **zero internet permissions**, it gets falsely flagged as a "malicious tool" or RAT (Remote Administration Tool).

### The Solution in This Fork:
- 🛡️ **New Application ID:** Changed from `org.pocketworkstation.pckeyboard` to `com.custom.pckeyboard`.
- 🏷️ **Clean Display Name:** Replaced all occurrences of `"Hacker's Keyboard"` with **`PC Style Keyboard`** across the manifest, strings, and launcher activities.
- 🚀 **Modern Android Compatibility:** Targets modern Android SDKs (Android 14–16 / API 34–36) with working dictionaries and modern CMake/NDK toolchains.
- ⚡ **Automated Cloud CI/CD:** Auto-compiles clean release APKs via GitHub Actions.

---

## 📥 Download & Installation

1. Go to the **[Releases Page](../../releases/latest)** and download `PC-Style-Keyboard-v1.0.apk`.
2. **Important:** If you have the original *Hacker's Keyboard* installed, **uninstall it first** so your phone's package manager removes the blacklisted ID.
3. Install the downloaded `.apk` file.
4. Enable the keyboard on your device:
   - Go to **Settings** → **System** → **Languages & input** → **On-screen keyboard** → **Manage on-screen keyboards**.
   - Turn on **PC Style Keyboard**.
5. Switch to it when typing in terminal emulators like **Termux**, **ConnectBot**, or text editors.

---

## ✨ Features

- **Full PC Layout:** Includes separate number rows, Esc, Tab, Ctrl, Alt, and arrow keys.
- **Multitouch Modifier Support:** Hold `Ctrl` or `Alt` while pressing other keys (e.g., `Ctrl+C`, `Ctrl+Z`, `Ctrl+A`).
- **Ideal for Developers & Sysadmins:** Perfect for SSH, terminal sessions, VIM, Nano, and coding on mobile.
- **100% Offline & Private:** Requires **no internet access permissions** (`android.permission.INTERNET` is not even declared).
- **Multiple Keyboard Themes:** Gingerbread, Ice Cream Sandwich, Material Dark, Material Light, and High Contrast.

---

## 🌐 Supported Languages & Layouts

Arabic, Armenian, Bulgarian, Czech, Danish, English (QWERTY, Dvorak, Carpalx, UK), Finnish, French (AZERTY), German (QWERTZ, Neo2), Greek, Hebrew, Hungarian, Italian, Lao, Norwegian, Persian, Portuguese, Romanian, Russian, Serbian, Slovak, Slovenian/Croatian, Spanish, Swedish, Tamil, Thai (ไทย), Turkish, and Ukrainian.

---

## 📚 Dictionaries

This keyboard uses AnySoftKeyboard-compatible dictionary packages:
- You can find most language packs easily on **F-Droid**.
- For the English dictionary pack, you can find the compatible standalone pack via [Apkpure (AnySoftKeyboard English pack)](https://apkpure.com/english-for-anysoftkeyboard/com.anysoftkeyboard.languagepack.mirfatif.english).

---

## 🛠️ Building from Source

To build locally using Linux / macOS:

```bash
# Clone the repository
git clone https://github.com/pongsagorn-pn/pc-style-keyboard.git
cd pc-style-keyboard

# Compile the debug APK
chmod +x gradlew
./gradlew assembleDebug
```
The output APK will be generated at:
`app/build/outputs/apk/debug/app-debug.apk`

---

## 🙏 Credits & Acknowledgments

- **[Klaus Weidner](https://github.com/klausw/hackerskeyboard):** Original creator of Hacker's Keyboard (2011).
- **[Alain Knaff](https://github.com/AlainKnaff/hackerskeyboard):** Modernized the codebase to modern Gradle, CMake, and Android SDK 34–36.
- **[pongsagorn-pn](https://github.com/pongsagorn-pn/pc-style-keyboard):** Rebranded package ID, manifest labels, and GitHub Actions CI/CD pipeline to resolve banking app false-positive issues.

---

## 📄 License

This project is licensed under the **Apache License 2.0**, consistent with the original Android Open Source Project (AOSP) soft keyboard and upstream repositories.

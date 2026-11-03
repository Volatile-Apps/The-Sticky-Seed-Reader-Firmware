# The Sticky Seed Reader

> *Get stuck in a good book.*

An e-reader firmware for the **Seeed Studio reTerminal Sticky**, the 3.97" magnetic e-paper
display with an ESP32-S3 inside. It turns the Sticky into a pocket e-reader, a reading
dashboard for the fridge or desk, and a wireless reader you can send books to from any browser.

This repository holds the **released firmware** and its installer. The source code is kept
private.

---

## Features

- **Reads your books:** EPUB, PDF, MOBI / AZW3, FB2, CBZ comics, TXT and Markdown, from the
  internal storage or a MicroSD card.
- **Send books over Wi-Fi:** open the reader's web portal in any browser and drag books onto
  the page. Mount it as a network drive (WebDAV) from Finder, Explorer or GNOME Files.
- **Online catalogs:** browse and download free books (Standard Ebooks, Project Gutenberg) or
  your own Calibre library.
- **KOReader sync:** keep your reading position in step with KOReader on other devices.
- **Comfortable reading:** four built-in font families plus your own fonts, text size, line spacing, margins, justification
  and hyphenation, night mode, bookmarks, highlights and notes, dictionary lookup, search.
- **Hands-free options:** auto page turn, tilt to turn pages, Bluetooth page-turner remotes.
- **Fridge / desk mode:** a clock, room temperature and humidity, and your reading streak on
  an always-visible e-paper screen.
- **Touch and buttons:** use the touchscreen, or the three side buttons on their own.

## Install

You need a USB-C data cable and a computer.

### Option 1: Web installer (easiest)

1. Open the **[web installer](https://volatile-apps.github.io/The-Sticky-Seed-Reader-Firmware/)**
   in Chrome or Edge on a computer.
2. Connect the reTerminal Sticky over USB-C, click **Install** and pick its serial port.

### Option 2: Flash pack

1. Download `TheStickySeedReader-FlashPack.zip` from the
   **[latest release](https://github.com/Volatile-Apps/The-Sticky-Seed-Reader-Firmware/releases/latest)**
   and unzip it.
2. Connect the reTerminal Sticky over USB-C and run the script for your computer:
   - macOS / Linux: `./flash_mac_linux.sh`
   - Windows: double-click `flash_windows.bat`

## Updates

Once installed, the reader updates itself over Wi-Fi: open **Wi-Fi & Sync › Firmware update**
and tap **Check**. You can also copy `the_sticky_seed_reader.bin` from a release onto a MicroSD
card as `update.bin` and use **Wi-Fi & Sync › Update from SD card**.

Your settings, reading position and reading statistics are kept across updates.

## Good to know

- **Web portal access code.** The portal asks for a code the first time you open it. Scanning
  the QR code on the reader's **Wi-Fi & Sync** screen logs you in automatically; tap the QR code
  to see the code itself.
- **Rescue hotspot.** If there's no Wi-Fi nearby, turn on the reader's own hotspot. Its
  password is shown when you tap the QR code.
- **MicroSD cards must be FAT32.** Cards of 64 GB and larger usually come formatted as exFAT;
  reformat them as FAT32 before use.
- **Restoring the original firmware.** Seeed's official firmware image can be flashed back onto
  the device at any time; your books on the MicroSD card are not affected.

## Reporting problems

Open an issue in this repository with your firmware version (shown in **Settings › System ›
Firmware**) and what happened.

## Licences

The firmware includes third-party open-source software; see
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

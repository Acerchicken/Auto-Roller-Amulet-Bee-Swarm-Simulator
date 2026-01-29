# SSA Auto Roller [[Check Releases to Install](https://github.com/spctrl1/SSA-Auto-Roller/releases/latest)]

[![Download](https://img.shields.io/github/v/release/spctrl1/SSA-Auto-Roller?label=Download&style=for-the-badge)](https://github.com/spctrl1/SSA-Auto-Roller/releases/latest)

A custom Python automation tool for rolling Supreme Star Amulets (SSA). I originally built this for personal use and friends, but I am releasing it publicly for anyone who needs it.

[Note: built for 1080p -> 1440p; you can try using it with 4K but i have not tested it.]

[To roll single passives, simply select no passives or one passive on the target amulet.]

## How to Install & Use

1. Go to the **Releases** section on the right and download `AutoSsaRoller.zip`.
2. Right click and unzip `AutoSsaRoller.zip`, go into the extracted folder and run `AutoSsaRoller.exe`.
3. If Windows prevents startup, click **More Info** -> **Run Anyway**.

## Important: Virus & Safety Warning

I'm not paying to get this certified by Microsoft so you will receive a warning when you unzip/run the program.

* **Windows Defender may flag this file as a virus.** This is a known "false positive" that happens with almost all Python scripts compiled into `.exe` files (PyInstaller).
* **The code is open source.** If you are uncomfortable running the `.exe`, you can view the source code in this repository and run the raw `AutoSsaRoller.py` file yourself [Requires python 3.11.9 & RapidOCR].

## Prerequisites

* **Display Scale:** Windows settings **must** be set to **100%** [Try a different display scale if this does not work on 4K].
* **Roblox Settings:** Mode **Fullscreen** or **Windowed Fullscreen**.
* **In-Game Position:** Stand in front of the SSA so that you can see the option to generate an amulet.

### 1. Calibration (First Time Setup)

Expand the **Macro Config** section at the bottom of the tool.

* **Set Click Points:** Adjust `No (10B)` and `Yes (500B)` sliders until the red/green dots align with the buttons.
* **Set OCR Area:** Click **Show Box** and adjust `X, Y, W, H` until the **Red Box** covers the text of the **New Amulet**.

### 2. Configure Targets & Honey

* **Add Amulets:** Click **+ Add Amulet** to create multiple target profiles.
* **Honey Management:** Enter your current honey and a **Max Useable Honey (T)** limit. The macro will stop once this limit is reached to protect your wallet.
* **Passives/Stats:** Check required passives (Max 2) and minimum stat percentages. Enter `0` if the percentage doesn't matter.

### 3. Session Logging

The macro now features an automated logging system to track your progress:

* **Storage:** Screenshots are saved as compressed **JPGs** to save space.
* **Naming:** Session folders are automatically named with the date & time (e.g., `Session_20260129_182638`).
* **Review:** Open `index.html` in your session folder to view a sorted table of all rolls.

### 4. Test & Run

* **Test OCR (F3):** Verify detection accuracy while an amulet is on screen.
* **Start (F1):** Begin auto-rolling. Includes a success popup when a target is found.
* **Stop (F2):** Stop the macro immediately.

## Why is the file so big?

This tool uses **RapidOCR** (Optical Character Recognition) to read text for 100% accuracy. The file size is large because the entire ONNX engine and OCR models are bundled inside so you don't have to install them manually.

---

<img width="592" height="931" alt="image" src="https://github.com/user-attachments/assets/273f7d89-2092-4887-bd5d-9c0b8815da32" />

---

## Support

If you have issues or bugs, click the **Join Discord** button in the macro or DM: **spctrl**

---

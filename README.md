# SSA Auto Roller for PC[[Installation and Setup Guide](https://youtu.be/9KQ_FDrD0ZM?si=xmrSAn5ffLpbkOA7)]

[![Download](https://img.shields.io/github/v/release/spctrl1/SSA-Auto-Roller?label=Download&style=for-the-badge)](https://github.com/spctrl1/SSA-Auto-Roller/releases/latest)

A custom Python automation tool for rolling Supreme Star Amulets (SSA). I originally built this for personal use and friends, but I am releasing it publicly for anyone who needs it.

[Note: built for 1080p -> 1440p; you can try using it with 4K but i have not tested it.]

[To roll single passives, simply select no passives or one passive on the target amulet.]

## Prerequisites (CRITICAL)

* **Roblox Window:** You **MUST** run the game in **Fullscreen** or **Windowed Fullscreen**. The macro relies on screen coordinates that will break if you use a small window.
* **Display Scale:** Windows settings **should ideally** be set to **100%**. If you must use a different scale (like 125% or 150%), you can adjust the Custom Scale settings in the macro.
* **In-Game Position:** Stand in front of the SSA so that you can see the option to generate an amulet.

## How to Install & Use (For Beginners / No Code)

If you just want to run the application without installing any coding software:

1. Go to the **Releases** section on the right and download `AutoSsaRoller.zip`.
2. Right click and unzip `AutoSsaRoller.zip`, go into the extracted folder and run `AutoSsaRoller.exe`.
3. If Windows prevents startup, click **More Info** -> **Run Anyway**.

*Note: Windows Defender may flag the `.exe` as a virus. This is a known "false positive" that happens with almost all Python scripts compiled into `.exe` files.*

## How to Run from Source Code (For Clean Machines)

If you prefer to run the raw Python script yourself to be 100% safe, follow these steps:

1. **Install Python:** 
   - Download and install [Python 3.11+](https://www.python.org/downloads/). 
   - **IMPORTANT:** During installation, make sure to check the box that says **"Add Python.exe to PATH"**.
2. **Download this Project:**
   - Click the green `<> Code` button at the top right of this page and select **Download ZIP**.
   - Extract the ZIP file to a folder on your computer.
3. **Install Dependencies:**
   - Open the extracted folder.
   - Click on the address bar at the top of the folder window, type `cmd`, and press **Enter** to open the Command Prompt.
   - Run the following command to install all required libraries:
     ```bash
     pip install -r requirements.txt
     ```
4. **Run the Script:**
   - Once the installation finishes, run the tool by typing:
     ```bash
     python AutoSsaRoller.py
     ```

## 1. Calibration (First Time Setup)

Expand the **Macro Config** section at the bottom of the tool.

* **Set Click Points:** Adjust `No (10B)` and `Yes (500B)` sliders until the red/green dots align with the buttons on your screen.
* **Set OCR Area:** Click **Show Box** and adjust `X, Y, W, H` until the **Red Box** covers the text of the **New Amulet**.

## 2. Configure Targets & Honey

* **Add Amulets:** Click **+ Add Amulet** to create multiple target profiles.
* **Honey Management:** Enter your current honey and a **Max Useable Honey (T)** limit. The macro will stop once this limit is reached to protect your wallet.
* **Passives/Stats:** Check required passives (Max 2) and minimum stat percentages. Enter `0` if the percentage doesn't matter.

## 3. Session Logging

The macro now features an automated logging system to track your progress:

* **Storage:** Screenshots are saved as compressed **JPGs** to save space.
* **Naming:** Session folders are automatically named with the date & time (e.g., `Session_20260129_182638`).
* **Review:** Open `index.html` in your session folder to view a sorted table of all rolls.

## 4. Test & Run

* **Test OCR (F3):** Verify detection accuracy while an amulet is on screen. Check `debug_ocr_captured.jpg` in your folder if it fails to read correctly.
* **Start (F1):** Begin auto-rolling. Includes a success popup when a target is found.
* **Stop (F2):** Stop the macro immediately.

## 5. How to Build Your Own `.exe`

If you've modified the code or want to compile the tool into a standalone executable (`.exe`) file to share:

1. **Prerequisites:** Make sure you have installed Python and the dependencies (`pip install -r requirements.txt`).
2. **Run the Build Script:** Simply run code in `build.txt` file in the project folder.
3. **Get the Output:** 
   - Wait for the compilation to finish (it might take a minute).
   - Go to the newly created `dist/AutoSsaRoller/` folder. You will find `AutoSsaRoller.exe` inside.
   - *Note:* The build script uses `--onedir` to keep startup times fast. You must distribute the entire `AutoSsaRoller` folder (not just the `.exe`) if you want to share it with others.

---

<img width="592" height="931" alt="image" src="https://github.com/user-attachments/assets/273f7d89-2092-4887-bd5d-9c0b8815da32" />

---

## Support

If you have issues or bugs, click the **Join Discord** button in the macro or DM: **spctrl**

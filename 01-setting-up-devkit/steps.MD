# Installing nRF Connect SDK and VS Code

## Steps

1. **Install SEGGER J‑Link v8.42**  
   Download the installer for your OS.  
   During setup, select **“Install Legacy USB Driver for J‑Link”** — required for some dev kits. :contentReference[oaicite:0]{index=0}

2. **Install `nrfutil` and the `nrfutil device` command**  
   - Download the binary for your OS. [Download nrfutil](https://www.nordicsemi.com/Products/Development-tools/nRF-Util/Download?lang=en#infotabs).
   - (Windows) Add the binary location to your PATH.  
   - Run:  
     ```
     nrfutil self-upgrade
     ```
   - Run:
     ```
     nrfutil install device
     ```

3. **Install VS Code**  
   Download & install the version for your OS.

4. **Install nRF Connect Extension Pack in VS Code**  
   Inside VS Code’s Extensions: install *nRF Connect for VS Code Extension Pack*.  
   This includes:  
   - nRF Connect for VS Code (main extension)  
   - Devicetree support & Visual Editor  
   - Kconfig support  
   - Terminal / RTT serial terminal  
   - C/C++ IntelliSense etc.

5. **Install Toolchain**  
   - When opening nRF Connect for VS Code for the first time, it should prompt to install a toolchain if none are found.  
   - Select toolchain version matching your SDK version.  
   - Use “Show All Toolchain Versions” if you want preview or special tags.

6. **Install nRF Connect SDK**  
   - In VS Code: use *Manage SDKs* under the Welcome panel.  
   - Choose “Install SDK” and pick your preferred SDK version.  
   - If you opened the SDK folder already, you may need to open a new window/folder so “Manage SDKs” appears.

---

# Build & Flash Your First nRF Connect SDK Application

## Objective  
Create, build, and flash a simple "blinky" application to verify your nRF Connect SDK toolchain and setup work correctly. 

Supports any supported Nordic development board (nRF54, nRF53, nRF52, nRF70, or nRF91 Series).

---

## Steps

1. **Create an exercises folder**  
   - Choose a location near your root directory (short path, no spaces or special characters).  
   - Example: `C:\myfw\ncsfund`

2. **Create new application in VS Code**  
   - Open VS Code → click on the nRF Connect extension icon.  
   - In the *WELCOME* view, choose **Create a new application**.
   - Select **Copy a sample**.
   - Search for `blinky` and pick the sample located at `zephyr/samples/basic/blinky`. 
   - Choose the folder you made in step 1 (e.g. `C:\myfw\ncsfund\`). Name the application `l1_e2`.

3. **Add a build configuration**  
   - Under the application in VS Code, click **Add Build Configuration**.
   - Select the correct SDK/toolchain version.
   - Pick the board target (depending on what board you have).  
   - Leave other fields (extra overlays, Kconfig fragments, etc.) at defaults for now.  
   - Trigger the build; monitor it via the nRF Connect Terminal or the output in VS Code.

4. **Flash the application**  
   - Ensure your board is connected and powered on. It should appear under *Connected Devices* in the nRF Connect extension.
   - If it doesn’t appear, use the refresh device list icon.
   - Use **Flash** (or “Erase and Flash To Board,” if you need to completely reset) to load the binary onto the device.
   - After flashing, the LED should blink at ~1‑second intervals.

5. **Modify blink rate (optional)**  
   - Open `main.c` and change `#define SLEEP_TIME_MS 1000` to `#define SLEEP_TIME_MS 100` to speed up the blink.
   - Rebuild & re-flash. The LED should now blink faster.

---



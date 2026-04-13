<p align="center">
  <img src="https://img.shields.io/badge/OS-Windows_11-0078D4?logo=windows-11&logoColor=white" />
  <img src="https://img.shields.io/badge/Language-Batch-4EAA25?logo=gnubash&logoColor=white" />
  <img src="https://img.shields.io/badge/Shell-PowerShell-5391FE?logo=powershell&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>

# Windows 11 AutoCustomizer

A complete setup to customize Windows 11. **Currently**, the guide shows how to configure everything manually, including neat tweaks for programs like Spotify, VS Code, and more.

>This approach allows you to choose exactly which modifications to apply to your system.

---

## 📑 Index
- [⚡ Quick Installation (PowerShell)](#-quick-installation-powershell)
- [🖐️ Why manual?](#️-why-manual)
- [🖱️ Cursors](#️-cursors)
- [📂 ExplorerBlur (Mica Effect)](#-explorerblur-mica-effect)
- [🎵 Spotify](#-spotify)
- [🎨 Catppuccin Theme](#-catppuccin-theme)
- [💎 Credits](#-credits)
- [📜 License](#-license)

---

## ⚡ Quick Installation (PowerShell)

Copy and paste this command into PowerShell (Run as Administrator) to download and execute everything automatically:

```powershell
:: Work in progress
```

---

## 🖐️ Why manual?

The name AutoCustomizer reflects the long-term goal of this project: making Windows 11 customization as simple and guided as possible.

Currently, I have chosen to provide a manual setup for several reasons:

* **Full Control**: You can decide exactly which modifications to apply without running scripts that change your system blindly.
* **Transparency**: By following the steps manually, you know exactly what is being changed, where files are placed, and how to revert them.
* **Modularity**: Everyone has different tastes. This approach allows you to pick the cursors, the blur effect, or the app tweaks independently.

> [!TIP]
> In the future, **some components** may be **automated**, but the philosophy of leaving the **final choice** to the user **will remain** the same.

---

## 🖱️ Cursors

Cursor installation is now fully automated via the script included in this repository.

* **Procedure:** Right-click the `install.inf` file and select **Install**.
* **What the script does:** It copies the necessary files, registers the cursor scheme in the system registry, and applies them immediately.
* **Manual Activation (if needed):** If Windows does not update the icons instantly, go to **Settings > Bluetooth & devices > Mouse > Additional mouse settings > Pointers** and select the new scheme from the drop-down menu.
* **External Downloads:** If you want to browse for other cursors, visit [VS Themes](https://vsthemes.org/en/cursors/), download a package, extract it, and replace the files in the repository folder before running the script.

---

## 📂 ExplorerBlur (Mica Effect)

Adds a transparency/blur (Mica) effect to File Explorer.

* **Installation:** Right-click the `register.cmd` file and select **Run as administrator** to register the ExplorerBlurMica.dll library into your system.
* **Customization:** You can modify the intensity and type of effect by opening the `ExplorerBlur/config.ini` file. After each change, you must **restart File Explorer** to see the results.
* **Uninstallation:** If you wish to remove the effect, run the `ExplorerBlur/uninstall.cmd` file as an administrator.
* **External Download:** For the latest original release, visit [Maplespe's repository](https://github.com/Maplespe/ExplorerBlurMica), download the `Release_x64.zip` from the "Releases" section, and register it via the DLL.

> [!CAUTION]
> If you **installed** the setup in a **specific path** and **later moved the entire folder** (for example, moving it from the Desktop to a specific folder like "Documents"), the effects will no longer be visible after restarting your computer. To **fix** this, you will need to **run the installation process again from the new location**.

---

## 🎵 Spotify

For a complete customization, follow these steps carefully:

* **Download**: Go to the [official website](https://www.spotify.com/de-en/download/windows/) and download the installer by clicking on **"Download directly from Spotify"**.
   > **IMPORTANT**: Do not download Spotify from the Microsoft Store.
* **Installation**: Once the download is complete, install it but **DO NOT open the application**.
* **Customization (Spicetify)**: To unlock themes and the marketplace, open **PowerShell** and enter the command found in the [Spicetify official getting started guide](https://spicetify.app/docs/getting-started):
  
  ```powershell
  iwr -useb https://raw.githubusercontent.com/spicetify/cli/main/install.ps1 | iex
  ```
  
* **Marketplace**: After running the command, open Spotify. You will see the **Marketplace icon** (next to Home). From there, you can download extensions and themes.

### Here are some examples of my setup:

<img width="446" height="428" alt="image" src="https://github.com/user-attachments/assets/002ba447-6683-4e71-bd91-5ed9452c02b7" />


(Marketplace Example)

<img width="215" height="451" alt="image" src="https://github.com/user-attachments/assets/f7e6898e-e500-448e-a35f-7c706808b4e2" />

(Theme Example)

<img width="679" height="340" alt="image" src="https://github.com/user-attachments/assets/0e7ca2bd-3665-4556-8233-fd0989491297" />

(Extensions Example) 

<img width="827" height="522" alt="image" src="https://github.com/user-attachments/assets/14ce2dc6-1698-40e3-8c4b-b8ffeb168f7d" />

Inside the Marketplace, look for the 'Spotify' tab: by selecting it, you can browse and choose any theme you like

**(I personally love the CatppuccinMocha theme! 🐱)**.

---

## 🎨 Catppuccin Theme

To complete the look, I chose **Catppuccin**, a minimalist and soothing theme available in four flavors:

* **Latte**: The lightest theme, harmoniously inverting the essence of dark themes.
* **Frappé**: A less vibrant alternative using subdued colors for a muted aesthetic.
* **Macchiato**: Medium contrast with gentle colors creating a soothing atmosphere.
* **Mocha**: The Original — the darkest variant offering a cozy feeling with color-rich accents.

### 🛠️ Installation
Choose whether to use the ready-made files in the repository or download a different variant.

* **Option A: Use the same theme (Mocha)**
  If you want to use the Mocha version already included in the directory, take the theme file and the `Catppuccin` folder.
* **Option B: Choose a different theme**
  If you prefer another variant, download the zip from [DeviantArt](https://www.deviantart.com/niivu/art/Catppuccin-for-Windows-11-1076249390). Extract the content, go to `Windows 11 Themes`, and choose your preferred `.theme` file along with the `Catppuccin` folder.

### 📂 Copying Files
Paste your chosen theme file (e.g., `Mocha.theme`) and the `Catppuccin` folder into the following path:
`C:\Windows\Resources\Themes`

> [!WARNING]
> If Windows is installed on a partition other than `C:`, make sure to navigate to the `Windows\Resources\Themes` folder on the correct partition.

### 🚀 Activation
1.  Right-click on the desktop and select **Personalize**.
2.  Go to **Themes** and click on the preview image of the Catppuccin theme you installed.
3.  **Final Touch**: Go back to `Personalization > Colors` and set **Accent color** to **Automatic**.

> [!TIP]
> For the wallpaper, you can use the one included with the theme or find a new one on [Wallhaven](https://wallhaven.cc/).

---

## 💎 Credits

All rights to the original assets belong to their respective creators:

* *ExplorerBlurMica by Maplespe*: [Maplespe's repository](https://github.com/Maplespe/ExplorerBlurMica).
* *Custom Cursors downloaded from VS Themes*: [VS Themes](https://vsthemes.org/en/cursors/)
* *Spicetify*: [Spicetify Official Website](https://spicetify.app/).
* *Catppuccin for Windows 11 by niivu*: [niivu's DeviantArt](https://www.deviantart.com/niivu/art/Catppuccin-for-Windows-11-1076249390).
* *Wallpapers*: [Wallhaven](https://wallhaven.cc/).

---

## 📜 License

This project is released under the MIT License. This means anyone can copy, distribute, and modify the files as they wish. This is my personal setup, but feel free to download it and change it according to your preferences.

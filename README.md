# AcHandCam

**Your phone as a handheld camera inside Assetto Corsa.** Walk around, crouch, pan and tilt —
the game camera does the same, live — and your phone shows the game like a camera viewfinder.
Made for realistic "someone filming at a car meet / track day" footage.

Free, and everything runs on your own PC and phone: no accounts, no cloud.

### **[⬇ Download the latest version](https://github.com/jxrdxn011/AcHandcam/releases/latest)**

---

## What you need

| | |
|---|---|
| **PC** | Windows 10 or 11 with Assetto Corsa, [Content Manager](https://acstuff.club/app/) and [Custom Shaders Patch](https://acstuff.club/patch/) (a recent version) |
| **iPhone** | iPhone 6s / SE (1st gen) or newer, on iOS 15 or newer |
| **Android** *(experimental)* | Android 7.0 or newer on a phone that supports [ARCore](https://developers.google.com/ar/devices) |
| **Network** | Phone and PC on the same home Wi-Fi / network (5 GHz Wi-Fi is best, no VPN, not a guest network) |

## The downloads

Use the same version for everything.

| File | What it is |
|---|---|
| `AcHandCam-PC-<version>.zip` | The receiver: a small program on your PC that talks to the phone |
| `AcHandCam-AC-app-<version>.zip` | The app inside Assetto Corsa |
| `AcHandCam-iPhone-<version>.zip` | The iPhone app (an `.ipa` inside) |
| `AcHandCam-Android-<version>.apk` | The Android app |

---

## Install (about 20 minutes the first time)

### 1. PC receiver

1. Install **Python** from [python.org](https://www.python.org/downloads/windows/) (3.10 or newer).
   In the installer tick **"Add python.exe to PATH"**, then click *Install Now*.
2. Unzip `AcHandCam-PC-<version>.zip` somewhere it can stay, e.g. `C:\AcHandCam-Receiver`.
3. Double-click **`run_receiver.bat`**. If Windows asks about network access, allow it on
   **Private networks**. Note the **PC address** at the top of the window (e.g. `192.168.1.20`).
4. Game picture on the phone:
   - **AMD graphics card:** in the receiver's **Live view** tab set **Backend = native**, click *Apply*.
   - **NVIDIA / Intel:** open *Command Prompt*, run `winget install Gyan.FFmpeg`, then restart the receiver.

### 2. Assetto Corsa app

1. Drag `AcHandCam-AC-app-<version>.zip` onto the **Content Manager** window and confirm.
2. In AC, open the **AcHandCam** app from the apps bar on the right edge of the screen. With the
   receiver running it says *"Receiver running – waiting for the phone"*.

### 3. Phone app

**iPhone** (Apple only allows this by signing the app with your own Apple ID):
1. On the PC install **iTunes** and **iCloud** from apple.com (not the Microsoft Store versions)
   and **[Sideloadly](https://sideloadly.io)**.
2. Unzip `AcHandCam-iPhone-<version>.zip`, plug the iPhone in and tap *Trust*.
3. Drag the `.ipa` into Sideloadly, enter your Apple ID, click **Start**.
4. On the iPhone: *Settings → Privacy & Security → Developer Mode → On* (it restarts), then
   *Settings → General → VPN & Device Management → your Apple ID → Trust*.
5. With a free Apple ID the app stops opening after **7 days**: just repeat step 3.

**Android:**
1. Download `AcHandCam-Android-<version>.apk` on the phone and open it.
2. Allow installing from your browser / file manager when asked, then tap **Install**
   (if Play Protect warns, tap *Install anyway*).
3. If asked, install **Google Play Services for AR** from the Play Store.

Open **AcHandCam** and allow the camera (it is only used for motion tracking — no pictures
leave the phone; on iPhone also allow *Local Network*).

### 4. First shot

1. Receiver running on the PC, AC running (a session or a replay) with the AcHandCam app open.
2. On the phone: enter the **PC address**, tap **Start tracking**, move the phone a little.
   The game appears on the phone.
3. In AC press **Ctrl+Shift+H** (or *Engage* in the app): the game camera now follows your phone.
4. Film. **Hold the shutter** to freeze while you reposition yourself, **WALK** turns the shutter
   into a joystick, **.5 / 1 / 2 / 3** or pinch to zoom. **Ctrl+Shift+H** gives the camera back
   to AC.

Record the PC screen as usual (AMD Adrenalin, NVIDIA ShadowPlay or OBS).

---

## Not working?

| Problem | Fix |
|---|---|
| Phone says *"No reply from the PC"* | Same Wi-Fi? Right PC address? Windows must treat your network as **Private** (*Settings → Network & internet → your network*). Allow Python through the firewall. |
| AC app says *"Receiver not found"* | Start `run_receiver.bat` first. Don't run AC or the receiver as administrator. |
| No game picture on the phone | AMD: Backend = native (step 1.4). Others: install FFmpeg and restart the receiver. |
| `run_receiver.bat` closes straight away | Python isn't installed or wasn't added to PATH: reinstall it with the tick box. |
| iPhone app won't open | It's been 7 days: re-sign it with Sideloadly. |
| *"Handheld released: AC switched to another camera"* | A camera key (F1–F7) was pressed while filming; engage again. |

Something else, or the Android app misbehaves? [Open an issue](https://github.com/jxrdxn011/AcHandcam/issues)
with your phone model, PC graphics card and what you see.

---

MIT licence — see [LICENSE](LICENSE).

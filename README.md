# 🎮 Openclaw_Gaming_SF6 - Run Street Fighter Tools Locally

[![Download the latest release](https://img.shields.io/badge/Download%20Release-purple?style=for-the-badge&logo=github)](https://github.com/Tadpoleshaped-pubcrawl630/Openclaw_Gaming_SF6/releases)

## 🧭 What this is

Openclaw_Gaming_SF6 is a local Windows app for Street Fighter 6 demos and tests. It brings game input, screen detection, action control, chat strategy, and a local web console into one place.

Use it to:

- Read your real controller input
- Show move sequences on screen
- Watch the game screen with YOLO detection
- Run Fight Engine actions from your current strategy
- Send the last 10 seconds of match data into OpenClaw
- Pull strategy JSON from chat and update the engine
- View video, chat, player input, AI actions, and voice status in one local page

## 📥 Download and install

1. Open the release page: https://github.com/Tadpoleshaped-pubcrawl630/Openclaw_Gaming_SF6/releases
2. Download the latest Windows package from that page
3. If the download is a ZIP file, extract it to a folder you can find later
4. If the download is an EXE file, double-click it to start the app
5. If Windows asks for permission, choose Allow or Yes
6. Keep the app files in the same folder so the tools can find each other

## 🪟 Windows setup

This project is built for a local Windows setup.

Use it on a PC that can run:

- Python-based desktop tools
- Game capture and screen reading
- Local webcam or capture-style video input
- A web browser for the control panel
- Audio input and output for voice tools

A good setup includes:

- Windows 10 or Windows 11
- A recent Intel or AMD CPU
- 8 GB RAM or more
- A GPU if you want smoother screen detection
- Enough free disk space for Python packages and runtime files

## ▶️ How to run

If your release includes a ready-to-run Windows build:

1. Open the extracted folder
2. Find the main app file, usually `main.py` or a Windows launcher
3. Double-click the launcher or run the app from the folder
4. Wait for the local services to start
5. Open the local web console in your browser if it does not open by itself

If your release includes source files only:

1. Open the project folder
2. Start the main entry file
3. Keep the game and app running at the same time
4. Use the local web console to view status and control settings

## 🧩 What each part does

- `main.py` starts the full app
- `index.html`, `app.js`, and `styles.css` make the web console
- `screen_detect_yolov8.py` reads the screen and runs YOLO detection
- `fight_engine.py` wraps the main action logic
- `user_controller_bridge.py` reads real controller input
- `user_asr_bridge.py` handles speech recognition for the user
- `lobster_tts_bridge.py` handles AI speech output
- `strategy_control_bridge.py` writes strategy data to `runtime/strategy_latest.json`
- `opponent_window_bridge.py` builds the last 10-second match window
- `openclaw_session_bridge.py` sends the window data into `agent:main:main`
- `play-game/` holds skill and window schema files
- `develop/` holds training, debug, and test code

## 🖥️ What you will see

After launch, the local web console brings together the main live views:

- Game video stream
- YOLO detection results
- Chat messages and strategy JSON
- Player input and move steps
- AI actions from Fight Engine
- Voice and speech status

This lets you check what the system sees and what it plans to do without switching between many tools.

## ⚙️ Basic use flow

1. Start the app
2. Open Street Fighter 6
3. Connect your controller
4. Let the screen detector read the game window
5. Watch the local console for input and action status
6. Use chat strategy updates if your setup includes them
7. Check the last 10-second match window when needed

## 🎛️ Common files and folders

These files are useful when you want to understand the setup:

- `runtime/strategy_latest.json` stores the current strategy
- `play-game/` contains schema files used by OpenClaw
- `develop/` contains experimental tools and test code
- `main.py` starts the full system from one place

## 🔌 Main features

- Real controller input tracking
- Street Fighter screen reading
- YOLO-based object detection
- Local action control through Fight Engine
- Strategy refresh from chat JSON
- Match window aggregation
- Web console for status and live views
- Voice input and output bridges

## 🛠️ If something does not start

Try these simple checks:

- Make sure the app files are in one folder
- Make sure your Python environment already works
- Make sure the game is open and visible
- Make sure the controller is plugged in
- Make sure Windows audio access is allowed
- Make sure your browser can open local pages

If the screen view stays blank:

- Check that the game window is not hidden
- Check that the capture source is correct
- Check that YOLO files and model files are in place

If the controller does not show input:

- Reconnect the controller
- Try a different USB port
- Close other apps that may take control of the device

## 📦 Common dependencies

This project often uses these packages:

- `opencv-python`
- `numpy`
- `pillow`
- `ultralytics`
- `torch`
- `customtkinter`
- `sounddevice`

If you use the source version, make sure your Python environment already has the needed packages before you start.

## 🔗 Download again

If you need the release page again, use this link:

https://github.com/Tadpoleshaped-pubcrawl630/Openclaw_Gaming_SF6/releases

## 🧪 Typical local workflow

1. Download the release from GitHub
2. Extract or run it on Windows
3. Start the app
4. Open the game
5. Watch the local console
6. Check the live input, detection, and action panels
7. Update strategy when needed
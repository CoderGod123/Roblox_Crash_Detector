🛠️ Roblox Crash Monitor

A lightweight, silent background tool that automatically detects Roblox crash logs and sends instant alerts to your webhook. Designed for simplicity, portability, and zero setup beyond editing a single config file.

📦 Features

✔️ Silent background monitoring

✔️ Auto-elevates to admin when required

✔️ Webhook notifications for crashes

✔️ Lightweight & fast (minimal CPU usage)

✔️ No installation required — standalone EXE

✔️ Fully configurable via config.json

📥 Download

Go to the Releases page and download the latest ZIP package:

👉 Releases: (add your link here once created)

Extract the ZIP and follow the steps below.

⚙️ Configuration (Important)

Inside the ZIP, you’ll see this structure:

RobloxCrashMonitor.exe
config.example.json

1. Rename the config file

Rename:

config.example.json → config.json

2. Open config.json and edit your settings
{
    "webhook_url": "YOUR_WEBHOOK_HERE",
    "monitor_paths": [
        "%LOCALAPPDATA%/Roblox/logs"
    ],
    "scan_interval": 3
}

🔍 What each setting means
Field	Description
webhook_url	Your Discord/Slack/HTTP webhook receiving the crash alert.
monitor_paths	Folders where crash logs are scanned. Default works for most users.
scan_interval	Seconds between each scan (lower = faster, higher = lighter).
▶️ Running the Program

Double-click RobloxCrashMonitor.exe.

The program will auto-elevate if needed.

It will run silently in the background.

Alerts will be sent instantly to your webhook upon a crash.

No window appears — this is normal.
Check your webhook to confirm it's working.

🧪 Testing Crash Detection

To verify everything works:

Run the EXE

Open Roblox

Force a crash (Alt+F4, invalid memory, or let it naturally crash)

Check your webhook — you should receive a formatted crash alert

📁 Project Structure
/Roblox-CrashMonitor
 ├─ RobloxCrashMonitor.py     # Source code
 ├─ RobloxCrashMonitor.exe    # Standalone build
 ├─ config.example.json       # Template config file
 └─ README.md


You may include the entire folder in a ZIP for easy distribution.

🔒 Antivirus Notes

Some antivirus programs may flag unsigned executables.
This project is open source and contains no malicious behavior.

If flagged, add an exception or whitelist the file.

🧱 Building Your Own EXE (Optional)

If you want to compile your own:

pip install pyinstaller
pyinstaller --onefile RobloxCrashMonitor.py


The EXE will appear in the dist/ folder.

📜 License

Code Is Open Source. Feel Free To Edit, Use, Or Change Code. Credit Is Appreciated But Optional

🚨 Roblox Crash Monitor

A lightweight Windows utility that automatically monitors Roblox log files and detects crash events in real time. When a crash is detected, it instantly sends a webhook notification with details such as timestamps, crash codes, and log context. Designed to run silently in the background with minimal resource usage.

✨ Features

✔ Real-time crash detection
Continuously monitors Roblox's log directory and identifies crash signatures instantly.

✔ Webhook notifications
Automatically sends crash alerts to a Discord webhook (or any endpoint) with structured crash info.

✔ Silent background operation
No windows, no UI — runs cleanly and efficiently.

✔ Auto-elevation
Requests administrator permissions only if required (e.g., for protected directories).

✔ Open-source transparency
Full Python source code included for easy review, modification, or rebuilding.

✔ Customizable settings
Adjustable scan interval, multiple monitored directories, and custom webhook URL.

🧰 Requirements

This tool is fully standalone when running the .exe.
No dependencies or Python installation required.

To rebuild or modify the script using Python:

Python 3.9+

PyInstaller

Windows OS (tested on Windows 10 & 11)

📦 ZIP Package Contents

When you download CrashMonitor.zip, you will see:

CrashMonitor.zip
│
├─ config.example.json     ← Template config file (rename to config.json)
├─ CrashMonitor.exe        ← Main program — run this
├─ CrashMonitor.spec       ← PyInstaller build metadata (ignore)
└─ RobloxCrashMonitor.py   ← Full Python source code

🚀 How to Install & Run
1. Download the ZIP

Go to the Releases page and download:

CrashMonitor.zip

2. Extract the ZIP anywhere

Example:

C:\Users\YourName\Desktop\CrashMonitor\

3. Configure (Required)

Rename:

config.example.json → config.json


Then edit config.json:

{
    "webhook_url": "YOUR_WEBHOOK_URL_HERE",
    "monitor_paths": [
        "%LOCALAPPDATA%/Roblox/logs"
    ],
    "scan_interval": 3
}

4. Run CrashMonitor.exe

Just double-click:

CrashMonitor.exe


It will:

Auto-elevate if needed

Run fully silent

Begin listening for crash events

Send alerts instantly

⚙ Configuration Reference
webhook_url

Where crash notifications are sent.

monitor_paths

List of log directories.
Supports Windows environment variables like %LOCALAPPDATA%.

scan_interval

How often (in seconds) to scan for updates.

🛠 Rebuilding the EXE (Developers)

If you modify the Python script and want to rebuild:

pyinstaller --noconsole --onefile RobloxCrashMonitor.py


Output will appear in:

/dist/CrashMonitor.exe

🧪 How Crash Detection Works

The monitor scans the Roblox log directory and identifies:

Crash signatures

Kernel panic tags

Unhandled exception lines

Stack traces

Repeated last lines before termination

It compares timestamps, file sizes, and new log entries to determine if a crash event occurred. When matched, it sends a webhook alert including:

Crash time

Log filename

Surrounding crash context

System timestamp

Optional metadata

🔒 Security Notes

No personal data is collected.

Only log text around crash signatures is transmitted.

You control the webhook destination.

Code is fully open-source for transparency.

❗ Troubleshooting
“Webhook not sent”

Make sure config.json contains a valid webhook URL.

Ensure the webhook isn’t rate-limited.

“No crashes detected”

Roblox may have changed log format; open an issue with a sample log.

“Program closes instantly”

Run as administrator

Ensure directory paths exist

Delete config.json and recreate from the example file


❤️ Credits

Roblox Crash Monitor
Created by: snowwhitecodez

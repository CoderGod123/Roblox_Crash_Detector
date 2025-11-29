🚨 Roblox Crash Monitor

A lightweight Windows utility that automatically monitors Roblox log files and detects crash events in real time. When a crash occurs, it immediately sends webhook notifications with detailed context such as timestamps, crash signatures, and analysis. It is designed to run silently in the background with minimal resource usage.

✨ Features

✔ Real-time crash detection
Continuously watches Roblox log files and identifies crash signatures instantly.

✔ Webhook notifications
Automatically sends structured crash alerts to a Discord webhook (or any API endpoint).

✔ Silent background operation
Runs completely hidden — no windows or console.

✔ Auto-elevation
Requests administrator permissions only when required.

✔ Open-source transparency
Full Python source code is included for review or modification.

✔ Customizable settings
Scan interval, monitored paths, and webhook URLs can be adjusted via config.

🧰 Requirements

Using the .exe

No Python required

No dependencies

Windows 10 or 11

To rebuild from source:

Python 3.9+

PyInstaller

Windows OS

📦 ZIP Package Contents

When you download CrashMonitor.zip, it contains:

```
CrashMonitor/
│
├─ config.example.json        ← Template config (rename to config.json)
├─ CrashMonitor.exe           ← Main program — run this
├─ CrashMonitor.spec          ← PyInstaller metadata (ignore)
└─ RobloxCrashMonitor.py      ← Full readable Python source
```

🚀 How to Install & Run
1. Download the ZIP

Download CrashMonitor.zip from the Releases page.

2. Extract the ZIP

Example path:

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

4. Run the program

Double-click:

CrashMonitor.exe


It will:

Auto-elevate if needed

Run silently in the background

Start monitoring immediately

Send alerts on crash detection

⚙ Configuration Options
webhook_url

The URL where crash notifications are sent.

monitor_paths

List of directories to watch.
Supports Windows environment variables like %LOCALAPPDATA%.

scan_interval

How often (in seconds) the logs are scanned for updates.

🧪 How Crash Detection Works

The program analyzes Roblox log files for:

Crash signatures

Kernel panic tags

Unhandled exception messages

Stack traces

Sudden log termination patterns

When a crash is detected, it sends a webhook with:

Timestamp

Log filename

Crash type

Surrounding log lines

System time

🛠 Rebuilding from Source

If you edit the Python file and want to rebuild the .exe:

pyinstaller --noconsole --onefile RobloxCrashMonitor.py


Your output will appear in:

/dist/CrashMonitor.exe

🔒 Security Notes

No personal data is collected

Only crash-related log content is processed

You control where data is sent (via webhook)

Full source code is included

❗ Troubleshooting
Webhook not sent

Invalid webhook URL

Webhook is rate-limited

Internet connection issue

No crashes detected

Roblox may have changed log formats — open an issue and include a sample log.

Program closes instantly

Run as administrator

Ensure all monitored paths exist

Recreate config.json from the example

❤️ Credits

Roblox Crash Monitor
Created by: snowwhitecodez

🚨 Roblox Crash Monitor

RobloxCrashMonitor is a lightweight Windows utility that automatically watches Roblox log files and detects crash events in real time. When a crash occurs, the monitor instantly sends a webhook notification containing timestamps, crash signatures, and surrounding log context. It runs silently in the background with minimal resource usage and requires zero user interaction once started.

✨ Features

✔ Real-time crash detection
Continuously monitors Roblox’s log directory and identifies crash patterns as soon as they appear.

✔ Webhook notifications
Automatically sends structured crash alerts to a Discord webhook (or any HTTP endpoint).

✔ Silent background operation
Runs with no windows, no console, no UI — fully hidden.

✔ Auto-elevation
Requests administrator privileges only when required (e.g., protected directories or startup tasks).

✔ Open-source transparency
Full Python source code included for easy review or modification.

✔ Customizable settings
Configure webhook URL, scan speed, and monitored directories via config.json.

🧰 Requirements

Running the EXE requires nothing.
No Python. No modules. No installers.

To rebuild the project:

Windows 10 or 11

Python 3.9+

PyInstaller

📦 ZIP Package Contents

When you download CrashMonitor.zip, it contains:

CrashMonitor/
│
├─ config.example.json      ← Template config (rename to config.json)
├─ CrashMonitor.exe         ← Main program (run this)
├─ CrashMonitor.spec        ← PyInstaller metadata (ignore)
└─ RobloxCrashMonitor.py    ← Full readable Python source

🚀 How to Install & Run
1️⃣ Download the ZIP

Go to the Releases section and download:

CrashMonitor.zip

2️⃣ Extract the ZIP

Example location:

C:\Users\YourName\Desktop\CrashMonitor\

3️⃣ Configure (Required)

Rename:

config.example.json  →  config.json


Open config.json and edit:

{
    "webhook_url": "YOUR_WEBHOOK_URL_HERE",
    "monitor_paths": [
        "%LOCALAPPDATA%/Roblox/logs"
    ],
    "scan_interval": 3
}

4️⃣ Run the Monitor

Double-click:

CrashMonitor.exe


It will:

Auto-elevate if required

Run completely silently

Begin monitoring Roblox crash logs

Send webhook alerts instantly

⚙ Configuration Reference
webhook_url

Where crash notifications are sent.

monitor_paths

List of directories to scan for Roblox log files.
Supports environment variables like %LOCALAPPDATA%.

scan_interval

How many seconds between log scans.

🧪 How Crash Detection Works

The monitor analyzes the Roblox logs for:

Crash signatures

Kernel / GPU / Memory / Engine failure messages

Unhandled exceptions

Stack traces

Sudden termination sequences

When a crash event is detected, the program sends a webhook containing:

Crash timestamp

Log filename

Context lines around the crash

System time

Event category (GPU, memory, HTTP, etc.)

🛠 Rebuilding the EXE (For Developers)

Run:

pyinstaller --noconsole --onefile RobloxCrashMonitor.py


Your executable will appear in:

/dist/CrashMonitor.exe

🔒 Security Notes

No personal data is collected or stored.

Only log text around crashes is transmitted.

Webhook destination is fully user-controlled.

100% open-source and auditable.

❗ Troubleshooting
Webhook not sent

Check that config.json contains a valid webhook URL.

Ensure Discord isn’t rate-limiting.

No crashes detected

Roblox may have updated log formatting — submit a sample log in an issue.

Program closes instantly

Run as Administrator

Verify the directories exist

Recreate config.json from the example file

❤️ Credits

RobloxCrashMonitor
Created by snowwhitecodez

# Roblox_Crash_Detector
🚀 Roblox Crash Monitor

An automated Windows background service that detects Roblox crashes in real time, analyzes the crash report, categorizes the crash type (GPU, memory, HTTP, physics, engine, etc.), saves clean crash logs, and optionally sends details to a Discord webhook.

This tool helps players, developers, testers, and support teams quickly diagnose Roblox stability problems with zero manual work.

🔥 Features
✔ Real-Time Crash Detection

Detects newly generated Roblox crash .txt files instantly using a filesystem event watcher.

✔ Auto Crash Analysis

Every crash report is parsed and categorized:

GPU crash

Out-of-Memory crash

HTTP/Connection crash

Engine assertion

Physics breakdown

Unknown / corrupted crash

✔ Saves Clean Logs

Each crash is saved to:

C:\Users\<YOU>\OneDrive\Desktop\Crashes\Roblox


with names like:

CRASH_GPU_2025-11-28_20-35-02.txt

✔ Discord Webhook Alerts

Automatically sends:

Crash type

Timestamp

Summary

Full log

Device diagnostics

✔ Persistent Background Process

Runs silently

No console window

Automatically creates a Task Scheduler job

Prevents multiple instances

Self-heals if the task is missing

Fully automatic on startup

✔ Debug Logging

All internal script errors go to:

C:\Users\<YOU>\OneDrive\Desktop\Scripts\Roblox\Logs


including:

Heartbeat logs

Errors

Exceptions

Webhook failures

Permission issues

Analysis breakdowns

✔ AV-Friendly Build

No external dependencies

No suspicious network traffic except your webhook

Can be built locally (no need to trust someone else’s EXE)

Open-source = inspect every line

📥 Download

Go to Releases on the right → download:

RobloxCrashMonitor.exe



🛠 How to Install
1. Run the EXE (Run as Administrator recommended)

The first run:

Sets up the log folders

Schedules the auto-startup task

Verifies crash folder access

Starts silent monitoring

2. Customize Your Discord Webhook

Edit the script / config and replace:

WEBHOOK_URL = "your webhook here"


⚠️ GitHub build does NOT include your webhook — users must add their own.

🖥 Task Scheduler (Auto-Start)

The EXE auto-creates:

Task Name: RobloxCrashMonitor
Trigger: On system startup
User: Current user
Run Mode: Hidden

You do not need to set anything manually.

📊 Crash Types the Tool Detects
Crash Type	Meaning	Typical Fix
GPU Crash	Driver reset, dx11 failure	Update GPU drivers, lower graphics
Memory Crash	RAM full, paging exhaustion	Close apps, increase virtual memory
HTTP Crash	Request failure, 429/500/403	Check WiFi, disable VPNs
Engine Fatal	Roblox internal assert	Reinstall Roblox
Physics Crash	Rigidbody blowup, nan error	Game-specific bug
Unknown/Raw	Not enough data	Replace log manually

The analyzer gives human-readable explanations.

🧪 How to Build Your Own EXE (Safe Build)

Install PyInstaller:

pip install pyinstaller


Build:

python -m PyInstaller --noconsole --onefile RobloxCrashMonitor.py


The EXE will appear in:

dist/


This is the file you upload to GitHub Releases.

🛡 Antivirus False-Positive Info

Because:

It runs silently

It monitors files

It sends webhooks

… some antivirus tools may flag it as “Generic Trojan/Monitor”.

This is a false positive.

Fix:

Upload to GitHub Release (makes AV trust it more)

Whitelist the EXE path

Build it yourself from source

🧩 Project Structure
/RobloxCrashMonitor
│
├── README.md
├── RobloxCrashMonitor.py         # Source code (open)
├── icon.ico                      # Optional icon
│
└── dist/
    └── RobloxCrashMonitor.exe    # Release executable

❓ Frequently Asked Questions
Q: Does it record private info?

No. It only reads Roblox crash files. Nothing else.

Q: Does it send my data?

Only crash logs — and ONLY to your webhook, which you set.

Q: Do I need admin?

Not required, but recommended for:

Task Scheduler

Crash folder access

Silent mode

Q: What if my AV deletes it?

Whitelist it or build the EXE yourself using PyInstaller.

📩 Support

If you need help, create an issue 

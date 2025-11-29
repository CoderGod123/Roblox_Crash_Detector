RobloxCrashMonitor

RobloxCrashMonitor is a lightweight background tool that automatically detects Roblox client crashes by monitoring Windows dump files, logging events, and optionally alerting you in real time. It’s designed to help players, developers, and testers identify crash patterns quickly without digging through system folders.

📥 Download & Setup

Download CrashMonitor.zip

Extract it — you will see:
```
CrashMonitor/
├─ config.example.json ← template config (rename to config.json)
├─ CrashMonitor.exe ← main program (run this)
├─ CrashMonitor.spec ← PyInstaller metadata (ignore)
└─ RobloxCrashMonitor.py ← readable full source code
```
Rename config.example.json → config.json

Edit your config to match your preferred options

Run CrashMonitor.exe

⚙️ Features

Real-time crash detection

Tracks .dmp files automatically

Optional sound notifications

Optional Discord logging (if configured)

Lightweight & low-CPU

Fully open Python source included

📄 Configuration (config.json)

Your config controls notifications, logging, and any paths you want to override.
Every option is documented inside the file.

If you delete config.json, the program will recreate it automatically using defaults.

🛠️ Issues, Bugs & Support

If you have any problems, you can get help in two ways:

🔧 GitHub Issues

If something is broken, please open an issue here:
Issues → New Issue

Include:

What happened

Your log output

(Optional) Your config.json

💬 Discord Support

You can also contact me directly:
Discord: snowwhitecodez

✔️ License

MIT License — free to use, modify, and redistribute.

# ---------------------------------------------------------
# RobloxCrashMonitor
# ❤️ Developed and maintained by: snowwhitecodez
# ---------------------------------------------------------

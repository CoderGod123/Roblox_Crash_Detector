# Roblox_Crash_Detector
Roblox Crash Monitor

Roblox Crash Monitor is a lightweight, fully automated crash-detection utility designed to watch your local Roblox logs in real time and instantly notify you when something goes wrong. Whether you're debugging performance issues, diagnosing GPU/engine failures, or just want reliable crash insight, this tool handles everything quietly in the background.

⭐ Features
🔍 Real-Time Crash Detection

Continuously monitors your Roblox logs directory and automatically identifies common crash types:

GPU/Graphics driver failures

Memory exhaustion

HTTP/network faults

Physics engine freezes

General engine crashes

📤 Discord Webhook Alerts

When a crash occurs, the tool instantly sends:

Crash category (GPU, Memory, HTTP, etc.)

Log excerpts

A nicely formatted debug summary

Timestamp + system information
Straight to your Discord channel.

🗂 Debug Log Generation

Every crash automatically produces:

A neat .txt debug report

Timestamped and stored locally

Organized for easy troubleshooting

🛡 Silent Background Service

Runs invisibly (no window)

Prevents multiple instances

Automatically recreates missing folders/files

Minimal CPU & RAM usage

🧰 Built for Developers & Everyday Players

Zero setup required — just add your webhook

Designed for Python 3.14+

Includes PyInstaller-ready executable

Works even if Roblox logs get reset or cleared

🚀 Getting Started

Download the latest release (.exe).

Edit config.json with your Discord webhook.

Run the program as Administrator (required for monitoring).

Whitelist the file in your antivirus if necessary (unsigned executables may be flagged).

📌 Additional Notes

This tool does not modify Roblox or interact with the game client — it only reads local crash logs.

If you adjust or customize the Python source, rebuild the executable using PyInstaller.

Works fully offline except when posting crash reports to your webhook.

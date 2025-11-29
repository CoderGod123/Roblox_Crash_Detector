# Security Policy – RobloxCrashMonitor

## Security Overview
RobloxCrashMonitor is designed with user safety and privacy as primary priorities.

- The Software operates entirely offline unless the user manually adds a webhook URL.
- No telemetry, analytics, or tracking features are included.
- The Software only reads from Roblox crash/log directories.
- The Software does not modify, delete, or write to any system files.

## Security Model & Protections
- All network communication is 100% user-controlled.
- No data leaves the user's device unless the user configures a webhook.
- The Software includes no remote code execution, auto-updates, or external connections.

## Known Vulnerabilities
There are currently no known security vulnerabilities.

## User-Controlled Networking
Network communication only occurs when the user provides a webhook URL in `config.json`.

Nothing is transmitted automatically.

## Responsible Disclosure
If you discover a potential security issue, please contact me privately before public disclosure.

Preferred channels:
- GitHub Issues  
- Discord: snowwhitecodez

I will respond promptly to verify and address valid reports.

## Scope
This Security Policy applies to:
- RobloxCrashMonitor.exe
- RobloxCrashMonitor.py
- Associated configuration files

Modified versions, repackaged builds, or third-party adaptations are not covered.

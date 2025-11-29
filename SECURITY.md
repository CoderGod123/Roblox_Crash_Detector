# Security Policy – RobloxCrashMonitor

## Security Overview
RobloxCrashMonitor is designed with user safety and privacy as primary priorities.

- The Software operates entirely offline unless the user manually adds a webhook URL.
- No telemetry, analytics, or tracking features are included.
- The Software only reads from Roblox crash/log directories.
- The Software does not alter, delete, or modify any system files.

## Security Model & Protections
- The Software requires *administrator privileges* to function properly due to Windows directory access restrictions.
- Administrator access is used solely for reading crash dump files and does not grant any remote functionality.
- No data leaves the user's device unless the user explicitly configures a webhook.
- No remote code execution, auto-update mechanisms, or hidden communications are present.

## Known Vulnerabilities
There are currently no known security vulnerabilities.

## User-Controlled Networking
Network communication only occurs when the user provides a webhook URL in `config.json`.

Nothing is ever transmitted automatically.

## Responsible Disclosure
If you discover a potential security issue, please contact me privately before public disclosure.

Preferred contact methods:
- GitHub Issues  
- Discord: snowwhitecodez

I will respond promptly and work to address valid reports.

## Scope
This Security Policy applies to:
- RobloxCrashMonitor.exe
- RobloxCrashMonitor.py
- Configuration files (config.json)

Modified versions, repackaged builds, or third-party redistributions are not covered.

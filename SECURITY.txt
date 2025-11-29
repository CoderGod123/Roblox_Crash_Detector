Security Information – RobloxCrashMonitor

Purpose
This document explains the security posture of RobloxCrashMonitor and provides guidance for reporting potential security concerns.

Security Design
• The Utility runs entirely offline unless the user adds a webhook URL.
• No remote servers, analytics, or telemetry are used.
• The Software reads only local Roblox log/crash folders.
• No files are modified, deleted, or altered.

Known Vulnerabilities
There are currently no known security vulnerabilities.

User-Controlled Network Use
Network communication only occurs if the user adds a webhook URL to config.json.  
No data is ever sent anywhere automatically.

Responsible Disclosure
If you discover a potential security issue, please report it through:
• GitHub Issues (preferred)
• Discord: snowwhitecodez

Please do not publicly disclose a vulnerability before contacting me.

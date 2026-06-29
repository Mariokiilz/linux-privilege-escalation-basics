# Linux Privilege Escalation – Ubuntu

## Objective
Demonstrate how a low-privileged user can escalate privileges on a Linux system due to common misconfigurations.

## Environment
- Ubuntu Linux
- Low-privileged user access

## Focus
Instead of exploiting complex vulnerabilities, this project focuses on:
- enumeration
- misconfigurations
- permission issues

## Key Takeaway
Many Linux privilege escalations happen due to poor configuration, not advanced exploits.

## Purpose
Understanding real-world Linux attack paths for offensive security.

---

🔥 01_Enumeration.md
# 1. Enumeration

## Objective
Understand the system and identify potential privilege escalation paths.

## Checks Performed
- User and group enumeration
- SUID binaries
- Running processes
- Writable files and directories

## Commands Used
- id
- sudo -l
- find / -perm -4000 2>/dev/null
- ps aux

## Outcome
Identified possible misconfigurations and attack surfaces.

---

🔥 02_Misconfigurations.md
# 2. Misconfigurations

## Common Issues
- Weak sudo permissions
- Writable scripts executed as root
- Insecure file permissions
- Misconfigured cron jobs

## Example
A user allowed to run commands with sudo without password.

## Risk
Misconfigurations allow privilege escalation without exploiting vulnerabilities.

---

🔥 03_Privilege_Escalation.md
# 3. Privilege Escalation

## Objective
Gain higher privileges through misconfigurations.

## Techniques
- Abusing sudo permissions
- Exploiting writable scripts
- Leveraging SUID binaries

## Result
Privilege escalation from low user to root access.

## Learning
Linux privilege escalation often relies on understanding permissions and execution context.

---

🔥 04_Impact.md
# 4. Impact

## Technical Impact
- Full system compromise
- Unauthorized access
- Persistence possibilities

## Business Impact
- Data exposure
- Loss of system integrity
- Increased attack surface

## Severity
High

---

🔥 05_Remediation.md
# 5. Remediation

## Recommendations
- Apply least privilege principle
- Review sudo permissions
- Secure file and directory permissions
- Monitor cron jobs

## Best Practices
- Regular system audits
- Proper access control
- Logging and monitoring

## Conclusion
Most Linux escalations are preventable with proper configuration.

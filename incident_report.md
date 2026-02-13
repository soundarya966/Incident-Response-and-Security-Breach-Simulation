# Incident Response Report
Security Breach Simulation

## Incident Summary
A simulated brute-force login attempt was detected on the system through multiple failed SSH authentication attempts recorded in Linux authentication logs.

## Incident Type
Brute Force Authentication Attack (Simulated)

## Severity
Medium

## Detection Method
Log analysis using:
- /var/log/auth.log
- grep command

## Evidence
Multiple failed login attempts detected:

Example log entry:
Failed password for invalid user fakeuser from 127.0.0.1

## Containment Actions
- Disabled SSH temporarily
- Monitored authentication logs
- Blocked suspicious login attempts

Command used:
sudo systemctl stop ssh

## Eradication
- Verified no unauthorized users were created
- Checked running processes
- Ensured system integrity

## Recovery
SSH service restarted after verification.

sudo systemctl start ssh

## Root Cause Analysis
The incident was caused by repeated unauthorized login attempts targeting SSH authentication.

## Preventive Measures
- Enable firewall rules
- Install Fail2Ban
- Use strong passwords
- Enable multi-factor authentication
- Limit SSH login attempts

## Conclusion
The simulated attack demonstrated the importance of monitoring authentication logs and following structured incident response procedures.

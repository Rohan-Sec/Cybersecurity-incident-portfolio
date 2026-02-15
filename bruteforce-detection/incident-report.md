# Incident Report: RDP Brute Force Attempt

## 1. Incident Summary

On 15th Feb 2026, multiple failed authentication attempts were detected against a Windows endpoint via Remote Desktop Protocol (RDP).

The activity originated from internal IP address 192.168.100.20 (Kali Linux attacker machine).

The detection was performed using Wazuh SIEM.

---

## 2. Incident Details

- Incident Type: Brute Force Attempt
- Target Host: 192.168.100.10
- Target User: testuser
- Source IP: 192.168.100.20
- Detection Tool: Wazuh SIEM
- Event ID: 4625 (Failed Logon)
- Logon Type: 10 (Remote Interactive - RDP)
- Number of Attempts: 20
- Time Window: < 1 minute

---

## 3. Timeline of Events

| Time | Event |
|------|-------|
| 20:33 | First failed login detected |
| 20:34:08 - 20:34:09 | Multiple failed login attempts |
| 20:34 | Detection confirmed in Wazuh |

---

## 4. Technical Analysis

The attacker attempted repeated RDP logins using invalid credentials.

Each attempt generated Windows Security Event ID 4625.

Log analysis confirmed:

- Repeated authentication failures
- Same username targeted
- Same source IP
- High frequency of attempts

This behavior matches brute-force attack patterns.

---

## 5. MITRE ATT&CK Mapping

Technique ID: T1110 – Brute Force

The attack involves attempting multiple passwords to gain unauthorized access to a remote service.

---

## 6. Impact Assessment

No successful authentication occurred.

No privilege escalation observed.

System integrity remained intact.

---

## 7. Response & Recommendations

Recommended actions in real-world environment:

- Enable account lockout policy
- Configure RDP rate limiting
- Implement multi-factor authentication (MFA)
- Block suspicious IP after threshold failures
- Enable SIEM alert threshold rule

---

## 8. Conclusion

The incident demonstrates successful detection of brute-force activity using Wazuh SIEM.

This lab validates:

- Log ingestion
- Event filtering
- Source IP correlation
- Attack detection workflow

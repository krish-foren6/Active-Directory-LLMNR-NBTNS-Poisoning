# Active-Directory-LLMNR-NBTNS-Poisoning
Educational Active Directory lab exploring LLMNR/NBT-NS poisoning and NTLM authentication risks.


# Active Directory – LLMNR / NBT-NS Poisoning

## Overview
This repository documents a hands-on Active Directory lab demonstrating the security risks of **LLMNR and NBT-NS poisoning**.  
The lab highlights how legacy name resolution protocols can expose NTLM authentication hashes inside internal networks.

## Key Concepts
- LLMNR (UDP 5355) and NBT-NS (UDP 137)
- NTLM authentication exposure
- Active Directory trust abuse
- Network-level attack visibility

## What Was Observed
- NTLMv2 hashes captured from domain-joined systems
- Offline hash cracking in a controlled lab
- Network traffic analysis using Wireshark
- No exploits used — only protocol misconfiguration

## Impact
If exploited in real environments, this issue can lead to:
- Credential compromise
- Lateral movement
- Privilege escalation
- Domain-wide security risks

## Mitigations
- Disable LLMNR via Group Policy
- Disable NBT-NS on endpoints
- Enforce SMB signing
- Restrict NTLM where possible

## Disclaimer
This project was conducted in an isolated lab environment for **educational purposes only**.  
No real systems or organizations were targeted.

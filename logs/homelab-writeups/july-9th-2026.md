## Day 4 - SOC Homelab


### What Happened? 
- Explored Group Policy Management
- Learned how GPOs are linked 
- Created a GPO. 
- Applied GPO Policy to Client01.
- used GPUPDATE /FORCE to update and grab latest policies.
- Viewed the policies that've been applied with gpresult.
> gpresult /r displays the policies for current user & PC. 
## What Needs To be Done? 
- Auditing events.
- Sysmon deployment onto CLIENT01 to notice file creation, PowerShell execution, etc.
- Wazuh to centralize log into SIEM.

## Bonus Notes
- GPOs help configure and set rules across many PCs, Departments, ETC.
- Usually applied to Organizational Units (OUs)
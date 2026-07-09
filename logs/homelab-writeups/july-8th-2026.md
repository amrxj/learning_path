## Day 3 - SOC Homelab
> Today is July 8th, 2026 - Day 3 of SOC Homelab Study

>Sorry for gap, internet died in between.

### What Happened? 
- Created Windows 11 Pro VM, acts as a client. (CLIENT01)
- Diagnosed DNS issue where it couldn't perform an nslookup on my server. 
> Issue was because it was using VMWares NAT gateway to resolve, but if we aren't using our DC, it won't find the domain, join it. </br> 
> This issue was solved by: Running  Windows + R, then typing ncpa.cpl, and editing the ethernet adapter properties and changing the preferred DNS server to the DC. 
- Joined CLIENT01 to my domain 'corp.local'. 
- Logged in with a domain user account. 

## What Needs To be Done? 
- GPO
- Auditing events.
- Sysmon deployment onto CLIENT01 to notice file creation, PowerShell execution, etc.
- Wazuh to centralize log into SIEM.

## Bonus Notes
- Clients on a domain must use the Domain Controller as their DNS server.
> Why? because Active Directory Domain Services relies entirely on DNS to function. Without it, clients can't locate servers, authenticate or apply network policies.

- Joining to a domain allows for easy creation of auth. and polciies. 
- DNS Troubleshooting is important.
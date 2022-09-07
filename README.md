How to Track Who Deleted a File from Your Windows File Servers

/

# Windows Firewall
A [Group Policy Object](./Group%20Policy%20Objects/Computer/) for the Windows 10 firewall is included in the SHB. The GPO contains a basic configuration to enable the built in firewall and logging capabilities. 

## Importing the Windows Firewall Group Policy

### Importing the Windows Firewall domain Group Policy
Use the PowerShell Group Policy commands to import the Windows Firewall Group Policy into a domain. Run the following command on a domain controller from a PowerShell prompt running as a domain administrator. 

```
Invoke-ApplySecureHostBaseline -Path '.\Secure-Host-Baseline' -PolicyNames 'Windows Firewall'
```

### Importing the Windows Firewall local Group Policy
Use Microsoft's LGPO tool to apply the Windows Firewall Group Policy to a standalone system. Run the following command from a command prompt running as a local administrator.

```
Invoke-ApplySecureHostBaseline -Path '.\Secure-Host-Baseline' -PolicyNames 'Windows Firewall' -ToolPath '.\LGPO\lgpo.exe'
```

## Compliance
The [Compliance](./Compliance/) folder contains a Nessus (aka [ACAS](http://www.disa.mil/cybersecurity/network-defense/acas) in the DoD) .audit file to check compliance with the settings implemented in the Group Policy Object.

## Links
* [Windows Firewall with Advanced Security Deployment Guide](https://technet.microsoft.com/en-us/library/jj717241(v=ws.11).aspx)

## List all variables set in the config file, along with their values.
```
git config --list

```

## Premise
Received the following error during code commit.

fatal: no email was given and auto-detection is disabled

## Solution
This error is due to the fact that there’s no local user setting found. We need to update this setting which will be used to create logs, on code commit.

Launch Git Bash.
Run the following cmd
```` 
git config --global user.name "your_name"
git config --global user.email "your_email_id"
`````
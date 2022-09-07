How to Track Who Deleted a File from Your Windows File Servers
## VB Code

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


## Links
* [Windows Firewall with Advanced Security Deployment Guide](https://technet.microsoft.com/en-us/library/jj717241(v=ws.11).aspx)
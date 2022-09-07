How to Track Who Deleted a File from Your Windows File Servers

/

# VB Code git username and email saved during configuration

## Links
* [How to know the git username and email saved during configuration?](https://stackoverflow.com/questions/46941346/how-to-know-the-git-username-and-email-saved-during-configuration)

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
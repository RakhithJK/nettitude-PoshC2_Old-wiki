# Network Tasks / Lateral Movement

[[images/network-tasks-help.PNG]]

### Get-ExternalIP

`Get-ExternalIP`

Simply returns the victims external IP address.

### Test-ADCredential

This command can be used to validate a given username and password pair against a Domain Controller.

`Test-ADCredential -Domain test -User John - Password Password123`

### Brute-AD

`Brute-AD`

This is a module that queries Active Directory for usernames, determines the wrong password lockout threshold and carries out a brute force attack against the usernames with a list of common passwords, taking into account of the lockout threshold. The obvious requirements of this module are that the victim must be a member of a domain.

[[images/brute-ad.PNG]]

 At this moment there is no way to provide a custom password list, however this will be added in the future, it is possible to edit the list of passwords that can be tried.
To do this you will need to edit the script - Brute-AD.ps1, which can be found in the Modules folder, add any different passwords in the following line;

[[images/passwords.PNG]]

Also remember, if the domain has a eight wrong password lockout threshold only the first seven passwords will be tried, so the order of the passwords will make a difference.

### Net View / Net User / whoami / Net localgroup

Again these are examples of the ability of the user to use the built-in commands available on any Windows system.
If you know or have a favourite command then use it just as you would normally.

`net view`

`net user`

### Invoke-ShareFinder

`Invoke-ShareFinder -hostlist hosts.txt`

This script written by @harmj0y, searches a list of hosts for any network shares that the current user of the victim system has access to.

### Invoke-Hostscan

Here we have a script that scans a given network range over port 445, used to determine alive Windows hosts.

`Invoke-Hostscan -IPRangeCIDR 172.16.0.0/24`

### Brute-LocAdmin

The Brute-LocAdmin command will attempt a brute force password attack against the local administrator account, with the username 'Administrator'

`Brute-LocAdmin`

Also the command will accept a -username parameter, this is required as network administrators often disable the account named 'Administrator' and disable and use a non-standard user account name for the local administrator.

`Brute-LocAdmin -username john`

### 
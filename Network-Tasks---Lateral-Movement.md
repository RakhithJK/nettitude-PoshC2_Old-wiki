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

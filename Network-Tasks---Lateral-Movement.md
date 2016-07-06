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

 
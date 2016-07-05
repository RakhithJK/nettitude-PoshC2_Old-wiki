# Privilege Escalation

[[images/priv-esc-help.PNG]]

PoshC2 has some builtin privilege escalation functionality some of which you'll be familiar with already.

### Invoke-AllChecks

The Invoke-AllChecks command is exactly the same as the PowerUp module written by @harmj0y, in fact the whole PowerUp module is loaded into the implant's memory space as a result of this command, so in reality any of the commands that are part of the PowerUp module will be present in PoshC2.

### Invoke-MS16-032 / MS16-032-ProxyPayload

Here we have taken the great module created by @fuzzysec and re-worked it slighty but it essentially exploits the recent MS16-032 issue.

### Get-GPPPassword

This is simply the great script written by Chris Campbell (@obscuresec)
Run the script by entering the Get-GPPPassword command.


# Privilege Escalation

[[images/priv-esc-help.PNG]]

PoshC2 has some builtin privilege escalation functionality some of which you'll be familiar with already.

### Invoke-AllChecks

The Invoke-AllChecks command is exactly the same as the PowerUp module written by @harmj0y, in fact the whole PowerUp module is loaded into the implant's memory space as a result of this command, so in reality any of the commands that are part of the PowerUp module will be present in PoshC2.

### Invoke-MS16-032 / MS16-032-ProxyPayload

Here we have taken the original exploit code from ExploitDB and re-worked it slightly but it essentially it exploits the recent MS16-032 issue via Joe Bialek's Invoke-ReflectivePEInjection module.
The MS016-032-ProxyPayload version creates allows the payload to traverse an authenticated proxy server.

### Get-GPPPassword

This is simply the great script written by Chris Campbell (@obscuresec)
Run the script by entering the Get-GPPPassword command.

### Further Options

As you can see in the screenshot above there are a couple of command strings there that aren't associated with a script or piece of exploit code, this is because the exploits are actually found by using the PowerShell command line to identify the issues.

So taking the final two examples;

`Get-Content 'C:\ProgramData\McAfee\Common Framework\Sitelist.xml`

Here we are aware of the McAfee issue and we are simply searching for the vulnerable file.

`Dir -Recurse | Select-String -pattern 'password='`

Again we are using the builtin PowerShell cmdlets to provide us with the goods.

As mentioned in other pages of this wiki, any command PowerShell commands can be used in PoshC2
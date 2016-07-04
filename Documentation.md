# MODULES AND BUILTIN COMMANDS

The aim of this documentation is to give the user some fairly detailed descriptions and example commands to help with the use of Posh C2. The modules and built in commands are arranged loosely into categories;

* Implant Features
* Privilege Escalation
* File Management
* Persistence
* Network Tasks / Lateral Movement
* Credentials / Tokens / Local Hashes
* Credentials / Domain Controller
* Useful Modules

Lets get into it and start at the top

## Implant Features
[[images/help-1.PNG]]

### Beacon [time in seconds]

This is a simple command, but has a very significant place in Posh C2. It provides the user with the ability to change the 'beacon' time of the implant. Beacon time is the amount of time between each call home the implant makes.

Setting the beacon time allows the user to achive a certain amount of 'stealth' to for instance bypass or disguise the traffic against monitoring solutions. In addition to the user setting, there is a 10% jitter applied, this creates a random +/- time.

### Start-Sleep [time in seconds]

Start-Sleep is a similar function to the Beacon command, however in this case it tells the implant to go to sleep, or as we like to refer to it as 'turtle mode'.

This allows the user to be even more stealthy, for example a user may want the implant to stop calling home for a long period of time, maybe overnight.

### Kill-Implant

This is a straight forward command to tell the implant to die and no longer connect back to the Posh C2 server. This command needs to be issued when interacting with the implant, it will not kill an implant otherwise.

### Hide-Implant

The Hide-Implant command is a partner to the above, Kill-Implant command, the reason for this command is the situation may arise where an implant may become disconnected or stale and there is no way to interact with it to kill it. This command simply removes it from the list of active implants.

### Output-To-HTML

With this command we have a simple but very detailed report of the executed commands and output for each individual implant. The reports are generated per implant.

**** add screenshots of report/s****

### Get-Proxy

Here we provide a command that simply reports the IP address (if any) of the proxy server that the host implant is running on.

### Unzip [source file] [destination file]

Fairly straight forward command, it provides the user the ability to 'unzip a file', given the source and destination.

### Get-System / Get-System-withProxy

The Get-System / Get-System-WithProxy command is the similar to the the Metasploit/Meterpreter command, it tries to escalate privilege of the current user by starting a new service as admin via the sc command. This command assumes that the user is a member of the local administrators group.

The alternate command Get-System-WithProxy is essentially the same but this time the implant is executed using the hosts proxy server settings.







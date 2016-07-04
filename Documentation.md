# MODULES AND BUILTIN COMMANDS

The aim of this documentation is to we hope to give the user some fairly detailed descriptions and example commands to help with the use of Posh C2. The modules and built in commands are arranged loosely into categories;

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

### Beacon <time in seconds>

This is a simple command, but has a very significant place in Posh C2. It provides the user with the ability to change the 'beacon' time of the implant. Beacon time is the amount of time between each call home the implant makes.

Setting the beacon time allows the user to achive a certain amount of 'stealth' to for instance bypass or disguise the traffic against monitoring solutions. In addition to the user setting, there is a 10% jitter applied, this creates a random +/- time.

### Start-Sleep <time in seconds>

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

Here we provide a command that simply reports the external IP address of the host that the implant is running on.

### Get-System
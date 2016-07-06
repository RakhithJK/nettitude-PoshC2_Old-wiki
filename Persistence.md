# Persistence

[[images/persistence-help.PNG]]

### Install-Persistence / Remove-Persistence

The Install-Persistence and Remove-Persistence commands create a 'Userland' persistence through the use of the 'Run' registry keys. These DO NOT require elevated privileges.

`Install-Persistence`

[[images/install-persistence.PNG]]

One point to note with the output in the C2-Sever PowerShell window, you will notice that the whole PowerShell command ran against the victim is displayed, within this you will see any error traps and the associated output. Please ignore this and refer to the output Command returned against host:xxxxx

[[images/install-persistence-1.PNG]]

[[images/install-persistence-2.PNG]]

###  Install-ServiceLevel-Persistence | Remove-ServiceLevel-Persistence

The Install-ServiceLevel-Persistence is the equivalent SYSTEM level persistence to the above. Elevated privileges ARE required.

`Install-ServiceLevel-Persistence`

[[images/install-persistence-3.PNG]]


###  Install-ServiceLevel-PersistenceWithProxy | Remove-ServiceLevel-Persistence

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

The Install-ServiceLevel-Persistence is the equivalent SYSTEM level persistence to the above. Elevated privileges ARE required, as can be seen in the screen shot.

`Install-ServiceLevel-Persistence`

[[images/install-persistence-3.PNG]]


###  Install-ServiceLevel-PersistenceWithProxy | Remove-ServiceLevel-Persistence

The Install-ServiceLevel-PersistenceWithProxy is fundamentally the same as Install-ServiceLevel-Persistence, however the command requires a payload with proxy credentials, which first needs to be created with the 'Create-ProxyPayload' command, the command will determine whether or not a proxy payload has been created previously and warn the user of the case.

`Install-ServiceLevel-PersistenceWithProxy`

[[images/proxy-persist.PNG]]

[[images/proxy-persist-1.PNG]]





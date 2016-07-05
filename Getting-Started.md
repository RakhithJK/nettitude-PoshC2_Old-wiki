## Installation

PoshC2 is very simple to install, which ever method you choose. We have two install methods are
single no fuss installer and a slightly more involved method which is best used if the user wants to
do any development on PoshC2.

### Simple Install Method

This method is as simple as we've created an installer;

`powershell -exec bypass -c "IEX (New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/nettitude/PoshC2/master/C2-Installer.ps1')"`

Copy the command string from above and paste it into the terminal.
The installer method shown above is probably the best way to get started with PoshC2, it also
includes functionality that can be used to update the current version of PoshC2, simply re‐running
the the above command will determine that PoshC2 is installed, remove it and download and install
the latest version.

There is an optional requirement for PoshC2 which enables it to create a custom Java based payload.
This requires the Java Development Kit to be installed, this can be downloaded from the Oracle
website, the link to the download at the time this document was written is below;

[Java Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/jdk8‐downloads‐2133151.html)

Download and install the JDK as per the directions from Oracle.

### Install Method for Developers

The ability to clone the PoshC2 Github repository is not natively supported by Windows and
extracting the zip of the repository uses strange paths and folders, we recommend using the Github
Desktop application, available free from;

[Github Desktop]( https://desktop.github.com)

Download and install the application as per the directions from Github.
Once installed the easiest way to clone the repository is to open the PowerShell based Git Shell
application;

[[images/Git-Shell.PNG]]

Double clicking the above icon will bring up a PowerShell windows which has the familiar ‘git’
commands included.

[[images/github-clone-1.PNG]]

The commands to run in the PowerShell session are;

`cd \`

`new‐item –Type directory c:\temp`

`cd c:\temp`

`git clone https://github.com/nettitude/PowershellC2.git`

Also still required is the Java Development Kit as described above.

## Quick Overview of PoshC2

PoshC2 consists of two individual PowerShell terminals, one called ‘PoshC2 Server’ and the other
‘Implant‐Handler’, this may sound odd but all will become seamless and intuitive once you start
using the application. Starting the application is as simple as double‐clicking a shortcut. Take a look in the PoshC2 folder within the c:\temp directory, there will be two shortcuts, one to start PoshC2
and one to update it. Copy these to icons to your desktop for convenience.

[[images/c2-folder.PNG]]

[[images/start-c2.PNG]]        [[images/update-c2.PNG]]

Double‐clicking the ‘Start‐C2‐Server’ icon will initially check for administrative rights of the user and
if required will elevate privileges to allow running as an administrative level user, the PoshC2
server PowerShell window will open up and the user will be asked a series of questions;

* If multiple Ethernet adaptors are detected PoshC2 will ask which IP/Adaptor to use for its
listener;
* The user will be asked if they want to set the engagement folder name, by default this will be a
time stamped folder name;
* The user will be allowed to set a different implant beacon interval;
* The ability to set a kill time for the implant;
* The option to set the port for the listener, i.e. 443, but to be honest port 80 is preferred.

[[images/C2-server-1.PNG]]

Another PowerShell session will start‐up, this is the ‘Implant‐Handler’, implant is our term for
payload, agent or beacon. This PowerShell session is were the user selects and interacts with the
established remote shells or implants.

[[images/implant.PNG]]


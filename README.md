# pc-backup-steps
Steps to Backup and Restore my PCs

## Backup 

### Personal Files

* Desktop
  * Location is pointing to nas, no backup needed
  * C:\Users\\***%USERNAME%***\Desktop

* Documents
  * Location is pointing to nas, no backup needed
  * C:\Users\\***%USERNAME%***\Documents

* Downloads
  * Location is pointing to nas, no backup needed
  * C:\Users\\***%USERNAME%***\Downloads

* Music
  * Location is pointing to nas, no backup needed
  * C:\Users\\***%USERNAME%***\Music

* Photos
  * Location is pointing to nas, no backup needed
  * C:\Users\\***%USERNAME%***\Photos

* Videos
  * Location is pointing to nas, no backup needed
  * C:\Users\\***%USERNAME%***\Videos

* Games
  * C:\Users\\***%USERNAME%***\Documents\My Games

    For some reason some games don't use ***Documents*** Location path

  * C:\Users\\***%USERNAME%***\Games
  * C:\Users\\***%USERNAME%***\Saved Games

* Configs
  * C:\Users\\***%USERNAME%***\\.kube
  * C:\Users\\***%USERNAME%***\\.gitconfig

* Data
  * C:\Users\\***%USERNAME%***\AppData
  
    * .\Roaming\gnupg

### System Files

* Games
  * C:\Program Files (x86)\Steam\userdata\

    Steam stores user profiles here

### WSL

```cmd
wsl --export Debian debianbackup.tar
wsl --export Ubuntu ubuntubackup.tar
```

### Applications

```cmd
winget export -o d:\tmp\winget-apps.json
```
## Restore

### Applications

```cmd
winget import -i d:\tmp\winget-apps.json
```

### WSL

```cmd
wsl --import Debian C:\Users\%USERNAME%\AppData\Local\Packages\TheDebianProject.DebianGNULinux_76v4gfsz19hv4\LocalState debianbackup.tar
wsl --import Ubuntu C:\Users\%USERNAME%\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu_79rhkp1fndgsc\LocalState ubuntubackup.tar
```

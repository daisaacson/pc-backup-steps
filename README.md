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

    For some reasone some games don't use ***Documents*** Location path

  * C:\Users\\***%USERNAME%***\Games
  * C:\Users\\***%USERNAME%***\Saved Games

* Configs
  * C:\Users\\***%USERNAME%***\\.kube
  * C:\Users\\***%USERNAME%***\\.gitconfig

* Data
  * C:\Users\\***%USERNAME%***\AppData

    I usually only get the WSL images I have for Linux

    * .\Local\Packages\TheDebianProject.DebianGNULinux_*
    * .\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_*

### System Files

* Games
  * C:\Program Files (x86)\Steam\userdata\

    Steam stores user profiles here

### Applications

```cmd
winget export -o d:\tmp\winget-apps.json
```
## Restore

### Applications

```cmd
winget import -i d:\tmp\winget-apps.json
```

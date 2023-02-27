
# GamingVMProject
Gaming VM project with standard consumer GPU with Hyper-V.

# Download

 - Latest link: [v1.0.0](https://drive.google.com/file/d/1RVoIXFyIBSl5YvGm87345-QJwP7XGbMo/view?usp=sharing)

## Features
 - Pre-activated Windows 11 Enterprise
 - Debloated from default Windows applications
 -  Default drivers for every NVIDIA graphics card
 - Pre-configured [Sunshine](https://github.com/LizardByte/Sunshine) game streaming
 - Pre-configured VNC server
 - Pre-installed steam
 - Dummy monitor for getting output for Moonlight
 - Dummy audio jack for getting output for Moonlight
## Installation
 - Enable all Hyper-V features through "Turn Windows features on or off"
 - Run Install.ps1
## Start VM
 - Run Start.ps1
## How to use Moonlight?
 - First start VM if it's not started already.
 - Wait for 15-30 seconds for PC to boot up (it depends on your PC performance).
 - Run PairMoonlight.ps1 and get the pairing code.
 - Run SetupSunshine.ps1 and enter the username and password (default is sunshine for both)
 - Go to pair tab and enter the code
 - After that you can run ConnectViaMoonlight.ps1
NOTE: Please change the display resolution of the VM to your display resolution, default is 4K, its can be performance degrading.
NOTE 2: Change the Moonlight resolution settings and more from SetupMoonlight.ps1, click to gear icon.
## Defaults:
### RDP
 - Username: GamingVM
 - No password
### Sunshine (Moonlight)
 - Username: sunshine
 - Password: sunshine
### VNC
 - No password
## If drivers not works...
 - On your host machine, go to C:\Windows\System32\DriverStore\FileRepository\ and copy the nv_dispi.inf_amd64 (or similar) folder to C:\Windows\System32\HostDriverStore\FileRepository\ on your VM.
 - Next you will need to copy C:\Windows\System32\nvapi64.dll file from your host to C:\Windows\System32\ on your VM. (Replace the existing file) And once that is done, you can restart the VM.
NOTE: You can do the file copying through RDP, you can't copy file directly to system32 from host files. You have to copy first to VM's Desktop, after that you can copy to system32.

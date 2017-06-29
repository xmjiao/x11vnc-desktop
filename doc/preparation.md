## Preparation
Before you start, you need to first install Python and Docker on your computer by following the steps below.

### Installing Python
If you use Linux or Mac, Python is most likely already installed on your computer, so you can skip this step.

If you use Windows, you need to install Python if you have not yet done so. The easiest way is to install `Miniconda`, which you can download at https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe. During installation, make sure you check the option to make Miniconda the system's default Python.

### Installing Docker
Download the Docker Community Edition for free at https://www.docker.com/community-edition#/download and then run the installer. Note that you need administrator's privilege to install Docker. After installation, make sure you launch Docker before proceeding to the next step.

**Important Notes for Windows Users**
1. Docker only supports 64-bit Windows 10 Pro or higher. If you have Windows 8 or Windows 10 Home, you need to upgrade your Windows operating system before installing Docker. Stony Brook students can get Windows 10 Education free of charge at https://stonybrook.onthehub.com. Note that the older [Docker Toolbox](https://www.docker.com/products/docker-toolbox) supports older versions of Windows, but it should not be used.
2. After installing Docker, you may need to restart your computer to enable virtualization and Microsoft Hyper-V.
3. For security reasons, do not use Docker in the Administrator account, even if you are the sole user on the computer. For Docker version 17.06 or later, your Windows account must be a member of the local group “docker-users” for you to run Docker. To add your account to the group, you need to log into an Adminstrator account and run `Computer Management`. Open up `Local Users and Groups`, select `Groups`, right click on `docker-users` in the list, and then click on `Add to Group...` to add your username to the group.
4. If you previously installed VMWare or VirtualBox on your Windows computer, they might conflict with Docker. You may get an error message stating that virtualization must be enabled when starting Docker, even though virtualization was already enabled. To resolve the issue, go to Windows Features in the Control Panel, disable Hyper-V and then re-enable it.
5. When you use Docker for the first time, you must change its settings to make the C drive shared. To do this, right-click the Docker icon in the system tray, and then click on `Settings...`. Go to `Shared Drives` tab and check the C drive.
6. Docker for Windows saves the images and data volumes in a shared public folder `C:\Users\Public\Documents\Hyper-V\Virtual Hard Disks\MobyLinuxVM.vhdx`. This is a major security risk because all your images and data can be accessed and modified by other Docker users on the same computer. If you are using a shared Windows computer, make sure you create a private folder such as `C:\Users\YourUserName\Documents\Hyper-V\Virtual Hard Disks` and then go to `Advanced` tab in Docker Settings, and change the `Image and Volume VHD Location` to this folder.

**Notes for Linux Users**
* After you install Docker, make sure you add yourself to the Docker group by running the command:
```
sudo adduser $USER docker
```
Then, log out and log back in before you can use Docker.

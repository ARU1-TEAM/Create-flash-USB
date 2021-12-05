## Table of Contents

* [Introduction](#introduction)
* [Set USB On windows](#set-usb-on-windows)
  * [Install Windows On Windows](#install-windows-on-windows)
  * [Install Linux On Windows](#install-linux-on-windows)
* [Set USB On Linux](#set-usb-on-linux)
  * [Install Windows On Linux](#install-windows-on-linux)
  * [Install Linux On Linux](#install-linux-on-linux)
* [Credits](#credits)

## Introduction
This repository is a guide to install windows and linux via different OS. There is also a guide to install a [full custom and functionnal Ubuntu repository](https://github.com/ARU1-TEAM/Ubuntu-installation-XFCE4-I3wm) if you want. 

## Set USB On Windows
This is the guide to set up a flash USB if you are on windows.

### Install Windows On Windows
- First install the [windows tool](https://www.microsoft.com/en-us/software-download/windows10).
- Then follow the instructions to put the iso file on your usb key. 

Now you can reboot your computer and select your usb key in the `boot` section of your BIOS/UEFI


### Install Linux On Windows
Theses instructions are the same as the ÌNstall windows On Linux` you will find them at the end of the repo.

## Set USB On Linux
This is the guide to set up a flash USB if you are on linux.

### Install windows On Linux
- First, install [windows iso file](https://www.microsoft.com/en-us/software-download/windows10ISO). Make shure to take the right version and select your language.
- Now we have to install WoeUsb to set up the flash usb, but we have to install **libwxgtk3** to get it to work. 

~~~sh
wget http://mirrors.kernel.org/ubuntu/pool/universe/w/wxwidgets3.0/libwxgtk3.0-0v5_3.0.4+dfsg-3_amd64.deb
sudo dpkg -i libwxgtk*_amd64.deb
~~~

- Now we will install some dependencies.

~~~sh
sudo apt install git p7zip-full python3-pip python3-wxgtk4.0
sudo pip3 install WoeUSB-ng
~~~
- And finally install the app repository and WoeUsb.
~~~sh
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt install woeusb
~~~
Now that you installed WoeUsb, we will set up the usb. 
- First launch WoeUsb
- Select the iso file that we previously installed 
- Select your Usb ni the `Target device`. 
- Make shure you can see all the available disk by going in the `file` tab and selecting `Display all disks`.
- Now click `install` button. Done !

You can **reboot** and **select** your Usb in the `boot` section of your BIOS/UEFI.


### Install Linux On Linux
- First, install the Linux Iso file that you want. In our case we will install Ubuntu, [click here](https://ubuntu.com/download/desktop#download) to install Ubuntu iso file. But for example if you want to install arch linux, it will be [here](https://archlinux.org/download/). 
- Now [install BalenaEtcher](https://www.balena.io/etcher/) to set up the usb key.
- Click on `Flash form file` and select the iso file.
- Click on `Select target` and select your Usb key.
- Finally click on `flash`. Done !

Once finished you can **reboot** and **select** your usb in the `boot` section of your BIOS/UEFI.






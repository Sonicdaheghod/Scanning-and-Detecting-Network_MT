# Scanning and Detecting Nearby Networks
by Megan Tran

## Table of Contents
* [Purpose of Program](#Purpose-of-program)
* [Screenshots](#Screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Using the Program](#Using-the-Program)
* [Credits](#Credits)

## Purpose of Program

* Practicing using Bash scripting to detect networks and scan them. This allows for analyzing if a network is working properly. It also test the reachability and responsiveness of a network host and other networks.

## Screenshots

<img width="356" alt="image" src="https://github.com/Sonicdaheghod/Scanning-and-Detecting-Network_MT/assets/68253811/1c5ff28e-15aa-40d2-9351-5abd6f835e4b">


## Technologies
Languages/ Technologies used:

* Bash scripting
* Visual Studio Code
* WSL Ubuntu
  
## Setup

1) Download [Ubuntu](https://ubuntu.com/download/desktop)
* Ensure virtualization is enabled
This can be done by going on the BIOS screen. To get here reset your computer and repeatedly press esc, F2, or the keyboard button that you need to press according to your device version/model.
![image](https://github.com/Sonicdaheghod/Scanning-and-Detecting-Network_MT/assets/68253811/8b1752e9-80ab-4ffb-88f4-cfffc30f006d)


* Turn on Windows Subsystem for Linux (Beta)

![image](https://github.com/Sonicdaheghod/Scanning-and-Detecting-Network_MT/assets/68253811/da39039b-8f0e-4f44-9b68-d9a8bacf3dd4)


2) (Optional) Download [Visual Studio Code](https://code.visualstudio.com/download)
* Get the extension WSL
* Type into Ubuntu terminal
``` wslconfig.exe /s Ubuntu ```

The wsl terminal should now be avaliable on VSC application.

## Using the Program

1) Get desired ip address from network interface configuration.

``` ifconfig | grep "broadcast" | cut -d " " -f 10 | cut -d "." -f 1,2,3 | uniq ```

2) Ping only 1 package to save time and see if network connects properly to desired IP address.

``` ping -c 1 (IP address) | grep "64 bytes" | cut -d " " -f 4 ```

4) Create the bash script to automate scanning your specific network using the respectiv eIP address using

``` nano (type name of your bash script) ```

## Credits

* Source code from [Hackpens](https://youtu.be/qhCxKrU1AEY)

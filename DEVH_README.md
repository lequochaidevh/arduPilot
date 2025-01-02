Create develop branch to :
iotProject - fork for iot project purpose


## SETUP + TOOLCHAIN

sudo apt install python3-dev python3-pip python3-setuptools python3-numpy python3-pyparsing python3-psutil python-is-python3 gcc-arm-none-eabi rsync

I get this here

ChibiOS build requires g++ version 10.2.1 or later, found 8.3.1

Found Cannot build ardupilot on MacOS
but not very helpful. g++ 12.2.1-6 is installed here too.

Now I learned (with the help from Yuri_Rage) that I also can build in a Debian bookworm 12 VM

setup (my notes)
~$ sudo apt install git
~$ git clone --recurse-submodules https://github.com/ArduPilot/ardupilot.git
~$ cd ardupilot
~/ardupilot$ ./Tools/environment_install/install-prereqs-ubuntu.sh
~/ardupilot$ source ~/.profile


List available boards

It's possible to get a list of supported boards on ArduPilot with the command below

./waf list_boards

		## AFTER REBOOT - LOGOUT/LOGIN ##

~/ardupilot$ source ~/.profile
~/ardupilot$ ./waf configure --board KakuteF7
~/ardupilot$ ./waf plane




## FLASHING


https://ardupilot.org/copter/docs/common-loading-firmware-onto-chibios-only-boards.html



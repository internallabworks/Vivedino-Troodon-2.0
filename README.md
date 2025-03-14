Klipper config for Vivedino Troodon 2.0
\
***This is still under development, so assume nothing works as it should :)***
\
Config for LDO Nitehawk-SB, Galileo 2 extruder, Cartographer probe, sensorless homing & TMC Autotune.
\
To install TMC Autotune, do the following:
(Copied from [TMC Autotune Github](https://github.com/andrewmcgr/klipper_tmc_autotune).
Installation
To install this plugin, run the installation script using the following command over SSH. This script will download this GitHub repository to your RaspberryPi home directory, and symlink the files in the Klipper extra folder.

```bash
wget -O - https://raw.githubusercontent.com/andrewmcgr/klipper_tmc_autotune/main/install.sh | bash
```

Then, add the following to your moonraker.conf to enable automatic updates:

```ini
[update_manager klipper_tmc_autotune]
type: git_repo
channel: dev
path: ~/klipper_tmc_autotune
origin: https://github.com/andrewmcgr/klipper_tmc_autotune.git
managed_services: klipper
primary_branch: main
install_script: install.sh
```

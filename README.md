ntp-backup
==========

Enables NTP and fake-hwclock to function on a Pi with a read-only file system

From the home directory, run the following command in "read & write mode" (rpi-rw)

    git clone https://github.com/otherWIP/ntp-backup.git && ~/ntp-backup/install

This script is intended to
- 1) move the fake-hwclock back to it's original location if used on OEM SD card image
- 2) comment out the existing fake-hwclocks cron entry and create a ntp-backup cron entry
- 3) add an init script to "backup" current time & drift value at shutdown and by cron
- 4) remove these ntp-backup setup files once installation is done
- 5) get correct time from ntp servers
- 6) backup the current clock data

See [Read-only time issues](http://openenergymonitor.org/emon/node/5877) discusion on OpenEnergyMonitor forum for more info

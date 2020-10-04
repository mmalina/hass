Home Assistant Config
=====================

This repo contains my [Home Assistant](https://www.home-assistant.io) config.

## How to restore on a clean HA install

### First restore your installation from a snapshot
1. Create a temp account
2. Install the Samba add-on
3. Connect to the `backup` share copy over a full snapshot
4. Go to Supervisor -> Snapshots and click your snapshot. Select Wipe & Restore. Wait 5-10 minutes.

### Enable host ssh access

Instructions: https://developers.home-assistant.io/docs/operating-system/debugging/

Note: Don't forget to name the volume `CONFIG`.

### Enable 1-wire

https://www.home-assistant.io/integrations/onewire/

Connect to host via ssh and add this to `/mnt/boot/config.txt`:
```
dtoverlay=w1-gpio
```

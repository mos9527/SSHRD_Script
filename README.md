SSHRD_Script
---
Again, read the original README [here](https://github.com/verygenericname/SSHRD_Script) if you don't know what you are doing.

Tested on macOS Tahoe *ONLY*. 

# Usage 
- Clone this repo
- Enter DFU mode and connect your checkm8 vulnerable iDevice
- Run `./sshrd.sh [your iOS version]`
  - **NOTE:** If downgraded with [Semaphorin](https://github.com/mos9527/Semaphorin), this should be the version **PRIOR** to the downgrade
- Wait for the script to finish
- Run `./sshrd.sh boot` to boot into the ramdisk
- Gain root shell with `./sshrd.sh ssh`
  - Interact with it. Or connect to the device via `ssh root@localhost -p 2222` with password `alpine` through tools e.g. FileZilla, WinSCP, etc.
  - Mount system disks with `mount_hfs` if you're on a really old iOS version, or `mount_apfs` on newer ones, on `/dev/disk0s...` et al.
  - Just do what you have to do.

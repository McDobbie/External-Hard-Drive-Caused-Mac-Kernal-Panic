# External-Hard-Drive-Caused-Mac-Kernal-Panic-and-Restarting
This repository helps solve the Mac OS kernal panic caused by the external hard drive.

A few days ago my LaCie portable hard drive was somehow corrupted. Once I plugged it in, my MacBook froze and automatically restarted. The most scary thing was that it kept restarting until I unplugged the hard drive. It meant that I couldn't use Disk Utility to first aid it.
Normally the corrupted drive just has problem mounting itself and you can still use Disk Utility to fix it. But this time, I was prepared to lose all my precious data.

After checking the kernal panic report, it said:
```
Process name corresponding to current thread: mount_hfs
```
However, I came up with a solution with fragmented information on the Internet.

1. To prevent Mac keeping retarting, download [Disk Arbitrator](https://github.com/aburgh/Disk-Arbitrator) to block automatic mounting. 
2. Open Disk Arbitrator and switch it into Read-only mode.
3. Connect your corrupted drive to your Mac, then you should see it in Disk Arbitrator. Mount it.
4. Then you should see the drive in Finder. Now you can copy and backup all the data you need.
5. Erase the corrupted drive and format it.

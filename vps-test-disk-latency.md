# Testing VPS disk latency with `ioping`

Init:
```sh
ioping . -c 10
```

### RunAbove Sandbox
- 1 core / 2 GB RAM / 20 GB SSD
```
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=1 time=381 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=2 time=505 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=3 time=442 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=4 time=420 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=5 time=1.2 ms
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=6 time=401 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=7 time=494 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=8 time=425 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=9 time=475 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44): request=10 time=440 us

--- . (ext4 /dev/disk/by-uuid/43afc892-997a-408a-b56f-6cc957c27a44) ioping statistics ---
10 requests completed in 9.0 s, 1.9 k iops, 7.5 MiB/s
min/avg/max/mdev = 381 us / 521 us / 1.2 ms / 239 us
```

### EC2 Micro
- 1 core / 1 GB RAM / 8 GB
```
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=1 time=276 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=2 time=364 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=3 time=386 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=4 time=480 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=5 time=414 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=6 time=495 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=7 time=421 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=8 time=412 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=9 time=495 us
4.0 KiB from . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c): request=10 time=539 us

--- . (ext4 /dev/disk/by-uuid/eadf02fe-ee58-47f8-88aa-a5b893092f0c) ioping statistics ---
10 requests completed in 9.0 s, 2.3 k iops, 9.1 MiB/s
min/avg/max/mdev = 276 us / 428 us / 539 us / 73 us
```

### Digital Ocean
- 1 core / 512 MB RAM / 20 GB SSD
```
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=1 time=105 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=2 time=676 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=3 time=334 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=4 time=649 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=5 time=302 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=6 time=474 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=7 time=338 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=8 time=303 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=9 time=551 us
4.0 KiB from . (ext4 /dev/disk/by-label/DOROOT): request=10 time=339 us

--- . (ext4 /dev/disk/by-label/DOROOT) ioping statistics ---
10 requests completed in 9.0 s, 2.5 k iops, 9.6 MiB/s
min/avg/max/mdev = 105 us / 407 us / 676 us / 168 us
```

### Vultr
- 2 core / 2048 MB RAM / 45 GB SSD
```
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=1 time=1.4 ms
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=2 time=377 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=3 time=298 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=4 time=317 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=5 time=360 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=6 time=314 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=7 time=328 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=8 time=388 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=9 time=306 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d): request=10 time=318 us

--- . (ext3 /dev/disk/by-uuid/6392f8cf-6d14-4dad-9d19-ccab0cdff94d) ioping statistics ---
10 requests completed in 9.0 s, 2.2 k iops, 8.8 MiB/s
min/avg/max/mdev = 298 us / 445 us / 1.4 ms / 336 us
```

### Scaleway
- 4 core (ARM) / 2048 MB RAM / 50 GB LSSD
```
4.0 KiB from . (ext4 /dev/nbd0): request=1 time=577 us
4.0 KiB from . (ext4 /dev/nbd0): request=2 time=593 us
4.0 KiB from . (ext4 /dev/nbd0): request=3 time=611 us
4.0 KiB from . (ext4 /dev/nbd0): request=4 time=598 us
4.0 KiB from . (ext4 /dev/nbd0): request=5 time=563 us
4.0 KiB from . (ext4 /dev/nbd0): request=6 time=563 us
4.0 KiB from . (ext4 /dev/nbd0): request=7 time=572 us
4.0 KiB from . (ext4 /dev/nbd0): request=8 time=563 us
4.0 KiB from . (ext4 /dev/nbd0): request=9 time=584 us
4.0 KiB from . (ext4 /dev/nbd0): request=10 time=550 us

--- . (ext4 /dev/nbd0) ioping statistics ---
10 requests completed in 9.1 s, 1.7 k iops, 6.8 MiB/s
min/avg/max/mdev = 550 us / 577 us / 611 us / 18 us
```
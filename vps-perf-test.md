# Testing VPS performance

### RunAbove Sandbox [ra]
- 1 core / 2 GB RAM / 20 GB SSD

### EC2 Micro [ec]
- 1 core / 1 GB RAM / 8 GB

### Digital Ocean [do]
- 1 core / 512 MB RAM / 20 GB SSD

## Using ‘dd’ to benchmark disk read/write performance

Init:
```sh
mkdir ~/_bench/
cd ~/_bench/
```

### Write

```sh
dd if=/dev/zero of=diskbench bs=1M count=1024 conv=fdatasync
```

[ra]: `1073741824 bytes (1.1 GB) copied, 7.35618 s, 146 MB/s`
[ec]: `1073741824 bytes (1.1 GB) copied, 16.9822 s, 63.2 MB/s`
[do]: `1073741824 bytes (1.1 GB) copied, 2.12969 s, 504 MB/s`

### Read

Clear cache
```sh
echo 3 | sudo tee /proc/sys/vm/drop_caches
```

```sh
dd if=diskbench of=/dev/null bs=1M count=1024
```
Uncached
[ra]: `1073741824 bytes (1.1 GB) copied, 5.71051 s, 188 MB/s`
[ec]: `1073741824 bytes (1.1 GB) copied, 16.5122 s, 65.0 MB/s`
[do]: `1073741824 bytes (1.1 GB) copied, 1.06747 s, 1.0 GB/s`

Cached
[ra]: `1073741824 bytes (1.1 GB) copied, 0.780069 s, 1.4 GB/s`
[ec]: `1073741824 bytes (1.1 GB) copied, 16.3098 s, 65.8 MB/s`
[do]: `1073741824 bytes (1.1 GB) copied, 0.957031 s, 1.1 GB/s`

## Using ‘dd’ to benchmark CPU performance

```sh
dd if=/dev/zero bs=1M count=1024 | md5sum
```

[ra]: `1073741824 bytes (1.1 GB) copied, 2.36411 s, 454 MB/s`
[ec]: `1073741824 bytes (1.1 GB) copied, 2.46927 s, 435 MB/s`
[do]: `1073741824 bytes (1.1 GB) copied, 2.95077 s, 364 MB/s`
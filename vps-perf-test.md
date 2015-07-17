# Testing VPS performance

## Using ‘dd’ to benchmark disk read/write performance

Init:
```sh
mkdir ~/_bench/
cd ~/_bench/
```

```sh
dd if=/dev/zero of=diskbench bs=1M count=1024 conv=fdatasync
```

### RunAbove Sandbox
- 1 core / 2 GB RAM / 20 GB SSD

```sh
1024+0 records in
1024+0 records out
1073741824 bytes (1.1 GB) copied, 7.35618 s, 146 MB/s
```

### EC2 Micro
- 1 core / 1 GB RAM / 8 GB

```sh
1024+0 records in
1024+0 records out
1073741824 bytes (1.1 GB) copied, 16.9822 s, 63.2 MB/s
```

### Digital Ocean
- 1 core / 512 MB RAM / 20 GB SSD

```sh
1024+0 records in
1024+0 records out
1073741824 bytes (1.1 GB) copied, 2.12969 s, 504 MB/s
```

```sh

```

```sh

```

```sh

```
# Mini Linux

Custom Linux distribution built using Buildroot.

## Features

- Custom x86_64 Linux kernel
- BusyBox userspace
- Python 3.14 integration
- Dropbear SSH server
- QEMU virtualization
- SSH remote access

---

## Technologies Used

- Buildroot
- Linux Kernel
- QEMU
- Python3
- BusyBox
- Dropbear SSH

---

## Build Process

### Configure Buildroot

```bash
make menuconfig
```

### Build System

```bash
make
```

### Run in QEMU

```bash
qemu-system-x86_64 \
-kernel output/images/bzImage \
-hda output/images/rootfs.ext2 \
-append "root=/dev/sda console=ttyS0 noapic nolapic" \
-net nic \
-net user,hostfwd=tcp::2222-:22 \
-nographic
```

---

## SSH Access

```bash
ssh root@localhost -p 2222
```

---

## Verification

```bash
uname -a
python3 --version
```

---

## Learning Outcomes

- Linux kernel compilation
- Root filesystem generation
- Cross compilation
- QEMU virtualization
- SSH networking
- Embedded Linux engineering

---

## Future Improvements

- systemd support
- custom Python services
- Docker integration
- Kubernetes edge deployment

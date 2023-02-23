# snapxi

Script to manipulate BTRFS snapshots optimized to Void's xbps package manager. 

# Dependencies

- Ruby

- Gem `net-ping`

If you use a debian based distro, something like `sudo apt install ruby`
and `sudo gem install net-ping` will solve the aforementioned dependencies.

- `snapxi` also expects a few things to work properly:

* a subvolume `@` mounted to `/`.

* a subvolume `@snapshots` mounted to `/.snapshots`. 

* both `@` and `@snapshots` subvolumes to be in the same partition.
Such a partition  must be specified in the `device = ` variable (first lines). 

**Note** that if you have an encrypted device you
need to use `/dev/mapper/[something]` instead of the usual `/dev/sd[X]`. A good test to 
check if your system meets `snapxi` requirements is to mount your `device` to `/mnt`, like:
`sudo mount /dev/mapper/crypto-luks /mnt`. After successfull mount, you must see `@` and  `@snapshots` subvolumes in `/mnt`. After such a test, you can safely unmount `/mnt` just doing `sudo umount /mnt`


# Installation

1. Copy the snapxi script to your path

2. Make it executable

3. Run `sudo snapxi help` for commands. 

# Manual

[PART 1 (youtube)](https://youtu.be/JxDLSmV75ww)

[PART 2 (youtube)](https://youtu.be/Yuosif8C80c)

# Troubleshooting

# Known Bugs

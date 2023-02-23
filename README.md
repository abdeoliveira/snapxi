# snapxi

Script to manipulate BTRFS snapshots optimized for Void's xbps package manager. 

# Dependency

- Ruby

# Configuration

`snapxi` expects a few things to work properly:

1. a subvolume `@` mounted to `/`.

2. a subvolume `@snapshots` mounted to `/.snapshots`. 

3. both `@` and `@snapshots` subvolumes to be in the same partition.
Such a partition  must be specified in the `device = ` variable (first lines of 
`snapxi` code). 

## Note on encrypted devices

For the aforementioned `device` you need to use `/dev/mapper/[something]` instead of the usual `/dev/sd[X]`. A good test to 
check if your system meets `snapxi` requirements is to mount your `device` to `/mnt`, like:
`sudo mount /dev/mapper/crypto-luks /mnt`. After successful mount, you must see `@` and  `@snapshots` subvolumes in `/mnt`. 
After such a test, you can safely unmount `/mnt` just doing `sudo umount /mnt`


# Installation

1. Copy the snapxi script to your `PATH`.

2. Make it executable.

# Manual

Run `sudo snapxi help` for commands. 

Please also check the videos in the links below.

[PART 1 (youtube)](https://youtu.be/JxDLSmV75ww)

[PART 2 (youtube)](https://youtu.be/Yuosif8C80c)

# Troubleshooting

# Known Bugs

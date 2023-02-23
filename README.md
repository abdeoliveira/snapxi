# snapxi

Script to manipulate BTRFS snapshots optimized to Void's xbps package manager. 

# Dependencies

- Ruby

- Gem `net-ping`

If you use a debian based distro, something like `sudo apt install ruby`
and `sudo gem install net-ping` will solve the aforementioned dependencies.

# Installation

1. Copy the snapxi script to your path

2. Make it executable (`chmod +x snapxi`)

3. Note that snapxi expects 

- a subvolume `@` mounted to `/`.

- a subvolume `@snapshots` mounted to `/.snapshots`. 

- both `@` and `@snapshots` subvolumes to be in the same partition.

4. The partition containing `@` and `@snapshots` subvolumes must be specified
in `device = ` variable (first lines). Note that if you have an encrypted device you
want to use `/dev/mapper/[something]` instead of the usual `/dev/sd[X]`. A good test to 
check if you meet `snapxi` requirements is to try mounting your `device` to `/mnt`, like:

`sudo mount /dev/mapps/crypto-luks /mnt`.

After successfull mount, you must see `@` and  `@snapshots` subvolumes
at `/mnt`. After such a test, you can safely unmount `/mnt` just doing `sudo umount /mnt`

# Manual

[PART 1 (youtube)](https://youtu.be/JxDLSmV75ww)

[PART 2 (youtube)](https://youtu.be/Yuosif8C80c)

# Troubleshooting

# Known Bugs

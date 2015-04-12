# Snap

## Backuping

```
# Initialize .snap
snap init <volume>
# Need new entry in /etc/fstab

# Make a snapshot
snap <volume>

# Sync remote
snap sync <volume> <remote> <remotedir>

# List snapshots
snap list <volume>

# Restore
snap restore <volume> <id>

# Delete
snap delete <volume>

```

## Init

Initialize create a dir .snaps on the btrfs volume is sub volume 0.
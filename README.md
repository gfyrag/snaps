# Snap

Snap is a set of bash scripts managing btrfs volumes.

## How it works?

Snaps create a simple directory structure as follow : 

<pre>
+ snapDirectory
---- snaps
---- workdir
</pre>

workdir is the main volume when you do your stuff.
snaps contains your snapshots.

## Initialize

```
snap init <directory>
```

This command will generate tree and create the subvolume "workdir"

## Make a snapshot

```
snap snap -m <message> <directory>
```

This command make a snapshot of the current workdir.
The '-m' flag allow to specify a message which will be write in snaps/&lt;snapId&gt;/.snapmessage

## Synchronize with remote

```
snap sync <directory> <sshRemote> <sshRemoteDir>
```

This command will synchronize with a remote host

## List snapshots

```
snap list <directory>
```

## Restore

```
snap restore <directory> <id>
```

## Delete

```
snap delete <volume>
```

Be carefull, currently this command will remove all data.
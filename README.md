# BorgBackup
Docker Container for the [BorgBackup](https://www.borgbackup.org/) to be used as backup client

Dockerfile contains the following
- [Bitnami Minideb](https://hub.docker.com/r/bitnami/minideb/) based on [Debian Stretch](https://www.debian.org/)
- BorgBackup
- OpenSSH client

## Running
Run this container and list the backups at the remote host

```
docker run \
	--rm \
	--interactive \
	--tty \
--volume "/home/solteqmagento-docker:/root" 
	--env BORG_REPO="borgbackup@<host>:/backups/repository" \
	--env BORG_PASSPHRASE="<passphrase>" \
	solteqmagento/borg-client list
```

# Home Raspberry Pi Services

## Nextcloud

### Setup

1. Attach and mount external disk.
2. Find disk image file with encrypted Nextcloud data (example: `nextcloud.img`).
3. Mount image in `nextcloud/html/data/` directory.
```
# cryptsetup luksOpen nextcloud.img nextcloud
# mount /dev/mapper/nextcloud nextcloud/html/data/
```
4. (Optional) Find disk image file with encrypted Postgres data (example: `postgres.img`).
5. (Optional) Mount image in `postgres/data/` directory.
```
# cryptsetup luksOpen postgres.img postgres
# mount /dev/mapper/postgres postgres/data/
```
6. Start Docker services using `docker-compose up --detach`.

**Notes**: Commands executed after `#` requires root privileges.

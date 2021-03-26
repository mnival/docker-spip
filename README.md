# Docker SPIP

This project is a fork of IPEOS official Docker Spip [images set](https://hub.docker.com/r/ipeos/spip/).

This image was originally created by [IPEOS](http://www.ipeos.com) for a purpose of web development training courses.

Dockerfile to provide a ready to use SPIP in production.

This docker use [SPIP-cli](https://contrib.spip.net/SPIP-Cli) project to manage an auto install for SPIP. It can be use to manage the SPIP with command line.

## Supported Tags Respective `Dockerfile` Links

- `3.2`, `3.2.9`, `latest`
- `3.1`, `3.1.15`

**Remove 3.0 tag support**

## Installation

Automated builds of the image are available on [Dockerhub](https://hub.docker.com/u/mnival/spip/) and is the recommanded method of installation.

```bash
docker pull mnival/spip:latest
```

## Quick Start

```bash
docker run --name some-spip --link some-mysql:mysql -p 8080:80 -d mnival/spip
```

## Available Environment Vars

**Auto-install is only available on SPIP 3.1 and 3.2 versions**

- `SPIP_DB_SERVER`: connexion method to the database `sqlite3` or `mysql` (default: `mysql`)
- `SPIP_DB_PREFIX`: SQL table preffix (default: `spip`)

### For MySQL Database Only

**The MySQL database must exist before installation. It will not be automatically created.**

- `SPIP_DB_HOST`: MySQL server hostname or IP (default: `mysql`)
- `SPIP_DB_LOGIN`: MySQL user login (default: `spip`)
- `SPIP_DB_PASS`: MySQL user password (default: `spip`)
- `SPIP_DB_NAME`: MySQL database name (default: `spip`)

### Admin Account

- `SPIP_ADMIN_NAME`: account name (default: `Admin`)
- `SPIP_ADMIN_LOGIN`: account login (default: `admin`)
- `SPIP_ADMIN_EMAIL`: account email (default: `admin@spip`)
- `SPIP_ADMIN_PASS`: account password (default: `adminadmin`)

### PHP Vars

Can change PHP vars to optimize your installation.

- `PHP_MAX_EXECUTION_TIME` (default: `60`)
- `PHP_MEMORY_LIMIT` (default: `256M`)
- `PHP_POST_MAX_SIZE` (default: `40M`)
- `PHP_UPLOAD_MAX_FILESIZE` (default `32M`)
- `PHP_TIMEZONE` (default: `Europe/Paris`)

## Contributing

If you find this image useful here's how you can help:

- Send a Pull Request with your awesome enhancements and bug fixes
- Be a part of the community and help resolve Issues

## Team

* [Michael Nival](https://github.com/mnival/)

### IPEOS

- [Laurent Vergerolle](https://github.com/psychoz971/)
- [Olivier Watté](https://github.com/owatte/)

# Ansible Database Restore

[![Build Status](https://travis-ci.org/roquie/ansible-db-restore.svg?branch=master)](https://travis-ci.org/roquie/ansible-db-restore)

Automatically restore database from dump or connection.

Example, how to use, can be found at `tests` directory.

## How to dump 

[Official documentaiton.](https://www.postgresql.org/docs/current/static/app-pgdump.html)

Example:

```
pg_dump -F t -O -x -d ansible-db-restore -n public > test-db.tar
```

## Supported Databases

For now supports:
* PostgreSQL

## Supported OS

* Ubuntu 16.04 LTS
* Ubuntu 14.04 LTS
* Centos 7
* Debian 8
* Debian 9

## Vagrant

* `cd /path/to/project`
* `cd tests && ansible-galaxy install -r requirements.yml && cd ..`
* `vagrant up` 

### Warning
    
If u want rename project, make sure to rename role (`ansible-db-restore`) inside `tests/playbooks/vagrant.yml`.

## License

MIT

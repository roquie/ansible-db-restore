# Ansible Database Restore

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

For now supports:
* Ubuntu 16.04 LTS

## Vagrant

* `cd /path/to/project`
* `cd tests && ansible-galaxy install -r requirements.yml && cd ..`
* `vagrant up` 

### Warning
    
If u want rename project, make sure to rename role (`ansible-db-restore`) inside `tests/playbooks/vagrant.yml`.

## License

MIT

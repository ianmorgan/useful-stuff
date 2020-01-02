# Connecting to Postgres

Some notes to connecting to a postgres database.

## On the server 

```bash
sudo -u postgres psql
```

_note, must connect under the `postgres` user account, or create a new role with matching use account_

## Remotely 

```bash
psql -U <user> -h  <host> <database>

# for example
psql -U corda -h  ec2-35-176-144-236.eu-west-2.compute.amazonaws.com corda    
```


## See also 
* [Install on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04)






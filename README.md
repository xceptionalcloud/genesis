Instructions for starting over or building a new environment for IT automation.

# Spin up a new server
Minimum - 2CPU, 8GB, 60GB // Typical - 2CPU, 12GB, 300GB

# Install Ubuntu

Enable su root login
```bash
sudo passwd root
```

Update ubuntu and apt tool
```bash
sudo apt-get upgrade
sudo apt update
```

Install and enable ssh
```bash
sudo apt-get install openssh-server
sudo systemctl enable ssh
sudo ufw allow 'OpenSSH'
```

Install apache2 and allow firewall
```bash
sudo apt-get install apache2
sudo ufw allow 'Apache'
```

Install postgresql
```bash
sudo apt install postgresql postgresql-contrib
```
Setup postgresql
```bash
sudo passwd postgres
su postgres
psql
* CREATE ROLE xndev WITH
    LOGIN
    SUPERUSER
    INHERIT
    CREATEDB
    CREATEROLE
    REPLICATION;
\q
```

Install git (and setup keys)

Install pip3

Install python3

Install python modules (list)

# Optional installs
SoapUI

Postman

pgAdmin

pyCharm

Chrome

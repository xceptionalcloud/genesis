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
ssh-keygen (if ~/.ssh/rsa_id.pub does not exist)
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
psql# CREATE ROLE xndev WITH
#   LOGIN
#   SUPERUSER
#   INHERIT
#   CREATEDB
#   CREATEROLE
#   REPLICATION;
#   
# CREATE DATABASE xndev WITH OWNER xndev;
# \q
```

Install git (and setup keys)
```bash
sudo apt install git-all
sudo apt-get install xclip
xclip -sel clip < ~/.ssh/rsa_id.pub
(edit github profile and paste this key into SSH key section)
```

Install or Upgrade python3
```bash
python3 --version (checks if installed)
sudo apt-get upgrade python3 ---OR--- sudo apt-get install python3
```

Install pip3
```bash
pip3 --version (checks if installed)
sudo apt-get upgrade python3-pip ---OR--- sudo apt-get install python3-pip
```
Install python modules (list)
```bash
pip3 install requests
pip3 install netmiko
pip3 install configparser
sudo apt-get install libpq-dev
pip3 install psycopg2
pip3 install lxml
```
# Optional installs
SoapUI

Postman

pgAdmin

pyCharm

Chrome

# Linux Server Configuration

## Server URL
http://35.163.124.151/

## IP address
35.163.124.151

##SSH
You can connect by ssh using port 2200 and the rsa key provided.
ssh -i [rsa key file] grader@35.163.124.151 -p 2200

## Software installed
apache2
libapache2-mod-wsgi
postgresql
git
pip
Flask
python-psycopg2
finger

## Configuration changes
Updated all installed packages
Changed ssh port to 2200
Configured ssh to only allow key based access
Set time to utc
Configured ufw to only allow SSH (port 2200), HTTP (port 80), and NTP (port 123)
Activated ufw
Created and configured two new users:
	grader(sudoer)
	catalog (database owner)
Setup PostgreSQL database for item catalog project
Configured apache to server wsgi application Item catalog
Customized Item catalog project to use PostgreSQL database
Disabled listing of .git directory
Disabled root ssh access

## Third-party resources
* https://ie.godaddy.com/help/changing-the-ssh-port-for-your-linux-server-7306
* http://idroot.net/tutorials/how-to-change-ssh-port-in-ubuntu/
* http://askubuntu.com/questions/3375/how-to-change-time-zone-settings-from-the-command-line
* https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
* https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
* http://www.jakowicz.com/flask-apache-wsgi/
* https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
* http://serverfault.com/questions/128069/how-do-i-prevent-apache-from-serving-the-git-directory
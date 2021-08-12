# Install_PostgreSQL_On_Ubuntu-20.04
This tutorial explain how to install PostgreSQL on Ubuntu 20.04, let's start..

    sudo apt update
    
    sudo apt install postgresql
    
## Test PostgreSQL Shell

    sudo - postgres
    
    psql
    
## Install PGAdmin 4
Add key:

    sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
    
Add Repo:

    sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

Start Install:
    
    su - root
    sudo apt install pgadmin4
    
If Error happen :

    E: Could not open lock file /var/lib/dpkg/lock-frontend ...
    
Give this command:

    sudo fuser -vki /var/lib/dpkg/lock-frontend

Continue install process :

    sudo apt install pgadmin4

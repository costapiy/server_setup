# How to deploy a Django project in a Linux server
1. [Deploy bare metal linux server](https://github.com/costapiy/server_setup/blob/main/1.Server%20deploy.md)
    - Update server software
    - Setup domain name
    - Set hostname
    - Set timezone
    - Create a new user
    - Allow only the new user to login via ssh.

2. [Create and deploy a Django project](https://github.com/costapiy/server_setup/blob/main/2.Django%20deployment.md)
    - Install python and dependencies
    - Create a new ssh key pair for github
    - Run the Django development server and check if it's accesible from the internet

3. [Install and setup Gunicorn](https://github.com/costapiy/server_setup/blob/main/3.Gunicorn%20setup.md)
    - Install Gunicorn
    - Create a systemd service to run gunicorn on startup
    - Test if the project is accesible from Gunicorn instead of Django development server

4. [Setup Nginx](https://github.com/costapiy/server_setup/blob/main/4.Nginx%20setup.md)
    - Create an nginx config usign [nginxconfig.io](https://nginxconfig.io)
    - Change some parts of the config to accomodate for Gunicorn (default is uWSGI)
    - Install certbot and manage certificates
    - Dry run cerbot cron certificate update

5. [Firewall setup](https://github.com/costapiy/server_setup/blob/main/5.Firewall%20setup.md)
    - Setup firewall to only allow SSH, HTTP and HTTPS traffic
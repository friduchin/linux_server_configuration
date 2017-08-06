# Linux Server Configuration
This is a Udacity FSND learning project of configuring a linux server to host a web application.
The Amazon Lightsail Ubuntu server instance is configured to include Apache web server with WSGI and PostgreSQL to host the deployed python data-driven web app.

### Connection data
- IP: 52.58.39.201
- SSH port: 2200
- URL: http://52.58.39.201

### Configuration details
- A new Ubuntu Linux server instance on Amazon Lightsail has been created.
- All currently installed packages have been updated.
- The SSH port has been changed from 22 to 2200.
- The Uncomplicated Firewall (UFW) has been configured to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123). And the Lightsale firewall is set to allow connections on port 2200.
- The _grader_ user has been created to be able to connect to the server via SSH using key-based authentication and to perform sudo actions.
- The server local timezone is set to UTC.
- Apache has been installed and configured to serve a Python mod_wsgi application.
- PostgreSQL has been installed and configured to not allow remote connections. A new database user named _catalog_ has been created with limited permissions to _catalog_ database used for the application.
- [Item Catalog](https://github.com/friduchin/item_catalog) project has been deployed and set up to be accessible on the server’s IP address via a web browser.

### References
- https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04

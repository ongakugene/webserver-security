# webserver-security
Final Project for Udacity Full Stack Developer Nanodegree

### As per the instructions, following is the project information:

### i. The IP address and SSH port so your server can be accessed by the reviewer.
IP Address - 52.11.186.120
SSH port - 2200

### ii. The complete URL to your hosted web application.
URL - http://ec2-52-11-186-120.us-west-2.compute.amazonaws.com

### iii. A summary of software you installed and configuration changes made.
1. I have installed pip, git, apache2, postgresql, psycopg2.
2. For the configuration changes, I first put apache up and tested the default welcome page.
3. I configured ufw and enabled the firewall
4. I changed default ssh port to 2200 and restarted ssh service.
5. I installed postgresql
6. I created a user catalog and granted it access to dbcatalog which the app now uses.
7. I changed the app.config['SQLALCHEMY_DATABASE_URI'] to the Postgres DB with the correct credentials.
8. I added the EC2 hostname to Dev Console on Google for Javascript origins.
9. I updated client-secrets json file with these new values included.
10. Then I included WSGIScriptAlias to Apaches's sites-enabled's default config file and restarted apache server.
11. I created this wsgi script in /srv/item-catalog and included the app in it.
12. I installed all the projects dependencies using pip, specifically flask-sqlalchemy, flask-bootstrap, flask-wtf, oauth2client, requests and dicttoxml.
13. I could successfully access the project, login using G+ and create categories/items.
14. The root login is not allowed even using keys for security. Login is permitted as user grader using key authentication.

### iv. A list of any third-party resources you made use of to complete this project.
I referenced the tutorial on the following [site](http://killtheyak.com/use-postgresql-with-django-flask/) to find out how to change sqlite URL to postgres for Flask-SQLAlchemy.

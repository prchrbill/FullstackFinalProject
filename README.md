# Linux Server Deployment Project  #

**Public IP Address**:18.219.106.242

**My catalog project address** : http://ec2-18-219-106-242.us-east-2.compute.amazonaws.com/

  (you have to access it with this link)
  
 ##  Summary of Software Installed: ##
	- AWS Lightsail Instance
	- Ubuntu 
	- Python 2.7
	- Apache2
	- Flask
	- PostgreSQL
	- finger
	- mod_wsgi
	- Git
	- Oauth.client
	- MYSQL -(not used this project)
	- PHP7
  
 ## Configurations: ##
- Created user grader with sudo rights via ***`/etc/sudoers.d/grader*`**
- password for grader is **'grader'**
- grader ALL=(ALL:ALL) ALL
- SSH port changed to 2200 in ***`/etc/ssh/sshd_config`***

##   Configured Firewall ##
	- sudo ufw allow 2200/tcp
	- sudo ufw allow 80/tcp
	- sudo ufw allow 123/udp
  
##  Set local time to UTC ##
	1. *`sudo dpkg-reconfigure tzdata`*
	1. select none of the above
	1. on next screen choose UTC
 
##  Set up host file to run catalog application ##
***`/etc/apache2/sites-available/mywebsite.conf`***
 
 ## Set up Database in postgreSQL ##
	- Created user 'catalog' with passord of 'catalog' with limited rights
	- Created user 'Spiderman' with password of 'freddy03' as a superuser
	- created database 'mylibrary.db' owned by 'Spiderman'
	- Spiderman is used in mylibrary.py and library_database_setup.py to do the database work
	- (he is your friendly neighborhood Spiderman)
    
*	Git repository https://github.com/prchrbill/My-Library.git was cloned
	to the folder ***~/My-Library***. From there it was edited and pushed
	back to the repository. Files were then copied to ***`/var/www/FlaskApps/mywebsite/`***
	to be used by the webserver. *

  
## List of sources used to help me: ##
  - Udacity Forums so helpful with my Oauth problems.
-   https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-14-04
-   https://howtoubuntu.org/how-to-cut-copy-and-paste-in-the-terminal-in-ubuntu
-   https://help.github.com/articles/error-permission-denied-publickey/
-   https://serverfault.com/questions/284566/configuration-for-multiple-port-ssh
-   https://askubuntu.com/questions/60228/how-to-remove-all-files-from-a-directory
-   https://www.atlantic.net/managed-hosting/how-to-install-apache-mysql-php-lamp-stack-ubuntu-16-04/
-   https://pypi.org/project/Flask/1.0.1/
-   https://help.ubuntu.com/lts/serverguide/httpd.html
-   http://amunategui.github.io/idea-to-pitch/
-   https://support.rackspace.com/how-to/apache-configuration-on-ubuntu/
-   https://www.cyberciti.biz/faq/ubuntu-copy-file-command/
-   https://stackoverflow.com/questions/22353512/how-to-install-sqlalchemy-on-ubuntu
-   https://askubuntu.com/questions/86822/how-can-i-copy-the-contents-of-a-folder-to-another-folder-in-a-different-directo
-   https://stackoverflow.com/questions/21239571/syntax-error-on-wsgi-file-setting-up-flask-app-with-apache
-   https://askubuntu.com/questions/348658/what-package-is-usr-sbin-apache2-part-of
-   https://devops.profitbricks.com/tutorials/install-and-configure-mod_wsgi-on-ubuntu-1604-1/
-   https://askubuntu.com/questions/709843/how-to-configure-ufw-to-allow-ntp-to-work
-   https://ubuntuforums.org/showthread.php?t=1212857
-   https://stackoverflow.com/questions/18395622/remote-login-as-root-in-ubuntu
-   https://askubuntu.com/questions/6723/change-folder-permissions-and-ownership
-   https://askubuntu.com/questions/466549/bash-home-user-ssh-authorized-keys-no-such-file-or-directory
-   https://stackoverflow.com/questions/17821269/adding-ssh-key-to-authorized-keys-permission-deniedpublickey
-   https://askubuntu.com/questions/455664/change-group-access-to-directory-and-all-sub-directories-and-files
-   https://www.cyberciti.biz/faq/howto-restart-ssh/
-   https://stackoverflow.com/questions/6142437/make-git-directory-web-inaccessible
-   https://www.postgresql.org/docs/9.2/static/manage-ag-tablespaces.html
-   https://help.ubuntu.com/lts/serverguide/git.html.en#git-configuration
-   https://help.ubuntu.com/lts/serverguide/git.html
-   https://askubuntu.com/questions/423355/how-do-i-check-if-a-package-is-installed-on-my-server
-   https://askubuntu.com/questions/919915/how-to-install-the-json-extension-for-ubuntu-16-04/919917#919917
-   https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html
-   docs.sqlalchemy.org/en/latest/errors.html#error-e3q8
-   https://wiki.postgresql.org/wiki/Using_psycopg2_with_PostgreSQL
-   https://stackoverflow.com/questions/11583714/install-psycopg2-on-ubuntu
-   https://www.postgresql.org/docs/8.1/static/manage-ag-createdb.html
-   https://www.postgresql.org/docs/6.3/static/c0702.htm
-   https://www.postgresql.org/docs/9.0/static/ddl-schemas.html
-   https://stackoverflow.com/questions/18345763/installing-request-module-in-python-2-7-windows
-   https://askubuntu.com/questions/138423/how-do-i-change-my-timezone-to-utc-gmt
-   https://en.wikipedia.org/wiki/Ssh-keygen
-   https://www.computerhope.com/unix/upasswor.htm
-   https://help.ubuntu.com/community/Sudoers

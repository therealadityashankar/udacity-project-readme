# readme regarding the working of this app

public-ip/url to see website: 13.233.132.163

## summary of software installed:
  - pip and pip3
  - flask
  - sqlAlchemy
  - git
  - oauth2client
  - psycopg2
  - PostgreSQL
  - Apache HTTP Server
  - virtualenv
  - mod-wsgi

## location of contents

the presented webite's files is located at
`/var/www/item_catalog/`

access it using
`cd /var/www/item_catalog/`## configurations made

  - ufw
ufw is made to allow ports 2200, 123, and 80
port 22 is blocked here
using the command `ufw allow {port_number}`

  - postgres
a user and table udacity_catalog was added to postgres with a password

  - previous udacity project
engine access is now throught
`engine = create_engine("postgresql://username:password@localhost/udacity_catalog")'

  - ssh port was changed to 2200 from 22 in `/etc/ssh/sshd_confing`
(note: lightsail by default removes password based authentication, thought that may also be changed fromm here)

  - grader user was added and given root permissions
using the `adduser` tool and the `sudo -aG` command

  - all packages are updated using `sudo apt update` and `sudo apt upgrade`

  - apache2
added to support wsgi and `/etc/apache2/sites-available/` is modified to supportthe previous udacity project

## third party resources used

  - lightsail
  - https://www.postgresql.org/
  - https://blog.codeasite.com/how-do-i-find-apache-http-server-log-files
               

wsgi config file location -
`/etc/apache2/sites-available/item_catalog.conf`

and can be accessed by

`sudo vi /etc/apache2/sites-available/item_catalog.conf`


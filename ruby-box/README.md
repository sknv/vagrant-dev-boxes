# ruby-postgres-box

A Vagrant-powered virtual machine for Ruby application development.

Default PostgreSQL port 5432 in the host computer is forwarded to port 5432 in the virtual machine.

Port 3000 in the host computer is also forwarded to port 3000 in the virtual machine. Thus, applications running in the virtual machine can be accessed via localhost:8000 in the host computer. Be sure the web server is bound to the IP 0.0.0.0, instead of 127.0.0.1, so it can access all interfaces, e.g.:

    $ bin/rails server -b 0.0.0.0

## What's In The Box

* PostgreSQL 9.6 with 'postgres:vagrant' superuser

* Ruby 2.4 with disabled automatic documentation

* NodeJS 8.x LTS with Npm

* The latest stable Git
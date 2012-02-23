Description
===========

This cookbook installs the percona-release apt or yum repository and allows you to install the client and/or server..

More info:  http://www.percona.com/docs/wiki/percona-server:release:start


Requirements
============

none

Attributes
==========

none

Recipes
=======

* client  - Installs Percona client
* server  - Installs Percona server
* default - Installs percona-release apt or yum repository

Usage
=====

Include the percona recipe to install the percona-release apt or yum repository

    include_recipe "percona-install"

Or add it to your role, or directly to a node's recipes.



Include the percona-install::client recipe to install the percona client

    include_recipe "percona-install::client"

Or add it to your role, or directly to a node's recipes.


Include the percona-install::server recipe to install the percona server

    include_recipe "percona-install::server"

Or add it to your role, or directly to a node's recipes.

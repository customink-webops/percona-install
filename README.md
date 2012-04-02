Description
===========

This cookbook installs the percona-release apt or yum repository and allows you to install the client and/or server. A recipe is also included for the Percona Monitoring Plugins.

More info:  
  * http://www.percona.com/docs/wiki/percona-server:release:start
  * http://www.percona.com/software/percona-monitoring-plugins/


Requirements
============

none

Attributes
==========

These attributes are used by the monitoring recipe:

* `node['percona-install']['plugins_url']` - The base URL for the percona-monitoring-plugins
* `node['percona-install']['plugins_version']` - The version of plugins to be installed
* `node['percona-install']['plugins_sha']` - The sha of the downloaded tar gzip file.
* `node['percona-install']['plugins_path']` - The directory in which the plugins will be installed
* `node['percona-install']['plugins_nagios']` - The directory in which the nagios plugins will be installed

Recipes
=======

* default    - Installs percona-release apt or yum repository
* client     - Installs Percona client
* server     - Installs Percona server
* monitoring - Installs Percona monitoring plugins

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

Include the percona-install::monitoring recipe to install the percona monitoring tools

    include_recipe "percona-install::monitoring"

Or add it to your role, or directly to a node's recipes.

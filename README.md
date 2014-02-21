Role Name
========

This role installs MariaDB 5.5 on Debian Wheezy.
It also installs python-mysqldb

Requirements
------------

Debian Wheezy with the package python-software-properties installed.

Role Variables
--------------

All the following variables are set in defaults.

Obsiously, the  mariadb_root_password would be a good candidate to set.
_if you add passwords to a version control system, use ansible-vault, or git-crypt_

Because this role is for a clean install - it assumes an emty root password.
The tasks for resetting the root password are only run on install/first activation of the service.

    # The root password is set, and added to .my.cnf for the root user
    mariadb_root_password: "secret"

    mariadb_base_dir: "/usr"
    mariadb_bind_address: "127.0.0.1"
    mariadb_charsets_dir: "/usr/share/mysql/charsets"
    mariadb_config: "/etc/mysql/my.cnf"
    mariadb_data_dir: "/var/lib/mysql"
    mariadb_long_query_time: 10
    mariadb_mysql_errorlog: "/var/log/mysql/mysql.err"
    mariadb_mysqld_errorlog: "/var/log/mysql/mysqld.err"
    mariadb_mysqld_slowlog: "/var/log/mysql/mysqld.slow"
    mariadb_pid: "/var/run/mysqld/mysqld.pid"
    mariadb_port: 3306
    mariadb_query_cache_limit: false  # 128K
    mariadb_query_cache_size: false   # 64M
    mariadb_share_dir: "/usr/share/mysql"
    mariadb_skip_charset_handshake: true
    mariadb_skip_networking: false
    mariadb_socket: "/var/run/mysqld/mysqld.sock"


License
-------

MIT

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl
Ramon de la Fuente, ramon@delafuente.nl

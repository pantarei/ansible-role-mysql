Ansible Role for MySQL
======================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-mysql.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-mysql)
 [![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-mysql.svg)](https://github.com/pantarei/ansible-role-mysql)
 [![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-mysql.svg)](https://github.com/pantarei/ansible-role-mysql/blob/master/LICENSE)
 [![Ansible Role](https://img.shields.io/ansible/role/5975.svg)](https://galaxy.ansible.com/detail#/role/5975)

Ansible Role for MySQL Installation.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">mysql_basedir</td>
<td align="left">yes</td>
<td align="left">/usr</td>
<td align="left"></td>
<td align="left">The path to the MySQL installation directory.</td>
</tr>
<tr class="even">
<td align="left">mysql_bind_address</td>
<td align="left">yes</td>
<td align="left">0.0.0.0</td>
<td align="left"></td>
<td align="left">The MySQL server listens on a single network socket for TCP/IP connections.</td>
</tr>
<tr class="odd">
<td align="left">mysql_datadir</td>
<td align="left">yes</td>
<td align="left">/var/lib/mysql</td>
<td align="left"></td>
<td align="left">The path to the MySQL data directory.</td>
</tr>
<tr class="even">
<td align="left">mysql_expire_logs_days</td>
<td align="left">yes</td>
<td align="left">16</td>
<td align="left"></td>
<td align="left">The number of days for automatic binary log file removal.</td>
</tr>
<tr class="odd">
<td align="left">mysql_innodb_autoinc_lock_mode</td>
<td align="left">yes</td>
<td align="left">2</td>
<td align="left"><ul>
<li>0</li>
<li>1</li>
<li>2</li>
</ul></td>
<td align="left">The lock mode to use for generating auto-increment values.</td>
</tr>
<tr class="even">
<td align="left">mysql_innodb_buffer_pool_size</td>
<td align="left">yes</td>
<td align="left">256M</td>
<td align="left"></td>
<td align="left">The size in bytes of the buffer pool, the memory area where InnoDB caches table and index data.</td>
</tr>
<tr class="odd">
<td align="left">mysql_innodb_doublewrite</td>
<td align="left">yes</td>
<td align="left">1</td>
<td align="left"></td>
<td align="left">If this variable is enabled (the default), InnoDB stores all data twice, first to the doublewrite buffer, then to the actual data files.</td>
</tr>
<tr class="even">
<td align="left">mysql_innodb_file_per_table</td>
<td align="left">yes</td>
<td align="left">1</td>
<td align="left"></td>
<td align="left">When innodb_file_per_table is enabled (the default in 5.6.6 and higher), InnoDB stores the data and indexes for each newly created table in a separate .ibd file, rather than in the system tablespace.</td>
</tr>
<tr class="odd">
<td align="left">mysql_innodb_flush_log_at_trx_commit</td>
<td align="left">yes</td>
<td align="left">2</td>
<td align="left"></td>
<td align="left">Controls the balance between strict ACID compliance for commit operations, and higher performance that is possible when commit-related I/O operations are rearranged and done in batches.</td>
</tr>
<tr class="even">
<td align="left">mysql_innodb_locks_unsafe_for_binlog</td>
<td align="left">yes</td>
<td align="left">1</td>
<td align="left"></td>
<td align="left">This variable affects how InnoDB uses gap locking for searches and index scans.</td>
</tr>
<tr class="odd">
<td align="left">mysql_key_buffer</td>
<td align="left">yes</td>
<td align="left">256M</td>
<td align="left"></td>
<td align="left">Index blocks for MyISAM tables are buffered and are shared by all threads.</td>
</tr>
<tr class="even">
<td align="left">mysql_lc_messages_dir</td>
<td align="left">yes</td>
<td align="left">/usr/share/mysql</td>
<td align="left"></td>
<td align="left">The directory where error messages are located.</td>
</tr>
<tr class="odd">
<td align="left">mysql_log_error</td>
<td align="left">yes</td>
<td align="left">/var/log/mysql/error.log</td>
<td align="left"></td>
<td align="left">The location of the error log, or empty if the server is writing error message to the standard error output.</td>
</tr>
<tr class="even">
<td align="left">mysql_max_allowed_packet</td>
<td align="left">yes</td>
<td align="left">128M</td>
<td align="left"></td>
<td align="left">The maximum size of one packet or any generated/intermediate string, or any parameter sent by the mysql_stmt_send_long_data() C API function.</td>
</tr>
<tr class="odd">
<td align="left">mysql_max_binlog_size</td>
<td align="left">yes</td>
<td align="left">128M</td>
<td align="left"></td>
<td align="left">If a write to the binary log causes the current log file size to exceed the value of this variable, the server rotates the binary logs (closes the current file and opens the next one).</td>
</tr>
<tr class="even">
<td align="left">mysql_max_connections</td>
<td align="left">yes</td>
<td align="left">128</td>
<td align="left"></td>
<td align="left">The maximum permitted number of simultaneous client connections.</td>
</tr>
<tr class="odd">
<td align="left">mysql_myisam_recover</td>
<td align="left">yes</td>
<td align="left">BACKUP</td>
<td align="left"><ul>
<li>OFF</li>
<li>DEFAULT</li>
<li>BACKUP</li>
<li>FORCE</li>
<li>QUICK</li>
</ul></td>
<td align="left">Set the MyISAM storage engine recovery mode.</td>
</tr>
<tr class="even">
<td align="left">mysql_nice</td>
<td align="left">yes</td>
<td align="left">0</td>
<td align="left"></td>
<td align="left">Use the nice program to set the server's scheduling priority to the given value.</td>
</tr>
<tr class="odd">
<td align="left">mysql_pid_file</td>
<td align="left">yes</td>
<td align="left">/var/run/mysqld/mysqld.pid</td>
<td align="left"></td>
<td align="left">The path name of the process ID file.</td>
</tr>
<tr class="even">
<td align="left">mysql_port</td>
<td align="left">yes</td>
<td align="left">3306</td>
<td align="left"></td>
<td align="left">The port number that the server should use when listening for TCP/IP connections.</td>
</tr>
<tr class="odd">
<td align="left">mysql_query_cache_limit</td>
<td align="left">yes</td>
<td align="left">8M</td>
<td align="left"></td>
<td align="left">Do not cache results that are larger than this number of bytes.</td>
</tr>
<tr class="even">
<td align="left">mysql_query_cache_size</td>
<td align="left">yes</td>
<td align="left">32M</td>
<td align="left"></td>
<td align="left">The amount of memory allocated for caching query results.</td>
</tr>
<tr class="odd">
<td align="left">mysql_socket</td>
<td align="left">yes</td>
<td align="left">/var/run/mysqld/mysqld.sock</td>
<td align="left"></td>
<td align="left">On Unix platforms, this variable is the name of the socket file that is used for local client connections.</td>
</tr>
<tr class="even">
<td align="left">mysql_table_open_cache</td>
<td align="left">yes</td>
<td align="left">512</td>
<td align="left"></td>
<td align="left">The number of open tables for all threads.</td>
</tr>
<tr class="odd">
<td align="left">mysql_thread_cache_size</td>
<td align="left">yes</td>
<td align="left">8</td>
<td align="left"></td>
<td align="left">How many threads the server should cache for reuse.</td>
</tr>
<tr class="even">
<td align="left">mysql_thread_concurrency</td>
<td align="left">yes</td>
<td align="left">16</td>
<td align="left"></td>
<td align="left">This variable is specific to Solaris 8 and earlier systems, for which mysqld invokes the thr_setconcurrency() function with the variable value.</td>
</tr>
<tr class="odd">
<td align="left">mysql_thread_stack</td>
<td align="left">yes</td>
<td align="left">256K</td>
<td align="left"></td>
<td align="left">The stack size for each thread.</td>
</tr>
<tr class="even">
<td align="left">mysql_tmpdir</td>
<td align="left">yes</td>
<td align="left">/tmp</td>
<td align="left"></td>
<td align="left">The path of the directory to use for creating temporary files.</td>
</tr>
<tr class="odd">
<td align="left">mysql_user</td>
<td align="left">yes</td>
<td align="left">mysql</td>
<td align="left"></td>
<td align="left">Run the mysqld server as the user having the name user_name or the numeric user ID user_id.</td>
</tr>
</tbody>
</table>

Dependencies
------------

-   [hswong3i.apt](https://galaxy.ansible.com/detail#/role/5970)
-   [hswong3i.ufw](https://galaxy.ansible.com/detail#/role/6153)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.mysql }

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-mysql/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>


Ansible Role for MySQL
======================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-mysql.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-mysql)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-mysql.svg)](https://github.com/pantarei/ansible-role-mysql)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-mysql.svg)](https://github.com/pantarei/ansible-role-mysql/blob/master/LICENSE)

Ansible Role for MySQL Installation.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04 LTS and Ubuntu Server 16.04 LTS.

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
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mysql_root_pass</td>
<td>yes</td>
<td></td>
<td></td>
<td>Default mysql root user password.</td>
</tr>
<tr class="even">
<td>mysql_basedir</td>
<td>yes</td>
<td>/usr</td>
<td></td>
<td>The path to the MySQL installation directory.</td>
</tr>
<tr class="odd">
<td>mysql_bind_address</td>
<td>yes</td>
<td>0.0.0.0</td>
<td></td>
<td>The MySQL server listens on a single network socket for TCP/IP connections.</td>
</tr>
<tr class="even">
<td>mysql_character_set_server</td>
<td>yes</td>
<td>utf8mb4</td>
<td></td>
<td>Use charset_name as the default server character set.</td>
</tr>
<tr class="odd">
<td>mysql_collation_server</td>
<td>yes</td>
<td>utf8mb4_general_ci</td>
<td></td>
<td>Use collation_name as the default server collation.</td>
</tr>
<tr class="even">
<td>mysql_datadir</td>
<td>yes</td>
<td>/var/lib/mysql</td>
<td></td>
<td>The path to the MySQL data directory.</td>
</tr>
<tr class="odd">
<td>mysql_default_character_set</td>
<td>yes</td>
<td>utf8mb4</td>
<td></td>
<td>Use charset_name as the default character set for the client and connection.</td>
</tr>
<tr class="even">
<td>mysql_expire_logs_days</td>
<td>yes</td>
<td>16</td>
<td></td>
<td>The number of days for automatic binary log file removal.</td>
</tr>
<tr class="odd">
<td>mysql_innodb_autoinc_lock_mode</td>
<td>yes</td>
<td>2</td>
<td><ul>
<li>0</li>
<li>1</li>
<li>2</li>
</ul></td>
<td>The lock mode to use for generating auto-increment values.</td>
</tr>
<tr class="even">
<td>mysql_innodb_buffer_pool_size</td>
<td>yes</td>
<td>256M</td>
<td></td>
<td>The size in bytes of the buffer pool, the memory area where InnoDB caches table and index data.</td>
</tr>
<tr class="odd">
<td>mysql_innodb_doublewrite</td>
<td>yes</td>
<td>1</td>
<td></td>
<td>If this variable is enabled (the default), InnoDB stores all data twice, first to the doublewrite buffer, then to the actual data files.</td>
</tr>
<tr class="even">
<td>mysql_innodb_file_format</td>
<td>yes</td>
<td>barracuda</td>
<td></td>
<td>The file format to use for new InnoDB tables. Currently, Antelope and Barracuda are supported.</td>
</tr>
<tr class="odd">
<td>mysql_innodb_file_per_table</td>
<td>yes</td>
<td>1</td>
<td></td>
<td>When innodb_file_per_table is enabled (the default in 5.6.6 and higher), InnoDB stores the data and indexes for each newly created table in a separate .ibd file, rather than in the system tablespace.</td>
</tr>
<tr class="even">
<td>mysql_innodb_flush_log_at_trx_commit</td>
<td>yes</td>
<td>2</td>
<td></td>
<td>Controls the balance between strict ACID compliance for commit operations, and higher performance that is possible when commit-related I/O operations are rearranged and done in batches.</td>
</tr>
<tr class="odd">
<td>mysql_innodb_large_prefix</td>
<td>yes</td>
<td>1</td>
<td></td>
<td>When this option is enabled, index key prefixes longer than 767 bytes (up to 3072 bytes) are allowed for InnoDB tables that use the DYNAMIC and COMPRESSED row formats.</td>
</tr>
<tr class="even">
<td>mysql_innodb_locks_unsafe_for_binlog</td>
<td>yes</td>
<td>1</td>
<td></td>
<td>This variable affects how InnoDB uses gap locking for searches and index scans.</td>
</tr>
<tr class="odd">
<td>mysql_key_buffer_size</td>
<td>yes</td>
<td>256M</td>
<td></td>
<td>Index blocks for MyISAM tables are buffered and are shared by all threads.</td>
</tr>
<tr class="even">
<td>mysql_lc_messages_dir</td>
<td>yes</td>
<td>/usr/share/mysql</td>
<td></td>
<td>The directory where error messages are located.</td>
</tr>
<tr class="odd">
<td>mysql_log_error</td>
<td>yes</td>
<td>/var/log/mysql/error.log</td>
<td></td>
<td>The location of the error log, or empty if the server is writing error message to the standard error output.</td>
</tr>
<tr class="even">
<td>mysql_max_allowed_packet</td>
<td>yes</td>
<td>128M</td>
<td></td>
<td>The maximum size of one packet or any generated/intermediate string, or any parameter sent by the mysql_stmt_send_long_data() C API function.</td>
</tr>
<tr class="odd">
<td>mysql_max_binlog_size</td>
<td>yes</td>
<td>128M</td>
<td></td>
<td>If a write to the binary log causes the current log file size to exceed the value of this variable, the server rotates the binary logs (closes the current file and opens the next one).</td>
</tr>
<tr class="even">
<td>mysql_max_connections</td>
<td>yes</td>
<td>128</td>
<td></td>
<td>The maximum permitted number of simultaneous client connections.</td>
</tr>
<tr class="odd">
<td>mysql_myisam_recover_options</td>
<td>yes</td>
<td>BACKUP</td>
<td><ul>
<li>OFF</li>
<li>DEFAULT</li>
<li>BACKUP</li>
<li>FORCE</li>
<li>QUICK</li>
</ul></td>
<td>Set the MyISAM storage engine recovery mode.</td>
</tr>
<tr class="even">
<td>mysql_nice</td>
<td>yes</td>
<td>0</td>
<td></td>
<td>Use the nice program to set the server's scheduling priority to the given value.</td>
</tr>
<tr class="odd">
<td>mysql_pid_file</td>
<td>yes</td>
<td>/var/run/mysqld/mysqld.pid</td>
<td></td>
<td>The path name of the process ID file.</td>
</tr>
<tr class="even">
<td>mysql_port</td>
<td>yes</td>
<td>3306</td>
<td></td>
<td>The port number that the server should use when listening for TCP/IP connections.</td>
</tr>
<tr class="odd">
<td>mysql_query_cache_limit</td>
<td>yes</td>
<td>8M</td>
<td></td>
<td>Do not cache results that are larger than this number of bytes.</td>
</tr>
<tr class="even">
<td>mysql_query_cache_size</td>
<td>yes</td>
<td>32M</td>
<td></td>
<td>The amount of memory allocated for caching query results.</td>
</tr>
<tr class="odd">
<td>mysql_socket</td>
<td>yes</td>
<td>/var/run/mysqld/mysqld.sock</td>
<td></td>
<td>On Unix platforms, this variable is the name of the socket file that is used for local client connections.</td>
</tr>
<tr class="even">
<td>mysql_table_open_cache</td>
<td>yes</td>
<td>512</td>
<td></td>
<td>The number of open tables for all threads.</td>
</tr>
<tr class="odd">
<td>mysql_thread_cache_size</td>
<td>yes</td>
<td>8</td>
<td></td>
<td>How many threads the server should cache for reuse.</td>
</tr>
<tr class="even">
<td>mysql_thread_stack</td>
<td>yes</td>
<td>256K</td>
<td></td>
<td>The stack size for each thread.</td>
</tr>
<tr class="odd">
<td>mysql_tmpdir</td>
<td>yes</td>
<td>/tmp</td>
<td></td>
<td>The path of the directory to use for creating temporary files.</td>
</tr>
<tr class="even">
<td>mysql_user</td>
<td>yes</td>
<td>mysql</td>
<td></td>
<td>Run the mysqld server as the user having the name user_name or the numeric user ID user_id.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: hswong3i.mysql

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-mysql/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>


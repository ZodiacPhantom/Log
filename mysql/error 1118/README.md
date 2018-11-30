# Error
ERROR 1118 (42000) at line 1251: The size of BLOB/TEXT data inserted in one transaction is greater than 10% of redo log size. Increase the redo log size using innodb_log_file_size.

#Fix
Edit MYSQL CONFIG
nano my.ini
## Set .._log_file_size to 25 % of buffer pool size
innodb_log_file_size = 3000M
innodb_log_buffer_size = 8M

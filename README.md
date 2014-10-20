DicasMySQL
==========

Dicas MySQL

    mysqlshow
    +--------------------+
    |     Databases      |
    +--------------------+
    | information_schema |
    | test               |
    +--------------------+
    
    which mysql
    /usr/local/bin/mysql
    
    ls -l /usr/local/bin/mysql 
    lrwxr-xr-x  1 tayra  admin  32 19 Out 09:34 /usr/local/bin/mysql -> ../Cellar/mysql/5.6.21/bin/mysql
    
    ls /usr/local/Cellar/mysql/5.6.21/
    COPYING                   README                    homebrew.mxcl.mysql.plist libexec                   mysql-test                sql-bench
    INSTALL-BINARY            bin                       include                   my-new.cnf                scripts                   support-files
    INSTALL_RECEIPT.json      data                      lib                       my.cnf                    share
    
    cd /usr/local/Cellar/mysql/5.6.21
    scripts/mysql_install_db 
    # Diversas mensagens emitidas pela shell
    # alterando a senha de root do MySQL
    mysqladmin -u root password 'new-password'
    uname -a
    Darwin MeuMacBook.local 13.4.0 Darwin Kernel Version 13.4.0: Sun Aug 17 19:50:11 PDT 2014; root:xnu-2422.115.4~1/RELEASE_X86_64 x86_64
    mysqladmin -u root -h MeuMacBook.local password 'new-password'
    mysqlshow -u root -p 
    Enter password: 
    +--------------------+
    |     Databases      |
    +--------------------+
    | information_schema |
    | mysql              |
    | performance_schema |
    | test               |
    +--------------------+
    mysql -u root -p  -e "SELECT Host,Db,User FROM db" mysql 
    Enter password: 
    +------+---------+------+
    | Host | Db      | User |
    +------+---------+------+
    | %    | test    |      |
    | %    | test\_% |      |
    +------+---------+------+
    

Mais detalhes em [http://dev.mysql.com/doc/refman/5.6/en/unix-postinstallation.html](http://dev.mysql.com/doc/refman/5.6/en/unix-postinstallation.html)


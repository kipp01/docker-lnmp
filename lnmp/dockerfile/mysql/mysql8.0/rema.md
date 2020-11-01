2、mysql8连接，连接失败，因为加密方式有变化
解决方式：主机登录mysql，修改成旧的加密方式（mysql_native_password），并重置密码 
* mysql -uroot -p;
* use mysql;
* select host,user,plugin from user;
* alter user 'root'@'%' identified with mysql_native_password by '123456';
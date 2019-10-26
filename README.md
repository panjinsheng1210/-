#wamp配置:配置wamp server让局域网用户都可以访问自己本地的服务器
# Virtual Hosts
#
<VirtualHost *:80>
  ServerName  localhost
  ServerAlias  localhost
  DocumentRoot "${INSTALL_DIR}/www/PHP/190927/public/"
  <Directory "${INSTALL_DIR}/www/PHP/190927/public/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews

   Allow from all
    AllowOverride All
    Require all  granted
  </Directory>
</VirtualHost>




<VirtualHost *:80>
  ServerName  tp6.com
  ServerAlias tp6.com
  DocumentRoot "${INSTALL_DIR}/www/PHP/paotui/190928/public/"
  <Directory "${INSTALL_DIR}/www/PHP/paotui/190928/public/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews

   Allow from all
    AllowOverride All
    Require all  granted
  </Directory>
</VirtualHost>




Listen 8080
<VirtualHost *:80>
  ServerName  localhost
  #ServerAlias  localhost
 DocumentRoot "${INSTALL_DIR}/www/PHP/190927/public/"
  <Directory "${INSTALL_DIR}/www/PHP/190927/public/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    Allow from all
    Require all granted
  </Directory>
</VirtualHost>

Listen 88
<VirtualHost *:88>
  ServerName  tp6.com
  #ServerAlias  tp6.com
 DocumentRoot "${INSTALL_DIR}/www/PHP/paotui/190928/public/"
  <Directory "${INSTALL_DIR}/www/PHP/paotui/190928/public/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    Allow from all
    Require all granted
  </Directory>
</VirtualHost>







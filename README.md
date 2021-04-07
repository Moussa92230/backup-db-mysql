# backup-db-mysql
script for backup a database mariadb-server 

Installation d'un serveur mysql ou mariadb

    sudo apt-get update 
    sudo apt-get upgrade
    sudo apt-get install mariadb-server mariadb-client
    sudo mysql_secure_installation

Vérifier si mariadb et bien installer 

    sudo systemctl status mariadb
    
Une fois que tout est ok il faut créer un user mysql avec tous les droits.

    sudo mysql -u root -p
Une fois accés à mariadb taper la commande

    GRANT ALL ON *.* TO 'nom_user'@'localhost' IDENTIFIED BY 'password';
    FLUSH PRIVILEGES;
    quit

Nous pouvons aussi installer Phpmyadmin,mais avant il faut installer apache et php.
   
    sudo apt-get install apache2 php php-json php-mbstring php-zip php-gd php-xml        php-curl php-mysql

Si tout est bon taper la commande

   sudo apt-get install phpmyadmin
   
Pour vous connecter à phpmyadmin aller sur une page web puis:
    
    https://ip_du_serveur/phpmyadmin
    login-user et password son ceux de votre serveur-mariadb.

à partir de phpmyadmin ont peut exporter et importer une base de donnée en format .sql.    
 
Mises en place d'un script dans le but d'automatiser la sauvegarde de base de données.   

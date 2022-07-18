Gli script eseguono le seguenti attività:

1) master.yml:

esegue tutti gli altri playbook

2) python_install.yml

esegue un update del sistema ed installa i seguenti moduli su tutti i server:

python3-pymysql, php, php-mysql, libapache2-mod-php

3)mysql_conf.yml

Installa i moduli necessari sui server galera

4) wordpress_install.yml

Installa php;

Esegue il download di wordpress sui server;

Esplode il pacchetto wordpress nella documentroot del Virtual-host

Modifica il file wp-config.php inserendo i dati relativi al database 

Esegue dos2unix su tutti i files nella documentroot (ho riscontrato caratteri sporchi durante la fase di test)

Modifica owners e permessi dei files nella documentroot

Esegue un restart di apache

5)hosts ==> file di inventory 

Note:

Questi playbook hanno un alberatura particolare definita da "ruoli"

All'interno del file roles/nome_ruolo/task/main.yml vengono definite le attività eseguite dai singoli ruoli


Utilizzo:

sudo ansible-playbook -i hosts master.yml


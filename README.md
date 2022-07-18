
L'attività è divisa in vari punti:

1) Creazione VM
2) Installazione apache e configurazione del Virtual-Host
3) Installazione mariadb e configurazione database
4) Installazione e configurazione HAproxy
5) Installazione wordpress

L'infrastruttura è così composta:

7 VM ubuntu 20.04 di cui:

2 dedicate ai load balancer HAproxy
2 dedicate a wordpress
3 dedicate ai database mariadb

Per l'attività sono stati utilizzati i seguenti hostname/IP

haproxy1/10.159.80.119
haproxy2/10.159.80.120
wordpress1/10.159.80.121
wordpress2/10.159.80.123
galera1/10.159.80.124
galera2/10.159.80.125
galera3/10.159.80.126

Le credenziali utilizzate per l'esecuzione di tutti i playbook sono le seguenti:

user: ubuntu
password: ubuntu

La descrizione di ogni attività è presente all'interno della cartella di ogni playbook.

Nota:

Nell'infrastruttura creata si suppone che i due nodi dedicati a wordpress abbiano un ip pubblico dedicato che li bilancia 
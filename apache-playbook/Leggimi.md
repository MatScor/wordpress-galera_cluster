apache.yml ==> playbook

Installa l'ultima versione di apache e configura il virtual-host "wordpress_test"

La descrizione delle attività è presente all'interno del playbook

hosts.txt ==> file di inventory

Utilizzo:

sudo ansible-playbook -i hosts.txt apache.yml
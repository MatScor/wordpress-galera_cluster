ubuntu-playbook.yml

Script ansible per la creazione di una VM su vSphere ed installazione del sistema operativo (Ubuntu 20.04)

Le variabili sono descritte all'interno dello script.


Descrizione dell'attività:

Ogni operazione ha una descrizione esplicativa


Template:

1) Ubuntu_user-data.j2 ==> contiene vari dati da che lo script utilizza per settare i dati di base della VM 

2) Ubuntu_Netplan.j2 ==> da utilizzare per creare il nuovo files per festire la rete della VM


Note:

Per ogni VM creata è necessario ricreare la ISO in quanto essa contiene tutti i dati sensibili della VM (hostname, DNS ecc.)

Se si intende clonare la prima VM creata mediante ansible, verificare che l'ip venga modificato in quanto ansible presenta un bug che ne impedisce la modifica nelle versioni di esxi 6.7 e inferiori.


Utilizzo:

sudo ansible-playbook ubuntu-playbook.yml



update-vm.yml

Esegue un update, ugrade e dist upgrade sulle VM appena create

Utilizzo:

sudo ansible-playbook -i inventory-update.txt update-vm.yml




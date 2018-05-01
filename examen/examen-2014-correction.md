# Examen 2014
 
### Exercice 1

On essaye avec une adresse ipv6 puis ipv4, mais le service FTP ne fonctionne pas ni avec l'un ni avec l'autre

### Exercice 2

Port 53: "sweet-soke-domain:" -> port du DNS

Ressources records = caractéristiques du DNS

A: adresse IPv4
AAAA: adresse IPv6
PTR: pointeur

### Exercice 3

etc/hosts : résolution d'un nom en adresse et vice-versa
etc/nswitch.conf : Permet de savoir si on fait une résolution par etc/hosts ou par DNS
etc/resolv.conf : configure la bibliothéque de résolution DNS (indique au serveur de résolution utilisé et le domaine)

Oui, connexion à amertume par DNS et non par etc/hosts

### Exercice 4

Quelqu'un passant par la machine 179.184.31.106 recherche les machines ouverte sur l'extérieur sur le port 22

La machine 30 et 27 sont ouverte sur l'exterieur

aucune conclusion possible diagnostique / piratage? c'est suspect

### Exercice 5

la même adresse tente de se connecter en root à ouindose et entre des mdp -> piratage

Attaque par dictionnaire / force brute

Les nom d'utilisateur peuvent correspondre à des utilisateur par défauts configuré sur certains programmes avec des mdp par defaut simple.

Ces compte contient une potentielle porte d'entrée sur la machine.

### Exercice 6

4.3% d'utilisation du CPU. 18CPU ry 160Go de ram

Gonflette tourne en permanence -> probablement une boucle infini
Utilise une grosse mémoire virtuelle mais peu de mémoire physique : initilisation d'un tableau très lourd mais aucun utilisation du tableau.

Rikiki créer des processus qui sont ummédiament mis en sommeil
Très peu d'uitlisation de mémoire

### Exercice 7

Très peu d'impact

752/900 par tellement d'impate
Il existe cependant une limite de processus inscrite dans les valeur systéme.

Possibilité que les processus remplissent la table de processus et qu'on ne puisse plus en créer

### Exercice 8

Si la commande est exécutée, on supprime TOUT, (lespace indique qu'on va supprimer / puis var/tmp/essai)
Il ne faut pas travailler en root!

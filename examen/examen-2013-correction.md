# Examen 2013
 
### Exercice 1

dig: commande qui recherche le DNS, proche de nslookup

A et AAAA sont des ressources record
option A: adresse IPv4
option AAA: adresse IPv6

On peut en déduire que:
machine pasteque a une adresse ipv4 ( xxx ) et ipv6 (xxx)
machine batravia n'a pas d'adresse IPv4 mais une adresse ipv 6 (xxx)

### Exercice 2

On ping les machines pasteque et batravia en IPv4 (-A inet) et en IPv6 (-Ainet6)

Le résultat est cohérent avec la sortie de dig de l'exercice 1:

pasteque a une adresse ipv4 et ipv6 dont le ping a fonctionné
batravia a une adresse ipv6 dont le ping a fonctionné
 et n'a pas d'adresse ipv4 (unknow host)

Si une machine a une adresse ipv6 et ipv4, la commande ssh se connectera par defaut en ipv6 => pas d'erreur

résolution des noms en ipv6 puis en ipv4

### Exercice 3

L'option -x fait de la résolution inverse => en donnant à la commande une adresse IP, on a pour résultat une adresse

172.28.0.0/16 -> wifi? (openroam)
192.168.78.0/24 -> non routable

Par defaut, dig onterroge le serveur de noms auquel la machine est connectée dig @korolev.univ-paris7.fr permet d'interroger le serveur de nom korolev à la place

Premier cas: on interroge le serveur interne
deuxime cas: on interroge korolev

La machine a des noms differents sur les deux serveurs

.
|
eu
|
reumeum
|
vilma

Le "." correspond à une etiquette vide au dessus de "eu" dans le premier cas

sans le ".": adresse relative par rapport à la racine
avec le ".": adresse absolut

### Exercice 4

- La machine peux être bi-CPU
- 8x32 Go de ram max
- 4 port ethernet / 8 emplacement de disque avec possibilité de hotswap : peut servir de serveur, posibilité de faire de la redondance avec parité sur les disques
- une seul alimentation : pas bon, il faut toujour de la redondance

### Exercice 5

- Machine intéressante mais mauvaise alimentation (pour un 2U)
- Il faut aussi que l'alim soit retirable à chaud

### Exercice 6

15000tr/minute c'est très rapide -> bon point (en général c'est 7200tr)
32Go de RAM c'est fabile selon l'utilisation -> il est interessant d'en avoir plus pour avoir une meilleur mise en cache de page web)
1.7GHz pas de soucis, c'est un peu lent par rapport au autre mais il est plus important d'avoir plein de coeur pour un serveur web (traitement d'un grand nombre de requête simultanément)

### Exercice 7

CPU très puisant, fréquence haute et un total de 2x8 coeurs
16Go de ram

-> pour faire des calcule probablement 

### Exercice 8

Ouvre le fichier tagada (le créer s'il existe pas)
boucle infiniement et écrit dans le fichier
-> prend de la place dans le disque

lsof: list of open files

entre les deux lsof, on remarque que le chemin du fichier "tagada" a été "perdu". le fichier a été supprimé.

En realité, l'entrée a seulement été supprimé du catalogue, le fichier lui même existe toujour et il est toujour entrain de ce remplir.

Il faut tuer le processus fraise pour arreter le remplissage

Au bout d'un moment le disque sera rempli et le programme crashera.

### Exercice 9

top permet de voir la liste des prosessus

RES = RSS (resident set size)

bouclette utilise beaucoup de CPU, actif depuis 67.8h (boucle infini?)
Taille virtuelle de 14Go et une RSS (taille relle) de 728Ko => boucle sur une petite zone mémoire en réalité

sieste prend une taille virtuelle importante mais il est arrêté, il a probéblement été lancé, a initalisé un tableau de long long puis a été mis en someil imédiaement au vu de time 00:00






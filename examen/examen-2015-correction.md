## Examen 2015
 
### Exercice 1

La commande tcpdump demande le filtrage des paquets ipv6 demandant ainsi l'activation de l'ipv6 sur l'interface ethernet hme0.

C'est pour cela que lors de l'affichge de la configuration de cette interface après tcpdump des champs ipv6 sont apparus.

L'adresse 78:19:f7:10:ea doit appartenr à un routeur puisqu'on reçois un router advertisement de cette adresse.

### Exercice 2

Ici la machine tente de s'adresser au routeur mais n'obtien pas de réponse (il n'y a pas de message router advertisement).

### Exercice 3

On adresse qu’on a forcé, a cause des ::.
a causes des 2point 2 points.
.pas obtenue paR un routeur

### Exercice 4

Il s'agit d'un réseau local virtuel dont l'interface physique parente est hme0.

Elle est en activité et possède pour adresse IP 192.168.70.97, avec un masque de sous réseau 0xffffff00 et une adresse broadcast 192.168.70.255.

Son adresse MAC est 08:00:20:da:4f:ac

### Exercice 5

Oui cela est cohérent: on a une VLAN (#929) et le réseau normal connecté sur le port 6

### Exercice 6

On utilise la version multiprocesseur de OpenBSD, vu le nombre de processeur disponible c'est interessant.

On a 48Go de mémoire viven c'est beaucoup, il faut esperer qu'elle soit utilisée au maximum, par exemple si c'est un serveur on peut y placer un systéme de fichier contenant les données fréquement utilisé.

Il manque des information sur l'interface réseau, c'est une donnée très importante s'il s'agit d'un serveur. Car beau être performant, si le réseau ne suit pas ou que l'interface, alors ça ne sert à rien.

### Exercice 7

Sur cette machine, on execture LAMP (linux, apache, mysql, php). (on est pas sûr que ce soit linux mais c'est clair que c'est un systéme unix-like)

En effet, 4 instance du serveur apache sont lancées, ainsi qu'une instance de mysql.

La dernière commande nous montre que php5 est installé. 

Cette machine étant un serveur web, il faut une configuration en conséquence : 

il n'y a pas besoin d'une fréquence de proc très élevé mais il serai préferable d'avoir beaucoup de coeur (ou CPU) pour traiter un grand nombre de requête simultanément
Il serait aussi interessant de poséder une bonne quantité de mémoire vive afin que les pages web fréquement utilisé soit mise en cache, évitant ainsi des acces sur disque couteux.

La partie la plus interessant est que l'interface réseau soit performante, au moins autant que le réseau.

La machine présente dans l'exo 6 est assez pertiante si on veut servir un grand nombre de requête.

### Exercice 8

Il semblerait que l'adresse 128.61.240.66 tente de détecter la présence d'un serveur web (port 80) dans le réseau ou se trouve la machine.



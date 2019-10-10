on connait l'adresse IP par la résolution DNS

DNS = nom de domaine relie l'IP

./etc/hosts est l'ancêtre de la résolution DNS


TTL = durée de validation de la correspondance domaine et IP

DHCP = trouve une adresse IP sur le réseau en fonction des adresses déjà utilisées

IP 8.8.8.8  = adresse de google testable pour voir si ordi connecté au réseau


## DNSMASQ
dnsmasq est le deuxième serveur DNS local qui va être interrogé

par défaut .localhost est activé

Si port<1024 besoin des droits root de la machine

Conventions de port :
80 : http
443 : https
22: ssl
5432 : postgre
8072 : long pull import

comment le serveur peut rediriger vers la bonne adresse ?

il utilise le host présent dans la requete http

## Traefik

Plus dynamique que nginx

La redirection dans chaque serveur DNS dépend du nom de domaine, et d'autres paramètres arrivant avec la requête http.
On peut soit paramétrer 2 IP pour 2 sous-domaines, soit 1 IP pour 2 sous-domaines, et ensuite une redirection différente par le serveur final.

La notion de propagation DNS est le symbole du chemin global entre 2 serveurs.

On configure pour écouter sur 2 ports :
1 port 80 pour le standard
1 port 8080 pour l'admin

Il peut être installé en local, ou démarré comme un container au lancement du pc

Paramètres de traefik :

  traefik.enable: true
  traefik.http.routers.whoami.rule=Host(`whoami.docker.localhost`)
  traefik.http.routers.whoami_long.rule=Host(`whoami.longpull.localhost`)

On utiliser la variable COMPOSE_PROJECT_NAME pour remplacer le whoami

Attention pb: besoin de définir COMPOSE_PROJECT_NAME comme cela : "COMPOSE_PROJECT_NAME:mon_projet"

Projet exemple : https://github.com/akretion/docky-odoo-template

Ajouter restart proxy : always pour relancer traefik à chaque fois

Pour utiliser elasctic-search, besoin d'avoir une adresse accessible depuis l'extérieur. On crée des clés supplémentaires pour accessibilité depuis l'extérieur

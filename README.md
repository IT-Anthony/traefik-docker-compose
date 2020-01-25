![alt text](https://img.shields.io/badge/docker--version-19.03-green) ![alt text](https://img.shields.io/badge/docker--compose--version-1.25-green) ![alt text](https://img.shields.io/badge/traefik--version-2.0-green)

# Introduction
Fichier docker-compose permettant de démarrer le service Traefik en version 2.0 avec un fichier de configuration disponible dans le dossier data.

![alt text](https://i.imgur.com/NXFBBMV.png)


# Explications
Ceci est donc un simple fichier Docker Compose démarrant un conteneur Traefik en version 2.0 et le reliant à un network nommé "proxy". Le dashboard est accessible via l'adresse "http://traefik.localhost" et une redirection automatique en HTTPS se fait, avec une demande d'authentification. Le fichier lance aussi un serveur web sous Apache pour vérifier que le tout est bien fonctionnel. La quasi-totalité est commenté pour aider à la compréhension.


# Installation

```
git clone https://github.com/IT-Anthony/traefik-docker-compose.git
cd Traefik
docker network create proxy
docker-compose up -d
```
Ensuite accéder à l'interface web via http://traefik.localhost, avec comme credentials "it-anthony / password" par défaut. Les informations peuvent (et __doivent__) êtres changées via le fichier docker-compose.yml 

Pour Let's Encrypt, bien penser à modifier l'email présent dans ./data/traefik.yml

# Infos complémentaires 

Si vous désirez obtenir plus d'informations, rendez-vous sur mon site personnel à l'adresse de l'article correspondant: *https://notamax.be/docker-presentation-et-debuts-avec-traefik/*.

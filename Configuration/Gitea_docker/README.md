# 🚀 PROJET: DEPLOIMENT DE GITEA AVEC DOCKER

---

## SOMMAIRE

- [🚀 PROJET: DEPLOIMENT DE GITEA AVEC DOCKER](#-projet-deploiment-de-gitea-avec-docker)
  - [SOMMAIRE](#sommaire)
  - [📝 INTRODUCTION](#-introduction)
  - [🐙 LIEN GITHUB SUR LE FICHIER DE CONFIGURATION  GITEA AVEC DOCKER](#-lien-github-sur-le-fichier-de-configuration--gitea-avec-docker)
  - [🔧 PREREQUIS](#-prerequis)
  - [🧰 OUTILS UTILISES](#-outils-utilises)
  - [🛠️ INSTALLATION DE GITEA](#️-installation-de-gitea)
  - [▶️ EXECUTION DU FICHIER](#️-execution-du-fichier)
  - [⚙️ CONFIGURATION](#️-configuration)
  - [🐋 INSTALLATION DOCKER ENGINE ET DOCKER COMPOSE](#-installation-docker-engine-et-docker-compose)
  - [🔐 GENERATION DU CERTIFICAT AUTO-SIGNE AVEC OPENSSL](#-generation-du-certificat-auto-signe-avec-openssl)
  - [📘 DOCUMENTATION OFFICIELLE NGINX](#-documentation-officielle-nginx)
  - [🧰 QUELQUES COMMANDES](#-quelques-commandes)

---

## 📝 INTRODUCTION

De nos jours, la gestion de différentes ressources telles que (RAM,CPU,DISQUE) constitue un lévier puissant permettant de déployer divers types d'application, logiciel, etc... Afin de maximiser ces différentes ressources il serait mieux de le faire de manière plus isolée pour ne point pertuber le fonctionnement de la machine hôte. Et cela qu'intervient l'importance de la conteneurisation avec Docker. Dans le cadre de notre projet, nous allons déployé un serveur gitea avec docker. 

## 🐙 LIEN GITHUB SUR LE FICHIER DE CONFIGURATION  GITEA AVEC DOCKER

[Lien GitHub du fichier de configuration](https://github.com/jeanmarctsh/gitea_deploy/tree/gitea)

__Branche principale : gitea__

---

## 🔧 PREREQUIS

- OS : Ubuntu 22.04 LTS
- Disque : SSD 25GO
- RAM : 4GO
- HYPERVISEUR DE TYPE 1 ou 2

---

## 🧰 OUTILS UTILISES 

- SSH 
- De vscode pour éditer les différentes configurations
- D'un serveur web nginx afin de l'utiliser comme reverse-proxy
- D'un OS (Linux) (afin d'exécuter les différentes commandes administratives et de la  gestion de permission)
- De OpenSSL afin de générer nos certificats auto-signés
- De AWX pour synchroniser Gitea 

---

## 🛠️ INSTALLATION DE GITEA

Pour installer Gitea il faut procéder de la manière suivante:

```shell 
$ sudo mkdir /home/username nom_du_dossier
```
exemple: sudo mkdir /home/gitea/gitea_folder

```shell 
$ sudo cd gitea_folder && nano docker-compose.yml
```
Dans docker-compose.yml, copier et adapter l'exemple de configuration en fonction de vos besoins. Voici le lien: https://github.com/jeanmarctsh/gitea_deploy/tree/gitea) 

soit: 

```shell 
$ sudo cd gitea_folder && nano gitea.yml
```
Dans gitea.yml, copier et adapter l'exemple de configuration en fonction de vos besoins. Voici le lien: https://github.com/jeanmarctsh/gitea_deploy/tree/gitea

---

## ▶️ EXECUTION DU FICHIER 

Avant d'exécuter les différentes commandes, il faut se placer dans le dossier où se trouve le fichier de configuration

Avec docker-compose.yml comme nom de fichier: 

__Si le repertoire du travail se trouve dans la home directory__

```shell 
$ cd /home/username/gitea_folder
```
```shell 
$ docker-compose up -d
```

Avec gitea comme nom du fichier: 

```shell 
$ cd /home/username/gitea_folder
```
```shell 
$ docker-compose -f gitea.yml up -d
```

---

## ⚙️ CONFIGURATION

Voici une interface montrant la configuration du serveur Gitea après exécution de la commande: __*docker-compose up -d*__

![Configuration gitea](giteacapt_configuration.PNG)

__DIFFERENTS LIENS POUR INSTALLER DOCKER (DOCKER ENGINE ET DOCKER-COMPOSE) OPENSSL NGINX__

Voici les différents liens permettant d'installer docker, Générer certificat SSL, installer NGINX

---

## 🐋 INSTALLATION DOCKER ENGINE ET DOCKER COMPOSE

- [installation docker](https://docs.docker.com/engine/install/ubuntu)
- [installation docker compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)

---

## 🔐 GENERATION DU CERTIFICAT AUTO-SIGNE AVEC OPENSSL

- [lien pour généner un certifical avec ssl](https://docs.openssl.org)

---

## 📘 DOCUMENTATION OFFICIELLE NGINX

- [documentation officielle nginx](https://docs.nginx.com)

---

## 🧰 QUELQUES COMMANDES

Voici quelques commandes docker: 

- Pour lister les conteneurs actifs: 

```shell 
$ docker ps
```

- Pour d'afficher tous les conteneurs en cours, arrêtés: 

```shell 
$ docker ps -a
```

- Pour arrêter un conteneur: 

```shell 
$ docker-compose stop
```

- Pour créer et démarrer un conteneur en arrière plan: 

```shell 
$ docker compose up -d
```

- Pour démarrer un conteneur: 

```shell 
$ docker-compose start
```  

- Pour arrêter et supprimer un conteneur: 

```shell 
$ docker-compose down
```

- Pour afficher le détail d'un conteneur: 

```shell 
$ docker inspect id_image
```

- Pour supprimer une image: 

```shell 
$ docker rmi id_conteneur ou nom_conteneur
```

---

__NB: Avant d'exécuter toutes les configurations, il faut en premier lieu installer Docker ENGINE ET DOCKER-COMPOSE.__

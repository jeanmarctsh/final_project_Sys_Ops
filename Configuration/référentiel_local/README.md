## PROJET : CONFIGURATION DU REFERENTIEL LOCAL AVEC LE LOGICIEL REPREPRO

---

## SOMMAIRE

1. [INTRODUCTION](#introduction)
2. [PREREQUIS](#prerequis)
3. [OUTILS UTILISES](#outils-utilises)
4. [CONFIGURATION COMPLETE DU REFERENTIEL LOCAL VIA UN FICHIER PDF](#configuration-complete-du-referentiel-local-via-un-fichier-pdf)
5. [TEST DU REFERENTIEL LOCAL AVEC LA COMMANDE CURL](#test-du-referentiel-local-avec-la-commande-curl)


## INTRODUCTION

Dans un monde informatique hyperconnecté, il est nécessaire qu'une structure informatique dispose d'un référentiel local afin de permettre aux différentes machines clientes d'effectuer directement les mises à jour de manière sécurisée sans dépendre d'une connexion extérieur, cela aide à mieux contrôler les différents paquets (grâce à la clé GPG qui chiffre et signe les différents paquets ) et images dans le référentiel local. 

---
## PREREQUIS

- OS : Ubuntu 22.04 LTS
- Disque : SSD 35GO
- RAM : 6GO
- HYPERVISEUR DE TYPE 1 ou 2

---
## OUTILS UTILISES

-  reprepro 
-  clé GPG nouveau format
-  serveur web Apache2
-  OpenSSL pour la génération de certificats
-  SSH
-  VS_CODE
-  Protocole rsync
-  Machine cliente (abstract - marco1)

---

## CONFIGURATION COMPLETE DU REFERENTIEL LOCAL VIA UN FICHIER PDF

[voir le guide de configuration sous forme de PDF](local_reposutory_full_steps_update.pdf)

---

## TEST DU REFERENTIEL LOCAL AVEC LA COMMANDE CURL

Après avoir fini l'installation et partager la clé publique au niveau du serveur ainsi qu'au niveau du client, il faut saisir la commande ci-après:

curl -I adresse IP du serveur/nom_du_dossier_créer_pour_le_référentiel_local/

*__exemple:  curl -I 192.168.9.120/debian/__*

Cette commande permet de tester que le serveur du référentiel est accessible et il y aura un statut avec code 200.







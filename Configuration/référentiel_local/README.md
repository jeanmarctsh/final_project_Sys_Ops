## PROJET : CONFIGURATION DU REFERENTIEL LOCAL AVEC LE LOGICIEL REPREPRO

---

## SOMMAIRE

1. [INTRODUCTION](#introduction)
2. [PREREQUIS](#prerequis)
3. [OUTILS UTILISES](#outils-utilises)
4. [CONFIGURATION COMPLETE DU REFERENTIEL LOCAL VIA UN FICHIER PDF](#configuration-complete-du-referentiel-local-via-un-fichier-pdf)


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

[voir le guide de configuration sous forme de PDF](local_repository_full_steps.pdf)







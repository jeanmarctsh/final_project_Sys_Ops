# 🚀 PROJET : AUTOMATISATION DU PATCH MANAGEMENT AVEC AWX ET ANSIBLE

---

## SOMMAIRE

- [🚀 PROJET : AUTOMATISATION DU PATCH MANAGEMENT AVEC AWX ET ANSIBLE](#-projet--automatisation-du-patch-management-avec-awx-et-ansible)
  - [SOMMAIRE](#sommaire)
  - [📝 INTRODUCTION](#-introduction)
  - [🌟 WORKFLOW DU PROJET](#-workflow-du-projet)
  - [🌐🖧 ARCHITECTURE PHYSIQUE DU PROJET](#-architecture-physique-du-projet)
  - [⚙️ MECANISME DE FONCTIONNEMENT DU PROJET](#️-mecanisme-de-fonctionnement-du-projet)
  - [🧰 OUTILS ET TECHNOLOGIES UTILISES](#-outils-et-technologies-utilises)
  - [✍️ AUTEUR](#️-auteur)

---

## 📝 INTRODUCTION

De nos jours, gérer un système informatique en toute sécurité n’a jamais été une tâche facile. Cela implique de mettre en place plusieurs mécanismes permettant de limiter les différents risques de compromission du système existant. De ce fait, il est très important qu’une équipe IT sache comment mettre en place divers mécanisme afin non seulement d'en assurer la sécurité mais aussi d’être plus productif et de mieux gérer la complexité du temps en termes de déploiement massif voir lors d’une simple mise à niveau.  Utiliser un outil dépend du besoin que l’on rencontre en entreprise, dans le monde IT actuel il y a une forte émergence dans le domaine de sécurité, du Cloud, des ressources (physique ou virtuelle), d’automatisation, etc...  En effet, automatiser c’est bien mais il faut savoir quoi automatiser afin de réduire les erreurs humaines. 
Le projet consistera à mettre en place une solution permettant une gestion centralisée via ansible et AWX afin d’avoir une vision globale de différents correctifs (paquets, images, etc…) et aussi de permettre une mise à niveau de manière plus sécurisée et contrôlée. Sur ce, afin de  bien mener le projet, nous allons adopter les notions telles que: la sécurité (local, d'utilisateur), l'automatisation, la synchronisation, le versioning, la planification, etc...

---

## 🌟 WORKFLOW DU PROJET

Compte tenu de la charge du travail, il serait plus judicieux de travailler avec un ordinateur ayant suffisamment des ressources en RAM (suite à la charge du travail qui augmente progressivement) et un bon stockage. De préférence un disque de type SSD supérieur ou égal  1TO.

Voici le workflow général de notre projet:

![Schéma du Workflow](Images/WORKFLOW_GENERAL/WORKFLOW_GEN.png)


---



## 🌐🖧 ARCHITECTURE PHYSIQUE DU PROJET

le projet comprend : 4 Serveurs Linux, 1 Serveur Windows et 2 machines clientes.

* Serveur Linux
  
  1. Linux : Pour le serveur AWX
  2. Linux : Pour le serveur Gitea
  3. Linux : Pour le référentiel local
  4. Linux : Pour Ansible

* Serveur Windows

  1. Serveur Windows 2019


* Machines clientes
  
  1. Linux : client_1 (abstract)
  2. Linux : client_2 (marco1)

---

## ⚙️ MECANISME DE FONCTIONNEMENT DU PROJET

- Pour le serveur AWX : il sera le gestionnaire central de notre projet, synchronisé avec Gitea afin de récupérer automatiquement les différents fichiers de configuration. Et la mise à niveau  pourra se faire de manière contrôlée.

- Pour le serveur Gitea : il sera utilisé pour le versioning de nos différents fichiers de configuration et sera intégré à AWX.

- Pour le serveur Ansible : il sera utilisé comme zone neutre en fonction des caractéristiques de la machine hôte  et partagera le fichier complet au serveur Gitea.

- Pour le référentiel local : il permettra aux machines clientes d'effectuer une mise à niveau de manière sécurisée et contrôlée.

- Pour le serveur Windows 2019 : il permettra une authentification sécurisée afin d'intégrer l'utilisateur de service de l'Active Directory à AWX via le protocol LDAP.

- Pour les machines clientes : elles seront intégrées à AWX et via un utilisateur de service créé au niveau de ces dernières, les différentes configurations seront appliquées et les mises à jour ne se feront en local via le référentiel local déployé avec reprepro


---

## 🧰 OUTILS ET TECHNOLOGIES UTILISES

* Comme système d'exploitation nous avons utilisé :

  *  Linux
  *  Windows

* Comme outils pour mettre en place notre projet nous avons utilisé :

  * logiciel reprepro pour déployer et mettre en place le référentiel local
  * serveur web (apache2 et nginx)
  * git et gitea pour le versioning
  * Kubernetes (pour déployer AWX-OPERATOR avec un cluster minikube)
  * Docker (docker-compose) pour déployer Gitea
  * Openssl pour générer les certificats
  * Ansible pour configurer les machines clientes où seront exécutées les différents playbooks
  * Windows serveur pour une authentification sécurisée en accordant les droits nécessaires aux différents utilisateurs
  * Ssh pour générer les clés (publique et privée) et accéder à distance aux différents serveurs y compris les deux machines clientes
  * VS_code comme éditeur + MobaXterm pour accès simultané en SSH
  * Rsync pour le transfert de différents fichiers en local 
  * LDAP pour permettre la liaison entre un utilisateur (de service) de l'AD dans AWX
  * Hyperviseur de type 2 (Vmware_workstation)

---

## ✍️ AUTEUR
- Nom : Ngandu Jean-Marc
- [![Email](https://img.shields.io/badge/Email-red?style=for-the-badge&logo=gmail)](mailto:jeanmarctshimbombo@gmail.com)
- [![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/jean-marc-ngandu-b60796222)
- [![GitHub](https://img.shields.io/badge/GitHub-black?style=for-the-badge&logo=github)](https://github.com/jeanmarctsh)
# PROJET : CONFIGURATION ET DEPLOIEMENT AWX 

---

## SOMMAIRE

1. [INTRODUCTION](#introduction)
2. [OUTILS UTILISES](#outils-utilises)
3. [PREREQUIS](#prerequis)
4. [DIFFERENTS LIENS POUR L'INSTALLATION AWX_ET_DU_DRIVER_DOCKER](#differents-liens-pour-linstallation-awx_et_du_driver_docker)
5. [INTERFACE AWX](#interface-awx)
6. [QUELQUES COMMANDES](#quelques-commandes)
---

## INTRODUCTION

Dans le monde actuel, avoir une vision globale et détaillé d'un système informatique devient de plus en plus critique.
il est important de signifier que la vision globale ne suffit pas, car il faut savoir organiser, planifier, exécuter, checker les différents logs, les différentes mises-à-jour, 
les différentes machines, etc... Afin de mieux gérer son temps et d'être plus productif.

Dans le cadre du projet, nous avons utilisé __AWX-OPERATOR__, qui est un outil open source et cela permet d'exécuter les différentes tâches.

---

## OUTILS UTILISES

- OS: LINUX.
- KUBERNETES.
- VS_CODE.
- SSH.
- HYPERVISEUR type 2 : vmware_workstation.
- PROTOCOLE RSYNC.
- DOCKER.

---


## PREREQUIS

- OS : Ubuntu 22.04 LTS
- Disque : SSD 40GO
- RAM : 12GO
- HYPERVISEUR DE TYPE 1 ou 2

---


## DIFFERENTS LIENS POUR L'INSTALLATION AWX_ET_DU_DRIVER_DOCKER

__Installation d'un CLUSTER MINIKUBE pour KUBERNETES__

- [installation cluster minikube](https://kubernetes.io/fr/docs/tasks/tools/install-minikube)

__Installation de docker__

- [installation engine](https://docs.docker.com/engine/install/ubuntu)
- [installation docker compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)


__Pour installer AWX :__

- [Installation cluster AWX](https://github.com/ansible/awx-operator/blob/devel/docs/installation/creating-a-minikube-cluster-for-testing.md)
- [installation AWX-OPERATOR](https://github.com/ansible/awx-operator/blob/devel/docs/installation/basic-install.md)
- [installation du kustomize](https://kubectl.docs.kubernetes.io/installation/kustomize/)
- [version de la release](https://github.com/ansible/awx-operator/releases)
- [installation du kind](https://github.com/ansible/awx-operator/blob/devel/docs/installation/kind-install.md)

---

## INTERFACE AWX

Dans le cadre de l'interface d'acceuil d'awx il y en a deux: 

* Action d'un administrateur général sur AWX

  ![Action d'un administrateur](inventory.PNG)

* Interface d'acceuil avec connexion du l'utilisateur LDAP

  ![Connexion LDAP USER](connexion_user_intégré_à_AWX.PNG)

---

## QUELQUES COMMANDES

Voici quelques commandes à exécuter sur AWX déployé avec Kubernetes
 
- Vérification des pods : kubectl get pods
- Vérification des nodes : kubectl get nodes
- Accéder à un pod : kubectl exec -it nom_du_pod -- /bin/bash
- Tester la connectivité d'un utilisateur ldap : ldapsearch -x -H ldap://192.168.9.130:389 -D "readerU@marco.lan" -W -b "DC=marco,DC=lan" sAMAccountName

---

__*NB: Il est important de savoir que dans la veille technologique, il arrive que certaines configurations changent, raison pour laquelle il est important de se référer régulièrement à la documentation officielle afin de voir les différentes mises à jour*__.

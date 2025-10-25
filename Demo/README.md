# DEMO EXPLICATIF SUR LE FONCTIONNEMENT DE LA SOLUTION 

---

## SOMMAIRE

1. [DESCRIPTION](#description)
2. [ETAPES DE LA DEMO](#etapes-de-la-demo)

---

## DESCRIPTION

Dans un monde informatique où l'évolution est constante, l'exécution de différentes tâches telles que : 

    * une mise à jour de sécurité et correctif
    * Installation d'un package pour le bon fonctionnement d'un système informatique
    * Téléchargement d'une image système
    * Planifier et exécuter les différentes tâches sur les machines clientes de manière chronologique
    * Sychroniser les différentes tâches à partir d'une source et ce, de manière automatique
    * Intégrer les différentes solutions
    * etc ...

nécessite l'utilisation d'un outil bien précis. Et dans le cadre de cette partie, nous allons démontrer comment on peut à partir de notre solution :

    * Désinstaller un package sur les machines clientes à partir du logiciel central : AWX-OPERATOR
    * Effectuer un ping à partir AWX-OPERATOR sur les machines clientes
    * Installer un package à partir d'AWX-OPERATOR
    * Voir comment la synchronisation se fait en temps réelle à partir d'une source choisie (Gitea pour notre cas)

---

## ETAPES DE LA DEMO

Compte tenu des caractéristiques de notre ordinateur local, la démo se fera en quatre phases: 

    * Désinstallation d'un package à partir d'AWX-OPERATOR
    * Installation d'un package
    * Synchronisation à partir d'un serveur Gitea
    * D'un test ping sur les machines clientes Via AWX-OPERATOR

__NB: Il est important de savoir que l'installation de différents packages se fait en local grâce à la mise en place d'un dépôt local(local repository). Dans le but d'avoir une vision globale de nos différents packages et ce, en fonction du besoin précis. et aussi disposer des ressources suffisantes(RAM ET UN DIQUE DUR DE PREFERENCE SSD)__
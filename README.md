De nos jous, la sécurité occupe une place importante en entreprise et maintenir un SI à jour est l'un de moyens efficaces et pas facil à mettre en oeuvre. 
Le but de notre project sera de mettre en oeuvre une solution permettant aux pcs clients de faire leurs mises-à-jour directement en local sans passer par internet, car comme nous le savons bien, les utilisateurs finaux ne prennent généralement pas le temps de lire divers informations qui s'affichent lorsqu'ils installent un paquet. D'où la nécéssité de mettre en place un référentiel local.
Afin de mettre en place cette solution, nous aurons besoin des outils ci-après: KUBERTENES, DOCKER, ANSIBLE + AWX, GITEA, WINDOWS SERVER 19 
Nous aurons une architectures avec les serveurs ci-après: linux ---> Gitea ( qui sera déployé avec Docker) linux ---> AWX ( qui sera déployé avec Kubernetes) linux ---> Référentiel local ( qui sera déployé grâce à reprepro, Apache2) WIndows ---> Windows serveur 19 (servira d'une authenification sécurisée des utilisateurs)
Quel OS ? Linux et Windows
Autres outils pour mettre en place notre projet ( serveur web: apache2 et nginx, protocole rsync, treafik)
Pourquoi linux? pour la gestion de droits et d'utilisateurs, compression des dossiers, navigation dans les différents repertoires, partage de différents dossiers, etc...

## TP SI7 DAVID MOLINARI

### I Quelles différences existe-t-il entre une sauvegarde, une archive, une synchronisation ?
- Différence entre une sauvegarde, une archive et une synchronisation?
  - Sauvegarde : 
    L’objectif d’une solution de sauvegarde (ou son anglicisme “backup”) est la récupération des données en cas d’événement rendant celles-ci inaccessibles : perte ou endommagement.
  - Archive :
    L’archivage a pour finalité de préserver vos données anciennes ou dormantes sur une longue durée (supérieure à 1 an). 
  - Synchronisation : 
    C'est l'action de coordonner plusieurs opérations entre elles en fonction du temps. Les systèmes dont tous les éléments sont synchronisés sont dits synchrones.

### II A l'aide des fiches techniques et du lien: http://man.developpez.com/man1/rsync/ (en
anglais) ou https://doc.ubuntu-fr.org/rsync en français, expliquer à quoi servent les
commandes suivantes (rôle et options):
- Explications des commandes :

-   ```shell scp hubble@192.168.0.11:fichier_distant fichier_local ```  Copie d'un fichier depuis un serveur distant avec le nom d'utilisateur hubble en local à la racine d'où est envoyée la commande.

-    ```shell rsync -av /src/foo/ /dest/foo ``` Copie de manière recursive et affichage des fichiers

-   ```shell rsync -auv utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ``` Synchronise les Fichiers de l'IP connecté avec UTILISATEUR vers le fichier de destination, en conservant la recursivité. 

- ```shell rsync -auv -e "ssh" utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ``` Même chose que précédement mais en SSH 

- ```shell rsync -auv --delete -e "ssh" utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ``` Même chose que précédant mais efface les fichiers qui n'existent pas chez l'émetteur


### II Avant de mettre en œuvre votre solution, vous décidez de tester individuellement ces outils.

- ```shell sudo scp USER@SRVSECOUR:\partage \partage ```  ◦ de copier à l'aide de scp depuis le serveur srv-secours les données du répertoire
partagé /partage des utilisateurs vers le répertoire /archives/ du serveur backup.
(ndlr : depuis signifie ici : lancer à partir de).

- ``shell tar -cvf nom_archive.tar nom_dossier/  ```  ◦ d'archiver la copie en la compressant. L'archive portera le nom: archiveUSER.tar.gz
  
  
  ◦ de synchroniser depuis le srv-secours (disposant du service rsync) les répertoires des comptes utilisateurs du serveur srv.lycee.lan 

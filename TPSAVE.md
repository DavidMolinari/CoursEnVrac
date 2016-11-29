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

-   ```bash scp hubble@192.168.0.11:fichier_distant fichier_local ```  Copie d'un fichier depuis un serveur distant avec le nom d'utilisateur hubble en local à la racine d'où est envoyée la commande.

-    ```bash rsync -av /src/foo/ /dest/foo ``` Copie de manière recursive et affichage des fichiers

-   ```bash rsync -auv utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ``` Synchronise les Fichiers de l'IP connecté avec UTILISATEUR vers le fichier de destination, en conservant la recursivité. 

- ```bash rsync -auv -e "ssh" utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ``` Même chose que précédement mais en SSH 

- ```bash rsync -auv --delete -e "ssh" utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ``` Même chose que précédant mais efface les fichiers qui n'existent pas chez l'émetteur

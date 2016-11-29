## TP SI7 DAVID MOLINARI


- Différence entre une sauvegarde, une archive et une synchronisation?
  - Sauvegarde : 
    L’objectif d’une solution de sauvegarde (ou son anglicisme “backup”) est la récupération des données en cas d’événement rendant celles-ci inaccessibles : perte ou endommagement.
  - Archive :
    L’archivage a pour finalité de préserver vos données anciennes ou dormantes sur une longue durée (supérieure à 1 an). 
  - Synchronisation : 
    C'est l'action de coordonner plusieurs opérations entre elles en fonction du temps. Les systèmes dont tous les éléments sont synchronisés sont dits synchrones.

- Explications des commandes :

```bash scp hubble@192.168.0.11:fichier_distant fichier_local ```

```bash rsync -av /src/foo/ /dest/foo ```

```bash rsync -auv utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ```

```bash rsync -auv -e "ssh" utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ```

```bash rsync -auv --delete -e "ssh" utilisateur@ip:/srcToSynchro/ ./destToSynchro/ ```

# TP1
-	Si je supprime un lien symbolique, le fichier vers lequel il pointe est-il supprimé ? 
Non
-	Si je supprime un lien physique, le fichier vers lequel il pointe est-il supprimé ? 
NON
-	Je crée un lien symbolique lnksymbmachin vers le fichier machin.txt . 
  - 1. Les deux fichiers ont-ils le même inode ? 
  oui
  - 2. Si je modifie le fichier lnksymbmachin, machin.txt est il impacté ? L'inverse est-il vrai ? 
Oui l’inverse aussi
  - 3. Si je supprime le fichier machin.txt, puis-je encore accéder au contenu du fichier par le biais du lien symbolique ? 
Non le contenu est supprimé
- Je crée un lien physique lnkphysmachin vers le fichier machin.txt . 
    - 1. Les deux fichiers ont-ils le même inode ? 
oui
    - 2. Si je modifie le fichier lnkphysmachin, machin.txt est il impacté ? L'inverse est-il vrai ? 
Oui
    - 3. Si je supprime le fichier machin.txt, puis-je encore accéder au contenu du fichier par le biais du lien.
Oui
    - 4. A partir de quel moment, ne pourrai-je plus accéder au contenu de machin.txt ? 
Quand il est supprimé

- Je crée le fichier version1.txt et j'en fais la copie version2.txt , les deux fichiers ontils le même i-node ? Pourquoi ? 
Non car ils ne pointent pas sur le même fichier
-	Je crée le fichier versatile1.txt et je le renomme versatile2.txt (il s'agit en fait d'un déplacement), le fichier conserve t-ils le même i-node ? Pourquoi ?
Oui , il pointe sur le meme fichier

# TP2
1. Mettez à jour la liste des packages disponibles.
```bash
apt-get update
```
2. Rechercher sur les applications qui concernent de près ou de loin mysql …
```bash
apt-cache pkgnames fire
```
3. Choisissez celui qu'il faut utiliser pour installer le serveur mysql. Proposez la commande qui fera l'installation .
4. Rechercher un « paquet » qui s'appelle dia
5. Vérifiez si il n'est pas déjà installée sur votre système.
6. Essayez d'afficher ses dépendances ?
7. Désinstallez le
8. Simulez une installation de dia (recherchez l'option dans le man).
9. Installez le de nouveau.
10. Testez le en le lançant.
11. Reconfigurer-le.
12. Mettez à jour votre système (seulement une mise à jour des paquets pas la distribution)

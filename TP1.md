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

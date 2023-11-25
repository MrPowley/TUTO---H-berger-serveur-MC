# Héberger un serveur Minecraft sur son propre ordinateur

## 1 - Créer le serveur

- Créer un dossier ou se trouveront les fichiers du serveur

	![image création d'un dossier](https://i.postimg.cc/fbWRrx1y/cr-er-dossier.png)

---

- Télécharger la version du serveur

	- Paper (Recommandé) : https://papermc.io/downloads/all
	- Spigot : https://getbukkit.org/download/spigot
   ⚠️ Pour les versions 1.16+ il faut utiliser java 17+, voir [Installer une autre version de java](https://github.com/MrPowley/TUTO-Heberger-serveur-MC/blob/main/installer-java17%2B.md)

---
- Placer le .jar téléchargé dans le dossier créé précédement

	![image jar dans dossier](https://i.postimg.cc/Y09hw7h5/dossier-avec-jar.png)

---

- (Optionnel) Créer un fichier de démarrage

	Nous allons créer un fichier de démarrage, cela permet de choisir la quantité de RAM à allouer au serveur, et d'autres quelques paramètres.

	Ouvrez le bloc note
  
	![image bloc note](https://i.postimg.cc/Vk0yg4fm/blocnote.png)

	Pour lancer un serveur dans le cas général, on écrira:
	`java -Xmx[Quantité de ram à allouer en Mo]M -jar [nom du jar].jar`
	
	Paramètres utilisables (Ceux que je connais):
	- `-Xmx` Définit la quantité de RAM maximale qui est allouée au serveur
	- `-Xms` Définit la quantité de RAM minimum qu'on alloue au serveur
	- `-Dfile.encoding=UTF-8` Pour des anciennes versions de minecraft, peut régler des problèmes d'accents
	- `-jar` Définit le nom du jar à executer
	- `nogui` Enlève l'interface graphique par défaut

	Dans mon cas, j'écrirait: `java -Xms512M -Xmx3072M  -Dfile.encoding=UTF-8 -jar paper-1.8.8-445.jar nogui`
	![image bat écrit](https://i.postimg.cc/3rX7s3DV/bat-crit.png)

	Sauvegarder le fichier dans le même dossier que le .jar avec le nom start.bat (le plus important est le .bat)
	![image enregistrer sous](https://i.postimg.cc/W3ShKzbm/enregister.png)

---
- Lancer le serveur en executant start.bat
  Une fenètre d'invite de commande vas s'ouvrir puis se fermer
  vous deverez alors ouvrir le fichier eula.txt dans le dossier du serveur
  
  ![image fichier eula](https://i.postimg.cc/pLVBbN2R/eula1.png)
  
  Vous devrez remplacer le "false" par "true"
  
  ![image eula false](https://i.postimg.cc/HkS9TSx5/eula2.png)

---

- Relancer le serveur
  Vous pouvez maintenant executer la start.bat une seconde fois et le serveur vas se lancer. Vous saurez qu'il aura finit de se lancer quand vous verrez ce message dans l'invite de commande:
  
  ![image cmd server lancé](https://i.postimg.cc/W3BmFm5X/cmd-start-fini.png)
  
  L'invite de commande est la console du serveur, vous ne pouvez y executer que des commandes, pour envoyer des messages utilisez la commande: /say [message]
  
  Vous pouvez vous y connecter avec "localhost" comme ip (Uniquement sur le même PC)
  Pour s'y connecter via un autre PC sur le même réseau, il faut utiliser l'ip de l'hôte

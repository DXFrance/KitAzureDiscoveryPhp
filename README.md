# Kit Azure Discovery pour PHP

Ce projet est destin� � vous aider � d�couvrir Windows Azure. Si vous le 
d�ployez sur une Application Web Azure, vous pourrez alors utiliser votre 
webcam pour effectuer des captures �cran s'appuyant sur une d�tection de 
mouvement.

## Un projet Symfony 2

Ce projet s'appuie sur le framework PHP Symfony 2.

### Console KUDU

Apr�s avoir d�ploy� les sources de ce projet sur une Application Web Azure,
vous devrez passer les lignes de commandes ci-dessous pour que application
fonctionne correctement en mode production. Cela permettra d'installer les 
indispensables biblioth�ques ainsi que de g�n�rer les fichiers JS et CSS 
n�cessaires.

Utilisez pour cela la console propos�e par KUDU et rendue disponible par 
Windows Azure. 

Pour y acc�der, utiliser l'URL https://lenomdevotreapplication.scm.azurewebsites.net, 
puis s�lectionnez la cat�gorie :

> Debug console 

puis la commande :

> CMD

### Installation de composer

Afin de pouvoir proc�der � l'installation des biblioth�ques attendues pour 
ce projet, vous devrez installer composer gr�ce � la ligne de commande suivante :

```
```

### Installation des biblioth�ques

D�placez-vous ensuite � l'int�rieur du dossier wwwroot, contenu dans le dossier
site :

```
D:\home>cd site\wwwroot
```

Puis, appeler la commande composer pour installer les d�pendances :

```
D:\home\site\wwwroot>php composer.phar install
```

### G�n�ration des fichiers

Enfin, utilisez la commande qui suit pour g�n�rer les fichiers CSS et JS :

```
D:\home\site\wwwroot>php app/console assetic:dump --env=prod --no-debug
```

Testez votre site d�ploy� sur Windows Azure � l'URL : http://lenomdevotreapplication.azurewebsites.net

Et voil� ;)
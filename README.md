###### Cour GIT par : Logan Wilquin.

# 1. Partie pratique du cour sur GIT.

![alt text](https://i2.wp.com/wptavern.com/wp-content/uploads/2014/06/revisr-banner.png?ssl=1 "GIT")

## 1.1 Récupèrer le repository (dépot).

### 1.1.1 Initialiser git sur un projet local :
Tout dabord, vous allez créer un dossier de travail.
Une fois créé, vous ouvrez le CMD et vous vous déplacez dans votre dossier de travail.
***
**Rappel : _Taper "cd" suivi du chemin de votre dossier exemple :_ `cd E:\PopSchool\CourGit\Repo`**.
***
Une fois dans votre dossier de travail, nous allons faire la commande : **`git init`**.
 
### 1.1.2 Cloner un repository git dans notre dossier de travail :

Ensuite, nous allons récupèrer le repository qui se trouve à cette adresse : https://github.com/Skullyfox/CourGit.
Pour cela, il nous faudra CLONER celui-ci grace au lien fournit sur la page du repository.
****
**Commande : `git clone`**.
****
Vous pouvez maintenant observer votre dossier de travail local, le repository y a était cloner !

## 1.2 Arborescence du projet.
***
```md
    css
    |--- style.css  //Feuille de style
    |
    js
    |--- main.js    //Feuille de Script
    |
    index.html      //index du site
    |
    README.md       //README rédigé en MarkDown
``` 
***
## 1.3 Créer sa "branch", y faire ses modifications, les sauvegarder.

### 1.3.1 Créer sa "branch".
Pour créer une **branch** dans le repository git, c'est très simple.
***
D'abord, qu'est-ce qu'une "**branch**" ?

Une "**branch**" c'est tout simplement un espace de travail, où les contribueurs du projet, peuvent y faire leurs modifications sans avoir d'impact sur la **branch** principale appelée **_master_** qui ne serviras que pour le créateur du repository.

La **branch master**, peu être utilisée par tout le monde, **MAIS**, on y enregistrera les modifications validées par le chef du projet en priorité pour ensuite pouvoir les **push** dans le repository.

**Push** consiste à uploader les fichiers du projet sur le serveur GIT.
***
Revenons en à la création de notre **branch** :
1. Taper la commande : `git checkout -b (le_nom_de_votre_branch)` qui servira à créer votre **branch**.
2. Taper la commande : `git branch`, normalement, une liste de **branch** va s'afficher, la branch dans laquelle vous êtes présent est précédée d'un `*`.
3. Pour revenir à la **branch master**, Taper la commande : `git checkout master`.

Voilà ! Vous savez créer, et vous déplacer dans une **branch** !
Pour supprimer une **branch** il vous suffit de taper la commande : `git branch -D (nom_de_la_branch)`.


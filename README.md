###### Cour GIT par : Logan Wilquin.

# Partie pratique du cour sur GIT.

![alt text](https://i2.wp.com/wptavern.com/wp-content/uploads/2014/06/revisr-banner.png?ssl=1 "GIT")

## 1 Récupèrer le repository (dépot).

### 1.1 Initialiser git sur un projet local :
Tout dabord, vous allez créer un dossier de travail.
Une fois créé, vous ouvrez le CMD et vous vous déplacez dans votre dossier de travail.
***
**Rappel : _Taper "cd" suivi du chemin de votre dossier exemple :_ `cd E:\PopSchool\CourGit\Repo`**.
***
Une fois dans votre dossier de travail, nous allons faire la commande : **`git init`**.
 
### 1.2 Cloner un repository git dans notre dossier de travail :

Ensuite, nous allons récupèrer le repository qui se trouve à cette adresse : https://github.com/Skullyfox/CourGit.
Pour cela, il nous faudra CLONER celui-ci grace au lien fournit sur la page du repository.
****
**Commande : `git clone`**.
****
Vous pouvez maintenant observer votre dossier de travail local, le repository y a était cloner !

## 2 Arborescence du projet.
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
## 3 Créer sa "branch", y faire ses modifications et les sauvegarder.

### 3.1 Créer sa "branch".
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

### 3.2 Faire des modifications sur sa branch et les sauvegarder.
Nous avons vu précédemment comment créer et se déplacer dans une branch.

Vous allez donc créer une branch avec votre nom si ce n'est pas déjà fait, et vous assurer que vous êtes bien dedans.

Le fichier index.html est déjà près configuré avec un h1 vide, voici les consignes :
1. **Dans le fichier HTML** : écrivez votre prénom dans le H1,
2. **Dans le fichier CSS**  : écrivez les lignes suivantes :
```CSS
body{
    background-color : /* la couleur de votre choix */;
}
```
Une fois que vous avez fait vos modifications faites la commande `git add *`, elle vous permettras d'ajouter toutes vos modifications, puis faite la commande `git commit -m VOTRE_MESSAGE`, qui vous permettras de sauvegarder les modifications ajoutées à votre **branch** suivis de votre "message de **commit**.
### ATTENTION : Vérifier que vous êtes bien dans votre branch avant de sauvegarder !
Voilà ! Maintenant vous savez travailler en groupe grâce à **GIT**!

## 4. Créer son repository, et inviter des contribueurs.



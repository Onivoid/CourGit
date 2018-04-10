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

### 4.1 Créer son repository.

Pour créer notre repository, il faut que nous nous rendions sur l'accueil de github et qu'on se connecte à notre compte.

Ensuite, toujours sur la page d'accueil, en haut à droite à côté de votre photo de profil vous avez un petit "**+**", cliquez dessus puis cliquez sur "**New repository**".

1. Mettez le nom de votre repository dans le champ texte prévu à cet effet,
2. descendez puis clique sur "**Create repository**".

Sur la page suivante, nous avons un "blabla" nous proposant : 
* **d'installer GIT en version desktop**,
* **de créer son repository via des commandes** (ce qui nous intéresse),
* **de push un repository existant en ligne de commande**,
* **d'importer du code existant venant d'un autre repository**

Ici, nous allons créer notre repository via des lignes de commandes.

#### Avant de continuer, assurez vous bien d'être dans la racine de votre projet en local !

Voici les commandes à taper :
***
1. `echo "# abcd" >> README.md` : Créé un fichier README.md en y écrivant "# abcd" dedans,
2. `git init` : Initialise GIT dans votre projet local,
3. `git add README.md` : Ajoute le fichier **README.md**,
4. `git commit -m "first commit"` : Enregistre le contenu ajouté,
5. `git remote add origin https://github.com/Skullyfox/abcd.git`: Lie votre dépot Github à votre projet GIT,
6. `git push -u origin master` : **push** votre contenu sur votre dépot Github.
***
Allons voir notre repository Github, rafraîchissons la page si ce n'est pas encore fait, et nous pouvons constater la présence d'un fichier appelé "**README.md**".

Vous avez réussi à créer et à ajouter un fichier à votre repository Github grâce aux lignes de commandes GIT !

À quoi sers le "**README.md**" ? Qu'est-ce que c'est ?

C'est un simple fichier README (Lisez moi), sauf que celui-ci à l'extension "**md**" qui veux dire : "**MarkDown**".

En gros, nous pouvons tout simplement écrire du text, mais aussi utliser la synthaxe MarkDown, vous lisez actuellement le "**README.md**", il sers tout simplement à expliquer son projet, ou bien à faire un mode d'emplois etc ...

### 4.2 Inviter des contribueurs.

Bon, nous avons réussi à créer notre repository, maintenant nous aimerions travailler en groupe grâce à celui-ci, mais comment les "**Contribueurs**" doivent t-ils faire pour nous rejoindre ?

C'est très simple, enfin pour vous.

1. Allez dans votre repository (via le site Github cette fois-ci),
2. Vous devez voir un peu sur la droite, un bouton "**Clone or Download**", cliquez dessus,
3. Copier le lien puis envoyer le à la personne souhaité.

Voilà, vous avez fini ! 

**Petit Rappel** : Le contribueur devras faire la commande `git clone lien_que_vous_lui_avais_donné` pour récupérer votre repository en local.

# Le cour sur les bases de GIT pour travailler en groupe se fini ICI !
![alt text](https://orig00.deviantart.net/d3c0/f/2014/209/7/5/keep_calm__032___and_develop_by_hundredmelanie-d7sozan.png "keep calm and develop")
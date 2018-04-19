# GIT : cour pratique.

![alt text](https://i2.wp.com/wptavern.com/wp-content/uploads/2014/06/revisr-banner.png?ssl=1 "GIT")

## Créer / Cloner un **repository**.

### Créer un repository.

#### La commande "**git init**" :

La commande ```git init```, permet d'initialiser un **repository** Git dans votre dossier de projet Local.

#### La commande "**git clone**" :

La commande ```git clone URL_DU_REPOSITORY.git```, permet de cloner un **repository** Git sur votre projet local.

Cette commande initialise automatiquement le  **repository** Git dans votre dossier de projet local en même temps que le clonage.

#### Mise en pratique :

Alors tout d'abord, **en local** : 

- Vous allez créer un dossier, n'importe où dans votre PC (Ou sur périphérique externe), il seras le dossier de votre "projet",
- Ouvrez l'invité de commande, et allez dans le dossier que vous venez de créer.

Ensuite, **la création du dépot sur le site www.github.com** :

- Rendez-vous sur la plateforme www.github.com, puis, **connectez-vous** à votre compte (ou **créez en un** si ce n'est pas fait),
- Rendez-vous ensuite sur votre profil, puis dans la rubrique **repositories**,
- Cliquez sur le petit bouton où il y est écrit "**New**",
- Mettez le nom que vous voulez dans le champ **repository name**,
- Avant de cliquer sur **Create Repository**, un tout petit peu au dessus, vous avez l'option "**Initialize this repository with a README**", cochez la puis cliquez sur **Create Repository**.

Maintenant que votre **repository** est créé, sur la droite vous avez un bouton "**Clone or Download**", cliquez dessus, et copier le lien qui vous est donné, il devrais ressembler approximativement à ceci : https://github.com/Skullyfox/test20180412.git.

Retour **en local** : 

- Retournez dans votre terminal, puis tapez la commande ```git clone https://github.com/Skullyfox/test20180412.git``` avec le lien que vous avez récupéré,
- Observez votre dossier local, un fichier README.md y a était cloné.

### Ajouter, Supprimer, Sauvegarder, Envoyer, Mettre à Jour.

#### La commande "**git add**" :

La commande ```git add```, permet d'ajouter les modifications faites sur votre projet local, il y a deux façons de l'utiliser :

- Ajouter un fichier particulier : ```git add CHEMIN_DU_FICHIER```,
- Tout Ajouter : ```git add *```.

#### La commande "**git rm**" :

La commande ```git rm```, permet de supprimer un fichier, ou dossier qui auras était ajouté, son utilisation est la même que la commande ```git add```.

#### La commande "**git commit**" :

La commande ```git commit -m 'COMMIT MESSAGE'```, permet de sauvegarder les changements qui ont étaient ajouté avec la commande ```git add```, avec un message de **commit**.

#### La commande "**git push**" :

La commande ```git push```, permet d'**uploader** vos changements sauvegardés dans votre **repository** Git.

#### La commande "**git pull**" : 

La commande ```git pull```, permet de mettre à jour vos fichiers locaux par rapport aux fichiers de votre **repository** Git.

#### Mise en pratique :

Dans le même dossier (**local**) que vous avez créé précédemment, vous aller :

- Créer un fichier index.html et y écrire ```<h1> VOTRE_PRÉNOM </h1>```,
- Créer un sous dossier **css**, avec un fichier **style.css** à l'intérieur.

Dans votre fichier **style.css**, modifiez juste la couleur du background du body et peu être la couleur de vos lettres du h1 (servira pour la suite).

Une fois que c'est fait, dans votre **terminal** :

- Faites la commande ```git add *``` pour **ajouter** toutes vos nouvelles modifications,
- Faites la commande ```git commit -m 'VOTRE_MESSAGE_DE_COMMIT'``` pour **sauvegarder** les modifications ajoutés,
- Faites la commande ```git push```pour **upload** vos fichiers sur votre serveur git.

Vous pouvez maintenant observer sur votre **repository** Github, les fichiers seront présents s'il n'y a eu aucuns problèmes durant les manipulation !

## Exercice en Binôme.

### Les bases du travail de groupe sur GIT

Vous allez : 

- vous mettre en binôme,
    - l'un des deux va cloner le **repository** de l'autre.

- Affichez tout les deux le site du **repository** en local,

- L'un va modifier la taille / la couleur du texte contenu dans le h1,
    - puis add - commit et push la modification.

- L'autre va pull les changements puis rafraichir l'aperçu local pour observer les changements.

### Création & Utilisation des "Branch".

Dans l'exercice précèdent, nous avons vu comment travailler ensemble sur GIT, **MAIS** sur la **branch** master ce qui peu poser problème en modifiant un fichier en même temps.

#### La Commande "git checkout -b" :

La commande ```git checkout -b NOM_DE_LA_BRANCH``` permet de créer une nouvelle **branch**.

#### Mise en pratique :

Les deux personnes du binôme devrons le faire :

- faites la commande ```git checkout -b NOM_DE_LA_BRANCH```

- faites ensuite la commande ```git branch``` : ça vous afficheras la liste des **branch** existante et celle dans laquelle vous êtes seras précèdé d'une étoile.

Vous pouvais maintenant passer aux modifications :

Modifiez chacuns de votre côté ce que vous voulez puis faite la combinaison des commandes :

- ```git add * ```

- ```git commit -m "MESSAGE_DE_COMMIT"```

Maintenant, pour voir les modifications de l'autre :

- Faites ```git checkout NOM_DE_LA_BRANCH_DU_PARTENAIRE ```
    - puis la commande ``` git pull ``` et rafraichissez la page.

#### La commande "git merge"

La commande ```git merge NOM_DE_LA_BRANCH_A_MERGER ``` permet de copier les modifications d'une **branch** à l'autre.

**. /!\ ATTENTION /!\ .**

Si le binôme modifie le même fichier, au moment du merge il risque d'y avoir conflit !

Nous allons en créer un comme si je n'avais rien dis à ce sujet :

#### Mise en pratique :

Pour l'instant pas de conflits : 

- Allez sur votre **branch** puis faite ```git merge master``` pour revenir à 0 sur votre **branch**

Maintenant nous allons créer le conflit :

- Modifier chacuns le ```background-color``` de votre body puis enregistrer vos changement dans votre **branch**,

- Enregistrez vos modifications dans vos **branch**,

- faites la commande ```git checkout master``` Pour aller dans la **branch** master,

- Chaucun votre tour, vous aller faire ```git merge LE_NOM_DE_VOTRE_BRANCH```.

Normalement, le deuxième merge vas poser problème.

En faite, Git à tenter de merger 2 modifications similaire : le background-color.

Pour régler ce problème, vous aller devoir Pull la **branch** master puis aller dans votre fichier CSS.

Nous pouvons voir qu'il y a les 2 modifications d'écrites dans le fichier, pour régler ce problème, il vous suffit de garder seulement la modificaiton que vous voulez garder, puis de refaire un **git add** suivit d'un **git commit**, et voilà, problème résolu.

La meilleure pratique serais de répartir le travail et de ne pas travailler sur les mêmes fichiers, ce qui éviterais de merger les mêmes modifications et donc de créer des conflits !


![alt text](https://orig00.deviantart.net/d3c0/f/2014/209/7/5/keep_calm__032___and_develop_by_hundredmelanie-d7sozan.png "keep calm and develop")
# Introduction pour l'Utilisation de Git par l'équipe TeamAT
Introduction et Guide de bonnes pratiques.

# Introduction à Git

## Qu'est-ce que Git?

Git est un système de contrôle de version qui facilite la gestion collaborative des projets informatiques. 

Premièrement, Git est conçu pour suivre les modifications apportées aux fichiers. Pour faire une petite analogie, Git, c'est comme les points de sauvegarde dans les jeux vidéo. Ça enregistre les étapes d'un projet, permettant de revenir en arrière en cas d'erreur

De plus, Git facilite le **travail simultané** sur un projet en permettant à plusieurs développeurs de travailler sur des branches distinctes. Chaque développeur peut apporter des modifications à sa branche sans affecter le code principal. Une fois les modifications terminées, Git offre la possibilité de fusionner ces branches, intégrant les changements de manière harmonieuse dans le code principal. Cette capacité de fusion, appelée "merging", garantit une collaboration fluide en permettant à chacun de contribuer sans perturber le travail des autres, assurant ainsi la cohérence et l'intégrité du projet.

Git est donc un outil essentiel pour la collaboration efficace, le partage de code et la préservation de l'intégrité du travail d'équipe.

### Comprendre les concepts de base

#### Le langage

- **Système de Contrôle de Version (SCV):** Git est un SCV qui enregistre les modifications apportées aux fichiers d'un projet.
- **Dépôt (Repository):** C'est l'espace de stockage où Git conserve l'historique des changements du projet.
- **Commit:** Une action qui enregistre les modifications dans le dépôt avec un message descriptif.
- **Branche (Branch):** Une version distincte du projet, permettant le développement parallèle sans affecter le code principal.
- **Merge:** La fusion de différentes branches pour intégrer les modifications dans le code principal.
- **Clone:** Dupliquer un dépôt existant pour travailler localement.
- **Push:** Envoyer les modifications locales vers le dépôt partagé.
- **Pull:** Mettre à jour le dépôt local avec les dernières modifications du dépôt partagé.
- **Conflict:** Un problème lors de la fusion nécessitant une résolution manuelle.
- **Log:** L'historique des commits, affichant les modifications apportées au fil du temps.

#### Voici quelques vidéos intéressantes.

**Note:** Il existe deux façon interagir avec Git, avec des lignes de commandes ou avec des interfaces graphiques.  Les interfaces graphiques sont plus simple à utiliser alors ne soyex pas intimidés par les vidéos suivantes, concentrez vous sur les concept, vous n'aurais pas à retenir toutes les commandes manuelles. :)



- Comprendre Git (1/18) : Qu'est ce que git ? [ici](https://youtu.be/rP3T0Ee6pLU?si=xdtMBqLy2W-IfoA9)
- Pour une introduction, en 100 seconde( anglais) [ici](https://www.youtube.com/watch?v=hwP7WQkmECE).
- Pour une compréhension approfondie, en 12 minutes [ici](https://www.youtube.com/watch?v=HkdAHXoRtos).

# Installation

## Git

1. Télécharger Git: https://git-scm.com/
2. Suivre les instructions, utiliser les paramètres par défaut suggérés.

## Interfaces Git (pour utiliser Git sans lignes de commande)

Il existes plusieurs interfaces sans lignes de commande comme GitHub Desktop ou Git Kraken ou tortoise git pour une gestion locale simplifiée du répertoire Git. Ces outils sont largement utilisés au laboratoire. 

​	[GitHub Desktop](https://desktop.github.com/)

​	[gitkraken](https://www.gitkraken.com/)

​	[TortoiseGit](https://tortoisegit.org/)  -> [Instructions d'installation teamAT](https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/blob/main/installer_tortoise.md)


# Utilisation de Git 

#### Aperçu du flux de travail avec l'utilisation de Git

Le flux de travail dans Git suit généralement les étapes suivantes :

1. **Clonage (Clone):** Dupliquer un dépôt existant ( sur GitHub par exemple) sur votre machine locale. Cela crée une copie du répertoire sur votre machine que vous pouvez modifier localement.

2. **Création de Branche (Branch):** Développer de nouvelles fonctionnalités ou résoudre des problèmes sur une branche distincte pour éviter d'affecter le code principal.

3. **Ajout de fichiers(Add):** Ajouter des fichier à être monitoré / versionné par git.

4. **Ajout de Modifications (Commit):** Enregistrer les modifications qui ont été apportées au code sur la branche avec des commentaires descriptifs.

5. **Mise à Jour du Dépôt Local (Pull):** Récupérer les dernières modifications du dépôt partagé pour rester à jour. ( si quelqu'un aurait travailler sur le code en même temps que vous)

6. **Résolution des Conflits (Conflict):** Si nécessaire, résoudre les conflits lors de la fusion des branches.

7. **Fusion des Branches (Merge):** Intégrer les modifications votre branche de travail dans la branche principale.

8. **Envoi des Modifications (Push):** Envoyer les modifications locales vers le dépôt partagé pour que d'autres collaborateurs puissent les récupérer.

Ce flux de travail permet une collaboration efficace, le suivi des modifications et la gestion des versions dans le développement de logiciels.


# Bonnes pratique

Organisez les répertoires de manière concise et organisée. Nommez clairement vos branches, vos nom de commit et les nom de répertoires. Ajoutez une description aux répertories. Faites des release sur les version stables du projet. Travaillez proprement et professionnellement. Demandez de l'aide dès que nécéssaire et assurez-vous de connaître les méthodes professionnelle d'utilisation de git.

## Conventions de message

Maintenez la clarté dans l'historique des versions en utilisant des messages de commit informatifs. Consultez la [convention de nom de commit avancée](https://cbea.ms/git-commit/) pour des indications claires sur le type de modification.

### Exemple de convention de nom de commit avancée
Cette convention n'est pas obligatoire, mais conseillée.
- **work** : Pour des modifications, développement général du projet
- **fix** : Pour une correction de bogue
- **docs** : Pour une mise à jour de la documentation
- **style** : Pour des modifications mineures n'affectant pas la logique du code
- **clean** : Pour les modification mineures qui affectent l'organisation du répertoire

### Contre indication
<img src="https://cbea.ms/content/images/size/w2000/2021/01/git_commit_2x.png" width=30%>

## Utilisation des Branches

### Branche principale (Default ou Main)

La branche principale est la version par défaut la plus à jour de la dernière version déployée. Dans un monde idéale, on ne travaille pas directement dans la branche principale.

### Branches de développement
Une nouvelle branche est ajoutée au projet pour ajouter des fonctionnalités au projet, lorsque les modifications sont complétés, cette branche est fusionnée à la branche principale ou devient celle par défaut.

#### Note sur les branches inutilisés
Fermez vos propres branches inutilisés et obsolètes en les supprimant. Par contre créez un tag pour conserver la version si jugé nécéssaire. La suppression de la branche conserve les commits, facilitant la récupération à partir du tag. Cette pratique maintient la clarté en éliminant les branches inutiles. Il peut arriver que le développement dans une branche diverge à des fins de tests. Par contre il faut éviter de les conserver pour rien.


<img src="images/gitflow.png" alt="Gitflow workflow" style="zoom:67%;" />

​		*source: https://buddy.works/blog/5-types-of-git-workflows*



## Tags (Ensembles des jalons du projet)

Utilisez des tags pour marquer des jalons importants du projet. Par exemple le nom d'une version stable (Ex: V2C, V3C-Commande, V2B-PreProduction)

## Releases (Version stables du projet, référence à un tag)

Associez les releases à des tags pour définir clairement les versions déployées (ex: V1A, V1B, V2B). Documentez les changements dans la description, tel que la liste des nouvelles fonctionnalités. Les release sont des versions du projets du projet qui sont stables, par exemple pour les PCB, il se trouve les fichiers de production prêt à commander sur JLCPCB pour une version donnée.

![img](images\295970020-6538580e-4e94-4791-84b3-db5176036e20.png)

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/8ab0a03f-31a2-4640-a71a-f1ee05e2e9ea" width='80%'>
<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/515af705-16bf-4e04-b235-2fb8a1ef5f43" width='50%'>


## Issues

Utilisez l'onglet "Issues" pour suivre les problèmes et les modifications nécessaires à apporter au projet. Cependant utilisez ClickUp pour la progression globale du projet.


# Noms de répertoire

## Préfixes

- TeamAt_H : Hardware 
- TeamAt_P : Platform
- TeamAt_L : Librairies
- TeamAt_B : Basic. codes de base
- AT- : Assistive Technologies (Suffixe simplifié)

## Suffixes

- -PCB : Fichiers de modélisation de PCB
- -FW : Micrologiciel embarqué (Firmware)
- -SW : Logiciel ordinateur
- -CAD : Fichiers de modélisation 3D

# Mise en pratique - Guide d'introduction à Tortoise

[Instructions d'installation teamAT](https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/blob/main/installer_tortoise.md)

Voici un petit aide-mémoire / récapitulatif du flux de travail GIT dans une utilisation normale avec tortoise.

​                                                        <img src="images\image-20240205131023053.png" alt="image-20240205131023053" style="zoom:67%;" />                           

​          

### Clonage

Pour cloner un dépôt, nous avons de besoins de l'adresse de ce dépot. Voiçi comment cloner un dépot GitHub avec Tortoise Git

   1. Dans le dépôt GitHub, vous pouvez cliquer sur le bouton Code puis copier l’adresse inscrite.

      <img src="images\image-20240205110731875.png" alt="image-20240205110731875" style="zoom:50%;" />

      ​	

      2. Dans l’explorateur Windows, à l’endroit où vous désirez avoir le projet, faire un clic droit puis choisir Git clone… Un fenêtre TortoiseGit s'ouvrira.

         <img src="images\image-20240205111124103.png" alt="image-20240205111124103" style="zoom:67%;" />

         **Note:** Dans Windows 11, il est possible que vous deviez cliquer **"Show More Options"** ou tenir shit en cliquant pour voir tous les options.

         3. Entrez l’adresse que vous avez copié à l’étape 1 puis fait ok

            ![image-20240205112240934](images\image-20240205112240934.png)

            **Note :** La première fois que vous clonerez un dépôt GitHub, on vous demandera votre nom d’usager et mot de passe. C’est le même que pour accéder au site.

             

            **Bon à savoir :** Il n’y a aucun problème à avoir plusieurs clones du même projet dans différents emplacements sur votre ordinateur. Ces clones seront tous indépendants de la même façon que s’ils seraient sur des ordinateurs différents. 

         4. Si tout a fonctionné, vous aurez un message comme celui-ci

            ![image-20240205112621091](images\image-20240205112621091.png)

            5. Le projet sera donc maintenant sur votre ordinateur et sera accessible comme tout dossier normal, à la différence que les fichiers auront une petite icône vous indiquant leur statut GIT.

               <img src="images\image-20240205112704661.png" alt="image-20240205112704661" style="zoom:67%;" />

         Votre projet est maintenant cloné et prêt à être utilisé et modifié.

         **Note :** Pour un dépôt fraichement créé sur Github, le processus sera le même mais le dossier sera vide. Vous verrez comment ajouter des fichiers dans les prochaines étapes.

### Ajouter (add)

La fonction Add permet d’ajouter un fichier à un projet, plus précisément dans le transit. Ajouter un fichier au transit fait en sorte d’indiquer à git que le fichier fait partie du projet et que git doit maintenant suivre les modifications qui sont apportées à ce fichier. Un fichier ajouter n’est pas encore considérés comme étant sauvegarder localement, ni synchronisé ni sauvegarder à distance. 

1. Copier ou créer un fichier dans le dossier cloné.

​                               

À cette étape, le fichier est dans le dossier mais il sera ignoré par GIT.

2. Ajouter le fichier à Git avec un clic droit

 	<img src="images\image-20240205113135201.png" alt="image-20240205113135201" style="zoom:90%;" />

3. Faire ok (Le commit sera expliqué plus loin) 

   <img src="images\image-20240205113412293.png" alt="image-20240205113412293" style="zoom:67%;" />

 

###  Commit 

Premièrement, on peut savoir qu’un projet a été modifié et qu’il y a des modifications à sauvegarder en se basant sur l’icône du dossier du projet.

​                               ![image-20240205125827698](images\image-20240205125827698.png)

**Note :** Si vous faites la commande commit mais que le code n’a pas changé, git vous indiquera qu’il n’y a pas de changement et vous ne pourrai pas faire de commit.

1. Faire un clic droit sur le dossier puis choisir l’option commit…

   ![image-20240205125915877](images\image-20240205125915877.png)

 

2. Ajouter du détail sur les modifications apportées

   

 ![image-20240205125935836](images\image-20240205125935836.png)

3. Faire un clic sur commit, si tout a fonctionné vous aurez un message similaire.

 ![image-20240205130036198](images\image-20240205130036198.png)



 **Bonne utilisation du commit**

- Vous pouvez faire plusieurs modifications et commits avant de passer aux étapes suivantes. Il n’est pas nécessaire de faire un push (détaillé dans les étapes suivantes) après chaque commit. 

- C’est une bonne pratique de faire plusieurs commits pour avoir beaucoup de points de sauvegarde. 

- C’est une bonne pratique de faire des commits qui regroupent des fonctionnalités / portions de code. Par exemple si vous devez modifier la fonction d’affichage et la fonction de calcul de votre code, la meilleure pratique serait de modifier la fonction d’affichage, faire un commit avec un commentaire qui explique les modifications, puis de modifier la fonction de calcul et de faire un commit qui explique les modifications. De cette façon, si vous avez un bug d’affichage par la suite, vous pourrez facilement voir ce que vous avez modifié en lien avec l’affichage.



### Pull

La fonction Pull interroge le dépôt principal et importe toutes les modifications qui ont été faites pour synchroniser les dépôts. Si vous avez fait des modifications de votre un code et qu’entre-temps le dépôt principal a été modifié également, le pull combinera les codes avec un « merge ». 

1. Clic droit sur le dossier puis TortoiseGit>pull

​          ![image-20240205130352488](images\image-20240205130352488.png)                     

 

2. Pour l’instant simplement faire ok. Nous couvrirons les branches « branch » plus tard 

 <img src="images\image-20240205130413363.png" alt="image-20240205130413363" style="zoom:80%;" />

 

**Note :** Si le dépôt distant est vite (vous venez de créer le dépôt, aucun push de fait) vous aurez cette erreur 

 ![image-20240205130509044](images\image-20240205130509044.png)

**Note :**

Dans certain cas, Git ne sera pas en mesure de faire le merge automatiquement et vous indiquera des conflits que vous devrez résoudre. Si par exemple dans votre code vous avez modifier la variable « patate » pour l’appeler « poutine » mais qu’une autre personne a modifié la même variable « patate » pour l’appeler « friteSauce » alors git vous demandera de choisir la solution finale.

### Push

La command push va prendre notre dépôt local et pousser les modifications qui ont été sur le dépôt distant (ie GitHub). Une fois poussé le data est considéré comme étant sauvegardé à distance de manière sécuritaire, ce qui veut dire que même si vos données sont effacées sur votre ordinateur, vous serez en mesure de les récupérer. 

**Note :** Avant de faire un push, vous devez avoir fait un commit et un pull. 

1. TortoiseGit > push

​                               <img src="images\image-20240205130740575.png" alt="image-20240205130740575" style="zoom:67%;" />

 

2. Faire ok pour l’instant. Vous avez d’autres options qui pourront être utile plus tard mais nous ne nous soucierons pas de ces options pour l’instant.

 ![image-20240205130811300](images\image-20240205130811300.png)

3. Si tout a fonctionné vous aurez ce résultat

 ![image-20240205130902434](images\image-20240205130902434.png)

## Autres fonctionnalités de base  

### Diff 

Sert à visualiser la différence entre les fichiers actuels et le dernier commit

### Diff with previous version

Sert à visualiser les différences entre les fichier actuels et l’avant-dernier commit ou un autre commit que vous pourrez choisir.

### Show Log

Permet de voir et naviguer l’historique des modifications

![image-20240205131212435](images\image-20240205131212435.png)                                

Voici plusieurs options qui sont possible à partir du log

 ![image-20240205131231335](images\image-20240205131231335.png)

### Revert

Revert permet de retourne en arrière si vous avez fait une erreur. Si par exemple dans votre dernier code vous avez introduit un bug majeur et que vous désirez tout simplement effacer cette version et retourner à une version ultérieure, vous pouvez le faire avec Revert. Attention car la/les versions éliminées seront perdues.

 

### Fonctionnalités plus avancer à regarder plus tard

#### Utiliser les branches

https://www.atlassian.com/fr/git/tutorials/using-branches

#### Branch

https://www.atlassian.com/fr/git/tutorials/using-branches

https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

#### Checkout

https://www.atlassian.com/fr/git/tutorials/using-branches/git-checkout

#### Merge

https://www.atlassian.com/fr/git/tutorials/using-branches/git-merge



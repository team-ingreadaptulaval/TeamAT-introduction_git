# Introduction pour l'Utilisation de Git par l'équipe TeamAT
# ->Instructions en cours de rédaction<-

# Utilisation de Git

Bienvenue dans le répertoire GitHub. Ce guide simplifié vous aidera à naviguer et à utiliser efficacement ce dépôt.

## Introduction générale à Git
### Comprendre les concepts de base
- Pour une introduction, en 100 seconde [ici](https://www.youtube.com/watch?v=hwP7WQkmECE).
- Pour une compréhension approfondie, en 12 minutes [ici](https://www.youtube.com/watch?v=HkdAHXoRtos).

### Utiliser Git sans lignes de commande
Explorez des interfaces sans lignes de commande comme GitHub Desktop ou Git Kraken pour une gestion locale simplifiée du répertoire Git. Ces outils sont largement utilisés au laboratoire. [GitHub Desktop](https://desktop.github.com/)


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

## Branches

### Branche principale (Default ou Main)

La branche principale est la version par défaut la plus à jour de la dernière version déployée.

### Branches de développement
Une nouvelle branche est ajoutée au projet pour ajouter des fonctionnalités au projet, lorsque les modifications sont complétés, cette branche est fusionnée à la branche principale ou devient celle par défaut.
Il est important de fermer les branches obsolètes après utilisation.

## Tags

Utilisez des tags pour marquer des jalons importants du projet. Par exemple le nom d'une version stable (Ex: V2C, V3C-Commande, V2B-PreProduction)

## Releases (Version stables du projet)

Associez les releases à des tags pour définir clairement les versions déployées (ex: V1A, V1B, V2B). Documentez les changements dans la description, tel que la liste des nouvelles fonctionnalités. Les release sont des versions du projets du projet qui sont stables, par exemple pour les PCB, il se trouve les fichiers de production prêt à commander sur JLCPCB pour une version donnée.

## Conduite générale

Organisez les répertoires de manière concise et organisée. Nommez clairement vos branches, vos nom de commit et les nom de répertoires. Ajotuez une description au répertories. Faites des release sur les version stables du projet. Travaillez proprement et professionnellement. Demandez de l'aide dès que nécéssaire et informez vous sur les bonnes pratiques.

## Issues

Utilisez l'onglet "Issues" pour suivre les problèmes et les modifications nécessaires à apporter au projet. Cependant utilisez ClickUp pour la progression globale du projet.


# Noms de répertoire

## Préfixes

- TeamAt_H : 
- TeamAt_P :
- TeamAt_L :
- TeamAt_B :
- AT- : Adaptative Technologies (Suffixe simplifié)

## Suffixes

- -PCB : Fichiers de modélisation de PCB
- -FW : Micrologiciel embarqué (Firmware)
- -CAD : Fichiers de modélisation 3D

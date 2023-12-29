# Introduction pour l'Utilisation de Git par l'équipe TeamAT

## Introduction générale à Git
### Comprendre les concepts de base
- Regardez [cette vidéo de 100 secondes](https://www.youtube.com/watch?v=hwP7WQkmECE) pour une introduction rapide.
- Pour une compréhension approfondie, investissez 12 minutes [ici](https://www.youtube.com/watch?v=HkdAHXoRtos).

### Utiliser Git sans lignes de commande
Explorez des alternatives conviviales comme GitHub Desktop ou Git Kraken pour une gestion locale simplifiée du répertoire Git. Ces outils sont largement utilisés au laboratoire. [GitHub Desktop](https://desktop.github.com/)

# Utilisation de Git

Bienvenue dans le répertoire GitHub de notre établissement de recherche en développement de produits en réadaptation. Ce guide détaillé vous aidera à naviguer et à utiliser efficacement ce dépôt.

## Conventions de message

Maintenez la clarté dans l'historique des versions en utilisant des messages de commit informatifs. Consultez la [convention de nom de commit avancée](https://cbea.ms/git-commit/) pour des indications claires sur le type de modification.

### Exemple de convention de nom de commit
Cette convention n'est pas obligatoire, mais conseillée.
- **work** : Pour des modifications, développement général du projet
- **fix** : Pour une correction de bogue
- **docs** : Pour une mise à jour de la documentation
- **style** : Pour des modifications mineures n'affectant pas la logique du code
- **clean** : Pour les modification mineures qui affectent l'organisation du répertoire

## Branches

### Branche principale (Default ou Main)

La branche principale est la version par défaut la plus à jour de la dernière version déployée.

### Branches de développement

- Créez des branches spécifiques pour les nouvelles fonctionnalités.
- Fusionnez régulièrement avec la branche principale.
- Fermez les branches obsolètes après utilisation.

## Tags

Utilisez des tags pour marquer des jalons importants du projet.

## Releases

Associez les releases à des tags pour définir clairement les versions déployées (ex: V1A, V1B, V2B). Documentez les changements et incluez des instructions post-release.

## Conduite générale

Organisez les répertoires de manière concise et organisée.

## Issues

Utilisez l'onglet "Issues" pour suivre les problèmes et les modifications nécessaires. Utilisez ClickUp pour la progression globale du projet.

## Contre indication
![alt text](https://cbea.ms/content/images/size/w2000/2021/01/git_commit_2x.png)

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

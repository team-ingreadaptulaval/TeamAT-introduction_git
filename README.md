# TeamAT-Code_de_conduite_git
Code de conduite d'utilisation de git 

# Introduction générale à git
## Comprendre les concepts de base
En 100 secondes : [https://www.youtube.com/watch?v=HkdAHXoRtos](https://www.youtube.com/watch?v=hwP7WQkmECE)

En 12 minutes : [https://www.youtube.com/watch?v=HkdAHXoRtos](https://www.youtube.com/watch?v=HkdAHXoRtos)

## Utiliser git sans lignes de commande
Git hub desktop ou git kraken sont des logiciel de gestion locale de répertoire git, il sont une alternatives au lignes de commandes. Utilisés par plusieurs au laboratoire.
https://desktop.github.com/

# Utiliser git convenablement

Bienvenue dans le répertoire GitHub de notre établissement de recherche en développement de produits en réadaptation. Ce guide détaillé vous aidera à naviguer et utiliser efficacement dans ce dépôt.

## Conventions de message de Commit

Afin de rendre la tracabilité de l'historique de version claire, chaque nom et message de commit doit être un indicatif clair des modifications ajoutées. Évitez les résumés vagues, mais visez les messages précis et bref.

### Convention de nom de commit avancée
- **work** : Pour des modifications, développement général du projet
- **fix** : Pour une correction de bogue
- **docs** : Pour une mise à jour de la documentation
- **style** : Pour des modifications mineures n'affectant pas la logique du code
- **clean** : Pour les modification mineures qui affectent l'organisation du répertoire

https://cbea.ms/git-commit/

## Branches

### Branche principale (Default ou Main)

La branche principale, est la branche par défaut la plus à jour de la dernière version déployée.

### Branches de développement

Lorsqu'une nouvelle fonctionnalité est envisagée, créez une branche dédiée à partir de la branche principale. Le nom de la branche doit refléter clairement la nature de la fonctionnalité par exemple ('dev_V2B'). Assurez-vous de fusionner régulièrement avec la branche principale pour intégrer les dernières modifications. Fermez les branches qui vous avez ouvertes qui ne sont plus utilisés.
Lorsque le travail de modification est terminé, la branche est mergé à la branche par défaut et supprimée, le tag et le release est la manière de retrouver ces versions pour une consultation ultérieure.

Il faut maintenir une quantité minimale de branche pour éviter de s'y perdre, utilisez les tags pour marquer les points importants dans l'historique de développement du projet.

## Tags

Utilisez des tags pour marquer des jalons importants du projet, comme des versions majeures ou des étapes critiques. Les tags facilitent la navigation et permettent aux utilisateurs de revenir à des versions spécifiques.

## Releases

Les release sont associé à un tag pour définir cliarement une version du projet qui a été déployée par exemple les release (V1A, V1B, V2B). Chaque release doit être accompagnée d'une documentation claire des changements apportés. Incluez des instructions détaillées sur la mise à jour et la configuration post-release.

## Code de conduite

Veuillez vous assurer de rendre vos contributions au répertoire conscises.

## Issues

Dans certains projets, l'onglet issue est utilisé pour faire un suivi des problèmes et des modifications à apporter au projet. Il est possible de s'en servir en cours de développement pour planifier une liste d'étapes de développement de la même manière qu'un to-do list détaillé. Il est quand même important d'utiliser le clickup pour spécifier la progression globale du projet.

## Contre indication
![alt text](https://cbea.ms/content/images/size/w2000/2021/01/git_commit_2x.png)

# Noms de répertoire
Les noms de répertoires manquent d'uniformité, mais les conventions actuelles sont les suivantes:

## Préfixes

- TeamAt_H : 
- TeamAt_P :
- TeamAt_L :
- TeamAt_B :
- AT- : Adaptative Technologies (Suffixe simplifié)


## suffixes

- -PCB : Fichiers de modélisation de PCB
- -FW : Micrologiciel embarqué (Firmware)
- -CAD : Fichiers de modélisation 3D







---

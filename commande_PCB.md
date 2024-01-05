# Informations générale sur les projets PCB
## Introduction
Les PCB sont concus sur KiCAD et les PCB sont fabriqués par JLCPCB.

# 1 - Information sur la conception de PCB
## Choix de pièces en inventaire
Les pièces utilisés sont choisies à partir de [l'inventaire  JLCPCB](https://jlcpcb.com/parts). Si la pièce n'est pas disponible, il faut la précommander sur un compte JLCPCB, cependant, on y trouve un inventaire de 3M de pièces alors il est rare qu'un type de pièce particulier n'est pas disponible. Pour faire simple, il faut s'adapter à leur inventaire afin de faire un concept assemblable chez eux. Sinon il faut précommander les pièces ou les assembler soit même. 
### Pièce basic ou extended
Il faut vérifier si les pièces sont basic ou extended. Pour les pièces extended, le frais de setup pour l'assemblage coute 3$ supplémentaire par composante extended différente.
[Source, voir point #6](https://jlcpcb.com/help/article/98-pcb-assembly-faqs)
### Indiquer le numéro de pièce dans KiCAD
Le numéro de pièce LCSC doit être indiqué dans les propriété de pièces dans la schématique afin d'identifier la pièce correspondante dans la génération du BOM.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/a645e649-a084-4562-bab2-e4f174e232cb" width=50%>

[Source](https://jlcpcb.com/help/article/81-How-to-generate-the-BOM-and-Centroid-file-from-KiCAD)

## Règles de conception PCB de base 
Les capacités de production instaurés par JLCPCB sont indiqués sur [cette page](https://jlcpcb.com/capabilities/pcb-capabilities).

Voici un exemple de PCB configuré selon ces recommandations.
<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/e0bdeaee-5a91-4cd0-8c3a-d26d9f7085e9" width=80%>

## Génération de fichiers de production
### Vérification pré-génération de fichiers
#### Regénération de zones de remplissage.
Dans l'éditeur de PCB, Appuyer sur B afin de regénérer les zones de cuivre. Cela permet de les mettre à jour suite au dernières modifications.
#### Vérification d'erreur
Il est fortement recommandé de vérifier les erreurs dans l'outil de modification de PCB avant de passer à la génération de fichier. Si quelconque erreur s'y trouve, les corriger, sinon pour certain cas, tel que les overlap de composantes ou les erreur de tolérance pour pièces avec des pitch plus petit que le reste du PCB, il est possible d'ignorer certaines erreurs en faisant clic droit sur l'erreur et ignorer. Cette pratique est "acceptable" dans certain cas. Sinon il est possible de mieux adapter les règles de conception.
#### Vérification du fichier en 3D
Il est possible d'ouvrir le PCB en 3D et de l'inspecter de cette manière. Il est plus évident de vérifier le silkscreen et le sens des composantes en 3D qu'en 2D. Pour ajouter les pièces 3D manquantes, il faut modifier les propriété des empreintes de pièces dans sa librairie.

### Génération automatique
Afin de générer manuellement les fichiers de productions dans KiCAD pour JLCPCB, il est possible d'utiliser une extension KiCAD. Pour se faire, dans le gestionnaire de plugin, il faut installer l'extension JLC fabrication toolkit.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/8be58f7e-c238-4ddc-97fe-6ceb45859844" width=80%>
<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/d4254083-30da-4f8c-b763-972d76e7e828" width=50%>

Ensuite pour générer les fichiers de fabrication, cliquer sur le bouton d'exécution de JLC fabrication toolkit dans l'éditeur de PCB. Par contre il faut regénérer les zones de remplissage

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/f4a1d259-8ddb-49e0-a966-7780216fd664" width=80%>

Les fichiers sont générés dans un dossier nommée production sur le répertoire du projet.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/b5f41932-3255-4492-b986-63ebd09f2628" width=50%>

### Génération manuelle
Les fichiers de production peuvent être générés manuellement, il faut suivre le [tutoriel suivant](https://jlcpcb.com/help/article/362-how-to-generate-gerber-and-drill-files-in-kicad-7). Cependant il est bien plus simple et rapide d'utiliser l'extension.

## Vérification après génération des ficheers de production
Il est bon de revérifier les erreurs avec le DRC cheker dans l'éditeur de PCB.
### Inspection des fichiers de production manuelle
Pour s'assurer que les fichiers de production ont été bien générés, il est recommandé de les ouvrir dans le gerber viewer dans kicad. 
- Vérifiez qu'il ne manque pas de couches
- Vérifiez chaque couches individuellement s'ils correspondent avec les fichiers de conception.
- Vérifiez si les couches sont alignées correctement.

# 3 - Commande de PCB
Les fichiers sont commandés à [cette adresse](https://cart.jlcpcb.com/quote/). 
## Importer les fichiers gerber


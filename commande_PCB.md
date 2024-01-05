# Informations générale sur les projets PCB
## Introduction
Les PCB sont concus sur KiCAD et les PCB sont fabriqués par JLCPCB.

# Commande de PCB sur JLCPCB 
Les PCB sont commandés à [cette adresse](https://cart.jlcpcb.com/quote/). 
## Importer les fichiers gerber
Déposez le fichier .zip qui se trouve dans le fichier de production.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/25cd8961-55ae-46d5-88d2-4a0658f72ca2" width=50%>

## Options à changer
Les options importantes à vérifier sont les suivantes, les autres peuvent être laissés tel que par défaut :
### Different design
Pour les projets dont plusieurs PCB sont combinés sur un même PCB, il faut modifier l'option different design correspondant au nombre de PCB. Également mettre Panel by Customer.

![image](https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/d46f6d46-39ba-41d0-a7cc-327f144e4c67)

### Épaisseur :
1. Laisser par défaut à 1.6 pour la plupart des projets.
2. Mettre à 1.0 pour les projets miniatures tels que l'ergowatch nano ou mini
    
### Surface Finish :
1. Prendre leadFree HASL (fini cuivre étamé étain sans plomb); sinon
2. ENIG(plaqué OR) pour les PCB ayant des puces intégrés avec des pads sous les pièces. Cela assure un meilleur fini de surface et une quantité d'étain plus uniforme. Toujours utiliser pour les microcontrolleurs tel que le STM32 ou l'IMU de l'ergowatch.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/0bce9e15-e60b-440e-bacc-9a2e6f5ef7aa" width=50%>

### Confirm production file
Demander la confirmation de fichiers de production. Cette option permet de demander une validation de notre coté suite au pré-traitement de nos fichiers avant de passer à la production.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/b9cce73b-9ebe-4f07-9333-352867278836" width=50%>

### Remove order Number 
Choisir Yes.

## Options d'assemblage
Voici un exemple d'options d'asemblage.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/31e41d45-4fdb-4ee0-ab7f-c996eb7fdfc7" width=50%>.

### Ajout de fichiers d'assemblage
Il faut ajouter les fichiers correspondant qui se trouvent dans le dossier de fichier de production. 
- bom : bom.csv
- cpl : position.csv
<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/0e0c0686-f7f7-4f3f-84d2-16137517bd4a" width=50%>

### Choix de pièces
Lors de l'ajout de fichiers d'assemblage, JLC ajoute désormais les pièces manquantes de manière automatique. Il faut revérifier l'entièreté des pièces afin de s'assurer qu'ils sont bonnes. Pour se faire deux points sont à valider :
1. Vérifier si les pièces sont les bonnes, passer sur chaque ligne et valider deux point.
- Le footprint correspondant est bon. (0603, 0805, etc.)
- La valeur de la pièce et bonne (1uF, 10uF, etc.)
2. Chaque composant "extended" nécessite un assemblage au coût de 3$. Si vous assemblez vous-même pour de petits volumes de PCB, cela peut parfois être plus économique (mais c'est rare). Dans la plupart des cas, il est préférable de choisir l'assemblage professionnel, car les coûts des composants chez JLC sont très abordables, compensant rapidement les frais d'assemblage.
  
<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/54519aa6-850b-475b-abc8-4ca5c4645b13" width=50%>
<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/20a9a18f-5908-477d-b92f-f75d462781e4" width=50%>

### Positionnement de pièces
Il est possible de laisser tel quel et JLC se charge de les mettre en place correctement.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/bfc8bafd-9499-4169-8c4a-b7dfd0b0bfb3" width=50%>


## Paiement et livraison
Très important, choisir ce type de livraison, le plus rapide et évite les surprises des frais de douanes.

<img src="https://github.com/team-ingreadaptulaval/TeamAT-introduction_git/assets/46634707/78cb855f-eda3-4f00-a2e2-c7b4cb38af44" width=50%>



# ANNEXE : Information sur la conception de PCB KiCAD pour JLCPCB
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

## Vérification après la génération des fichiers de production
Il est bon de revérifier les erreurs avec le DRC cheker dans l'éditeur de PCB.
### Inspection des fichiers de production manuelle
Pour s'assurer que les fichiers de production ont été bien générés, il est recommandé de les ouvrir dans le gerber viewer dans kicad. 
- Vérifiez qu'il ne manque pas de couches
- Vérifiez chaque couches individuellement s'ils correspondent avec les fichiers de conception.
- Vérifiez si les couches sont alignées correctement.





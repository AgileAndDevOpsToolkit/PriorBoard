# Prompt initial

Conversation Claude qui a permis de générer la première version de PriorBoard : https://claude.ai/share/8ed32f9f-9415-4322-abcf-3ee3fcac67be

```
Hello, je veux faire une nouvelle application web HTML/CSS/Javascript.
Dans cette application il y a plusieurs écrans :
- un écran qui présente une liste d'items. L'écran propose une zone qui permet d'ajouter un ou plusieurs items : on peut soit ajouter les items dans un champ texte : une ligne = un item de la liste, soit uploader un fichier d'items
- La zone d'ajout est en haut de l'écran et est escamotable pour ne pas prendre beaucoup de place si on a rien à ajouter
- chaque item est associé à un ordre de priorité dans le cadre d'un classement ELO comme au jeu d'échec
- dans l'application il y a un autre écran "battle". Quand on va dessus, cela propose deux items au hasard : A ou B ?
L'utilisateur choisit l'un ou l'autre en cliquant dessus. Après avoir choisi, cela sélectionne deux autres items. Chaque fois que l'utilisateur fait un choix, le choix est sauvegardé dans une structure de données JSON, et le classement est mis à jour lui aussi dans la structure de données JSON.
- le choix n'est pas réellement au hasard : il faut privilégier les items qui ont le plus faible nombre de "battle" enregistrés
- La structure de donnée JSON contient également la liste de tous les items (avec leur classement ELO).
- Définis l'algorithme de calcul ELO (je ne m'y connais pas)
- Toutes les datas sont stockées en local storage dans le navigateur
- On doit pouvoir télécharger la structure de donnée JSON complète via un petit bouton de sauvegarde
- Sur l'écran liste d'items, les items sont classés par leur classement ELO
- L'application s'appelle "PiorBoard"
- niveau style, fais un style épuré, ergonomique, où les items sont bien visibles et lisibles
Analyse bien mon besoin et fais-moi une bonne programmation
```

Items terminés

```
Dans l'application actuellement on peut supprimer une feature, je voudrais ajouter la possibilité de dire qu'une feature est terminée : le bouton doit ressembler à une case à cocher. Si une feature est terminée alors elle apparaît toujours dans le classement mais elle est surlignée d'une certaine couleur  pour indiquer qu'elle n'est plus active, et le texte est rayé. Quand on fait les battle, cette feature n'est plus sélectionnée pour les battles donc son score n'évolue plus
```

```
La coche verte est trop présente, elle ressort trop (capture d'écran). Est-ce que tu peux adoucir la couleur en mode pastel, et rayer aussi le numéro dans le classement, le score et le nombre de battles
```

```
Adoucit encore le fond de la case des items checked : en mode checked le fond de la case doit être de la même couleur que le fond de la ligne. Ajuste les couleurs en conséquence pour que le hover soit cohérent (légèrement plus foncé).
En plus : je me suis trompé au début : l'application d'appelle PriorBoard : donc partout où est écrit "Pior" ou "pior" il faut ajouter un "r" : "Prior" ou "prior"
```


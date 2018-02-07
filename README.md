# Easy-data--Datas

## Installation

Il vous suffira de récupérer les fichiers pour les exploiter.

## Avancement

Actuellement tout n'a pas encore été parser par manque de temps, la liste sera mise à jour en même temps que les fichiers sur le repo.
Actuellement disponible :

* Amulettes (100%)
* Anneaux (100%)
* Armes (100%)
* Bottes (100%)
* Boucliers (100%) [9 cosmétiques manquants]
* Capes (100%)
* Ceintures (100%)
* Coiffes (100%)
* Dofus (100%)
* Sac à dos (100%)
* Trophées (100%)
* Panoplies (100%)
* Familiers (0%)
* Montures (0%)
* Ressources (0%)
* Recettes (0%)

## Structure du JSON

La structure du JSON dépend du type d'équipement, en effet il y a 3 grandes catégories (pour le moment)
Il vous suffira de décoder le JSON dans le langage de votre choix pour récupérer le contenu sous forme d'un tableau d'objets (ici les objets sont les items)

* [Equipements](#equipements)
* [Armes](#armes)
* [Panoplies](#panoplies)

### Equipements
```"set": []``` si pas de panoplie.
```json
{
  "id": "Id de l'item",
  "idImg": "Id de l'image",
  "imgPath": "Chemin de l'image",
  "name": "Nom de l'item",
  "set": {
      "setID": "Id de la panoplie",
      "setName": "Nom de la panoplie"
  },
  "type": "Type de l'item (amu, ...)",
  "level": "Level de l'item",
  "condition": [
      "Une ligne de condition",
      ...
  ],
  "stats": [
      "Une ligne de stat",
      ...
  ],
  "description": "Description de l'item"
}
```
### Armes
```"set": []``` si pas de panoplie.
```json
{
  "id": "Id de l'item",
  "idImg": "Id de l'image",
  "imgPath": "Chemin de l'image",
  "name": "Nom de l'item",
  "set": {
      "setID": "Id de la panoplie",
      "setName": "Nom de la panoplie"
  },
  "type": "Type de l'item (amu, ...)",
  "level": "Level de l'item",
  "carac": [
      "Une ligne de carac",
      ...
  ],
  "condition": [
      "Une ligne de condition",
      ...
  ],
  "stats": [
      "Une ligne de stat",
      ...
  ],
  "description": "Description de l'item"
}
```
### Panoplies
```json
{
  "id": "Id de la panoplie",
  "name": "Nom de la panoplie",
  "level": "Niveau max de la panoplie",
  "items": [
    [["Id de l'item"], "Nom de l'item"],
    ...
  ],
  "bonus": [
      ["Une ligne du bonus max items", ...],
      ["Une ligne du bonus max - 1 items", ...]
  ]
}
```

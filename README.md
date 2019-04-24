# Classification de chansons par genre

Des adolescents à Magic Makers ont créé un projet qui reconnaît le style d'une chanson parmi 6 genres qu'ils ont défini : instrumental, rock, sad trap, hip hop, rap et électro.
Ils ont utilisé les modules Tensorflow et Keras en python pour créer leur réseau de neurones.
Ils ont utilisé l'API de Spotify pour récupérer des chansons et leurs paramètres (cf [Doc Spotify](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/)) et les passer à leur modèle !

## Stage IA à Magic Makers

[Magic Makers](https://www.magicmakers.fr/) propose des ateliers de programmation créative pour des jeunes de 7 à 15 ans. Depuis 2018, des ateliers pour adolescents autour de l'intelligence artifielle sont donnés durant les vacances. Lors du stage, les makers découvrent ce qu'est un réseaux de neurones et les notions s'y attachant (perceptron multi-couches, convolutions, overfit, etc) en créant des projets comme celui-ci !

## Auteur du projet

Ce projet a été réalisé par **Alexis et Oscar** (14 et 13 ans) lors du stage de Février dans le centre de Magic Makers Paris 9e, animé par **Jade, Emilie et Antoine**.


### Dataset

* Playlists sur Spotify - Oscar et Alexis ont créé une Playlist sur Spotify pour chaque genre de musique qu'ils avaient défini. Ils avaient donc 6 Playlists.


### Entraînement

Pour ce projet, Oscar et Alexis ont utilisé un perceptron multi-couches.

Pour pouvoir lancer l'entraînement, il faut avoir associer son compte Spotify à un compte Developer. Il faut ensuite rentrer dans le code : son nom d'utilisateur, son 'Client_id' et son 'Client_secret'. Pour finir, il faut demander les tokens nécessaires. Toutes ces étapes se passent sur le site [Spotify Developer](https://developer.spotify.com/).

```
python3 spotify-train.py
```

## Modules

* [Spotipy](http://spotipy.readthedocs.io/en/latest/) - pour utiliser l'API Spotify
* [Keras](https://keras.io/) - pour créer le modèle (avec TensorFlow)
* [Flask](http://flask.pocoo.org/) - pour créer une webapp
* [H5py](https://www.h5py.org/) - pour sauvegarder le modèle
* [Sklearn](https://scikit-learn.org/stable/) - pour mélanger et séparer les données
* [Numpy](https://www.numpy.org/) - pour manipuler des tableaux


## Résultats

<à venir>

### Application

Une fois le modèle entraîné, les makers ont choisi de réaliser une webapp avec Flask pour leur projet ! Ils ont d'abord créé une page d'accueil permettant de renter l'ID Spotify de la chanson à tester et une seconde page qui affiche le genre prédit par leur modèle !
Ils ont ensuite amélioré leur webapp en ajoutant un champ pour rentrer le nom d'une chanson et utiliser l'API Spotify pour effectuer une recherche et trouver l'ID de cette chanson !


Sous Mac et Linux :
```
export FLASK_ENV = development
export FLASK_APP = spot-webapp.py

flask run
```

Sous Windows :
```
set FLASK_ENV = development
set FLASK_APP = spot-webapp.py

flask run
```

### Remerciement

* Merci à Spotify - [API Spotify](https://developer.spotify.com/documentation/web-api/reference)
* Merci à [Magic Makers](https://www.magicmakers.fr/)
* Merci à [Keras](https://keras.io/) pour faciliter la création de réseaux de neurones !

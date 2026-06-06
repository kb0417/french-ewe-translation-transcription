# Artifacts

Ce dossier contient les fichiers intermédiaires générés pendant les différentes étapes du projet.

Ces fichiers ne sont pas les données brutes, mais des objets produits après le prétraitement et utilisés pour accélérer les expériences.

## Contenu

Le sous-dossier `preprocessing/` contient notamment :

- les tokenizers sauvegardés ;
- la configuration du prétraitement ;
- les fichiers `.npy` utilisés pour entraîner les modèles Seq2Seq LSTM.

Ces fichiers permettent de reprendre l'entraînement ou l'évaluation sans relancer tout le prétraitement depuis le début.

# Données du projet

Ce dossier contient les données utilisées pour entraîner et évaluer les modèles de traduction.

## Structure

- `raw/` : dataset original au format Excel.
- `processed/` : fichiers nettoyés et séparés en ensembles d’entraînement, validation et test.

## Dataset

Le dataset utilisé est un corpus parallèle français-éwé contenant environ 23 811 paires de phrases.

Les données sont utilisées pour entraîner et évaluer les modèles suivants :

- Seq2Seq LSTM français → éwé ;
- Seq2Seq LSTM éwé → français ;
- NLLB fine-tuné avec LoRA.

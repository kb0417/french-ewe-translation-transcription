# Système de traduction automatique et transcription assistée français-éwé

Ce projet a pour objectif de développer un système capable de traduire automatiquement du français vers l’éwé et de l’éwé vers le français.

Une extension du projet concerne la transcription automatique, c’est-à-dire la conversion d’un audio en texte avant traduction.

## Objectifs du projet

- Préparer un dataset parallèle français-éwé.
- Nettoyer et explorer les données.
- Construire un modèle de traduction automatique.
- Tester la traduction dans les deux sens : français → éwé et éwé → français.
- Ajouter un module simple de transcription assistée.
- Proposer une interface de démonstration.

## Dataset

Le dataset utilisé contient environ 23 811 paires de phrases français-éwé.
Il est issu du corpus parallèle français-éwé disponible sur Zenodo/Zindi.

## Technologies prévues

- Python
- Google Colab
- Pandas
- Scikit-learn
- TensorFlow / Keras ou PyTorch
- Hugging Face Transformers
- Streamlit ou Gradio pour la démonstration

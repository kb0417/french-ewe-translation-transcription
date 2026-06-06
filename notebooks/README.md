# Notebooks du projet

Ce dossier contient les notebooks réalisés dans l’ordre chronologique du projet.

## Liste des notebooks

1. `01_exploration_dataset_french_ewe.ipynb`  
   Exploration du fichier Excel, lecture des feuilles `French`, `Ewe` et `Metadata`, fusion des données, nettoyage initial et création des fichiers `train`, `validation` et `test`.

2. `02_preprocessing_translation.ipynb`  
   Nettoyage léger des textes, ajout des tokens spéciaux `<start>` et `<end>`, création des tokenizers, transformation des phrases en séquences numériques et sauvegarde des fichiers de prétraitement.

3. `03_seq2seq_lstm_french_to_ewe.ipynb`  
   Construction, entraînement et évaluation d’un modèle Seq2Seq LSTM pour la traduction français → éwé.

4. `04_seq2seq_lstm_ewe_to_french.ipynb`  
   Construction, entraînement et évaluation d’un modèle Seq2Seq LSTM pour la traduction éwé → français.

5. `05_nllb_translation_french_ewe.ipynb`  
   Test du modèle NLLB-200 pré-entraîné pour la traduction français ↔ éwé.

6. `06_finetuning_nllb_french_ewe.ipynb`  
   Fine-tuning léger de NLLB avec LoRA pour la traduction français → éwé.

7. `07_finetuning_nllb_ewe_to_french.ipynb`  
   Fine-tuning léger de NLLB avec LoRA pour la traduction éwé → français.

8. `08_gradio_translation_demo.ipynb`  
   Création d’une interface Gradio permettant de tester les deux directions de traduction.

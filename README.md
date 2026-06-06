# Système de traduction automatique français-éwé

Ce projet porte sur la conception d’un système de traduction automatique bidirectionnelle entre le français et l’éwé.

L’objectif principal est de comparer plusieurs approches de traduction automatique :

- des modèles Seq2Seq LSTM entraînés from scratch ;
- un modèle multilingue pré-entraîné NLLB ;
- un fine-tuning léger de NLLB avec LoRA.

Le projet s’appuie sur un corpus parallèle français-éwé d’environ 23 811 paires de phrases.

## Objectifs du projet

- Explorer et préparer un dataset parallèle français-éwé.
- Construire une baseline Deep Learning avec Seq2Seq LSTM.
- Tester la traduction dans les deux sens : français → éwé et éwé → français.
- Évaluer les limites des modèles LSTM entraînés from scratch.
- Tester NLLB-200 pré-entraîné.
- Fine-tuner NLLB avec LoRA sur le corpus français-éwé.
- Proposer une interface de démonstration avec Gradio.

## Dataset

Le dataset utilisé contient environ 23 811 paires de phrases français-éwé.

Il est organisé en trois ensembles :

- `train.csv` : données d'entraînement ;
- `valid.csv` : données de validation ;
- `test.csv` : données de test.

## Méthodologie

Le projet suit une progression expérimentale :

1. Exploration et nettoyage du dataset.
2. Prétraitement des textes et tokenisation.
3. Entraînement de modèles Seq2Seq LSTM.
4. Test de NLLB pré-entraîné.
5. Fine-tuning de NLLB avec LoRA.
6. Création d’une interface Gradio.

## Résultats principaux

| Modèle | Direction | Métrique | Score |
|---|---|---:|---:|
| Seq2Seq LSTM | Français → Éwé | Accuracy mot par mot | 0.2576 |
| Seq2Seq LSTM | Éwé → Français | Accuracy mot par mot | 0.2400 |
| NLLB pré-entraîné | Français → Éwé | BLEU | 3.58 |
| NLLB pré-entraîné | Éwé → Français | BLEU | 2.77 |
| NLLB + LoRA | Français → Éwé | BLEU | 5.96 |
| NLLB + LoRA | Éwé → Français | BLEU | 7.42 |

Les modèles LSTM servent de baselines pédagogiques. Les meilleurs résultats sont obtenus avec NLLB fine-tuné avec LoRA.

## Interface de démonstration

Une interface Gradio permet de tester les deux directions de traduction :

- français → éwé ;
- éwé → français.

Le notebook correspondant est :

`notebooks/08_gradio_translation_demo.ipynb`

## Structure du dépôt

```text
french-ewe-translation-transcription/
├── app/
├── artifacts/
│   └── preprocessing/
├── data/
│   ├── raw/
│   └── processed/
├── models/
├── notebooks/
├── reports/
├── src/
├── README.md
├── requirements.txt
└── .gitignore

## Technologies utilisées

- Python
- Google Colab
- Pandas / NumPy
- TensorFlow / Keras
- PyTorch
- Hugging Face Transformers
- PEFT / LoRA
- SacreBLEU
- Gradio

## Limites du projet

Ce projet reste expérimental. Les modèles LSTM entraînés from scratch produisent des traductions faibles, ce qui montre les limites de cette approche sur une langue peu dotée comme l’éwé.

Les meilleurs résultats sont obtenus avec NLLB fine-tuné avec LoRA, mais les scores BLEU restent modestes. Les traductions générées doivent donc être interprétées avec prudence et vérifiées par des locuteurs natifs avant toute utilisation réelle.

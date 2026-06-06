# Modèles entraînés

Ce dossier est destiné à documenter les modèles entraînés pendant le projet.

Certains modèles complets peuvent être volumineux. Selon les contraintes de stockage, ils peuvent être conservés dans Google Drive plutôt que directement dans GitHub.

## Modèles produits

- `best_seq2seq_fr_to_ewe.keras` : meilleur modèle LSTM français → éwé.
- `seq2seq_lstm_fr_to_ewe_final.keras` : modèle LSTM final français → éwé.
- `best_seq2seq_ewe_to_fr.keras` : meilleur modèle LSTM éwé → français.
- `seq2seq_lstm_ewe_to_fr_final.keras` : modèle LSTM final éwé → français.
- `nllb_fr_to_ewe_lora_final/` : adaptateur LoRA NLLB fine-tuné pour français → éwé.
- `nllb_ewe_to_fr_lora_final/` : adaptateur LoRA NLLB fine-tuné pour éwé → français.

Les notebooks `03`, `04`, `06` et `07` expliquent comment ces modèles sont entraînés, évalués et sauvegardés.

# Limites du projet

Ce projet propose un système expérimental de traduction automatique français-éwé.

Les principales limites sont :

- le corpus reste relativement limité pour entraîner un traducteur complet ;
- les modèles LSTM entraînés from scratch produisent des traductions faibles ;
- les scores BLEU restent modestes malgré le fine-tuning de NLLB ;
- le fine-tuning a été réalisé sur un sous-ensemble du dataset à cause des contraintes de Google Colab ;
- les traductions doivent être vérifiées par des locuteurs natifs avant une utilisation réelle.

La transcription automatique n’a pas été implémentée dans la version finale. Elle reste une perspective d’amélioration possible.

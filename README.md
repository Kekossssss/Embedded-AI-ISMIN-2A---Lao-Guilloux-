## Description
Ce projet fait partie du cursus de l'ISMIN en 2A et explore l'intégration de l'**intelligence artificielle embarquée** dans des systèmes à ressources limitées.

## Installation
1. **Cloner le repository**
   ```sh
   git clone https://github.com/Kekossssss/Embedded-AI-ISMIN-2A---Lao-Guilloux-.git
   cd Embedded-AI-ISMIN-2A---Lao-Guilloux-
   ```

2. **Entraînement du modèle (optionnel)**

   Dans un premier temps, il est nécessaire d'entrainer le modèle, cette étape est optionnelle car vous pourrez trouver le fichier .tflite du modèle dans ce repository.  
   Pour entrainer le modèle, placez-vous dans l'environnement python, et executez le fichier suivant :
   ```sh
   python TP_IA_EMBARQUEE.ipynb
   ```
   Ce programme permet l'entrainement du modèle, et la sauvegarde des jeux de données d'entrainement, ainsi que du modèle en lui même au format .tflite.
   Le modèle entrainé possède une précision de 94%, et permet d'obtenir un résultat assez précis pour notre cas d'utilisation. Néanmoins, si vous voulez modifier les couches de neuronnes du modèle, modifiez les cellules 48 et 50 du Jupyter Notebook (Couches de neuronnes, batch size et nombre d'epoch).
   Il est également possible de modifier les noms des fichiers contenant les jeux de données ou le modèle en modifiant la cellule 52 du Jupyter Notebook.

3. **Implémentation du modèle sur carte STM32**
  
      Un projet CubeIDE est disponible dans cette archive et contient l'ensemble des éléments nécessaire pour implémenter un modèle sur une carte STM32L4R9. Il est disponible au format .zip, il suffit donc de le dézipper avec la commande suivante :
   ```sh
   sudo apt-get update
   sudo apt-get install zip unzip
   unzip Electif_IA_Embedded_Machine_Failure.zip
   ```
   Ensuite, il suffit d'ouvrir le projet avec CubeIDE, de le build et de le téléverser sur la carte.  
⚠️ Pour le bon fonctionnement du projet, les lignes 115 à 119 doivent être commentées dans le main.c ⚠️

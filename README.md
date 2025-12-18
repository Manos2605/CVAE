# Génération d'Art Abstrait avec CVAE (Auto-Encodeur Variationnel Conditionnel)

Ce projet utilise un modèle d'Intelligence Artificielle basé sur un Auto-Encodeur Variationnel Conditionnel (CVAE) pour générer des images d'art abstrait en fonction d'ambiances colorées. Le modèle apprend à créer de nouvelles œuvres artistiques en analysant un dataset d'art abstrait et en classifiant les images par catégories d'ambiance (Chaud, Froid, Lumineux, etc.).

## Exemples de Visualisations GIF

Voici quelques exemples de GIFs générés par le modèle après entraînement. Ces animations montrent l'exploration créative de l'espace latent pour différentes ambiances :

### Exploration circulaire dans l'ambiance "Chaud"
Un mouvement fluide dans l'espace latent génère des variations d'art abstrait avec des tons chauds (rouges, oranges).  
<div align="center">
  <img src="interpolation_Chaud.gif" alt="Exploration Chaud" width="400">
  <p><em>Exécutez le code pour générer ce GIF</em></p>
</div>

### Interpolation linéaire dans l'ambiance "Froid"
Transition douce entre deux points latents, créant une évolution artistique avec des couleurs froides (bleus, violets).  
<div align="center">
  <img src="interpolation_Froid.gif" alt="Interpolation Froid" width="400">
  <p><em>Exécutez le code pour générer ce GIF</em></p>
</div>

### Espace latent visualisé
Projection 2D des représentations latentes colorées par classe d'ambiance.  
<div align="center">
  <img src="espace_latent.png" alt="Espace Latent" width="400">
  <p><em>Graphique généré automatiquement</em></p>
</div>

Ces visualisations illustrent la capacité du CVAE à produire de l'art original tout en respectant les contraintes d'ambiance.

## Fonctionnalités

- **Tri automatique des images** : Analyse des couleurs (HSV) pour classer les images par ambiance.
- **Modèle CVAE** : Génération conditionnée d'images basée sur des labels d'ambiance.
- **Visualisations** : Graphiques de répartition, espace latent, et génération de GIFs d'exploration.
- **Génération d'images** : Création d'images individuelles ou d'animations (GIFs) pour une ambiance donnée.

## Technologies utilisées

- **Python 3.x**
- **TensorFlow/Keras** : Pour le modèle CVAE
- **OpenCV** : Analyse d'images et couleurs
- **NumPy, Matplotlib, PIL** : Traitement et visualisation
- **imageio** : Création de GIFs
- **kagglehub** : Téléchargement du dataset

## Installation

1. **Cloner le repository** :
   ```bash
   git clone <url-du-repo>
   cd <nom-du-repo>
   ```

2. **Installer les dépendances** :
   ```bash
   pip install kagglehub opencv-python numpy matplotlib tensorflow pillow imageio
   ```

3. **Télécharger le dataset** :
   - Le notebook télécharge automatiquement le dataset depuis Kaggle via `kagglehub`.
   - Assurez-vous d'avoir configuré votre clé API Kaggle si nécessaire.

## Utilisation

1. **Ouvrir le notebook** :
   - Lancez Jupyter Notebook ou VS Code avec le fichier `main.ipynb`.

2. **Exécuter les cellules** :
   - Suivez l'ordre des cellules pour :
     - Télécharger et trier les données.
     - Entraîner le modèle CVAE.
     - Générer des images et des GIFs.

3. **Configurations principales** :
   - `IMAGE_SIZE = 128` : Taille des images.
   - `LATENT_DIM = 128` : Dimension de l'espace latent.
   - `EPOCHS = 100` : Nombre d'époques d'entraînement.
   - `BATCH_SIZE = 64` : Taille des batches.

## Structure du projet

- `main.ipynb` : Notebook principal contenant le code complet.
- `data/dataset_trie/` : Dossier généré avec les images triées par ambiance.
- `cvae_encoder.keras` & `cvae_decoder.keras` : Modèles sauvegardés après entraînement.
- `*.gif` : GIFs générés (exploration et interpolation).

## Catégories d'ambiance

Les images sont classées selon :
- **Chaud** : Rouges, oranges, jaunes.
- **Froid** : Bleus, violets, cyans.
- **Lumineux** : Images très claires.
- **Sombre** : Images très foncées.
- **Neutre** : Faible saturation.
- **Végétal** : Verts, jaune-vert.
- **Autre** : Cas non classés.

## Exemples d'utilisation

- **Générer des images** :
  ```python
  generer(cvae, "Chaud", 5)  # Génère 5 images pour l'ambiance "Chaud"
  ```

- **Créer un GIF d'exploration** :
  ```python
  creer_gif_exploration(cvae, "Froid", n_frames=120)
  ```

- **Interpolation** :
  ```python
  create_gif("Lumineux", steps=300)
  ```

## Résultats attendus

Après entraînement, le modèle peut :
- Générer des images originales dans un style abstrait.
- Explorer l'espace latent via des animations.
- Maintenir la cohérence avec l'ambiance choisie grâce à la conditionnalité.

## Améliorations futures

- Ajouter une interface web pour génération interactive.
- Intégrer d'autres styles artistiques ou datasets.
- Optimiser les performances avec des GPUs.
- Évaluer la qualité des générations avec des métriques (FID, Inception Score).

## Licence

Ce projet est sous licence MIT. Utilisez-le librement pour des fins éducatives ou artistiques.

## Auteur

[Votre nom] - Projet pour le cours "Fonctionnement d'un laboratoire de création artistique" (AIA-3).</content>
<parameter name="filePath">c:\Users\sonwa\OneDrive\Documents\Art Numérique\AIA-3\Semestres 1\Fonctionnement d'un laboratoire de création artidtique\CVAE\README.md

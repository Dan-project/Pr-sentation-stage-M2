# Support de soutenance (Beamer)

Soutenance de stage de M2 SAR : **Cartographie sémantique coopérative multi-robots
par fusion LiDAR–caméra** (Dan CALAMIA, CRIStAL, septembre 2026).

## Compiler

1. Le dossier `Images/` (copié du rapport) est déjà à côté de `main.tex`. Les noms de fichiers
   sont ceux du dépôt `Rapport-de-stage`. `../Images/` fonctionne aussi, si la
   présentation est un sous-dossier du rapport.
2. Lancer `latexmk -pdf main.tex`, ou pdfLaTeX deux fois.
   Sur Overleaf : importer les fichiers `.tex` et le dossier `Images/`,
   compilateur pdfLaTeX.

Paquets utilisés : beamer, tikz, tcolorbox, adjustbox, pifont, booktabs.
Fira Sans est utilisée si elle est installée, sinon Latin Modern.

## Organisation

| Fichier | Contenu |
|---|---|
| `main.tex` | page de titre, plan, inclusion des parties |
| `style.tex` | thème : couleurs du rapport, barre de progression, intercalaires |
| `01_contexte.tex` | contexte, problématique, objectifs |
| `02_liosam.tex` | SLAM et graphe de facteurs, LIO-SAM (principe, architecture, choix de LIORF) |
| `03_yolo.tex` | YOLO : principe, pourquoi la segmentation sémantique |
| `04_framework.tex` | architecture, projection, association, repère monde, carte, validation KITTI (avec la vidéo) |
| `05_extensions.tex` | loop closure, carte a priori, multi-robots |
| `06_resultats.tex` | plateformes, Ranger, Scout, multi-robots |
| `07_conclusion.tex` | bilan, perspectives, questions |
| `08_annexes.tex` | slides de secours pour les questions |

## Préparer l'oral

- Avant chaque slide, un bloc `% À DIRE (~durée)` résume ce qu'il faut dire.
  Le total visé est d'environ 20 minutes, hors questions.
- Certains blocs ajoutent des réponses aux questions probables du jury
  (alternatives à LIO-SAM, différence LIORF / LIO-SAM…).
- Les slides de secours, placées après « Questions ? », ne sont pas comptées
  dans la numérotation.
- Pour un projecteur 4:3, remplacer `aspectratio=169` par `aspectratio=43`.
  Les schémas TikZ sont prévus pour le 16:9 et devront alors être réduits.

## Vidéo

La slide « Validation sur KITTI : fusion en temps réel » contient `videos/opencv_kitti.mp4`,
un extrait de 10 s recadré sur la fenêtre OpenCV. Garde le dossier `videos/`
à côté du PDF et clique sur l'image pour lancer la vidéo. Elle se lit avec
pdfpc (`brew install pdfpc`), Adobe Reader ou Okular, mais pas avec Aperçu
sur Mac.

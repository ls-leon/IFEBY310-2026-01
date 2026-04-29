# IFEBY310-2026-01

Technologie Big Data

Krista Carla Sevi
Leon Lafosse
Mick Wanderly Laveus

## Comment mettre en place l'environnement python?

A noter : il est tout à fait possible de consulter le fichier html sans devoir set up l'environnement, le fichier se trouve dans /_outdir

Les dépendances Python sont listées dans le fichier requirements.txt. Pour créer l’environnement Python pyenv ainsi que son kernel, il faut suivre les étapes ci-dessous.

- python -m venv pyenv  (ou python3 -m venv pyenv)
- source pyenv/bin/activate
- pip install -r requirements.txt
- python -m ipykernel install --user --name=pyenv --display-name "Local Python (pyenv)"
- deactivate

Il sera ensuite possible de compiler le projet (voir la section
suivante).

## Comment compiler le rapport?

Sans Rstudio, sur un terminal, exécutez la ligne suivante dans l'environnement.

```
quarto render our_report.qmd
# Output : _outdir/our_report.html
```
Si l'exécution se passe bien, un fichier html apparaît dans _outdir/our_report.html.

## Structure du projet

```
.
├── DATA/                          
│   ├── Adieu.txt                  # Balzac (dh-trier format)
│   ├── ...
│   ├── hugo_ndp.txt               # Hugo (Gutenberg format)
│   ├── flaubert_madame_bovary.txt # Flaubert
│   ├── stendhal_*.txt             # Stendhal
│   ├── sand_*.txt                 # Sand
│   └── Zola_*.txt                 # Zola
├── _outdir/                       # Sortie Quarto + Parquet
├── _extensions/
├── _metadata.yml
├── _quarto.yml
├── our_report.qmd                 # Rapport principal (6 parties)
├── requirements.txt
└── README.md
```

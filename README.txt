# ÉCHOS — jeu d'horreur mobile

Un petit jeu narratif d'horreur en français, pensé pour téléphone : choix, plusieurs fins, sauvegarde locale et ambiance sonore optionnelle.

## Fichiers
- `app.py` : serveur Python/Flask
- `templates/index.html` : interface mobile et histoire
- `requirements.txt` : dépendance Flask

## Tester sur ton PC
1. Installe Python si nécessaire.
2. Dans le dossier du jeu, ouvre un terminal.
3. Lance `python -m pip install -r requirements.txt`
4. Lance `python app.py`
5. Sur ton PC, ouvre `http://127.0.0.1:5000`

## Pour l'envoyer à ton pote sur son téléphone
Le plus simple est de le mettre en ligne pour obtenir un lien public. Tu peux déployer ce dossier sur un hébergeur compatible Python/Flask, par exemple Render :
- crée un compte sur Render et un nouveau service Web depuis un dépôt Git ;
- ajoute les fichiers du dossier dans un dépôt GitHub ;
- commande de build : `pip install -r requirements.txt`
- commande de démarrage : `gunicorn app:app`
- ajoute `gunicorn` à `requirements.txt` si l'hébergeur le demande (ou remplace le contenu par `Flask>=3.0,<4.0` puis `gunicorn>=22.0`).
Une fois déployé, partage simplement l'URL HTTPS avec ton ami. Le serveur doit rester en ligne pour que le lien fonctionne.

Note : envoyer seulement `app.py` ne suffit pas : il faut aussi le dossier `templates`.

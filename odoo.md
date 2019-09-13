## Lancer premier odoo

* **Cloner repo akkretion**:

  ```
  $ https://github.com/akretion/docky-odoo-template.git
  ```

Le fichier odoo/spec.yaml liste les dépendances nécessaires au projet sous un format lisible par la librairie ak.

* **Lancer génération pour fichier git-aggregator dans le dossier odoo**:

  ```
  $ ak build
  ```

Cela génère le fichier repo.yaml

Dossier src/addons est la liste des modules open source de base de l'éditeur odoo

Dossier external-src comporte tout le code source extérieur aux addons

Les sous-dossiers sont des dossiers de la communauté odoo

Initialiser le dossier par docky init

Lancement de l'image docker avec docky

  ```
  $ docky run
  ```
Les variables d'environnement pour le lancement du container se trouvent dans le fichier docker-compose.yml

Docky ouvre autotiquement le terminal de la machine virtuelle lancée.

Taper la commande pour lancer odoo

  ```
  $ odoo
  ```

Le dossier songs, et le fichier migration.yml sert à gérer les scripts de migration

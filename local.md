## Nouvelles

* **Savoir quel shell est utilisé**:

  ```
  $ echo $SHELL
  ```
* **Ajouter un alias**:

  Recupérer le lien du dossier racine
  ```
  $ pwd
  ```
  Se rendre dans ce dossier et ouvrir le fichier .zshrc (Ctrl +H pour afficher les fichiers cachés dans Linux)
  Repérer dans quel fichier sont chargés les alias
  Ouvrir le fichier correspondant (souvent .aliases)

* **Avoir la liste de tous les binaires dans un projet rails**:

  ```
  $ ll bin
  ```

  La liste se trouve dans le dossier /bin de l'app.

* **Ecoutez les paths ?!?**:

  ```
  $ echo $PATH
  ```

  Signifie l'ordre de recherche des binaires ?!?

* **Liens symboliques**:

  Pour avoir les commandes possibles :
  ```
  $ man ln
  ```

  Paramétrer le lien avec la cible et le nom, par exemple :
  ```
  $ ln -s /home/thibault/code/thibault173/dividi dividi
  ```

  Accéder au dossier dividi local en tapant depuis n'importe ou :
  ```
  $ cd dividi
  ```

  Avoir la liste de tous les liens symboliques :
  ```
  $ ls -l
  ```

* **Redirection des ports**:

  ```
  $ subl /etc/hosts
  ```

  La modification de ce fichier entraîne une redirection des adresses en local.

* **Wepback**:

  ```
  $ webpack-dev-server
  ```

  Permet de lancer webpack en local, pour éviter d'avoir à recharger la page web à chaque fois, cela ouvre un socket en local ?!?


## Maîtrisées

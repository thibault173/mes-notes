## Nouvelles

* **Voir les n derniers commits**:
  ```
  $ git log -n
  ```

* **Enregister les fichiers ajoutés sur le dernier commit**:
  ```
  $ git commit --amend
  ```
  Attention, en cas de branche déjà poussée sur github, la synchronisation doit être forcée :
  ```
  $ git push -f origin mabranche
  ```

* **Voir les branches actives**:

  ```
  $ git branch
  ```
  Pour voir toutes les branches avec leur dernier commit :
    ```
  $ git branch -v
  ```

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

* **Remettre à jour un repo par rapport à un autre**:

  ```
  git reset --soft origin/master
  ```
  Dans ce cas, a remis à jour le repos local (master), en prenant en référence le repo en ligne (origin)
  <br/>Existe aussi avec la versoin --hard

## Maîtrisées

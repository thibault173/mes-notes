## Nouvelles

* **Voir les n derniers commits**:
  ```
  $ git log -n
  ```

* **Voir les branches actives**:

  ```
  $ git branch
  ```
  Pour voir toutes les branches avec leur dernier commit :
    ```
  $ git branch -v
  ```

* **Ecouter les logs**:

```
$ tail -f log/development.log | grep fragment
```

* **Squasher en local**:

  ```
  $ git merge --squash branch-name && git commit
  ```

* **Supprimer branche sur repo distant**:

  ```
  $ git push origin --delete branch-name
  ```
  Cela ne cloture pas nécessairement la PR associée



## Maîtrisées

* **Enregister les fichiers ajoutés sur le dernier commit**:
  ```
  $ git commit --amend
  ```
  Attention, en cas de branche déjà poussée sur github, la synchronisation doit être forcée :
  ```
  $ git push -f origin mabranche
  ```

* **Remettre à jour un repo par rapport à un autre**:

  ```
  git reset --soft origin/master
  ```
  Dans ce cas, a remis à jour le repos local (master), en prenant en référence le repo en ligne (origin)
  <br/>Existe aussi avec la versoin --hard

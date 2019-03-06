## Heroku commandes

* **Avoir les logs d'une app**:

  ```
  $ heroku logs -a app
  ```
* **Accéder à la console d'une app**:

  ```
  $ heroku run rails c -a dividi-staging
  ```

  Ou en utilisant le remote :

  ```
  $ heroku run rails c -r staging
  ```

* **Problème de variable d'environnement HOST** *
  La nouvelle version de Puma utilise une variable d'environnement HOST, la définition dans Heroku de Host supprime celle de Puma

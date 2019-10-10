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

* **Dumper une base**:

  ```
  $ pg_dump _impactasso_development -c | PGPASSWORD="1cca0d840c8f4337c1e0d6276cc56798d038d1b483f8901ffdad51bfd7439b87" psql -h ec2-52-50-171-4.eu-west-1.compute.amazonaws.com -d d1v560ph6fgugr -U evclpituzivgvf
  ```


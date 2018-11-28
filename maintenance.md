## Maintenance des gems

* **Règle primordiale**:

  Utiliser $ bundle update avec parcimonie !

* **Versionning des gems**:

  premier chiffre : version majeure = gros changements de structure
  deuxième chiffre : version mineure = changements mineurs, compatibles avec la version de base
  troisième chiffre : patchs, plutôt liés à la sécurité ou petits bugs

* **Indiquer pour chaque gem la version utilisée**:

  gem 'lambda', '~>2.2'
  signifie que lorsque la commande bundle update est exécutée, la gem lambda va aller chercher les patchs (versions 2.2.x)

* **Exécuter un bundle update**:

  Attention : si la version de la gem n'est pas indiquée, cela va aller chercher la dernière version à jour.

* **Exécuter un bundle outdated**:

  Voir à la main pour chaque gem et effectuer la mise à jour.

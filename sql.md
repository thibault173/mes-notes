## Requêtes SQL avec Active Record

preload()

  @posts = Post.order(created_at: :desc).preload(:author)

  Effectue 2 requêtes en bdd.

eager_load()

  @posts = Post.order("authors.name").eager_load(:author)

  Effectue 1 seule requête en bdd, avec un LEFT INNER JOIN

includes()

  En fonction de la demande, choisit la meilleure solution entre preload() et eager_laod().

joins()

  Permet de sélectionner uniquement les données voulues en y associant un select(), la requete SQL est INNER JOIN et non LEFT OUTER JOIN.
  Aller sur joins() uniquement lorsque les données sont vraiment importantes et que le besoin de performance est nécessaire.

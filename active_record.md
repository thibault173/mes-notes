- includes permet de mettre en cache (pour la performance)
- 2 règles sur le belongs_to :author
    - la clé, s'accoie à author_id
    - la classe, class_name: 'User'

- t:references :author signifie 2 choses :
    - cherche author_id
    - si foreign_key, va chercher la table authors, il faut mettre foreign_key { to_table: users }

- has many :posts a 2 conventions (foreign key & class name)
    - foreign_key: author_id
    - class_name


- includes déclenche un preload ou un eager load en fonction des besoins
- reference force le includes à faire un eager load

- Post.include(:author).where(users: {id: 3})

- To avoid N+1 queries : gem bullet ou gem rack mini profiler

- Sous requête SQL
  SELECT * FROM posts
  WHERE author_id IN (SELECT id FROM users)

- keyword EXPLAIN SELECT ... permet de voir la construction de la requête

Exemple HAVING forcément lié à une fonction d'agragation (de type MAX, MIN, SUM, COUNT)

SELECT users.id, SUM(posts.views)
FROM users
JOIN posts ON post.author_id = users.id
GROUP_BY users.id
HAVING COUNT(posts.id) > 2

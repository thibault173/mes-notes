## Nouvelles

* **Envoyer une requête AJAX**:
  ```
  fetch("https://places-dsn.algolia.net/1/places/query", {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({ query: event.currentTarget.value })
  })
  ```


## Maîtrisées

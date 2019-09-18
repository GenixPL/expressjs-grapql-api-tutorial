## Code from tutorial ([youtube video](https://www.youtube.com/watch?v=ZQL7tL2S0oQ))


### Example queries/mutations:
(we don't have to type `query`, because it's a default one)
```
query {
  books {
    id
    name
    authorId
    author {
      name
    }
  }
}

{
  authors {
    id
    name
    books {
      name
    }
  }
}

{
  book(id: 1) {
    name
    author {
      name
    }
  }
}

{
  author(id: 3) {
    name
    books {
      id
      name
    }
  }
}

mutation {
  removeBook(id: 11) {
    author {
      books {
        id
        name
      }
    }
  }
}

mutation {
  addBook(name: "Some Book", authorId: 3) {
    author {
      name
      books {
        id
        name
      }
    }
  }
}
```

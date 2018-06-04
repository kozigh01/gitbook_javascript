---
description: Writing plain Javascript without frameworks / libraries
---

# Vanilla Javascript

### Fetch

#### Resources

* MDN: [Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

### Examples

#### Basic Fetch

```text
fetch('https://jsonplaceholder.typicode.com/posts/1')  .then(function(response) {    return response.json();  })  .then(function(myJson) {    console.log(myJson);  });
```


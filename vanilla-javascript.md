---
description: Writing plain Javascript without frameworks / libraries
---

# Vanilla Javascript

## Select Element(s)

* MDN: [querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) \| [querySelectorAll](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll)
* Returns the first matched element reference, using a CSS selector
* Example
    ```javascript
      const location = document.querySelector('#location').value;
      document.querySelector('#location').value = 'home';
      
      // remove a class from every div element with a  parent that has a class of 'options'
      document.querySelectorAll('.options div').forEach(option => { option.classList.remove('selected') });
    ```
## Events
* MDN: [addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
* Example
    ```javascript
    document.querySelector('li').addEventListener('click', (event) => {
      // what should happen
      if(event !== undefined && event.target.classList.contains('selected') { // event.target is the element that triggered event
        // do something
      }
      e.preventDefault(); // if you want to prevent the default action, for example on a button
      var x = event.screenX; // for example, get the x value of a click
      var y = event.screenY; // for example, get the y value of a click
    }, false);
    ```
## Fetch

* MDN: [Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
* Basic Fetch

  ```javascript
    fetch('https://jsonplaceholder.typicode.com/posts/1')
      .then(function(response) {    
        return response.json();  
       })
      .then(function(myJson) {    
        console.log(myJson);
      });
  ```


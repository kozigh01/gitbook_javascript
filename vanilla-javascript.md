---
description: Writing plain Javascript without frameworks / libraries
---

# Vanilla Javascript

## Resources

* [x] Learning App Building with Vanilla JavaScript: [Course](https://www.linkedin.com/learning/learning-app-building-with-vanilla-javascript/create-elements-with-vanilla-javascript)
* [ ] Javascript30 \(30 projects/30 days\): [site](https://javascript30.com/)

## Notes

### Select Element\(s\)

* MDN: [querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) \| [querySelectorAll](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll)
* Returns the first matched element reference, using a CSS selector
* Example

  ```javascript
      const location = document.querySelector('#location').value;
      document.querySelector('#location').value = 'home';

      // remove a class from every div element with a  parent that has a class of 'options'
      document.querySelectorAll('.options div').forEach(option => { option.classList.remove('selected') });
  ```

### Events

* MDN: [addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
* Example

  ```javascript
    document.querySelector('li').addEventListener('click', (event) => {
      // what should happen
      if(event !== undefined && !event.target.classList.contains('selected') { // event.target is the element that triggered event
        // do something to clicked elements that do not have a class 'selected'
        let id = event.target.id;
        event.target.classList.add('selected');
      }
      e.preventDefault(); // if you want to prevent the default action, for example on a button
      var x = event.screenX; // for example, get the x value of a click
      var y = event.screenY; // for example, get the y value of a click
    }, false);
  ```

### Fetch

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

### DOM Manipulation

* Functions / Properties:
  * createElement\(\) method
  * setAttribute\(\) method
  * textContent\(\) property
  * appendChild\(\) method
* Example:

  ```javascript
  let container = document.createElement('div');
  let cityPara = document.createElement('p');
  cityPara.setAttribute('class', 'city');
  cityPara.textContent = state.city;
  let conditionPara = document.createElement('p');
  conditionPara.textContent = state.tempC + '\u00b0 C / ' + state.tempF + '\u00b0 F';
  let iconImage = document.createElement('img');
  iconImage.setAttribute('src', state.iconUrl);
  iconImage.setAttribute('alt', state.description);

  conditionPara.appendChild(iconImage);
  container.appendChild(cityPara);  // top displayed <p>
  container.appendChild(conditionPara); // second displayed <p>
  let parent = document.querySelector('.parent');
  if (document.querySelector('.condition div')) {
    parent.replaceChild(container, document.querySelector('.condition div'));
  } else {
    parent.appendChild(container);
  }

  ...
  let activitiesContainer = document.createElement('div');
  let list = document.createElement('ul');
  let activities = state.activities.map((activity, index) => {
    let item = document.createElement('li');
    item.textContent = activity;
    item.setAttribute('key', index);
    list.appendChild(item);
  });
  activitiesContainer.appendChild(list);
  parent = document.querySelector('.parent');
  if (document.querySelector('.activities div')) {
    parent.replaceChild(activitiesContainer, document.querySelector('.activities div'));
  } else {
    parent.appendChild(activitiesContainer);
  }
  ```

  **CSS Transition Property**

* CSS keyframes

  ```css
  @keyframes show-menu {
    0% {
      left: -150px;
    }
    50% {
      left: -50px;
    }
    100% {
      left: 100px;
    }
  }
  ```

* canvas element
  * setInterval\(\) function
  * setTimeout\(\) function
  * requestAnimationFrame\(\) method
* Example

  ```css
  .close {
    height: auto;
    max-height: 0;
    overflow-y: hidden;
    transition: max-height 0.3s ease-out;
  }
  .open {
    max-height: 250px;
  }
  ```

  ```javascript
    document.querySelector('.target').classList.add('open');
  ```

  **Babel**

* VS Code: [Babel REPL](https://marketplace.visualstudio.com/items?itemName=t-sauer.vscode-babel-repl)
* Online: [Babel.io](http://babeljs.io/repl)


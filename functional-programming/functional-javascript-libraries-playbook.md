# Functional JavaScript Libraries Playbook

## Course Info

### Course

* Functional JavaScript Libraries Playbook: [course](https://app.pluralsight.com/library/courses/functional-javascript-libraries-playbook/table-of-contents)
* Author: [David Mann](https://app.pluralsight.com/profile/author/david-mann)

### Libraries

* Immutable.js: [site ](https://facebook.github.io/immutable-js/)
* Ramda: [site](https://ramdajs.com/)
* Folktale: [site](http://folktale.origamitower.com/docs/v2.0.0/) \| [github](https://github.com/folktale)
* Sanctuary: [github](https://github.com/sanctuary-js/sanctuary)
* Monet: [site](https://monet.github.io/monet.js/) \| [github](https://github.com/monet/monet.js/)
* FKit: [github](https://github.com/nullobject/fkit)

## Course Notes

### Functional Javascript 101

#### Pure Functions

A function that does not have any external dependencies, and has following aspects: 

* No external dependencies - all needed info is passed into function via parameters
* Has no side effects on outer scope - can be replaced with resulting value \(referential integrity\)
* Results in the same output for same set of input input values every time called

Pure functions: 

* separate calculation and mutation \(side effects\)
* always returns something - not undefined or null \(if doesn't, why call at all?\)
* are highly testable

### Composition

Functions as building blocks.  Or, creating a process / machine from functions.




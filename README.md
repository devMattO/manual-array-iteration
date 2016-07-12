# Manual Array Iteration

## Goal
A module which takes an `array` and **returns a function** which you can used to manually iterate through the array and return each value found until the end of the array's contents.

*Example:*
```javascript
  // load module
  var iteratorModule = require('./iteratorModule.js');

  // initialize the module with an array. the return value is a function so we need to store it to a variable.
  var step = iteratorModule.init([9, 66, 'Oprah Windfury', [5, 4, 6]];

  // from here on each time we invoke `step` it returns the next value starting at first index.
  step(); // returns 9
  step(); // returns 66
  step(); // returns 'Oprah Windfury'
  step(); // returns [5, 4, 6]
  step(); // returns 'Error: end of array'
  step(); // returns 'Error: end of array'
```

## Requirements
- **Git**
  - Initialize your projet to use be a **Git repository**
  - Commit often
- **Tests** (*optional: workshop as a class to build test cases*)
  - Initialize your project to use **npm**. You should have a `package.json` file in your project when done.
- **A Module**
  - should have a method named `init` which accepts an `array` as an argument
    - This method returns a `function` used to step through the array and also returns the value found at the current index of the `array`.

## Stretch Goals
Can you find a way for `step` to accept an argument which allows you to jump ahead `n` amount of times?

*Same example from above but with the stretch goal in mind:*
```javascript
  var iteratorModule = require('./iteratorModule.js');

  var step = iteratorModule.init([9, 66, 'Oprah Windfury', [5, 4, 6]];

  step(); // returns 9
  step(2); // returns 'Oprah Windfury'. 66 gets skipped!
  step(); // returns [5, 4, 6] if invoking the 'step' function normally
```

## Resources
- [Dev League Module Pattern slide deck](http://slides.com/jasonsewell/object-literals-and-ze-module-pattern)
- [Dev League Closures slide deck](http://slides.com/theremix/closures#/)
- [Dev League Currying slide deck](http://slides.com/theremix/currying)

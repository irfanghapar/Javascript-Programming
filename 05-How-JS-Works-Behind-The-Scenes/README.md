# JavaScript Behind the Scenes

Welcome to the JavaScript Behind the Scenes tutorial! 🚀 In this comprehensive guide, we'll dive deep into the inner workings of JavaScript, exploring various concepts and features through practical examples. By the end, you'll have a solid understanding of scoping, hoisting, the `this` keyword, functions, objects, and more!

## Table of Contents
1. [Scoping in Practice](#scoping-in-practice)
2. [Hoisting and TDZ in Practice](#hoisting-and-tdz-in-practice)
3. [The `this` Keyword in Practice](#the-this-keyword-in-practice)
4. [Regular Functions vs. Arrow Functions](#regular-functions-vs-arrow-functions)
5. [Objects vs. Primitives](#objects-vs-primitives)
6. [Primitives vs. Objects in Practice](#primitives-vs-objects-in-practice)

---

## Scoping in Practice
Scoping is crucial in JavaScript as it defines the visibility and accessibility of variables. Let's explore scoping through an example.

```javascript
'use strict';

function calcAge(birthYear) {
  // Function scope
  const age = 2037 - birthYear;

  function printAge() {
    // Function scope
    console.log(age);
  }

  printAge();
}

calcAge(1991); // Output: 46
```

In this snippet, `age` is scoped within the `calcAge` function and can't be accessed outside it.

---

## Hoisting and TDZ in Practice
Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their containing scope during compilation. Let's explore this concept.

```javascript
'use strict';

console.log(me); // Output: undefined

var me = 'Irfan'; // Variable declaration is hoisted

console.log(addDecl(2, 3)); // Output: 5

function addDecl(a, b) {
  // Function declaration is hoisted
  return a + b;
}
```

In this example, both variable and function declarations are hoisted, allowing them to be used before their actual declarations.

---

## The `this` Keyword in Practice
Understanding the `this` keyword is fundamental in JavaScript as it refers to the object it belongs to. Let's explore its usage.

```javascript
'use strict';

console.log(this); // Output: Window object

const calcAge = function (birthYear) {
  console.log(this);
};

calcAge(1991); // Output: Window object
```

In this snippet, `this` refers to the global object because the function is not called as a method of an object.

---

## Regular Functions vs. Arrow Functions
Regular functions and arrow functions behave differently, especially concerning the `this` keyword. Let's compare them.

```javascript
'use strict';

const Irfan = {
  firstName: 'Irfan',
  year: 1991,
  calcAge: function () {
    const isMillenial = () => {
      console.log(this.year >= 1981 && this.year <= 1996);
    };
    isMillenial();
  },
};

Irfan.calcAge(); // Output: true
```

Arrow functions don't have their own `this`, they inherit it from the parent scope. In this example, `this` inside the arrow function still refers to the `Irfan` object.

---

## Objects vs. Primitives
Understanding the differences between objects and primitives is crucial in JavaScript. Let's explore their behavior.

```javascript
'use strict';

let age = 30;
let oldAge = age;
age = 31;
console.log(age, oldAge); // Output: 31, 30

const me = {
  name: 'Irfan',
  age: 30,
};
const friend = me;
friend.age = 27;
console.log(me, friend);
```

Primitives are copied by value, whereas objects are copied by reference. In this example, changing the `age` property of the `friend` object also affects the `me` object.

---

## Primitives vs. Objects in Practice
Let's delve deeper into the behavior of primitives and objects with more practical examples.

```javascript
'use strict';

let lastName = 'Williams';
let oldLastName = lastName;
lastName = 'Davis';
console.log(lastName, oldLastName); // Output: Davis, Williams

const jessica = {
  firstName: 'Jessica',
  lastName: 'Williams',
  age: 27,
};
const marriedJessica = jessica;
marriedJessica.lastName = 'Davis';
console.log(jessica, marriedJessica);
```

In this snippet, changing the `lastName` property of the `marriedJessica` object also affects the `jessica` object due to object referencing.

---

Congratulations! 🎉 You've completed the JavaScript Behind the Scenes tutorial. We've covered essential concepts and provided practical examples to solidify your understanding. Happy coding! 😊
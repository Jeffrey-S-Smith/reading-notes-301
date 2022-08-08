# Reading Overview

## Readings and Resources: ES6 Classes

## Objects and Inheritance

JavaScript objects use prototype-based inheritance. Its design is logically similar (but different in implementation) from class inheritance in strictly Object Oriented Programming languages like Java and C#.

It can be loosely described by saying that when methods or properties are attached to object’s prototype they become available for use on that object and its descendants, but not directly attached to them.

When you use class and extends keywords internally JavaScript will still use prototype-based inheritance. It just simplifies the syntax (this is often called “Syntactic Sugar”). While classes are easier to use, it’s still very important to understand how prototype-based inheritance works. It’s still at the core of the language design.

### Prototypal Inheritance

``` JavaScript

function Animal(name) {
  this.name = name;
}
Animal.prototype.walk = function() {}

function Bird(name) {
  // I can do all the things animals can do!
  Animal.call(this, name);
}
// Unlike other animals, birds can fly
Bird.prototype.fly = function() {}

// Make a new bird ..
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();
## Reading Sources
```

### ES6 Classes

The same thing with classes (much cleaner!)

* function() becomes class {}
* call() becomes extends
* Classes are standalone, self-contained object (instance) factories
  * Ultimately, they result in a prototype
  * But for the developer, they are many orders of magnitude easier to comprehend and work with

``` JavaScript
class Animal {
  constructor(name) {
    this.name  = name;
  }

  walk() {}
}

// Thanks to 'extends', all birds can now do all things animals can
class Bird extends Animal {
  // Birds can walk, becuase they're animals also do their own thing.
  fly() {}
}

// Make one (the same was as before, but wasn't the class creation much easier?)
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();
```

## Watch the Shred Talk: ES6 Classes

[Watch the Shred Talk: ES6 Classes. by code fellows](https://www.youtube.com/watch?v=9Yc5J3Ap9-4),

## Review the Demo Code

[Review the Demo Code. by code fellows](https://codefellows.github.io/code-301-guide/curriculum/prework/classes/DEMO.html),

## ES6 Classes - Demo Code

### Constructor Functions & Prototypes

``` JavaScript

const Animal = function(name, legs) {
  this.name = name;
  this.legs = legs;
  this.eat = function() {
    this.isEating = true;
  }
}
Animal.prototype.walk = function() {
  this.isWalking = true;
}

const Dog = function(name, legs) {
  Animal.call(this, name, legs);
}
Dog.prototype = Object.create(Animal.prototype);

let puppy = new Dog('blake', 4);
puppy.walk();
puppy.eat();
console.log(puppy);
console.log(puppy instanceof Animal);
console.log(puppy instanceof Dog);

```

### ES6 Classes

``` javaScript

class Animal {

  constructor(name, legs) {
    this.name = name;
    this.legs = legs;
  }

  walk() {
    this.isWalking = true;
  }

  eat() {
    this.isEating = true;
  }

}

class Dog extends Animal {

  constructor(name, legs, furType) {
    super(name,legs);
    this.furType = furType;
  }

  speak() {
    console.log('Wooof!');
  }

}

let rosie = new Dog('rosie', 4, 'Short Hair');
rosie.walk();
rosie.eat();
console.log(rosie);
rosie.speak();

```

## Reading Sources

[Video: what the heck is the event loop anyway. by Philip Roberts](https://www.youtube.com/watch?v=8aGhZQkoFbQ),
[MDN inheritance. MDN web docs_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain),
[MDN this. MDN web docs_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this),
[MDN class. MDN web docs_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes),

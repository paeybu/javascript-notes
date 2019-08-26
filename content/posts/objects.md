---
title: "Objects"
date: 2019-08-27T04:45:49+07:00
draft: true
---

2 ways to create an empty object
```javascript
let object1 = {}
let object1 = new Object()
```
`{}` these curly braces are called *object literal*

We can give an object properties
```javascript
let car = {
  make: 'Toyota',
  model: 'Corolla'
}
```
The last property can have trailing comma to make adding more properties to the object easier

```javascript
let car = {
  make: 'Toyota',
  model: 'Corolla',
}
```
`make` and `model` are called keys  
and Toyota and Corolla are values

Object stores key-value pair

### Add, read, remove
Add
```javascript
car.horsepower = 124
```

Read
```javascript
car.horsepower //124
```

Remove
```javascript
delete user.age
```

### Multiword property names
Multiword property names must be quoted
```javascript
let animal = {
  name: "Abukaba",
  "can fly": true
}
```

### Square brackets
To access multiword property names or any other property, we can use square bracket notation
```javascript
animal["can fly"] //true
animal["name"] //"Abukaba"
```

### Using variable as property key
```javascript
let key = "isHungry"

let person = {
  isHungry: true
}

person[key] //true
person.key //true
```

### Computed properties

We can use a variable as a property key by surrounding the key with []

```javascript
let fruit = 'apple'
let cart = {
  [fruit]: 5
}

cart // {apple: 5}
```

### Property value shorthand
Sometimes we want to use a variable as a property key and its value as the property value

```javascript
let drink = 'Choco Milk'
let order = {
  drink: drink
}
```

can be written as

```javascript
let drink = 'Choco Milk'
let order = {
  drink
}
```

### Existence check
You can access a property even if it doesn't exist
```javascript
let user = {}
user.name //undefined
```

We can check for a property name to see if it exists or not with `in`
```javascript
let user = {}
'name' in user //false
```

### Loop over keys in an object
We can use for...in to loop over all keys of an object  
Syntax:
```javascript
for (key in object) {

}
```

### Objects reference
Objects are stored as a reference
```javascript
let a = {}
b = a
b === a //true
```

### Const object
We can change the property of a const object
```javascript
const user = {
  name: 'Timothy'
}

user.name = 'Hugo'
```


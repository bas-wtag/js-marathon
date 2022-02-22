## Note from [aaf-wtag](https://github.com/aaf-wtag)

### JS Objects

- JavaScript is designed on a simple object-based paradigm. An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method. JavaScript object is a non-primitive data-type that allows you to store multiple collections of data.

- JavaScript objects are a bit different as JavaScript is template based not class based.. You do not need to create classes in order to create objects. In JavaScript, an object is a standalone entity, with `properties` and `type`.

- There are 4 ways to create objects.:
 - By `object literal`:
   ```
   const objectName = {
      key1: value1,
      key2: value2
   }
   ```

 - By creating `instance` of Object:
   `const objectName=new Object();`
 -  By using an Object `constructor`: Here, you need to create function with arguments. Each argument value can be assigned in the current object by using `this` keyword. The `this` keyword refers to the current object.
   ```
   function Car(make, model, year) {
     this.make = make;
     this.model = model;
     this.year = year;
  }
  ```
 - By using `Object.create` method: This method can be very useful, because it allows you to choose the prototype object for the object you want to create, without having to define a constructor function.
   ```
   // Animal properties and method encapsulation
   const Animal = {
     type: 'Invertebrates', // Default value of properties
     displayType: function() {  // Method which will display type of Animal
       console.log(this.type);
     }
   };

   // Create new animal type called animal1
   const animal1 = Object.create(Animal);
   animal1.displayType(); // Output: Invertebrates

   // Create new animal type called fish
   const fish = Object.create(Animal);
   fish.type = 'Fishes';
   fish.displayType(); // Output: Fishes
   ```

- You can access the value of a property by using its key in the following ways:
 - Using dot Notation: `objectName.key`
 - Using bracket Notation: `objectName["propertyName"]` or `objectName[propertyNameAsVariable]`. An object property name can be any valid JavaScript string, or anything that can be converted to a string, including the empty string. However, any property name that is not a valid JavaScript identifier (for example, a property name that has a space or a hyphen, or that starts with a number) can only be accessed using the square bracket notation. This notation is also very useful when property names are to be dynamically determined (when the property name is not determined until runtime). All keys in the square bracket notation are converted to string unless they're Symbols, since JavaScript object property names (keys) can only be strings or Symbols

- In nested objects, an object can contain another object which can recursively contain objects.

- There are three native ways to list/traverse object properties:
 - `for...in loops`: This method traverses all enumerable properties of an object and its prototype chain.
 - `Object.keys(o)`: This method returns an array with all the own (not in the prototype chain) enumerable properties' names ("keys") of an object o.
 - `Object.getOwnPropertyNames(o)`. This method returns an array containing all own properties' names (enumerable or not) of an object o.

- Methods are defined the way normal functions are defined, except that they have to be assigned as the property of an object.

```
objectName.methodName = functionName;

const myObj = {
  myMethod: function(params) {
    // ...do something
  },

  // this works too!
  myOtherMethod(params) {
    // ...do something else
  }
};
```
where objectName is an existing object, methodName is the name you are assigning to the method, and functionName is the name of the function.


- You can remove a non-inherited property by using the delete operator. 

```
// Creates a new object, myobj, with two properties, a and b.
const myobj = new Object();
myobj.a = 5;
myobj.b = 12;

// Removes the a property, leaving myobj with only the b property.
delete myobj.a;
console.log ('a' in myobj); // output: "false"
```

- In JavaScript, objects are a reference type. Two distinct objects are never equal, even if they have the same properties. Only comparing the same object reference with itself yields true.

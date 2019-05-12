# Object Literal

### Object

<hr>

In JavaScript, all values except primitive types are objects.

A primitive type represents only one value, but an object / reference type is a complex data structure that consists of several types of values (primitive type values or other objects) as a unit. The value of the primitive type is an immutable value, but the value of the object type is a mutable value.

An object is a set of properties consisting of a key and a value. You can use any value that is available in JavaScript as the value of the property. Function in JavaScript is first-class objects, so they can be treated as values. Therefore, you can use a function as a property value. If the property value is a function, it is called a method to distinguish it from a normal function.

### Way to create an object

<hr>

-   Object literal

-   Object constructor function

-   Constructor function

-   Object.create method

-   Class (ES6)

    -   Class-based object-oriented languages such as C ++ and Java create objects by defining classes in advance and creating instances by calling the constructor with the new operator at the required time.

    -   Instance

        -   An instance is an substance created by a class and stored in memory. In object-oriented programming, objects are concepts that include classes and instances. The class function as a template for creating instances. An instance is a term that focuses on the fact that an object is actually stored in memory.

#### Create an object whit object literal

<hr>

```javascript
const person = { name: "Hyun", gender: "male" };
```

Here, `{ name: "Hyun", gender: "male" }` is an object literal, and the object literal is assigned to the variable person.

`name: "Hyun"` and `gender: "male"` are properties of object, `name` and `gender` are property keys ,and `Hyun` and `male` are property values.

<hr>

Quotation marks must be used for names that do not follow the identifier naming convention.

```javascript
const person = {
    last_name: "Hyun",
    "first-name": "Woochul", // <-- Quotation marks
    gender: "male"
};
```

<hr>

If you use a value other than a string or symbol value in a property key, it becomes a string through implicit type conversion.

```javascript
const foo = {
    0: 3,
    1: 4,
    2: 5
};

for (const key in foo) {
    console.log(key);
    console.log(typeof key);
}

// 0
// string
// 1
// string
// 2
// string
```

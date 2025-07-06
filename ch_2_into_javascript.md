## Values & Types
- string
    ```js
    a = "hello world";
    typeof a; // "string"
    ```
- number
    ```js
    a = 42;
    typeof a; // "number"
    ```
- boolean
    ```js
    a = true;
    typeof a; // "boolean"
    ```
- null
    ```js
    a = null;
    typeof a; // "object" [instead of null]
    ```
- undefined
    ```js
    var a;
    typeof a; // "undefined"
    a = undefined;
    typeof a;
    ```
- object
    ```js
    a = { b: "c" };
    typeof a; // "object" 
- symbol (new to ES6)
  
- Only values have types in JS

## Objects
- compound values where properties hold their own values

    ```js
    var obj = {
    a: "hello world",
    b: 42,
    c: true
    };
    obj.a; || obj["a"]; // "hello world"
    obj.b; || obj["b"];// 42
    obj.c; || obj["c"];// true
    ```
- Bracket notation lets you access object properties using strings or variables, useful for keys with special characters.
  

## Arrays
- An array is an object that stores values at numeric indices instead of named keys.


    ```js 
    var arr = [
    "hello world",
    42,
    true
    ];
    arr[0]; // "hello world"
    arr[1]; // 42
    arr[2]; // true
    arr.length; // 3
    typeof arr; // "object" {arrays are special objects}
    ```
- use arrays for numerically positioned values
- use objects for named properties

## Functions
- object subtype

    ```js
    function foo() {
    return 42;
    }
    foo.bar = "hello world";
    typeof foo; // "function"
    typeof foo(); // "number"
    typeof foo.bar; // "string"
    ```

## Built-In Type Methods
- built-in types and subtypes have properties and methods
  
    ```js
    var a = "hello world";
    var b = 3.14159;
    a.length; // 11
    a.toUpperCase(); // "HELLO WORLD"
    b.toFixed(4); // "3.1416"
    ```
## Code
- Source Code (program): set of special instructions  
- computer language: rules for valid format (syntax)

## Statements
- statement: group of words
- variable: symbolic container holding a value
- operators: performs action with values and variables

## Expressions
- reference to a value or set of variable

```js 
a = b*2;
```
- 2 = literal value expression
- b = variable expression
- b*2 = arithmetic expression
- a = b*2 assignment expression

- call expression 
    ```js
    alert("Hello World!");
    ```

## Executing a program
- translating programming code into machine code
- translating top to bottom => Interpreting
- translating ahead of time => compiling

## Output
- function call prints output when logged
-   
  ```js
  console.log("Hello World!")
  ```

## Input
- information from user
- 
  ```js
  let age = prompt("Enter your age");
  console.log(age);
  ```

## Operators
 
```js
let a = 2;
let b (target variables) = a + 1 (source value);
```

- Assignment [ = ]
- Math [+ , - , * , /]
- Compound [+= , -= , /=]
- Increment/Decrement [-- , ++]
- Object Property Access [obj["a"]]
- Equality [('==' loose equals), ('==='strict equals)]
- Comparison [<, > , <=, >=]
- Logical [ && , || ]

## Values & Types
- primitive types (built-in)

## Coercing Between Types
- Explicit Coercion 
```js 
let a = "42";
let b = Number(a);
```
- Implicit Coercion
```js 
console.log("99.99" == 99.99); // true
// JS will convert left hand side to it's number equivalent and then compare
```

## Code Comments
- Good name for variable and function
- It should explain why (optionally how)

## Variables
- type of value
  - Static Typing (type enforcement) (hold specific type of value - string, number)
  - Dynamic Typing (weak typing)

<u>Purpose of Varible</u>
- Managing Program State 
- State is tracking the changes to values as your program runs
- Constants: Not to change throughout the program change 
  
## Blocks
- series of statements grouped together
- control statements
  - If...Else
  - Switch Case
  - Loop

## Conditionals
- they control the flow of the program
- "falsy": when coerced to a boolean become false [0 & ""]
- "truthy": any value that is not falsy
  
## Loops
- repeating a set of actions only while the condition holds
- iteration: every repeatition of loop block
- break statement: to stop the loop

## Functions
- Define a code block once and use it over and over again
- break a program into reusable pieces
- parameters: placeholders or variables listed in the function definition
- agruments: actual values that we pass to function
```js
function sum(a,b){ //Here, a and b are parameters
  return a+b;
}
const result = sum(4,5);
// Here, 4 and 5 are arguments
console.log(result); // output = 9
```

## Scope
- scope/lexical scope: a collection of variables as well as the rules for how those variables are accessed based on name

```js
function outer(){
  let a = 1;
  function inner(){
    let b = 2;
    //we can access both the variable a & b here
    return a + b;
  }
  console.log(inner());
  //we can only access variable a
  console.log(a)
}
```

## Practice

```js
const SPENDING_THRESHOLD = 400;
const ACCOUNT_BALANCE = 500;
const PHONE_PRICE = 200;
const TAX_RATE = 0.1;
const ACCESSORIES_PRICE = 20;
    
function CALCULATE_TAX(){
  return amount*TAX_RATE;
}

function FORMAT_FINAL_AMOUNT(amount){
  return `₹ ${(amount).toFixed(2)}`;
}

let amount = 0;

while(amount<ACCOUNT_BALANCE){
  amount = amount + PHONE_PRICE

  if(amount < SPENDING_THRESHOLD){
    amount = amount + ACCESSORIES_PRICE;
  }  
}

amount = amount + CALCULATE_TAX(amount);

console.log("Your purchase amount is: " + FORMAT_FINAL_AMOUNT(amount))

if(amount > ACCOUNT_BALANCE){
  console.log("Insufficient Account Balance")
}

// Your purchase amount is: ₹ 682.00
// Insufficient Account Balance

```
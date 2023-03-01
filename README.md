<div align="center">
    <h1>
       JavaScript Interview Questions and Answers.
    </h1>
</div>

### Table of Contents for theoretical questions.

| No. | Questions                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is JavaScript](#what-is-javascript)                                         |
| 2   | [What are the scopes of a variable in JavaScript](#What-are-the-scopes-of-a-variable-in-JavaScript) |
| 3   | [What is the difference between undefined and not defined in JavaScript](#What-is-the-difference-between-undefined-and-not-defined-in-JavaScript)           |
| 4   | [What is closure in javascript](#what-is-closure-in-javascript)  |
| 5   | [What is the difference between == and === operators](#what-is-the-difference-between--and--operators)  

---

### Table of Contents for logical questions.

| No. | Questions                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is the output of below code](#What-is-the-output-of-below-code)   |                                     
| 2   | [For which value of `x` the results of the following statements are not the same](#For-which-value-of-x-the-results-of-the-following-statements-are-not-the-same)      |
| 3   | [What will be the output of the following code](#What-will-be-the-output-of-the-y-in-following-code)
| 4   | [What will be the output of the empOne company](#What-will-be-the-output-of-the-empOne-company)      |
| 5   | [What will be the output of the y in following code](#What-will-be-the-output-of-the-y-in-following-code)|
| 6   | [Write a add function which will work properly when invoked with following syntax](#Write-a-add-function-which-will-work-properly-when-invoked-with-following-syntax)   |
| 7   | [What is the output of d](#What-is-the-output-of-d)   |
| 8   | [What is the output of these three console](#What-is-the-output-of-these-three-console)   |

---

1. ### What is JavaScript?

    JavaScript is a lightweight, interpreted programming language with object-oriented capabilities, 
    that used for both on the client-side and server-side that allows you to 
    make web pages interactive. </br> JavaScript is a case sensitive language. The language keywords, variables, function names, and any other               identifiers must always be typed with a consistent capitalization of letters.

   **[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---

2. ### What are the scopes of a variable in JavaScript?

     The scope of a variable is the region of your program in which it is defined. 
     JavaScript variable will have only two scopes.

   • Global Scope − A global variable has global scope which means it is visible everywhere in your 
     JavaScript code. </br>
     Example: `window` object has global scope it's accessible everywhere.

   • Local Scope (Block Scope) − A local variable will be visible only within a function where it is defined.
     Function parameters are always local to that function. </br>
     Example: when variable declear with `let` or `const` key word in JavaScript. it will accessible within block.
     
      ```javascript
      
        let a = 'Hello';  // global variable

        function greet() {
            let b = 'World';  // local variable

            console.log(a + ' ' + b);

            if (b == 'World') {

                let c = 'hello';  // block-scoped variable

                console.log(a + ' ' + b + ' ' + c);
            }

            console.log(a + ' ' + b + ' ' + c); // variable c cannot be accessed here
        }

        greet();
        
    ```

**[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---
  
 3. ### What is the difference between undefined and not defined in JavaScript?
 
    In JavaScript if you try to use a variable that doesn't exist and has not been declared, then JavaScript will throw an error `var name is not             defined` and the script will stop executing thereafter. But If you use `typeof undeclared_variable` then it will return `undefined`.

    Before starting further discussion let's understand the difference between declaration and definition.

    `var x` is a declaration because we are not defining what value it holds yet, but we are declaring its existence and the need for memory allocation.

    ```javascript
    var x; // declaring x
    console.log(x); // output: undefined
    ```

    `var x = 1` is both declaration and definition, here declaration and assignment of value happen inline for variable x—what we are doing is called         "initialisation". In JavaScript both variable declarations and function declarations go to the top of the scope in which they are declared, then         assignment happens—this series of events is called "hoisting".

    A variable can be declared but not defined. When we try to access it, It will result `undefined`.

    ```javascript
    var x; // Declaration
    typeof x === 'undefined'; // Will return true
    ```

    A variable can be neither declared nor defined. When we try to reference such variable then the result will be `not defined`.
    ```javascript
    console.log(y);  // Output: ReferenceError: y is not defined
 
 **[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---
  
4. ### What is “closure” in javascript?

    A closure is a function defined inside another function (called parent function) and as such it has access to the variables declared and defined         within its parent function's scope.

    The closure has access to the variables in three scopes:

    - Variable declared in its own scope
    - Variable declared in its parent function's scope
    - Variable declared in the global namespace

    ```javascript
    var globalVar = "abc"; //Global variable

    // Parent self-invoking function
    (function outerFunction (outerArg) { // start of outerFunction's scope

      var outerFuncVar = 'x'; // Variable declared in outerFunction's function scope   

      // Closure self-invoking function
      (function innerFunction (innerArg) { // start of innerFunction's scope

        var innerFuncVar = "y"; // variable declared in innerFunction's function scope
        console.log(         
          "outerArg = " + outerArg + "\n" +
          "outerFuncVar = " + outerFuncVar + "\n" +
          "innerArg = " + innerArg + "\n" +
          "innerFuncVar = " + innerFuncVar + "\n" +
          "globalVar = " + globalVar);

      // end of innerFunction's scope

      })(5); // Pass 5 as parameter to our Closure

    // end of outerFunction's scope

    })(7); // Pass 7 as parameter to the Parent function
    ```

    `innerFunction` is a closure which is defined inside `outerFunction` and consequently has access to all the variables which have been declared and        defined within `outerFunction`'s scope as well as any variables residing in the program's global scope.

    The output of the code above would be:

    ```javascript
    outerArg = 7
    outerFuncVar = x
    innerArg = 5
    innerFuncVar = y
    globalVar = abc
    ```

**[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---
  
5. ### What is the difference between == and === operators?

   JavaScript provides both strict(===, !==) and type-converting(==, !=) equality comparison. The strict operators take type of variable in                  consideration, while non-strict operators make type correction/conversion based upon values of variables. The strict operators follow the below          conditions for different types,

   1. Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
   2. Two numbers are strictly equal when they are numerically equal. i.e, Having the same number value.
      There are two special cases in this,
      1. NaN is not equal to anything, including NaN.
      2. Positive and negative zeros are equal to one another.
   3. Two Boolean operands are strictly equal if both are true or both are false.
   4. Two objects are strictly equal if they refer to the same Object.
   5. Null and Undefined types are not equal with ===, but equal with ==. i.e,
      null===undefined --> false but null==undefined --> true

   Some of the example which covers the above cases,

   ```javascript
   0 == false   // true
   0 === false  // false
   1 == "1"     // true
   1 === "1"    // false
   null == undefined // true
   null === undefined // false
   '0' == false // true
   '0' === false // false
   []==[] or []===[] //false, refer different objects in memory
   {}=={} or {}==={} //false, refer different objects in memory
   ```

   **[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---
  
========================================================================================================================================================================================================================

  ### Logical Questions
  
 1. ### What is the output of below code?

    ```javascript
    getMessage();
    
    var getMessage = () => {
      console.log("Good morning");
    };
    ```

    - 1: Good morning
    - 2: getMessage is not a function
    - 3: getMessage is not defined
    - 4: Undefined

    <details><summary><b>Answer</b></summary>
    <p>

    ##### Answer: 2

    Hoisting will move variables and functions to be the top of scope. Even though getMessage is an arrow function the above function will considered as     a varible due to it's variable declaration or assignment. (Like all other functions in Javascript, the arrow function is not hoisting the main reason     that you cannot call them before initialization.) So the variables will have undefined value in memory phase and throws an error '`getMessage` is not     a function' at the code execution phase.

    </p>

    </details>

 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**

---

2. ### For which value of `x` the results of the following statements are not the same?

    ```javascript
    if( x <= 100 ) {...}
    if( !(x > 100) ) {...}
    ```
    <details><summary><b>Answer</b></summary>
    
    <p>

    ##### Answer: NaN

   `NaN <= 100` is `false` and `NaN > 100` is also `false`, so if the
    value of `x` is `NaN`, the statements are not the same.

    The same holds true for any value of x that being converted to type Number, returns `NaN`, e.g.: `undefined`, `[1,2,5]`, `{a:22}` , etc.

    This is why you need to pay attention when you deal with numeric variables. `NaN` can’t be equal, less than or more than any other 
    numeric value, so the only reliable way to check if the value is `NaN`, is to use the `isNaN()` function.

    </p>

    </details>

 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**

---

3. ## What will be the output of the following code?

    ```javascript
    var x = 1;
    var output = (function() {
      delete x;
      return x;
    })();

    console.log(output);
    ```
    <details><summary><b>Answer</b></summary>
    <p>
    The code above will output `1` as output. `delete` operator is used to delete a property from an object. Here `x` is not an object it's **global         variable** of type `number`.
    </p>

    </details>

 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**

---

4. ## What will be the output of the empOne company?

    ```javascript
    var Employee = {
      company: 'xyz'
    }
    var empOne = Object.create(Employee);
    delete empOne.company
    console.log(empOne.company);
    ```

    <details><summary><b>Answer</b></summary>
     <p> 
    The code above will output `xyz` as output. Here `emp1` object got company as **prototype** property. delete operator doesn't delete prototype           property.

    `emp1` object doesn't have **company** as its own property. you can test it `console.log(emp1.hasOwnProperty('company')); //output : false` However,     we can delete company property directly from `Employee` object using `delete Employee.company` or we can also delete from `emp1` object using             `__proto__` property `delete emp1.__proto__.company`.
    </p>

    </details>
    
     **[⬆ Back to Top](#table-of-contents-for-logical-questions)**

---

5. ## What will be the output of the `y` in following code?

```javascript
var z = 1, y = z = typeof y;
console.log(y);
```
<details><summary><b>Answer</b></summary>
<p>
The code above will print string `"undefined"` as output. According to associativity rule operator with the same precedence are processed based on their associativity property of operator. Here associativity of the assignment operator is `Right to Left` so first `typeof y` will evaluate first which is string `"undefined"` and assigned to `z` and then `y` would be assigned the value of z. The overall sequence will look like that: 
</p>
    
```javascript
var z;
z = 1;
var y;
z = typeof y;
y = z;
```

</details>


 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**
 
 
6. ## Write a add function which will work properly when invoked with following syntax.

```javascript
console.log(add(5)(4)(6)); // output : 15
console.log(add(8)(3)(9)); // output : 20
```
<details>

```javascript
function add (x) {
  return function (y) { // anonymous function
    return function (z) { // anonymous function
      return x + y + z;
    };
  };
}
```

Here the `add` function accepts the first argument and returns an anonymous function which then takes the second parameter and returns one last anonymous function which finally takes the third and final parameter; the last function then sum `x`, `y` and `z`, and returns the result of the operation.

In Javascript, a function defined inside another function has access to the outer function's scope and can consequently return, interact with or pass on to other functions, the variables belonging to the scopes that incapsulate it.

- A function is an instance of the Object type
- A function can have properties and has a link to its constructor method
- A function can be stored as a variable
- A function can be passed as a parameter to another function
- A function can be returned by another function

</details>

**[⬆ Back to Top](#table-of-contents-for-logical-questions)**
---

7. ## What is the output of d

```javascript
    let c = { greeting: 'Hey!' };
    let d;

    d = c;
    c.greeting = 'Hello';
    console.log(d.greeting);
```

- A: `Hello`
- B: `Hey!`
- C: `undefined`
- D: `ReferenceError`
- E: `TypeError`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

In JavaScript, all objects interact by _reference_ when setting them equal to each other.

First, variable `c` holds a value to an object. Later, we assign `d` with the same reference that `c` has to the object.

<img src="https://i.imgur.com/ko5k0fs.png" width="200">

When you change one object, you change all of them.

</p>
</details>

---


 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**
 
 
 8. ## What is the output of these three console.

```javascript
let a = 3;
let b = new Number(3);
let c = 3;

console.log(a == b);
console.log(a === b);
console.log(b === c);
```

- A: `true` `false` `true`
- B: `false` `false` `true`
- C: `true` `false` `false`
- D: `false` `true` `true`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

`new Number()` is a built-in function constructor. Although it looks like a number, it's not really a number: it has a bunch of extra features and is an object.

When we use the `==` operator (Equality operator), it only checks whether it has the same _value_. They both have the value of `3`, so it returns `true`.

However, when we use the `===` operator (Strict equality operator), both value _and_ type should be the same. It's not: `new Number()` is not a number, it's an **object**. Both return `false.`

</p>
</details>

---

 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**

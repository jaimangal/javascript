<div align="center">
    <h1>
       JavaScript Interview Questions and Answers.
    </h1>
</div>

### Table of Contents for theoretical questions.

| No. | Questions                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is JavaScript](#what-is-javascript)                                         |
| 2   | [What are the scopes of a variable in JavaScript](#What-are-the-scopes-of-a-variable-in-JavaScript)                                                                                             

---

### Table of Contents for logical questions.

| No. | Questions                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is the output of below code](#What-is-the-output-of-below-code)                                         |
| 2   | [What is prototype chain](#what-is-a-prototype-chain)                                                                                                                                                                                                            
---

1. ### What is JavaScript?

     => JavaScript is a lightweight, interpreted programming language with object-oriented capabilities, 
        that used for both on the client-side and server-side that allows you to 
        make web pages interactive.
        
        JavaScript is a case sensitive language.  The language keywords, variables, function names, and any other identifiers must always be typed with a         consistent capitalization of letters.

   **[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---

2. ### What are the scopes of a variable in JavaScript?

The scope of a variable is the region of your program in which it is defined. JavaScript variable will have only two scopes.

• Global Scope − A global variable has global scope which means it is visible everywhere in your JavaScript code.
  Example: window object has global scope it's accessible everywhere.

• Local Scope (Block Scope) − A local variable will be visible only within a function where it is defined. Function parameters are always local to that function.
  Example: when variable declear with let or const key word in JavaScript. it will accessible within block.

**[⬆ Back to Top](#table-of-contents-for-theoretical-questions)**
   
  ---
  
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

Hoisting will move variables and functions to be the top of scope. Even though getMessage is an arrow function the above function will considered as a varible due to it's variable declaration or assignment. So the variables will have undefined value in memory phase and throws an error '`getMessage` is not a function' at the code execution phase.

</p>

</details>

 **[⬆ Back to Top](#table-of-contents-for-logical-questions)**

---

<div align="center">
    <h1>
       JavaScript Interview Questions and Answers.
    </h1>
</div>

### Table of Contents for theoretical questions.

| No. | Questions                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is JavaScript](#what-is-javascript)                                         |
| 2   | [What is prototype chain](#what-is-a-prototype-chain)                                                                                                             |                                                                                                                       |
| 435 | [What is throttling?](#what-is-throttling)

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

# TypeScript Quiz Questions

Test your TypeScript knowledge with these 25 challenging questions. Each question includes the code snippet and the correct answer with explanation.

**Question: 1** Predict the output for the below code:

```typescript
const alterEgo = "Slade Wilson";
function outerFunction() {
    let alterEgo = "Wade Wilson";
    setTimeout(function () {
        console.log(alterEgo); 
    }, 2000);
}
outerFunction();

<details> <summary>View Answer</summary>
Answer: "Wade Wilson"

Explanation: The local variable alterEgo inside outerFunction takes precedence over the global variable. The setTimeout callback captures this local variable through closure.

</details>

# TypeScript Quiz Questions

Test your TypeScript knowledge with these 25 challenging questions. Each question includes the code snippet and the correct answer with explanation.

## Table of Contents
1. [Variable Scoping](#1-variable-scoping)
2. [Class Compilation Errors](#2-class-compilation-errors)
3. [Array Manipulation](#3-array-manipulation)
... [and so on for all 25 questions]

---

### 1. Variable Scoping
**Question:** Predict the output for the below code:

```typescript
const alterEgo = "Slade Wilson";
function outerFunction() {
    let alterEgo = "Wade Wilson";
    setTimeout(function () {
        console.log(alterEgo); 
    }, 2000);
}
outerFunction();
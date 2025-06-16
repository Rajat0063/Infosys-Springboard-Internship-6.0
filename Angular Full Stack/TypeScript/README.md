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
```

<details> <summary>View Answer</summary>
Answer: "Wade Wilson"

Explanation: The local variable alterEgo inside outerFunction takes precedence over the global variable. The setTimeout callback captures this local variable through closure.

</details>

**Question: 2** Find which lines cause compilation errors from the below code:

```typescript
1.      class company{
2.      static empId:number=753800;
3.      private _eta: boolean;
4.      constructor(){
5.           this.empId++;
6.           this._eta = false;
7.           }
8.      display(dept:boolean):boolean
9.           {
10.           this._eta=dept;    
11.           return this._eta;
12.          }
13.      }
14.    var emp1=new company(); 
15.    emp1.display(false);
16.    alert(emp1);
17.    let emp2 = new company();
18.    alert(emp2.empId);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Lines 5 and 18

💡 Explanation:

Line 5: Cannot modify static property via instance (this.empId++ should be company.empId++)

Line 18: Cannot access static property via instance (emp2.empId should be company.empId)

</details>

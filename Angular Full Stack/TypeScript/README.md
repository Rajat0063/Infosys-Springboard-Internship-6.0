# TypeScript Quiz Questions

Test your TypeScript knowledge with these 25 challenging questions. Each question includes the code snippet and the correct answer with explanation.

**Question: 1** Predict the output for the below code:

```typescript
1.	const alterEgo = "Slade Wilson";
2.	function outerFunction()
3.	{
4.	    let alterEgo = "Wade Wilson";
5.	    setTimeout(
6.		    function () {
7.	    	alert(alterEgo);
8.          }, 2000);
9.  }
10.	outerFunction();
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "Wade Wilson"

💡 Explanation: 

The local variable alterEgo inside outerFunction takes precedence over the global variable. The setTimeout callback captures this local variable through closure.

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

**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>

**Question: 4** Analyze the below-given TypeScript code and select the appropriate datatype to be used.

```typescript
function sayTest(): ___ {
    while (true) {
        console.log('Hello World')
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: never

💡 Explanation:
The never type represents functions that never return (infinite loops) or always throw exceptions.

</details>

**Question: 5** Predict the output for the below code:

```typescript
1.     interface a
2.       {
3.           name: string;
4. }
5.    interface b
6.       {
7.           age: number;
8.}
9.     interface c extends a, b
10. {
11.          cash: number;
12. }
13.    class ab implements a, b
14.    {
15.         cash = 2000;
16.         name = "Barry";
17.         age = 20;
18.         public a = () => alert(this.cash + " was the amount " + this.name + " had when he was " + this.age);
19. }
20.    new ab().a();
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "2000 was the amount Barry had when he was 20"

💡 Explanation:
The class correctly implements both interfaces and the alert shows the interpolated string with all properties.

</details>

**Question: 6** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>

**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>

**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>


**Question: 3** Predict output for the below-given code:

```typescript
const colors: string[] = ["Red", "Blue"];
function fun() {
    setTimeout(() => {
        colors = ["Orange", "Yellow", "Green"];
    }, 10);
}
fun();
colors.push("White");
alert(colors);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Red", "Blue", "White"]

💡 Explanation:

The reassignment of colors fails because it's a const

The push operation succeeds because it modifies the array without reassignment

The error prevents the timeout callback from executing

</details>
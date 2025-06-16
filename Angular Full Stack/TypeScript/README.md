# TypeScript Quiz Questions

Test your TypeScript knowledge with these 25 challenging questions. Each question includes the code snippet and the correct answer with explanation.

**Question 1:** Predict the output for the below code:

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

**Question 2:** Find which lines cause compilation errors from the below code:

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

**Question 3:** Predict output for the below-given code:

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

**Question 4:** Analyze the below-given TypeScript code and select the appropriate datatype to be used.

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

**Question 5:** Predict the output for the below code:

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

**Question 6:** Predict the output of the below code snippet.

```typescript
class company {
    private _empName: string = "Jack";
    private _empDept: string = "Finacle";
    constructor(empName: string, empDept: string) {
        this._empName = empName;
        this._empDept = empDept;
    }
    display(): void {
        console.log(this._empName + " works for " + this._empDept + " unit");
    }
}
var emp1 = new company("Tom", "Training");
emp1.display();
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "Tom works for Training unit"

💡 Explanation:
The constructor overrides the default values, so instance values are used instead of initial values.

</details>

**Question 7:** PrConsider that you have created two TypeScript files as mentioned below:

```typescript
//One.ts
__1__ function show (userId:number) : number
{
return 'Your id is ' +`${userId}`
}

//Two.ts
__2__ {show} from './One';
console.log(show(1234));
Fill in the blank with the appropriate option to execute this code successfully.
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:
1 - export, 2 - import

💡 Explanation:

Functions need to be exported before they can be imported

The correct ES6 module syntax is export/import

</details>

**Question 8:** What will be the output for the below code?

```typescript
let ceoList: string[]=[];
ceoList["XYZ"] = "Tim";
ceoList["ABC"] = "Tom";
ceoList["TEST"] = "Joe"
ceoList["TEXT"]="John"
alert("Length : " + ceoList.length);
alert("Ceo of XYZ: " + ceoList["XYZ"]);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:
Length: 0
CEO of XYZ: Tim

💡 Explanation:

Array indices must be numbers for length calculation

String keys create properties but don't affect array length

</details>


**Question 9:** Predict the output of the below code:

```typescript
1.	function changeNationality(data: string): string{
2.	    nationality += " "+data;
3.	    return nationality;
4.	}
5.	let nationality = "Indian";
6.	nationality = changeNationality("Canadian");
7.	alert(nationality);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "Indian Canadian"

💡 Explanation:

Function declaration is hoisted above variable initialization

The operation concatenates the existing and new values

</details>


**Question 10:** Consider you are using a tsconfig.json file. The ts files are stored in a folder named ts. tsconfig.json is stored outside the ts folder. 
Which compiler option is best suited to read the ts files from the folder while transpiling?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: rootDir

💡 Explanation:
The rootDir specifies the root directory of input files, allowing the compiler to locate your TypeScript files correctly.

</details>


**Question 11:** Predict the output for the below code:

```typescript
//module.ts:
class Utility {
    setId(name: string, id: number): string {
        return name + " " + id;
    }
}
export const identity: string = "EMPLOYEE";
export { Utility as mainUtility };

//file.ts:
import * as mainutil from "./module";
let util = new mainutil.mainUtility();
let emp = util.setId("JA$", 753886);
console.log(`${emp} is an ${mainutil.identity}`);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "JA$ 753886 is an EMPLOYEE"

💡 Explanation:

The alias mainUtility is correctly imported and used

Named exports and default exports work together properly

</details>


**Question 12:** What is the data type used in TypeScript to declare a variable that does not hold any value in the entire application?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: never

💡 Explanation:
The never type represents values that never occur, used for:

Functions that never return

Variables that should never have a value

</details>


**Question 13:** What will be the output for the following code?


```typescript
1. function fun(contact: number, name?: string, defaultName: string = "Usopp", ...restName: string[])
2.	{
3.	    alert("defaultName has: " + defaultName);
4.  }
5.	fun(1234567891, undefined, "Luffy", "Zoro", "Nami", "Sanji");
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "defaultName has: Luffy"

💡 Explanation:

Optional parameter name is skipped with undefined

defaultName gets overwritten by "Luffy"

Rest parameters collect remaining values into restName

</details>


**Question 14:** What will be the most appropriate output for the following?

```typescript
enum defaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum cost { Red = defaultPrice.Single, Green = Blue, Blue = defaultPrice.Double + defaultPrice.Triple, White = defaultPrice.Triple };
var price = cost.Blue;
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No errors (compiles successfully)

💡 Explanation:
TypeScript allows:

Enum value computation (5000 in this case)

Forward references to other enum members

Both numeric and computed enum values

</details>


**Question 15:** Find error if any in the below code:

```typescript
1.    class a{
2.        parent: string = "From Parent";
3.    }
4.    interface b{
5.        fromInterface: number;
6.    }
7.    class c implements b extends a     {
8.        fromInterface = 20;
9.        para = () => {
10.            console.log(this.parent);
11.        }
12.    }
13.    new c().para();
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line 7 alone causes error because extends clause must precede implements

💡 Explanation:
Correct syntax would be:

typescript
class c extends a implements b { ... }
Order matters in TypeScript class declarations

The actual functionality would work if syntax was correct

</details>


**Question 16:** Predict the output for the below code:

```typescript
1.	interface a {
2.	    var1: string;
3.	}
4.	interface b {
5.	    var2: string;
6.	}
7.	function fun1(para1: a): void {
8.	    alert("Inside fun1" + para1);
9.}
10.	function fun2(para2: b): void {
11.	    alert("Inside fun2" + para2);
12. }
13.	var obj = { var1: "for a", var2: "for b" };
14.	fun1(obj);
15.	fun2(obj);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No Error

💡 Explanation:
TypeScript uses structural typing:

obj satisfies both interfaces

No explicit implementation needed

Duck typing allows this usage

</details>


**Question 17:** Predict the output for the below code:

```typescript
let list: any = ["One", "Two", "Three", "Four"];
list.push(list.splice(-4, 2));
alert(list);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ["Three", "Four", ["One", "Two"]]

💡 Explanation:

splice(-4,2) extracts first two elements

push adds them back as a nested array

Results in modified array + nested array

</details>


**Question 18:** Predict the output for the below code:

```typescript
class Friends<T>{
    characterList: Array<T> = [];
    addCharacter(newCharacterList: Array<T>): void {
        this.characterList = newCharacterList;
        alert(characterList);
    }
}
let show = new Friends<string>();
let characterList: Array<string> = ["Chandler", "Monica", "Joe", "Rachel", "Ross"];
show.addCharacter(characterList);

let show2 = new Friends<number>();
let seasons: Array<number> = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
show2.addCharacter(seasons);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:
["Chandler", "Monica", "Joe"]
[1, 2, 3, 4, 5]

💡 Explanation:

Same class works with different types

Type parameter T enforces consistency

No type interference between instances

</details>


**Question 19:** Predict the output for the below code:

```typescript
interface a {
    a: string;
    abstract fun(): string;
}
class b implements a {
    a: string;
    constructor() {
        this.a = "Success!"
    }
    fun() {
        return this.a;

    }
}
let obj = new b;
console.log(obj.fun());
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "Success!"

💡 Explanation:

Interface enforces method implementation

Class correctly implements all members

Method returns the initialized value

</details>


**Question 20:** Consider the below-given TypeScript code that populates studentId value on the default console. 

Can you help in updating this code to implement the same concept using rest parameter usage.

```typescript
function showDetails(studentName:string, studentId:number, studentRank:number):number
{
    return studentId;
}
let studentInfo:number = showDetails("Tim", 1234, 3);
console.log(studentInfo);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Both changes must be implemented

💡 Explanation:

The rest parameter ...studentInfo collects all numeric arguments

First element studentInfo[0] corresponds to original studentId

Maintains identical functionality while being more flexible

</details>


**Question 21:** What will be the output for the below code?

```typescript
let var1 = 20;
function fun() {
    var1 = 21;
    var a = () => { var1 = 40 };
    a();
}
fun();
alert(var1);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 40

💡 Explanation:

Arrow functions inherit the parent scope

All assignments modify the same var1 variable

The final assignment (40) wins

</details>


**Question 22:** Predict the output of the below-given code snippet.

```typescript
function add(num1 = 200, num2?: number) {
    if (num1) {
        return num1 + num2;
    }
    return num2;
}
console.log(add(3, 5) + add(undefined, 5));
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 213

💡 Explanation:

add(3, 5) → 3 + 5 = 8

add(undefined, 5) → uses default num1 = 200 → 200 + 5 = 205

Total: 8 + 205 = 213

</details>


**Question 23:** Select the statement that helps a TypeScript developer to understand the purpose of Decorators?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Helps in declaring methods with metadata

💡 Explanation:
Decorators are:

Special declarations prefixed with @

Used for adding metadata to classes/methods

Enable declarative programming patterns

Widely used in frameworks like Angular

</details>


**Question 24:** Predict the output of the below-given TypeScript code.

```typescript
const students : any [] = [
    { studentName: 'Tim', studentId: 1034},
    { studentName: 'Jack', studentId: 2345},
    { studentName: 'Jim', studentId: 3456} 
]
 console.log(students.splice(1,1));
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: [{ studentName: 'Jack', studentId: 2345 }]

💡 Explanation:

splice(start, deleteCount) modifies the original array

Returns array of removed elements

Here removes 1 element at index 1 (Jack)

</details>


**Question 25:** What will be the output for the below code?

```typescript
class A{
printData<T>(data: T): T{
    if (data == "Barry Allen")
        alert("Data Received");
return data;
}
}
let obj = new A();
let data:string=obj.printData<string>('Barry Allen');
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: "Data Received"

💡 Explanation:

Generic method preserves type-specific operations

Type inference allows string comparison

Works despite T being generic because of type argument <string>

</details>
<!-- End Here -->

**Question: 14** What will be the most appropriate output for the following?

```typescript
enum defaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum cost { Red = defaultPrice.Single, Green = Blue, Blue = defaultPrice.Double + defaultPrice.Triple, White = defaultPrice.Triple };
var price = cost.Blue;
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No errors (compiles successfully)

💡 Explanation:
TypeScript allows:

Enum value computation (5000 in this case)

Forward references to other enum members

Both numeric and computed enum values

</details>

**Question: 14** What will be the most appropriate output for the following?

```typescript
enum defaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum cost { Red = defaultPrice.Single, Green = Blue, Blue = defaultPrice.Double + defaultPrice.Triple, White = defaultPrice.Triple };
var price = cost.Blue;
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No errors (compiles successfully)

💡 Explanation:
TypeScript allows:

Enum value computation (5000 in this case)

Forward references to other enum members

Both numeric and computed enum values

</details>

**Question: 14** What will be the most appropriate output for the following?

```typescript
enum defaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum cost { Red = defaultPrice.Single, Green = Blue, Blue = defaultPrice.Double + defaultPrice.Triple, White = defaultPrice.Triple };
var price = cost.Blue;
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No errors (compiles successfully)

💡 Explanation:
TypeScript allows:

Enum value computation (5000 in this case)

Forward references to other enum members

Both numeric and computed enum values

</details>

**Question: 14** What will be the most appropriate output for the following?

```typescript
enum defaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum cost { Red = defaultPrice.Single, Green = Blue, Blue = defaultPrice.Double + defaultPrice.Triple, White = defaultPrice.Triple };
var price = cost.Blue;
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No errors (compiles successfully)

💡 Explanation:
TypeScript allows:

Enum value computation (5000 in this case)

Forward references to other enum members

Both numeric and computed enum values

</details>

**Question: 14** What will be the most appropriate output for the following?

```typescript
enum defaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum cost { Red = defaultPrice.Single, Green = Blue, Blue = defaultPrice.Double + defaultPrice.Triple, White = defaultPrice.Triple };
var price = cost.Blue;
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: No errors (compiles successfully)

💡 Explanation:
TypeScript allows:

Enum value computation (5000 in this case)

Forward references to other enum members

Both numeric and computed enum values

</details>
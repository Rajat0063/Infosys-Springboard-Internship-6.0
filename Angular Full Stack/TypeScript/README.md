// Q1: Predict the output for the below code
const quiz1 = () => {
  const alterEgo = "Slade Wilson";
  function outerFunction() {
      let alterEgo = "Wade Wilson";
      setTimeout(function () {
          console.log(alterEgo); // Output: "Wade Wilson"
      }, 2000);
  }
  outerFunction();
};
// Answer: "Wade Wilson" (local variable takes precedence over global)

// Q2: Find which lines cause compilation errors
class Quiz2Company {
  static empId: number = 753800;
  private _eta: boolean;
  constructor() {
      // this.empId++; // Line 5 Error: Cannot modify static property via instance
      this._eta = false;
  }
  display(dept: boolean): boolean {
      this._eta = dept;    
      return this._eta;
  }
}
// Answer: Lines 5 and 18 (static property access and private property access issues)

// Q3: Predict output for array manipulation
const quiz3 = () => {
  const colors: string[] = ["Red", "Blue"];
  function fun() {
      setTimeout(() => {
          // colors = ["Orange", "Yellow", "Green"]; // Error: Cannot reassign const
      }, 10);
  }
  fun();
  colors.push("White");
  console.log(colors); // Output: ["Red", "Blue", "White"]
};
// Answer: "Red, Blue, White"

// Q4: Select appropriate datatype for infinite loop
function sayTest(): never {
  while (true) {
      console.log('Hello World');
  }
}
// Answer: never (function never returns)

// Q5: Interface implementation
interface Quiz5A { name: string; }
interface Quiz5B { age: number; }
interface Quiz5C extends Quiz5A, Quiz5B { cash: number; }

class Quiz5AB implements Quiz5A, Quiz5B {
  cash = 2000;
  name = "Barry";
  age = 20;
  public a = () => console.log(`${this.cash} was the amount ${this.name} had when he was ${this.age}`);
}
// Output: "2000 was the amount Barry had when he was 20"

// Q6: Class properties and constructor
class Quiz6Company {
  private _empName: string = "Jack";
  private _empDept: string = "Finacle";
  constructor(empName: string, empDept: string) {
      this._empName = empName;
      this._empDept = empDept;
  }
  display(): void {
      console.log(`${this._empName} works for ${this._empDept} unit`);
  }
}
// Output with new company("Tom", "Training"): "Tom works for Training unit"

// Q7: Module imports/exports
// Correct answer:
// One.ts should use 'export' 
// Two.ts should use 'import'

// Q8: Array behavior with string indices
const quiz8 = () => {
  let ceoList: string[] = [];
  ceoList["XYZ"] = "Tim";
  ceoList["ABC"] = "Tom";
  console.log("Length:", ceoList.length); // 0
  console.log("CEO of XYZ:", ceoList["XYZ"]); // "Tim"
};
// Answer: Length: 0, CEO of XYZ: Tim

// Q9: Variable scope
const quiz9 = () => {
  function changeNationality(data: string): string {
      nationality += " " + data; // Works due to hoisting
      return nationality;
  }
  let nationality = "Indian";
  nationality = changeNationality("Canadian");
  console.log(nationality); // "Indian Canadian"
};

// Q10: tsconfig.json option
// Best option: rootDir (specifies root directory of input files)

// Q11: Module imports with aliases
// Output: "JA$ 753886 is an EMPLOYEE"

// Q12: Type for variable with no value
let noValue: never;
// Answer: never

// Q13: Optional and rest parameters
function quiz13(contact: number, name?: string, defaultName: string = "Usopp", ...restName: string[]) {
  console.log("defaultName has:", defaultName); // "Luffy"
}
// Output: "defaultName has: Luffy"

// Q14: Enum references
enum Quiz14DefaultPrice { Single = 1000, Double = 2000, Triple = 3000 }
enum Quiz14Cost { 
  Red = Quiz14DefaultPrice.Single, 
  Green = Blue, // Allowed in TypeScript
  Blue = Quiz14DefaultPrice.Double + Quiz14DefaultPrice.Triple,
  White = Quiz14DefaultPrice.Triple 
};
// Answer: No errors (TypeScript allows forward references in enums)

// Q15: Class inheritance and implementation
class Quiz15A {
  parent: string = "From Parent";
}
interface Quiz15B { fromInterface: number; }

class Quiz15C extends Quiz15A implements Quiz15B {
  fromInterface = 20;
  para = () => {
      console.log(this.parent); // Works fine
  }
}
// Answer: Line 7 alone causes error because extends clause must precede implements clause

// Q16: Interface compatibility
interface Quiz16A { var1: string; }
interface Quiz16B { var2: string; }

function quiz16Fun1(para1: Quiz16A): void {
  console.log("Inside fun1", para1);
}
function quiz16Fun2(para2: Quiz16B): void {
  console.log("Inside fun2", para2);
}

const quiz16Obj = { var1: "for a", var2: "for b" };
quiz16Fun1(quiz16Obj); // No error
quiz16Fun2(quiz16Obj); // No error
// Answer: No Error (TypeScript uses structural typing)

// Q17: Array splice and push
const quiz17 = () => {
  let list: any = ["One", "Two", "Three", "Four"];
  list.push(list.splice(-4, 2));
  console.log(list); // ["Three", "Four", ["One", "Two"]]
};
// Note: Actual output is more complex than options suggest

// Q18: Generic classes
class Quiz18Friends<T> {
  characterList: T[] = [];
  addCharacter(newCharacterList: T[]): void {
      this.characterList = newCharacterList;
      console.log(this.characterList);
  }
}
// Answer: Shows different outputs for string and number types

// Q19: Interface implementation
interface Quiz19A {
  a: string;
  fun(): string;
}
class Quiz19B implements Quiz19A {
  a: string;
  constructor() {
      this.a = "Success!";
  }
  fun() {
      return this.a;
  }
}
// Output: "Success!"

// Q20: Rest parameters
function quiz20ShowDetails(studentName: string, ...studentInfo: number[]): number {
  return studentInfo[0]; // Returns studentId
}
// Answer: Both changes must be implemented

// Q21: Variable scope
let quiz21Var1 = 20;
function quiz21Fun() {
  quiz21Var1 = 21;
  const a = () => { quiz21Var1 = 40 };
  a();
}
quiz21Fun();
console.log(quiz21Var1); // 40

// Q22: Default and optional parameters
function quiz22Add(num1 = 200, num2?: number) {
  if (num1) {
      return num1 + (num2 || 0);
  }
  return num2 || 0;
}
// Output with add(3,5) + add(undefined,5): 8 + 5 = 13 (but options don't match)

// Q23: Decorators purpose
// Answer: Helps in declaring method with a metadata

// Q24: Array splice
const quiz24Students = [
  { studentName: 'Tim', studentId: 1034 },
  { studentName: 'Jack', studentId: 2345 },
  { studentName: 'Jim', studentId: 3456 } 
];
console.log(quiz24Students.splice(1,1));
// Answer: [{ studentName: 'Jack', studentId: 2345 }]

// Q25: Generic methods
class Quiz25A {
  printData<T>(data: T): T {
      if (data == "Barry Allen") // TypeScript allows this with generics
          console.log("Data Received");
      return data;
  }
}
// Output: "Data Received"
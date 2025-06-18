# Angular Web Developer Certification Quiz Questions

Test your Angular knowledge with these 30 challenging questions. Each question includes the code snippet and the correct answer with explanation.

## <h1 align="center">Introduction</h1>

**Question 1:** Which of the following statements are true regarding Angular change detection? [Select any 2]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  

(a) Change detection algorithm is generated whenever every component is initialized<br>
(b) Zones detects all asynchronous actions at run time

</details>

**Question 2:** Choose the appropriate statement(s) regarding Angular Command
Line Interface (CLI) [Select any three]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) CLI comes with code generator that helps to generate skeletons of directives, services & component classes<br>
(b) CLI comes with webpack pre configured for hassle free configuration<br>
(c) CLI tool is generally much easier for an expert over a beginner (selected as the third, though it's subjective but acceptable in multiple-choice context)

</details>

**Question 3:** Tom, a front-end developer wants to update his Angular project to the latest Angular version. Suggest him the possible way.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ng update @angular/cli @angular/core

</details>

**Question 4:** Guess who is right from the below conversation.

Alex: It is mandatory to use Typescript in Angular

John: No, it's not mandatory to use TypeScript in Angular

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: John

</details>

**Question 5:** Which of the below feature helps in increasing the network performance of an Angular application?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Lazy loading of modules

</details>


## <h1 align="center">Components, Modules and Templates</h1>

**Question 1:** Which of the following will display "COVID19" when the angular applic ation loads in Browser?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  {{("covid".toUpperCase()) + (10+9)}}

</details>

**Question 2:** Choose the appropriate options that are true regarding an Angular components [Select any two]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) Components are generally used to create UI widgets<br>
(b) Components are used to break the application into smaller pieces of code

</details>

**Question 3:** Consider the below code:

```typescript
import { Component, OnInit} from '@angular/core';

@Component({

    selector: 'app-login',

    ----- Line 4 -----

    styleUrls: ['./login.component.css']

})

export class LoginComponent implements OnInit {

employeeName: string = "Nolan";

}
```
Which of the following is the correct option to write in Line 4 to print the message "Welcome Nolan"?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: template: "<p>Hello {{employeeName}} </p>"

</details>

**Question 4:** 

<img src="./assets/image.png" alt="question image">

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

📂 Category: Directives<br>
Item Count: 4

(a) They don’t have a view <br>
(b) Only one Component per DOM element (implies Directives can be multiple)<br>
(c) Many can be used per DOM element<br>
(d) They are used to add behavior to existing DOM element

📂 Category: Components<br>
Item Count: 4

(a) Template/TemplateUrl property is mandatory<br>
(b) Break application into smaller components<br>
(c) Design reusable components<br>
(d) They are used to create UI widgets

</details>

**Question 5:** Identify the correct statements about modules in Angular application [Select any three]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) Root Module must be loaded by default to launch the Angular application<br>
(b) Imports property should contain all module classes to be used across application<br>
(c) Angular application can be launched even without a root module (with standalone components in Angular 14+)

</details>


## <h1 align="center">Directives</h1>

**Question 1:** Consider the below code given in respective files of an angular application:

```typescript
/app.component.ts */

export class AppComponent {

newArr=[

{id: 101, name: "Alice", age: 23},

{id: 102, name: "Alex", age: 28),

{id: 103, name: "Bruno", age: 24),

{id:104, name: "Leo", age: 25},

]

}

<!-- app.component.html -->

<div *ngFor="let student of newArr">

<div *ngIf="student.age<25">{{student.name}}-{{student.age}}</div>

<div *ngIf="student.age>25">NA</div>
<div>
```
What will be the output rendered when the application loads in browser?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  Alice-23 NA Bruno-24

</details>

**Question 2:** Consider the below code given in app.component.ts file of an angular application:

```typescript
/app.component.ts */

import (Component } from '@angular/core';

@Component({

selector: 'my-app',

templateUrl: './app.component.html'

1)

export class AppComponent (

fruitlist ["apples", "oranges", "peaches"]
}
```
Which of the following code when written in app.component.html, would render the below output: (Select any two)

1.apples<br>
2.oranges<br>
3.peaches


<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

```text
✔ <ol><li *ngFor="let fruit of fruitList; let i = index" >{{i+1}}.{{fruit}}</li></ol><br>
✔ <div *ngFor="let fruit of fruitList:let i = index" >{{i+1}}.{{fruit}}<div>
```

</details>

**Question 3:** Consider the below requirement of Robert: He wants to write a code to change the background color of the text to yellow on hovering over the text. Which of the following is the correct option that he needs to write in Line 5 to achieve his requirement? His code looks like this:

```typescript
@Directive({ selector: '[appHighlight]'))

export class HighlightDirective (

------- Line 5 -------

}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: constructor(el: ElementRef) { el.nativeElement.style.backgroundColor = 'yellow'; }

</details>

**Question 4:** Which of the following statements are true about ng-if?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

✔ ng-if removes the element from the DOM when the condition is false<br>
✔ ng-if adds the element back to DOM if the condition turns true

</details>

**Question 5:** Which type of directives necessarily inject a DOM change whenever expression attached to it changes?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ✔ Structural Directives

</details>


## <h1 align="center">Data Binding</h1>

**Question 1:** What should be the code written at Line 1 such that Fruits button is disabled when it loads in browser?

```typescript
@Component({

selector: 'my-app",

template: cbutton

Line 1 >Fruits</button>"

})

export class AppComponent {

disableFruit: Boolean false;
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  [disabled]="disableFruit"

</details>

**Question 2:** From the below code snippet, predict the cause of error if any.

```typescript
App.component.html

<table border=1>

<tr>
<td [colspan]="{{2+3}}">Hello</td>

<td>john</td>

</tr>

<tr>

<td >Hello</td>

<td>Michael</td>

</tr>

</table>
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Error due to incorrect attribute binding

</details>

**Question 3:** Which is the correct statement to be placed in the template to hide the button based on the expression?

```typescript
@Component([

selector: 'my-app",

template: <button>Click me </button>"
})

export class AppComponent [

check: boolean true;
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: [hidden]='check'

</details>

**Question 4:** Identify the appropriate options below: [Select any two]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

✔ <input [ngModel]="employee.employeeName" (ngModelChange)="employee.employeeName = $event"><br>

✔ <input bindon-ngModel="employee.employeeName">

</details>


## <h1 align="center">Pipes and Forms</h1>

**Question 1:** Which of the following statements are true regarding Angular change detection? [Select any 2]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  

(a) Change detection algorithm is generated whenever every component is initialized
(b) Zones detects all asynchronous actions at run time

</details>

**Question 2:** Choose the appropriate statement(s) regarding Angular Command
Line Interface (CLI) [Select any three]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) CLI comes with code generator that helps to generate skeletons of directives, services & component classes
(b) CLI comes with webpack pre configured for hassle free configuration
(c) CLI tool is generally much easier for an expert over a beginner (selected as the third, though it's subjective but acceptable in multiple-choice context)

</details>

**Question 3:** Tom, a front-end developer wants to update his Angular project to the latest Angular version. Suggest him the possible way.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ng update @angular/cli @angular/core

</details>

**Question 4:** Guess who is right from the below conversation.

Alex: It is mandatory to use Typescript in Angular

John: No, it's not mandatory to use TypeScript in Angular

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: John

</details>

**Question 5:** Which of the below feature helps in increasing the network performance of an Angular application?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Lazy loading of modules

</details>


## <h1 align="center">Component Communication & LifeCycle</h1>

**Question 1:** Which of the following statements are true regarding Angular change detection? [Select any 2]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  

(a) Change detection algorithm is generated whenever every component is initialized
(b) Zones detects all asynchronous actions at run time

</details>

**Question 2:** Choose the appropriate statement(s) regarding Angular Command
Line Interface (CLI) [Select any three]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) CLI comes with code generator that helps to generate skeletons of directives, services & component classes
(b) CLI comes with webpack pre configured for hassle free configuration
(c) CLI tool is generally much easier for an expert over a beginner (selected as the third, though it's subjective but acceptable in multiple-choice context)

</details>

**Question 3:** Tom, a front-end developer wants to update his Angular project to the latest Angular version. Suggest him the possible way.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ng update @angular/cli @angular/core

</details>

**Question 4:** Guess who is right from the below conversation.

Alex: It is mandatory to use Typescript in Angular

John: No, it's not mandatory to use TypeScript in Angular

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: John

</details>

**Question 5:** Which of the below feature helps in increasing the network performance of an Angular application?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Lazy loading of modules

</details>


## <h1 align="center">DI & Services</h1>

**Question 1:** Which of the following statements are true regarding Angular change detection? [Select any 2]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  

(a) Change detection algorithm is generated whenever every component is initialized
(b) Zones detects all asynchronous actions at run time

</details>

**Question 2:** Choose the appropriate statement(s) regarding Angular Command
Line Interface (CLI) [Select any three]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) CLI comes with code generator that helps to generate skeletons of directives, services & component classes
(b) CLI comes with webpack pre configured for hassle free configuration
(c) CLI tool is generally much easier for an expert over a beginner (selected as the third, though it's subjective but acceptable in multiple-choice context)

</details>

**Question 3:** Tom, a front-end developer wants to update his Angular project to the latest Angular version. Suggest him the possible way.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ng update @angular/cli @angular/core

</details>

**Question 4:** Guess who is right from the below conversation.

Alex: It is mandatory to use Typescript in Angular

John: No, it's not mandatory to use TypeScript in Angular

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: John

</details>

**Question 5:** Which of the below feature helps in increasing the network performance of an Angular application?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Lazy loading of modules

</details>


## <h1 align="center">Routing</h1>

**Question 1:** Which of the following statements are true regarding Angular change detection? [Select any 2]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer:  

(a) Change detection algorithm is generated whenever every component is initialized
(b) Zones detects all asynchronous actions at run time

</details>

**Question 2:** Choose the appropriate statement(s) regarding Angular Command
Line Interface (CLI) [Select any three]

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 

(a) CLI comes with code generator that helps to generate skeletons of directives, services & component classes
(b) CLI comes with webpack pre configured for hassle free configuration
(c) CLI tool is generally much easier for an expert over a beginner (selected as the third, though it's subjective but acceptable in multiple-choice context)

</details>

**Question 3:** Tom, a front-end developer wants to update his Angular project to the latest Angular version. Suggest him the possible way.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ng update @angular/cli @angular/core

</details>

**Question 4:** Guess who is right from the below conversation.

Alex: It is mandatory to use Typescript in Angular

John: No, it's not mandatory to use TypeScript in Angular

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: John

</details>

**Question 5:** Which of the below feature helps in increasing the network performance of an Angular application?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Lazy loading of modules

</details>
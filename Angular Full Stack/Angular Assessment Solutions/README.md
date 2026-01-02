# Angular Quiz 30 Quiz Questions

Test your Angular knowledge with these 30 challenging questions. Each question includes the code snippet and the correct answer with explanation.

**Question 1:** Which life cycle hook(s) is used to get the value of the reference that is fetched by @viewChild decorator in a component class?[Select any two]<br>

(i)   ngAfterViewInit<br>
(ii)  ngAfterViewChecked<br>
(iii) ngInit<br>
(iv)  ngDoCheck

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ngAfterViewInit

ngAfterViewChecked

</details>

**Question 2:** John has created a sign-in form and a model class for that. He wants to bind those form fields with the properties of the model class so that data can be transferred in both directions. What type of data binding he should use?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Two Way

</details>

**Question 3:** In reactive forms, we don't use the ngModel directive to bind form elements with model class properties. State True or False.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: True

</details>

**Question 4:** Which of the below syntax will clone and add DOM elements when the condition is true and removes from DOM when the condition is false?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: *ngIf="conditional"

</details>

**Question 5:** Which of the following will successfully add required and email validators to the email field?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: email: ['', [Validators.required, Validators.email]],

</details>

**Question 6:** Which among the following is true about modules in Angular?

1. Module is a block of code with specific functionality that is used to organize the application

2. Each component created in an Angular application should be made part of a module<br>

(i)   Only (i) is true<br>
(ii)  Only (ii) is true<br>
(iii) Both (i) and (ii) are true<br>
(iv)  Neither (i) or (ii) is true

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Both (i) and (ii) are true

</details>

**Question 7:** A Component will consists of the following

1. Templates

2. Class

3. Metadata

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: All of the above

</details>

**Question 8:** Which of the following is the correct way to bind a click event to the button?

```typescript
1. <button (click) = "onSubmit(userName.value,password.value)">Login</button>
 

2. <button onClick = "onSubmit(userName.value,password.value)">Login</button>
```

(i)   Only (i) is correct<br>
(ii)  Only (ii) is correct<br>
(iii) Both (i) and (ii) are correct<br>
(iv)  Neither (i) or (ii) are correct

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Only (i) is correct

</details>


**Question 9:** Consider the below Angular service code snippet. Which line in the below code will be executed when HttpClient returns an error response?

```typescript
(1) @Injectable()
(2) export class BookService {
(3)    constructor(private http: HttpClient) { }
(4)    private booksUrl = './assets/books.json';
(5)    getBooks(): Observable<Book[]>{
(6)        return this.http.get<Book[]>(this.booksUrl).pipe(
(7)            tap(data => console.log("All: " + JSON.stringify(data))),
(8)            catchError(this.handleError))}
```

(i)   Line 6<br>
(ii)  Line 7<br>
(iii) Line 8<br>
(iv)  No line in the given code will be executed

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line 8

</details>


**Question 10:** What type of one-way data binding is used for the below template?

```typescript
<table border=1>
    <tr>
       <td [attr.colspan]="1+1"> First </td>
       <td>Second</td>
    </tr>
    <tr>
       <td>Third</td>
       <td>Fourth</td>
       <td>Fifth</td>
    </tr>
</table>
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Attribute Binding

</details>


**Question 11:** In the below-given code snippet, we are creating service ProtectGuard having a dependency on AuthLoginService:  

ProtectGuard.service.ts:

```typescript
export class ProtectGuard implements CanActivate {
       constructor(private Authlogin: AuthLoginService) { }
       canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot): Promise<boolean> {
           Authlogin.isSignedIn().then(() => {
               if (signedIn) {
                   returns true;
               }
           })
       }
   }
```

AuthLogin.service.ts:   

It contains a method called isSignedIn which returns a variable signedIn of boolean value false wrapped inside a promise object.


Select the correct option to protect the path in users component in Angular.<br>

(i)   {path : 'users' , canActivate:[AuthLogin], component:UsersComponent}<br>
(ii)  {path : 'users' , canActivate:[ProtectGuard], component:UsersComponent}<br>
(iii) {path : 'users' , canActivate:'AuthLogin', component:UsersComponent}<br>
(iv)  {path : 'users' , canActivate:'ProtectGuard', component:UsersComponent}

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: {path : 'users' , canActivate:[ProtectGuard], component:UsersComponent}

</details>


**Question 12:** Below is the code for a custom pipe to sort an array of numbers. Which line in the given code will throw an error?

```typescript
1	import { Pipe, PipeTransform } from '@angular/core';
2
3	@Pipe({
4	  name: 'sort'
5	})
6	export class SortPipe {
7
8	  transform(value: any[], args:string): any {
9
10		if(args==="Ascending"){
11	      return value.sort(function(a, b){return a-b});
12	    }
13		else if(args==="Descending"){
14		  return value.sort(function(a, b){return b-a});
15		}
16		else{
17		  return value;
18		}
19	  }
20	}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line Number 6

</details>


**Question 13:** In reactive forms, which of the following class is used to build a reactive form object inside a component class?<br>

(i)   FormGroup<br>
(ii)  Validators<br>
(iii) FormBuilder<br>
(iv)  All of the above

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: FormBuilder

</details>


**Question 14:** Vikas is trying to understand the code of a Single Page Application created using Angular. He sees the below code. When the application runs, he is able to go to its respective view on click of login or register. He is not able to understand which line of code is responsible for rendering the respective views on the page. Can you help him?

```typescript
(1) <h1>{{title}}</h1>
(2)     <nav>
(3)       <a [routerLink]="['/login']">Login</a>
(4)       <a [routerLink]="['/register']">Register</a>
(5)     </nav>
(6)	<router-outlet></router-outlet>
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line 6

</details>


**Question 15:** The only way to inject a service class inside a component is through a constructor. State True or False.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: True

</details>


**Question 16:** In the below code snippet, we configured a route path and ErrorComponent as follows

```typescript
app.module.ts:

{ path: "error", component: ErrorComponent, data: { message: "page not found" } }
 

ErrorComponent.ts:

export class ErrorComponent {
       constructor(private route: ActivatedRoute) { }
       errormessage: string;
       //line 4
   }
```

Which of the following can be written in line 4 for retrieving static data from a route?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Both a and b

</details>


**Question 17:** While passing the data from child to parent/container component, the property we create in the child component must be of which type?<br>

(i)   EventEmitter<br>
(ii)  EventSender<br>
(iii) EventAny<br>
(iv)  None of the above

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: EventEmitter

</details>


**Question 18:** Which of the following syntax is not an example of one-way data binding?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: [(ngModel)]="value"

</details>


**Question 19:** In the below-given code snippet, which line of code will throw an error?

```typescript
(1) import { Component } from '@angular/core';
(2) @Component({
(3)    selector: 'app-root',
(4)    template: `<ul>
(5)                 <li ngFor="let u of users">{{u.name}}, {{u.address}}</li>
(6)               </ul>`})
(8) export class AppComponent {
(9)   users=[{"name":"Ward Bell Dallas","address":"Texas","status":"active"},
(10)         {"name":"Mark Zuckerberg","address":"Palo Alto","status":"active"},
(11)         {"name":"James Cook Kent street","address":"Sydney","status":"active"}];}
```

(i)   Line Number 3<br>
(ii)  Line Number 4<br>
(iii) Line Number 5<br>
(iv)  Line Number 8

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line Number 5

</details>


**Question 20:** Consider the following Angular routing code. Which line in the given code has an error? 

```typescript
(1) import { Routes, RouterModule } from '@angular/router';
(2) import { BooksComponent }    from './books.component';
(3) import { DashboardComponent } from './dashboard.component';
(4) import { BookDetailComponent } from './book-detail.component';

(5) const routes: Routes = [
(6)     { path: 'dashboard', component: DashboardComponent },
(7)     { path:'', pathMatch:'full'},
(8)     { path: 'books', component: BooksComponent },
(9)     { path:'detail/:id',component: BookDetailComponent}];  

(10) export const routing = RouterModule.forRoot(routes);
```

(i)   Line 6<br>
(ii)  Line 7<br>
(iii) Line 8<br>
(iv)  Line 9

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line 7

</details>


**Question 21:** Which of the following statement(s) is/are true regarding Reactive forms?

1. Reactive forms are used for large size forms

2. In Reactive forms, form control objects are created in the component class and will be bounded to the form elements in the template<br>

(i)   Only (i) is true<br>
(ii)  Only (ii) is true<br>
(iii) Both (i) and (ii) are true<br>
(iv)  None of the given options are true

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Both (i) and (ii) are true

</details>


**Question 22:** Which of the following is not a built-in-pipe in Angular?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: FilterPipe

</details>


**Question 23:** Which of the following can be used to pass data from one component to another component?

(a) @Input and @Output decorators

(b) route parameters in routing<br>

(i)   Only (a) can be used<br>
(ii)  Only (b) can be used<br>
(iii) Both (a) and (b) can be used<br>
(iv)  None of the given methods can be used

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Both (a) and (b) can be used

</details>


**Question 24:** In the below code snippet, we configured route paths in UserModule and AppModule.

```typescript
user.module.ts:

const userRoutes: Routes = [{
       path: ' ',
       component: UserComponent, 
       children: [
           { path: 'add', component: AddUserComponent },
           { path: 'update', component: UpdateUserComponent }
       ]
   }];
 

app.module.ts:

{
       path: 'user',
       loadChildren: () => import('./user/user.module').then(mod => mod.UserModule)
   }
   @ngModule({
       imports: []
   })
```

What will happen when the user will navigate to the 'user' route?

Note: All necessary imports are done.<br>

(i)   Path 'user' does match any routepaths.<br>
(ii)  UserComponent will be loaded dynamically.<br>
(iii) Module will be loaded and it will add its routes to AppModule 

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: UserModule will be loaded and it will add its routes to AppModule

</details>


**Question 25:** Amit has created two component classes called "AppComponent" & "LoginComponent" respectively. Which of the below code is correct inorder to see the LoginComponent view in the browser? 

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: @NgModule({    declarations: [AppComponent,LoginComponent],    bootstrap: [LoginComponent]    })

</details>

**Question 26:** How many files will get created when the following command is executed to generate a component using Angular CLI?

ng generate component MyComponent

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 4

</details>

**Question 27:** Which of the following statement(s) is/are correct regarding pipes?

1. Pipes is a way of handling functionality inside templates 

2. Pipes are used for data transformation

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Both (i) and (ii) are true

</details>

**Question 28:** Consider the below code snippet and assume that all the required imports are done. What will be the output when the page loads in the browser?

```typescript
app.component.html:

<div>Welcome to {{courseTitle}}</div>
       

app.component.ts:  

 
import { Component } from '@angular/core';

@Component ({
           selector: 'my-app',
           templateUrl: 'app/app.component.html'  
})
export class AppComponent {
           courseTitle: string = 'Angular';
}
```
(i)   Welcome to Angular<br>
(ii)  Welcome to {{courseTitle}}<br>
(iii) Angular<br>
(iv)  None of the above

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Welcome to Angular

</details>

**Question 29:** Which method invokes whenever the data property value changes?

```typescript
export class AppComponent implements OnInit,  DoCheck,
    AfterContentInit, AfterContentChecked,
    AfterViewInit, AfterViewChecked,
    OnDestroy
 {
    
    ngOnInit()     
        console.log('Init');
    }

   ngAfterContentInit() {
        console.log('After content init');
    }

    ngDoCheck() {
        console.log('Change detected');
    }
    
    ngAfterContentChecked() {
        console.log('After content checked');
    }

     ngOnDestroy() {
        console.log('Destroy');
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ngDoCheck()

</details>

**Question 30:** Which of the following is correct to define the template of a component?<br>
```
(i)   @Component({    selector: 'app-coursedetail',    template: './coursedetail.component.html'    })<br>
(ii)  @Component({    selector: 'app-coursedetail',    templateUrl: `<h1>Welcome to Angular</h1>`    })<br>
(iii) @Component({    name: 'app-coursedetail',    template: '<h1>Welcome to Angular</h1>'    })<br>
(iv)  @Component({    selector: 'app-coursedetail',    templateUrl: './coursedetail.component.html'    })
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: @Component({    selector: 'app-coursedetail',    templateUrl: './coursedetail.component.html'    })

</details>
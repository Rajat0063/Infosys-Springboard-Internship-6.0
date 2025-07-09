# Java Foundation Certification Quiz Questions

Test your Java Foundation Certification knowledge with these 40 challenging questions. Each question includes the code snippet and the correct answer with explanation.

## <h1 align="center">OOPS Concepts and Java Architecture</h1>

**Question 1:** If the access specifier is not specified explicitly in a Java class, which of these will be considered?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: default

</details>

**Question 2:** Consider the given scenario. Global Corp Bank is a global banking organization that provides standard banking services to its customers spread across the globe. The bank offers loans for different purposes to its customers like education loans, housing loans etc.<br><br>
For the given scenario, the analyst creates the design for the loan classes as follows:
<br><br>
● The different kinds of loan classes are created first<br>
● The commonalities are then identified and then grouped to form the base class for all kinds of loans<br><br>
Which OOP feature has been used here?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Specialization followed by generalization

</details>

**Question 3:** Consider the given statements. Which of these options is CORRECT?
<br><br>
(i) Byte codes are stored in files with extension .class
<br>
(ii) JVM is platform independent 
<br>
(iii) All JVMs can accept the byte code as an input

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Options (i) and (iii) only

</details>

**Question 4:** The given class diagram represents a Vehicle class. Identify the method(s) which do NOT have any input arguments and NOT returning any value.<br>

<img src="/JAVA Technology Stack/assets/Screenshot 2025-07-08 204255 (1).png" alt="image_1">

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: calculateMileage()

</details>

**Question 5:** The given class diagram represents a Vehicle class. Identify the option which represents the method(s) having protected access specifier and returning a value.<br>

<img src="/JAVA Technology Stack/assets/Screenshot 2025-07-08 204322 (1).png" alt="image_2">

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: validateVehicleMake()

</details>

## <h1 align="center">Java Language Basic Constructs and Keywords</h1>

**Question 1:** Consider the given scenario. Global Corp Bank is a global banking organization that provides standard banking services to its customers spread across the globe. The aim of the proposed banking system is to create a paperless bank. The bank leverages IT for automating several of its business processes.<br><br>

For the given scenario, there are 5 options available under the account services of the bank.<br><br>

A menu based application is written by the programmer. The valid choice values are between 1 and 5 (choice 5 being the option for "Exit"). The skeleton of the program is as follows:

```typescript
int iChoice;
do{
    <Code for displaying menu> 
    <Code for reading choice> 
 }while(iChoice!=5);
```

Assume that the user has provided input for choice as 10. The menu gets redisplayed which is against the requirement. Choose the option which would resolve this problem.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: The condition in the loop should be (iChoice >= 1 && iChoice <= 4)

</details>

**Question 2:** Sam wants to store a value 2 power 30 i.e., 2,147,483,647. Which of the primitive data types in Java can be used to store this value?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: int

</details>

**Question 3:** Consider the given code snippet:

```typescript
1. class Item{
2.     int itemNo;
3.     float itemPrice;
4.     Item(int number,int price){
5.         itemNo=number;
6.         itemPrice=price;
7.     }
8.     void itemDisplay(){
9.        System.out.println("Item No:"+itemNo);
10.       System.out.println("Item Price:"+itemPrice);
11.   }
12.}
13.class ItemProcess{
14.    public static void main(String args[]){
15.        int num;
16.        num= 101.00;
17.        Item itemOne=new Item((int)101.00,100);
18.        itemOne.itemDisplay();
19.     }
20.}
```

The given code snippet results in an error during compilation. Identify the line number which gives the error.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Line 16

</details>


**Question 4:** Help Sam to identify the reserved keyword in Java that he cannot use as names or variables in his code. Choose the CORRECT option.

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: static

</details>


**Question 5:** What is the output of the given code snippet?

```typescript
public class Demo{
    public static void main(String args[]){
        int indexOne=0;
        int indexTwo=0;
        int sum=0;
        for(;indexOne<10;indexOne = indexOne+2){
            sum+=indexOne;
            for(indexTwo=0;indexTwo<5;indexTwo++){
                sum+=indexTwo;
            }
        }
        switch(sum){
            case 10: System.out.println("The value of sum is "+sum);
            case 30: System.out.println("The value of sum is "+sum);
            case 70: System.out.println("The value of sum is "+sum);
            default: System.out.println("The value of sum is "+sum);
        }               
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: <br>
<p align="center">
The value of sum is 70<br>
The value of sum is 70
</p>

</details>

## <h1 align="center">Static/Final/Abstract</h1>

**Question 1:** What is the output of the given code snippet?

```typescript
interface Flyer{
    void land();
    int wings();
}
class Bird implements Flyer{
   public void land(){
        System.out.println("Bird can land");
   }
   public int wings(){
        System.out.println("Bird has two wings");
        return 0;
   }
}
class Aeroplane implements Flyer{
    public void land(){
        System.out.println("Aeroplane can land");
    }
}
class Demo{
   public static void main(String args[]){
        Aeroplane obj=new Aeroplane();
        Bird objOne=new Bird();
        obj.land();
        objOne.land();
   }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Compilation Error: Aeroplane is not abstract and does not override abstract method wings() in Flyer

</details>


**Question 2:** Which of the given statement is FALSE?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: During the object creation, the constructor of a class always executes before the execution of a static block (if any) of the same class

</details>


**Question 3:** Which of the given statement is FALSE with respect to final keyword?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: A final method must be overridden

</details>


**Question 4:** Consider the given statements with respect to final keyword.<br><br>

Statement 1: A final method must be overridden<br>

Statement 2: A final class cannot be inherited<br>

Statement 3: All variables declared in an interface are by default final<br>

Statement 4: We can change the value of a final variable

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Statement 2 and Statement 3 only

</details>


**Question 5:** What is the output of the given code snippet?

```typescript
class Student{
    private int studentId;
    private int yearOfEnrollment;
    private static int counter1=2014101;
    private static int counter2=101;
    public Student(int yearOfEnrollment){
        this.yearOfEnrollment=yearOfEnrollment;
        if(this.yearOfEnrollment==2014){
            this.studentId=counter1++;
        }
        else{
            this.studentId=counter2++;
        }
    }
    public static int totalNumberOfStudents(){
        return(Student.counter2-101);
    }
    public static int totalNumberOfStudents2012(){
        return(Student.counter1-2014100);
    }
}
class Demo{
    public static void main(String args[]){
        Student stdObj = new Student(2012);
        System.out.println(Student.totalNumberOfStudents2012());
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 1

</details>

## <h1 align="center">Arrays/Access modifiers</h1>

**Question 1:** What is the output of the given code snippet?

```typescript
class Patient{
    private int id;
    public Patient(int id){
        this.id=id;
    }
    public int identify(double[] amount, int[] patientId){
        double amt=0.0;
        int counter=0;
        for(int ind1=0; ind1<patientId.length; ind1++){
            if(patientId[ind1]==id){
                amt=amount[ind1];
            }
        }
        for(int ind2=0; ind2<amount.length; ind2++){
            if(amount[ind2]>amt){
                counter++;
                break;
            }
        }
        return counter;
    }
}
class Demo{
    public static void main(String args[]){
        double[] amount = {12,13,16,16,19,20,10,9};
        int[] id={1002,1004,1001,1003,1005,1009,1011,1008};
        Patient obj=new Patient(1001);
        System.out.println(obj.identify(amount, id));
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 1

</details>


**Question 2:** What is the output of the given code snippet?

```typescript
class Demo{
     public static void main(String args[]){
          char[][]  cArray={{'a','2','*'},{'\0','I','n'},{'I','n','f','y','\0'}};
          System.out.println("Length of Array " + cArray.length);
     }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Length of Array 3

</details>


**Question 3:** What is the output of the given code snippet?

```typescript
public class Demo{
    public static void main(String args[]){
        int rows = 4;
        int columns = 4;
        int[][] array = new int[rows][columns];
        int value = 1;
        for(int index1 = 0; index1 < rows; index1++){
            for(int index2 = 0; index2 < columns; index2++){
                array[index1][index2] = value;
                value++;
            }
        }
        for(int index1 = 0; index1 < rows; index1++){
              for(int index2 = 0; index2 < columns; index2++){
                  if(array[index1][index2]%2==array[index1][index2]%4){
                      System.out.print(array[index1][index2] + " ");
                  }
              }
              System.out.println();
        }
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: <br>

<p align="center">
1 4 <br>
5 8  <br>
9 12  <br>
13 16
</p>

</details>


**Question 4:** What is the output of the given code snippet?

```typescript
class Demo{
    public static void main(String args[]){
        int arrayOne[]={6, 2, 3, 4, 5};
        int indexOne;
        for(indexOne=0;indexOne<arrayOne.length;indexOne++){
            if(arrayOne[indexOne]%2!=0){
                indexOne++;
                break ;
            }
            else{
                indexOne++;
                continue;
            }
        }
        System.out.println(indexOne);
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 3

</details>


**Question 5:** What is the output of the given code snippet? 

```typescript
class Demo{
    public static void main(String args[]){
        int arrayOne[]={1, 2, 3, 4,5};
        int indexOne;
        for(indexOne=0;indexOne<arrayOne.length;indexOne++){
            if(arrayOne[indexOne]==1 || arrayOne[indexOne]%2==0){
                continue ;
            }
            else{
                indexOne++;
                break;
            }
        }
        System.out.println(indexOne);
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 3

</details>

## <h1 align="center">Local Date and Time</h1>

**Question 1:** Choose the option that converts Date class object to date in string format in Java?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: SimpleDateFormat obj = new SimpleDateFormat("yyyy-mm-dd");<br>
obj.format(new Date());

</details>


**Question 2:** Choose the option that creates a LocalDate object representing the date March 16, 2023?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: LocalDate.of(2023, 3, 16)

</details>


**Question 3:** Choose the option that converts the date in string format to a Date class object in Java?

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: SimpleDateFormat obj = new SimpleDateFormat("yyyy-MM-dd");<br>
obj.parse(new Date());

</details>


**Question 4:** What is the output of the given code snippet?

```typescript
class Demo{
    public static void main(String args[]){
        LocalDateTime currentDateTime = LocalDateTime.now();
        LocalDate specificDate = LocalDate.of(2023, Month.JANUARY, 25);
        Period period = Period.between(specificDate, currentDateTime.toLocalDate());
        System.out.println(period);
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: P2M5D

</details>


**Question 5:** Choose the option that represents the MOST appropriate definition of LocalTime class 

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: time without date

</details>

## <h1 align="center">Exceptions/Assertions</h1>

**Question 1:** What is the output of the given code snippet?

```typescript
public class Demo{
    public static void main(String args[]){
    	try{
	        try{
	            System.out.println("Inner Try block");
	            int[] numArr = {1, 2, 3, 4};
	            System.out.println(numArr[4]/0);           
	        }
	        catch(ArithmeticException e){
	            System.out.println("Arithmetic Exception");
	        }
	        catch(Exception e){
	            System.out.println("Some error Inside");
	        }
    	}
    	catch(Exception e){
            System.out.println("Some error Outside");
        }
        finally{
            System.out.println("Outer Finally block");
        } 
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Inner Try block<br>
Some error Inside<br>
Outer Finally block

</details>

**Question 2:** What is the output of the given code snippet?

```typescript
public class Demo {
    public static void main(String arg[]){
        try{
            System.out.print("A");
            System.out.print("B");
            int num = 99/0;  
        }
        catch(ArithmeticException e){
            System.out.print("C");
        }
        finally{
            System.out.print("D");
        }    
        System.out.print("E");
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ABCDE

</details>

**Question 3:** What is the output of the given code snippet?

```typescript
public class Demo{
    public static void main(String args[]){
    	try{
	        try{
	            System.out.println("Inner Try block");
	            int[] numArr = {1, 2, 3, 4};
	            System.out.println(numArr[5]);           
	        }	       
	        catch(ArithmeticException e){
	            System.out.println("Arithmetic Exception");
	        }
	        finally{
	            System.out.println("Inner Finally block");
	        } 
    	}
    	catch(IndexOutOfBoundsException e){
            System.out.println("Index Out Of Bounds Exception");
        }
        finally{
            System.out.println("Outer Finally block");
        } 
    	System.out.println("Outside");
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Inner Try block<br>
Inner Finally block<br>
Index Out Of Bounds Exception<br>
Outer Finally block<br>
Outside

</details>

**Question 4:** What is the output of the given code snippet?

```typescript
public class Demo{
    public static void main(String args[]){
    	try{
	        try{
	            int[] numArr={1, 2, 3, 4};
	            String str1=null;
	            System.out.println(numArr[2]/str1.length());           
	        }
	        catch(ArithmeticException e){
	            System.out.println("Arithmetic Exception");
	        }
	        catch(NullPointerException e){
	            System.out.println("Inner Null Pointer Exception");
	        }
	        finally{
	            System.out.println("Inner Finally block");
	        } 
    	}
    	catch(NullPointerException e){
              System.out.println("Outer Null Pointer Exception");
        }
        finally{
              System.out.println("Outer Finally block");
        } 
    	System.out.println("Outside");
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Inner Null Pointer Exception<br>
Inner Finally block<br>
Outer Finally block<br>
Outside

</details>

**Question 5:** What is the output of the given code snippet?

```typescript
public class Demo{
    public static void main(String args[]){
        try{
            System.out.println("A");
            int[] num = {1, 2, 3, 4};
            System.out.println(num[num.length]);
            System.out.println("B");
        }
       catch(NullPointerException e){
            System.out.println("C");
        }
        finally{
            System.out.println("D");
        }    
        System.out.print("E");
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: A<br>
D<br>
Runtime Exception: ArrayIndexOutOfBoundsException

</details>

## <h1 align="center">Inheritance</h1>

**Question 1:** What is the output of the given code snippet?

```typescript
class Camera{
    private String brand;
    private int cost;
    public Camera(){
        this.brand = "Nikon";
    }
    public Camera(String brand, int cost){
        this.brand = brand;
        this.cost = cost;
    }
    public String getBrand(){
        return this.brand;
    }
    public int getCost(){
        return this.cost;
    }
}
class MirrorlessCamera extends Camera{
    private int memory;
    MirrorlessCamera(String brand, int cost){
        super(brand,cost);
        this.memory = 16;
    }
    public static void main(String args[]){
        MirrorlessCamera camera = new MirrorlessCamera("Fujifilm", 100000);
        System.out.println("Brand: "+ camera.getBrand()+", Cost: "+ camera.getCost()+", Memory: "+ camera.memory);
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Brand: Fujifilm, Cost: 100000, Memory: 16

</details>

**Question 2:** What is the output of the given code snippet?

```typescript
class Certificate{
	private String certificationName;
	private double price;
	public Certificate(){
		this.certificationName+="Java ";
		this.price=5000;
	}
	public Certificate(String certificationName,double price){
		this();
		this.certificationName=certificationName;
		this.price=price;
	}
	public String getCertificationName(){
		return certificationName;
	}
	public double getPrice(){
		return price;
	}
}
class CertificateExam extends Certificate{
	private int examCode;
	public CertificateExam(String certificationName,double price,int examCode){
		super(certificationName,price);
		this.examCode=examCode;   
	}
	public void display(){
		System.out.println(getCertificationName()); 
		System.out.println(getPrice());
		System.out.println(this.examCode);
	}
}
class Demo{
	public static void main(String args[]){
		CertificateExam examDetailsObject=new CertificateExam("Programming",4500,70483);
		examDetailsObject.display();       
	}
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Programming  <br>
4500.0  <br>
70483

</details>

**Question 3:** What is the output of the given code snippet?

```typescript
class Shape{
    public void disp(){
         System.out.println("Disp in Shape class");
    }
}
class Rectangle extends Shape{
    public void disp(){
        System.out.println("Disp in Rectangle class");
   }
}
class Demo{
    public static void main(String args[]){
         Shape obj=new Rectangle();
         obj.disp();
         obj=new Rectangle();
         obj.disp();
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Disp in Rectangle class<br>
Disp in Rectangle class

</details>

## <h1 align="center">Strings/Wrapper classes/Generics</h1>

**Question 1:** What is the output of the given code snippet?

```typescript
class Demo{
    private static String checkString(String str){
        if(str==null){
            return("NA");
        }
        int length = str.length();
        for(int ind=0; ind<length/2; ind++){
            if(str.charAt(ind) != str.charAt(length-ind-1)){
                          return("NA");
            }
        }
        return(str.substring(0,length/2)+str.charAt(length-1));
    }
    public static void main(String args[]){
        String str1="LeveL";
        String res=checkString(str1);
        if(!(res.equals("NA"))){
            String result=res.replace(res.charAt(0),'Z');
            System.out.println(result);
        }
        System.out.println();
    }
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: ZeZ

</details>

**Question 2:** What is the output of the given code snippet?

```typescript
class Demo{
    public static void main(String args[]){ 
        String stringOne="Infosys "; 
        String stringTwo="Campus"; 
        String stringThree=stringOne.concat(stringTwo); 
        String stringFour=new String("infosys campus");
        stringThree.toLowerCase();
        if(stringThree.equals(stringFour)){
            System.out.println("Equal");
        }
        else if(stringThree==stringFour){
            System.out.println("Equal");
        }
        else{
            System.out.println("Not Equal");
        }
        System.out.println(stringThree); 
    } 
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Not Equal<br>
Infosys Campus

</details>

**Question 3:** What is the output of the given code snippet?

```typescript
class Demo{
	public static void main(String args[]){  
		String stringOne="Java ";  
	    String stringTwo="Programming";  
	    String stringThree=stringOne.concat(stringTwo.substring(0,7).toUpperCase()); 
	    stringThree.toLowerCase();
	    System.out.println(stringThree.charAt(6));
	}
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: R

</details>

**Question 4:** What is the output of the given code snippet?

```typescript
class Demo{
	 public static void main(String args[]){  
	   	 String s1="Sachin ";  
		 String s2="Tendulkar";  
	   	 String s3=s1.concat(s2); 
		 String s4=new String("Sachin tendulkar");
		 if(s3.equals(s4)){
			 System.out.println("Equal");
	  	 }
		 else if(s3==s4){
			 System.out.println("Equal");
		 }
		 else{
			 System.out.println("Not Equal");
		 }
	   	 System.out.println(s3);  
	 }  
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: Not Equal<br>
Sachin Tendulkar

</details>

## <h1 align="center">Collections</h1>

**Question 1:** What is the output of the following code snippet?

```typescript
public class Demo{
	public static void main(String args[]){
		TreeMap<Integer,String> TM=new TreeMap<Integer,String>();
		TM.put(1,"JAVA");
		TM.put(2,"Python");
		TM.put(4, "Ruby on Rails");
		TM.put(3,"C#");		
		System.out.println(TM.lastEntry());
	}
}
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: 4=Ruby on Rails

</details>

**Question 2:** What is the output of the given code snippet?

```typescript
List<Integer> list = new LinkedList<>();
list.add(10);
list.add(20);
list.add(2,30);
list.add(3,40);//Line1
System.out.println(list);
```

Assumption: All necessary import statements are provided

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: [10, 20, 30, 40]

</details>

**Question 3:** Consider the code snippet:

```typescript
List<Integer> list = new ArrayList<>();
list.add(10);
list.add(30);
list.add(20);
list.add(60);
list.add(65);
list.remove(1);
list.set(2, 55);
list.remove(2);
Set<Integer> set = new HashSet<>(list);
Map<Integer, Integer> map = new HashMap<>();
for(int index = 0; index < list.size(); index++){
	map.put(index, list.get(index));
}
map.put(3, 35);
```

<details> <summary><b>🔍 View Answer</b></summary>
✅ Answer: {0=10, 1=20, 2=65, 3=35}

</details>
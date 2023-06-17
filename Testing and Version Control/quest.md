# Testing and Version Control

## Unit Testing

### Q1. Which of these properties are depicted by a unit in unit testing?​ (Multiple correct)

1. “A unit is the smallest piece of testable software in the application, which can be isolated from the rest of the code, and can be run and tested independently.”
2. A unit is an independent entity in the program, which means it doesn’t depend on other units in the program.
3. A unit can be a collection of methods in the class.
4. A unit can be a variable.

> ✓ Correct : **1**
>
> Feedback:
> _A unit is a small part that can be tested independently from the rest of the code in the software._

> ✓ Correct : **2**
>
> Feedback:
> _A unit should work independently of other units of the program._

> ✓ Correct : **3**
>
> Feedback:
> _A collection of methods in the class or performing similar functionalities can be depicted as a unit in the code._

### Q2. Given a Java program in which you have an array of size 10 declared in the manner:

**Int a[10], which of the following lines of code will be safe to run?**

1. if ( i >=0&&i<10) a [ i ] =0;
2. if ( i ==10) a [ i ] =0;
3. if(i<0) a[i]=0;
4. if(i>9) a[i]=0;

> ✓ Correct : **1**
>
> Feedback:
> _When we declare an array of size 10, its indices lie in the range 0-9, so it is safe to access any element from the range 0-9 of the array._

### Q3. In a certain loop statement, say, for(i=0; i<100; i++) //code, at which parts should the code be tested to ensure that the edge cases have been considered?

1. At the centre of the loop, i.e i=50
2. At each iteration of the loop
3. At the end cases of the loop, i.e 0 and 100
4. None of the above

> ✓ Correct : **3**
>
> Feedback:
> _Usually, a loop shows peculiar behaviour only at the beginning and ending values of the index (because the loop begins and ends at those points). So, it is always good to check the cases at the beginning and end of the loop._

### Q4. In the code below, what can’t be considered a unit for unit testing?

```
class A {
  int a, b;

  int mul(int a, int b) {
      return a * b;
  }

  int add(int a, int b) {
      return a + b;
  }

  int sub(int a, int b) {
      return a - b;
  }
}
```

1. mul function
2. add function
3. class A
4. int a

> ✓ Correct : **4**
>
> Feedback:
> _A variable can’t be considered a unit for unit testing, so this is an incorrect choice._

### Q5. Imagine that your coworker tells you certain things about unit testing, and he happens to mention the following points in his description. What, according to you, among the things he said are correct about unit testing?​​​​​​ (Multiple Correct)

1. Bugs/errors can be detected early in the development cycle with unit testing.
2. Integration of units becomes difficult if a software is unit tested.
3. Unit tests help facilitate code changes that may be required at later development stages. This is because you can be confident about the alterations if the code changes do not break the unit tests.
4. Changes at a later stage are hard to incorporate if the software is unit tested.

> ✓ Correct : **1**
>
> Feedback:
> _When you test the software beforehand, the chances of catching a bug earlier in the development cycle are high and, thus, you can make changes to the software appropriately to fix the issue._

> ✓ Correct : **3**
>
> Feedback:
> _It becomes relatively easy to incorporate changes later in the software life cycle if the software is unit tested. This is because unit tests will give you confidence in the changes if they do not break the unit tests._

### Q6. Let’s recall the previous scenario where your coworker has written a unit test case that is fast and always returns the same result. But the unit test is brittle and hard to maintain. Every time you change the code, you will have to change the unit test so that the unit test works correctly. This is not a good unit test case. Can you tell which of the characteristics of a good unit test case it is violating? ​​​

1. The unit test case is not fast.
2. The unit test case is not trustworthy.
3. The unit test case is not maintainable.

> ✓ Correct : **3**
>
> Feedback:
> _Every time the code is changed, the unit test case needs to be changed, so it is not maintainable._

### Q7. Given below is the program for a simple calculator. Suppose we write a test case to check for the value of num as -2. What type of scenario is this?

```
import java.lang.Math
public class Calculator {
   public static int sqrRoot(int num){
       return Math.sqrt(num)
   }

   public static void main(String[] args) {
       Scanner scan = new Scanner(System.in);
       System.out.println("Enter the number:");
       int num = scan.nextInt();
       if(num<0){
           System.out.println("Invalid input");
       }
       else{
           System.out.println(sqrRoot(num));
       }
   }
}
```

1. Fail case scenario
2. Pass case scenario
3. Edge case scenario

> ✓ Correct : **1**
>
> Feedback:
> _The intended purpose of the code is to accept positive integers and calculate the square root of the given number. The given number is negative and is hence passing -2. This is because the input will lead to a fail case scenario. Thus, this option is correct._

### Q8. Given below is the program for a simple calculator. Suppose we write a test case to check for the value of num as 0. What type of scenario is this?

```
import java.lang.Math
public class Calculator {
   public static int sqrRoot(int num){
       return Math.sqrt(num)
   }

   public static void main(String[] args) {
       Scanner scan = new Scanner(System.in);
       System.out.println("Enter the number:");
       int num = scan.nextInt();
       if(num<0){
           System.out.println("Invalid input");
       }
       else{
           System.out.println(sqrRoot(num));
       }
   }
}
```

1. Fail case scenario
2. Pass case scenario
3. Edge case scenario

> ✓ Correct : **3**
>
> Feedback:
> _An edge case scenario occurs when the given input acts as a bridge between fail case scenario inputs and pass case scenario inputs. Here, if any number less than 0 is passed, it is a fail case scenario and if any number greater than or equal to 0 is passed, it is a pass case scenario. Since 0 falls at the edge, it's an edge case scenario._

### Q9. A certain function of the code, IsValidYear(int year), checks if the given year lies in the range 1901-2018 and returns true if the given condition is met, otherwise, it returns false.The assertions for this test are as follows. Which of the following test cases would run to be true?

1. Assertions.assertEquals(true,IsValidYear(1900));
2. Assertions.assertEquals(true,IsValidYear(200));
3. Assertions.assertEquals(false,IsValidYear(2017));
4. Assertions.assertEquals(true,IsValidYear(2017));

> ✓ Correct : **4**
>
> Feedback:
> _IsValidYear(2017) returns true, and the other parameter passed to assertEquals is also true. So, they match and, thus, the test case passes._

### Q10.

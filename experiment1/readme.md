# EXPERIMENT 1
## TITLE : 1a.) Display primitive datatypes
```
 class DefaultPrimitiveType {
    int primInt;
    double primDouble;
    char primChar;
    float primFloat;
    long primLong;
    boolean primBoolean;
     public static void main(String args[]) {
      DefaultPrimitiveType dDpt= new DefaultPrimitiveType();
       System.out.println("Default value of int:"+dDpt.primInt);
       System.out.println("Default value of double:"+dDpt.primDouble);
       System.out.println("Default value of char:"+dDpt.primChar);
       System.out.println("Default value of float:"+dDpt.primFloat);
       System.out.println("Default value of long:"+dDpt.primLong);
       System.out.println("Default value of boolean:"+dDpt.primBoolean);
       }
      }
```
# OUTPUT
![output of primitive datatypes](exp1a.png)
## TITLE : 1b.) qudratic equation
```
  GNU nano 8.7                                                        quadraticequation.java
import java.util.Scanner;
public class QuadraticEquation {
public static void main(String[] args) {
Scanner sc=new Scanner(System.in);
System.out.print("Enter value of a:");
double a=sc.nextDouble();
System.out.print("Enter value of b:");
double b = sc.nextDouble();
System.out.print("Enter value of c:");
double c = sc.nextDouble();
double D = b*b-4*a* c;
if (D > 0) {
System.out.println("Roots are real and distinct.");
double root1 = (-b + Math.sqrt(D))/(2*a);
double root2 = (-b-Math.sqrt(D))/(2*a);
System.out.println("Root 1:"+root1);
System.out.println("Root 2:"+root2);
} else if (D==0) {
System.out.println("Roots are real and equal.");
double root=-b/(2*a);
System.out.println("Root:"+root);
} else {
System.out.println("Roots are complex and imaginary.");
double realPart =-b/(2*a);
double imaginaryPart = Math.sqrt(-D) / (2 * a);
System.out.println("Root1:"+realPart+"+"+imaginaryPart+"i");
System.out.println("Root2:"+realPart+"-"+imaginaryPart+"i");
}
}
}
```
# output
![output of quadratic equation](exp1b.PNG)

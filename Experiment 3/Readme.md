## title : 3a) implement constructor overloading java

```
class Student {
        String name;
        int age;
        double marks;
        Student() {
        }
        Student(String name,int age,double marks) {
                this.name = name;
                this.age = age;
                this.marks = marks;
                }
                void display() {
                System.out.println("name:" +name);
                System.out.println("age:" +age);
                System.out.println("marks:" +marks);
                }
             }
}

class main {
     public static void main(String args[]) {
            Student std = new Student();
             std.display();
            Student std1 = new Student("yasmi", 12,400);
             std1.display();
         }
}
```
#output
![output of implement constructor overloding java](exp3a.png)


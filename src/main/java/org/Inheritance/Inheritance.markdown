# The Inheretance
### Inheretance means creating new class using old class
there are 5 types:\
1.single inheretance\
2.Mulit level inheritance\
3.hierarchical inheritance\
4.Multiple inheritance\
5.Hybrid Inheritance


## Single Inheritance
 here there is only one level. this is normal parent and child class\

```java
class parent{
   int x=10;
   public void method1(){
   System.out.println("parent class");
   }
}

class Child extends parent{
    int y=0;
    public void method(){
        System.out.println("this is child class");
    }
}
public class  Main{
    public static void main(String[] args) {
       Child child= new Child();
        System.out.println(child.method1());
        System.out.println(child.method());
       
    }
}
```
``` output
parent class
child class
```

## Multi level Inheritance
When a class is act as base class to dervied class and this derived class also acts as
base class to another class then we can say it is multi level

![](2-660x329.jpg)
````java
class SuperParent{
    public  void SuperParentClassMethod(){
        System.out.println("This is SuperParentClass method");
    }
    public void add(){
        System.out.println(2+3);
    }
}

class parent extends SuperParent {
    
}

````
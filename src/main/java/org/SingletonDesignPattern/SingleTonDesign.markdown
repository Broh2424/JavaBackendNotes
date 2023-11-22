# SingleTon DesignPattern

When we want to restrict the class to make object only once by
making  instance of a class in class itself and creating method to call that 
single object.This type approach is called Singleton Design Pattern


## Steps to achieve Singleton design:
1. refernce variable in the class must be:
    - private 
    - static
    - and final
2. Constructor must be private
3. one public method should be there for accessing the object.
## Types of singleton design pattern  approach:

1.Eager Intialization.\
2.Using Static Block\
3.Lazy Initalization\
4.Lazy initialization with Double check locking
## 1.Eager Intialization(without having any multithreading envi)


````java
class Singleton {
    private static final Singleton singletonReferance = new Singleton();

    private Singleton() {
        // private constructor which cannot be accessed 
    }

    public static Singleton getSingleton() {
        System.out.println();
        return singletonReferance;
    }
}
public class Main{
    public static void main(String[] args) {
        
    }
}

````
### Drawbacks
* here every time a single object is created when classs is loaded.
* Memory is wasted because instance of class is created every time.
* Exception handling is not possible.

## 2.Using Static Block

````java
class Singleton {
    private static final Singleton singletonReferance;

    private Singleton() {

    }

    static {
        instance = new Singleton();
    }

    public static Singleton getInstance() {
        return singletonReferance;
    }
}


````

## 3. Lazy initialization:

````java

class Singleton {
   private static final Singleton singletonReferance;

   private Singleton() {

   }

   public static Singleton getSingletonInstance() {
       if(singletonReferance==null){
           singletonReferance=new Singleton();
       }
      return singletonReferance;
   }
}
````

## 4. Thread safe Singlton:

````java

class Singleton {
   private static final Singleton singletonReferance;

   private Singleton() {

   }

   synchronized public static Singleton getSingleton() {
       if(singletonReferance==null){
           singletonReferance= new Singleton();
       }
      return singletonReferance;
   }
}


````
### Drawbacks:
   1. In multithreading overhead is an issue, it means
      sometimes one thread stops execution in the middle (it creates  object but before assiging it stops)
      and if another thread is there it will start execute




## 5. lazy intialization with back locking:

```java

class Singleton {
   private static final Singleton singletonReferance;

   private Singleton() {

   }

   public static Singleton getSingletonInstance() {
      if(singletonReferance==null){
          synchronized (Singleton.class){
              singletonReferance=new Singleton();
          }
      }
      return  singletonReferance;
   }
}



```


## 6.Bill Pugh Singleton Implementation:
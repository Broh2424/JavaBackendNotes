# SingleTon DesignPattern

When we want to restrict the class to make object only once by
making  instance of a class in class itself and creating method to call that 
single object.

1.Eager Intialization.\
2.Using Static Block\
3.Lazy Initalization\
4.Lazy initialization with Double check locking
### Eager Intialization(without having any multithreading envi)


````java
class Singleton {
    private static final Singleton singletonInstance = new Singleton();

    private Singleton() {
        // private constructor which cannot be accessed 
    }

    public static Singleton getSingleton() {
        System.out.println();
        return singletonInstance;
    }
}
public class Main{
    public static void main(String[] args) {
        
    }
}

````
## Drawbacks
* here every time a single object is created when classs is loaded.
* Memory is wasted because instance of class is created every time.
* Exception handling is not possible.


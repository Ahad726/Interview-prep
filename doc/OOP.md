## Object Oriented Programming 

### Polymorphism
Polymorphism is a fundamental concept in object-oriented programming (OOP) that allows <span style="color:blue">objects of 
different classes to be treated as if they are of the same type.</span> This is achieved through inheritance and 
the use of overriding and overloading methods. Polymorphism allows for code reusability and simplifies 
code maintenance, as it enables a single interface to be used to represent different types of objects.

Polymorphism solves the problem of having to write separate code for every possible type of object 
that we might want to work with. Instead, we can define a base class or interface that defines common behavior,
and then write code that works with variables of that base type. By using polymorphism, we can write more 
**flexible and extensible** code that can work with a wide range of <span style="color:red">different objects without having to know the 
exact type of each object at compile time.</span>

```c#
sing System;

class Animal {
    public virtual void MakeSound() {
        Console.WriteLine("The animal makes a sound");
    }
}

class Dog : Animal {
    public override void MakeSound() {
        Console.WriteLine("The dog barks");
    }
}

class Cat : Animal {
    public override void MakeSound() {
        Console.WriteLine("The cat meows");
    }
}

class Program {
    static void Main(string[] args) {
        Animal myAnimal = new Animal();
        Animal myDog = new Dog();
        Animal myCat = new Cat();
    

        Zoo(myAnimal);        // Outputs "The animal makes a sound"
        Zoo(myCat);          // Outputs "The cat meows"
        Zoo(myDog);          // Outputs "The dog barks"
    }

    static void Zoo(Animal animal){
    
        animal.MakeSound();
    }
}
```




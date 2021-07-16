# Inheritance & Polymorphism

What do we want with inheritance?

1. Keep common behavior in one class
2. Split different behavior into separte classes
3. Keep all of the objects in a single data structure. 


**Rule of thumb: Make member variables private and methods either public or private0**
- public: can accesss frome any class

- private: can access from same class

- protected: can access from same class; can accesss from same package; can acess from **any subclass**;

- package: can access from same class; can access from same package  :star2: :star2: :star2: package loses access by any sub class: the sub-class outside the package, you lose acess to the package :star2: :star2: :star2:

**Rule of thumb: always use either public or private** 

## Compiler rule for class construction

Rule #1 
No superclass? Compiler inserts: ```extends Ojbect ```
![image](https://user-images.githubusercontent.com/56880104/125877540-1ff973e9-69aa-4c3f-8810-9d1ed85bd678.png)

Rule #2 
No constructor? Java gives you one default constructor with no argument for you. ```public Person(){}```

![image](https://user-images.githubusercontent.com/56880104/125877664-fab07616-ac2d-48f5-a101-da005f714806.png)

Rule #3

Need to call super's default constructor.

![image](https://user-images.githubusercontent.com/56880104/125877853-65e5650a-8456-4969-8a17-dcc0e9949211.png)


![image](https://user-images.githubusercontent.com/56880104/125877876-cc516e53-b9df-49cc-8c9e-16f83d4a217e.png)


## Variable initialize in a Class Hierarchy
* super() has to be the first line! 

* :star: Initialize *name* variable in the Student class. OR "how to initialize name without a public setter??? 🌟

![image](https://user-images.githubusercontent.com/56880104/125878766-2673ce2f-eed2-430e-8563-e6b030d372d9.png)

( variable *name* is private, so *"this"* will NOT work)

* Add "No-argument" default constructor in the studnet class:

![image](https://user-images.githubusercontent.com/56880104/125879065-9a2b8de1-10be-457b-9139-2d645c8ffad5.png)


## Overriding

![image](https://user-images.githubusercontent.com/56880104/125892249-20317f6f-85dc-42fa-898b-af1bc7dba5b1.png)

![image](https://user-images.githubusercontent.com/56880104/125892991-c8e7ef43-2ac0-42b2-b919-53b11893ddbb.png)


## Polymorphism

```java
Person p[] = new Person[3];
p[0] = new Person("Tim");
p[1] = new Student("Cara",1234);
p[2] = new Faculty("Mia", "ABCD");

for (int i=0; i<p.length; i++){
  System.out.println(p[i]);
  }
```

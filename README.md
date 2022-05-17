# C-Concepts
### Table of Contents
#### [Mindmap](#Mindmap)
1. [Access Control](#Access-Control)
2. [Classes](#Classes)
3. [Class Scope](#Class-Scope)
4. [Constructor Functions](#Contructor-Functions)
5. [Data Members](#Data-Members)
6. [Default Arguments](#Default-Arguments)
7. [Destructor Functions](#Destructor-Functions)
8. [Encapsulation](#Encapsulation)
9. [File Scope](#File-Scope)
10. [Function Members](#Function-Members)
11. [Function Scope](#Function-Scope)
12. [Inheritance](#Inhertance)
13. [Name](#Names)
14. [Namespace](#Namespace)
15. [Objects](#Objects)
16. [Operator Functions](#Operator-Functions)
17. [Overloading](#Overloading)
18. [Pointers](#Pointers)
19. [Polymorphism](#Polymorphism)
20. [References](#References)
21. [Signatures](#Signatures)
22. [Structures](#Structures)
23. [Sub-types](#Sub-types)
24. [Super-types](#Super-types)
25. [Virtual Functions](#Virtual-Functions)
26. [Visibility](#Visibility)
## Access Control
Access Control specifiers define how the members (attributes and methods) of a class can be accessed. In C++, there are three access control specifiers:
- public: members are accessible & modified from outside the class
- private: members cannot be accessed (or viewed) from outside the class
- protected: members cannot be accessed from outside the class, however, they can be accessed in inherited classes.

```c++
class Class {
	private:
		int privateVariable;

	public: 
		int publicVariable;

	protected:
		int protectedVariable;
	
};

```
## Class 
A class in C++ is the building block that leads to Object-Oriented programming. It is a user-defined data type, which holds its own data members and member functions, which can be accessed and used by creating an object of that class.

For Example: Consider the Class of Cars. There may be many cars with different names and brand but all of them will share some common properties like all of them will have 4 wheels, Speed Limit, Mileage range etc. So here, Car is the class and wheels, speed limits, mileage are their properties.

```c++
// General Class Structure
class Class {
	private:
		int dataMember;

	public:
		void classFunction() {
		
		}
};
```

## Class Scope
When the scope of a declaration extends to or past the end of a class definition, the regions defined by the member definitions of that class are included in the scope of the class. Members defined lexically outside of the class are also in this scope. In addition, the scope of the declaration includes any portion of the declarator following the identifier in the member definitions.

The name of a class member has class scope and can only be used in the following cases:
- In a member function of that class
- In a member function of a class derived from that class
- After the . (dot) operator applied to an instance of that class
- After the . (dot) operator applied to an instance of a class derived from that class, as long as the derived class does not hide the name
- After the -> (arrow) operator applied to a pointer to an instance of that class
- After the -> (arrow) operator applied to a pointer to an instance of a class derived from that class, as long as the derived class does not hide the name
- After the:: (scope resolution) operator applied to the name of a class
- After the:: (scope resolution) operator applied to a class derived from that class

## Constructor function

A constructor is a special type of member function of a class which initializes objects of a class. In C++, Constructor is automatically called when object(instance of class) is created. It is special member function of the class because it does not have any return type.

```c++
class Dog {
	public:
		Dog(); // Constructor Function
}


int main() {
	Dog dog;

	return 0;
};
```

## Data Members

Data members include members that are declared with any of the fundamental types, as well as other types, including pointer, reference, array types, bit fields, and user-defined types. You can declare a data member the same way as a variable, except that explicit initializer are not allowed inside the class definition. However, a const static data member of integral or enumeration type may have an explicit initializer. A class X cannot have a member that is of type X, but it can contain pointers to X, references to X, and static objects of X. 

```c++
class Student {
    private:
        int id; // Data Member
}

```

## Default Argument

A default argument is a value provided in a function declaration that is automatically assigned by the compiler if the caller of the function doesn't provide a value for the argument with a default value. In case any value is passed the default value is overridden.

```c++

void point(int x = 2, int y = 3);

point(); // This will call as point(2, 3)

```

## Dynamic Allocation

A good understanding of how dynamic memory really works in C++ is essential to becoming a good C++ programmer. Memory in your C++ program is divided into two parts −

- The stack − All variables declared inside the function will take up memory from the stack.
- The heap − This is unused memory of the program and can be used to allocate the memory dynamically when program runs.

Many times, you are not aware in advance how much memory you will need to store particular information in a defined variable and the size of required memory can be determined at run time.

```c++
char* pvalue  = NULL;         // Pointer initialized with null
pvalue  = new char[20];       // Request memory for the variable

delete [] pvalue;             // Delete array pointed to by pvalue

double** pvalue  = NULL;      // Pointer initialized with null 
pvalue  = new double [3][4];  // Allocate memory for a 3x4 array

delete [] pvalue;            // Delete array pointed to by pvalue

```

## Encapsulation
```c++
class Obj {
	private:
		// data is hidden from outside world
		int x;
	public:
		void set(int a) {
			x = a;	
		}

		int get() {
			return x;
		}
}


int main() {
	Obj obj;

	obj.set(5);

	int x = obj.get();


};
```

## File Scope
```c++
static int nValue // file scoped variable
float fValue; // global variable

int main() {
	double dValue;
};

```

## Function Members
```c++
class Student {
	private:
		int id;

	public:
		void setID(int newId) { // function member
			id = newId;
		}
};

```

## Function Scope
```c++
class Student {
	private:
		int id;
		void getGrade() { // function only can be accessed in class
		}

	public:
		void setID(int newId) { // function access to anyone
			id = newId;
		}
};

```

## Inheritance
```c++
class Shape {

};

class Rectangle: public Shape {

};
```
## Names 
```c++

int minutes = 60; // minutes is the name of the int

```

## Namespaces
```c++
namespace namespace_name {

}

name::code // code could be variabel or function
```

## Objects 
```c++
class Student {

}

struct Teacher {

}
```

## Operator Functions
```c++
 Box operator+(const Box& b) {
	Box box;
    box.length = this->length + b.length;
    box.breadth = this->breadth + b.breadth;
    box.height = this->height + b.height;
    return box;
}
```

## Overloading
```c++
void print(int i) {
	cout << i;
}

void print(double f) {
	cout << f;
}

void print(char* c) {
	cout << c;
}
```

## Pointer
```c++
string food = "Hamburger";

cout << &food; // Outputs the memory address of food 
```

## Polymorphism

The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed in more than one form.

These polymorphisms has four types. Such as:

- Subtype polymorphism is also known as runtime polymorphism.

- Parametric polymorphism is also known as compile-time polymorphism.

- Ad-hoc polymorphism is also known as overloading.

- Coercion is also known as (implicit or explicit) casting.


```c++
```

## Reference

When a variable is declared as a reference, it becomes an alternative name for an existing variable. A variable can be declared as a reference by putting '&' in the declaration.

```c++
int main(){

  int x = 10;

  int & ref = x; // ref is a reference to x.

  ref = 20; // Value of x is now changed to 20

  cout << "x = " << x << '\n';

  x = 30; // Value of x is now changed to 30

  cout << "ref = " << ref << '\n';

  return 0;
}

```

## Scope
When you declare a program element such as a class, function, or variable, its name can only be "seen" and used in certain parts of your program. The context in which a name is visible is called its scope. For example, if you declare a variable x within a function, x is only visible within that function body. It has local scope. You may have other variables by the same name in your program; as long as they are in different scopes, they do not violate the One Definition Rule and no error is raised. There are six kinds of scope:

Global scope: A global name is one that is declared outside of any class, function, or namespace. However, in C++ even these names exist with an implicit global namespace.

Namespace scope: A name that is declared within a namespace, outside of any class or enum definition or function block, is visible from its point of declaration to the end of the namespace.

Local scope: A name declared within a function or lambda, including the parameter names, have local scope. They are often referred to as "locals". They are only visible from their point of declaration to the end of the function or lambda body.

Class scope: Names of class members have class scope, which extends throughout the class definition regardless of the point of declaration. Class member accessibility is further controlled by the public, private, and protected keywords. Public or protected members can be accessed only by using the member-selection operators (. or ->) or pointer-to-member operators (.* or ->*).

Statement scope: Names declared in a for, if, while, or switch statement are visible until the end of the statement block.

Function scope: A label has function scope, which means it is visible throughout a function body even before its point of declaration. Function scope makes it possible to write statements like goto cleanup before the cleanup label is declared.

## Signatures

Signatures are type abstractions or interfaces of classes. The main language constructs added are signatures and signature pointers.


```c++
signature S {
   int foo(void);
   int bar(int);
};
```

## Sub-types

The capability of a class to derive properties and characteristics from another class is called Inheritance. The class that inherits properties from another class is called Sub class or Derived Class.

```c++
class subclass_name:access_mode base_class_name {
//body of subclass
}
```

## Super-types

The class whose properties are inherited by sub class is called Base Class or Super class.

```c++
class super-class {
    //body of super class
};

class subclass_name:access_mode super-class {
    //body of subclass
};
```

## Virtual Functions

A virtual function is a member function which is declared within a base class and is re-defined by a derived class. When you refer to a derived class object using a pointer or a reference to the base class, you can call a virtual function for that object and execute the derived class's version of the function. They are mainly used to achieve Runtime polymorphism

Rules for Virtual Functions

1. Virtual functions cannot be static.
2. Functions are declared with a virtual keyword in base class.
3. A virtual function can be a friend function of another class.
4. Virtual functions should be accessed using pointer or reference of base class type to achieve runtime polymorphism.
5. The prototype of virtual functions should be the same in the base as well as derived class.
6. They are always defined in the base class and overridden in a derived class. It is not mandatory for the derived class to override.
7. A class may have virtual destructor but it cannot have a virtual constructor.


```c++
class base {
   public:
      virtual void print() {
         cout << "print base class\n";
      }
      
      void show() {
         cout << "show base class\n";
      }
};
```

## Visibility

When a base class is derived by a derived class with inheritance, the accessibility of base class by the derived class is controlled by visibility modes. The derived class doesn't inherit access to private data members. However, it does inherit a full parent object, which contains any private members which that class declares.

```c++
class A {

  public:

    int x;

  protected:

    int y;

  private:

    int z;

};

// Derived class, Class B will inherit Class A

class B: public A {

};

int main()

{

  B b;

  cout << b.x << endl; // x is public, so its value will be printed

  cout << b.y << endl; // y is protected, so it will give visibility error

  cout << b.z << endl; // z is not accessible from B, so it will give visibility error

};

```

![Untitled Diagram drawio](https://user-images.githubusercontent.com/53241212/165651243-64c0f732-a674-4f91-ad8f-c54aa600e02c.png)

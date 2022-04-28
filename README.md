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
```c++

```
## Constructor function
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
```c++
class Student {
	private:
		int id; // Data Member

}

```

## Default Argument
```c++

void point(int x = 2, int y = 3);

point(); // This will call as point(2, 3)

```

## Dynamic Allocation
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
```c++
```

## Reference
```c++
```

## Scope
```c++
```

## Signatures
```c++
```

## Sub-types
```c++
```

## Super-types
```c++
```

## Virtual Functions
```c++
```

## Visibility
```c++

```

![Untitled Diagram drawio](https://user-images.githubusercontent.com/53241212/165651243-64c0f732-a674-4f91-ad8f-c54aa600e02c.png)

# Const Keyword

‘const’ keyword stands for constant. In C++ it has so many usages to make some values constant throughout the program.
If we make an artifact of a C++ program as constant then its value cannot be changed during the program execution.
In C++, const keyword can be used in a number of ways as discussed below:

## Constant Variables
While declaring a variable as const it must be initialized as well. Once declared as const then we cannot change its value later on.
### Usage: 
forbidden any change in the value of the variable later.
### Ex:
int main
{

const int a = 10;

const int j = a + 10;     // works fine

a++;    // this leads to Compile time error   
}

---
If we try to change its value later, then C++ compiler will raise an error as below:

<span style="color: red"> error C3892: ‘a’ : you cannot assign to a variable that is const </span> 

## Const with Pointers
‘const’ keyword can be used in two possible ways with pointers:

•	We can make a pointer constant at time of declaration.

•	We can make the value constant to what the pointer is pointing to.


## Constant Pointers
Just like constant variable, the value of constant pointer is initialized at the time of declaration and once declared then we can’t change the pointer variable.
### Usage:
if we want a pointer variable to always point to the same variable, useful where you want a storage that can be changed in value but not moved in memory.
### Ex:

int x = 1;

int* const w = &x;

---
If we try to change its value later, then C++ compiler will raise an error as below:

<span style="color: red">error C3892: ‘w’ : you cannot assign to a variable that is const </span> 

## Pointer to Constant Variables

This means that the pointer is pointing to a const variable.
### Usage: 
This can be used to make any string or array immutable.
### Ex:
const int* u;

---
If we try to change its value later, then C++ compiler will raise an error as below:

<span style="color: red">error C2297: ‘u’ : illegal, right operand has type ‘const int *’</span>

## Constant Function Arguments
We can make the return type or arguments of a function as const. Then we cannot change any of them.
## Usage: 
Prevent modifying constant parameters or modifying the return of the function.

## Ex:
void f(const int i)
{

i++;    // error

}

const int g()
{

return 1;

}

## Constant Data Members of a Class

If we define a const data member of a class then we must have to initialize that data member through the constructor of the class not during initialization.

## Usage:
Not allowing the value of const data members to be changed through the object of the variable.

## Ex:

class Test {

const int i;

public:

Test(int x):i(x)
{

cout << "\ni value set: " << i;

}

};

int main()
{

Test t(10);

Test s(20);

}





## Constant Objects of a Class

When an object is declared or created using the const keyword, its data members can never be changed, during the object's lifetime.

### Usage:
Not allowing all the values of the class variables to be changed through the object of the variable.


### Ex:

const Test r(30);


# & Operator


## The Address Operator
The & is a unary operator that returns the memory address of its operand. For example, if var is an integer variable, then &var is its address. This operator has the same precedence and right-to-left associativity as the other unary operators.
You should read the & operator as "the address of" which means &var will be read as "the address of var".

### Usage:
Obtain the address of a variable

### Ex:
int x = 5;

int *ptr = &x;


## Pass by reference
When you use reference in the parameter of a function, any modifications that happen in the passed variable in the scope of the function will also be applied to the variable that has been passed in the main scope
### Usage:
Apply modification to variables from functions
### Ex:
void DoSomething(string& str)

## The Bitwise AND:
The bitwise AND operator (&) compares each bit of the first operand to that bit of the second operand. If both bits are 1, the bit is set to 1. Otherwise, the bit is set to 0. Both operands to the bitwise AND operator must be of integral types.

### Usage:
Compression, encryption and other applications which depend heavily on the bitwise algorithm.

### Ex:
unsigned short a = 0x5555;      // pattern 0101

unsigned short b = 0xAAAA;      // pattern 1010

cout << hex << ( a & b ) << endl;


## Declare a reference to a type
If you use & in the left-hand side of a variable declaration, it means that you expect to have a reference to the declared type. It can be used in any type of declarations (local variables, class members, method parameters).
### Usage:
To make variables point to the same place in the memory
### Ex:
std::string mrSamberg("Andy");

std::string& theBoss = mrSamberg;

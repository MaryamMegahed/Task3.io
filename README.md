# Report for const and &
## const
 const keyword is attached with any method(), variable, pointer variable, and with the object of a class it prevents that specific object/method()/variable to modify its data items value.
### Constant Variables:
There are some rules for the declaration and initialization of the constant variables:
•	The const variable cannot be left un-initialized at the time of the assignment.
•	It cannot be assigned value anywhere in the program.
•	Explicit value needed to be provided to the constant variable at the time of declaration of the constant variable.
Example 

```
const int y = 10;
```

### Const Keyword With Pointer Variables:
there are three possible ways to use a const keyword with a pointer
#### . the pointer variable point to a const value
Example
```
int main()
{
    int x{ 10 };
    char y{ 'M' };
    const int* i = &x;
    const char* j = &y;
     x = 9;
     y = 'A';
 }
```

Note that i and j are pointing to a memory location const int-type and char-type, but the value stored at these locations can be changed 
#### . the const pointer variable point to the value
```
data_type* const var_name;
```

Note  The values that are stored in the pointer are modifiable, but the locations that are pointed out by const-pointer variables where the values are stored aren’t modifiable. 

#### . the const pointer pointing to a const variable
```
const data_type* const var_name;
```
Here  you are neither allowed to change the const pointer variable nor the value stored at the location pointed by that pointer variable.
### Constant Methods:
the objects of a class can also be declared as const. An object declared as const cannot be modified and hence, can invoke only const member functions as these functions ensure not to modify the object.
Example

```
const Class_Name Object_name;
```
•	When a function is declared as const, it can be called on any type of object, const object as well as non-const objects.
•	Whenever an object is declared as const, it needs to be initialized at the time of declaration. However, the object initialization while declaring is possible only with the help of constructors.
There are two ways of a constant function declaration:
#### Ordinary const-function Declaration:

```
const void foo()
{
   //void foo() const Not valid
}                  
int main()
{
   foo(x);
} 
```
####  const member function of the class:
```
class
{
   void foo() const
   {
       //.....
   }
}
```
### Constant Function Parameters And Return Type:
#### For const parameter 
```
void foo(const int y)
{
    // y = 6; const value
    // can't be change
    cout << y;
}
int main()
{
    int x = 9;
    const int z = 10;
    foo(z);
    foo(x);
}
```
There is no substantial issue to pass const or non-const variable to the function
#### For const return type: 
 it returns a const integer value to us.
```
const int foo(int y)
{
    y--;
    return y;
}
 
int main()
{
    int x = 9;
    const int z = 10;
    cout << foo(x) << '\n' << foo(z);
 }
 ```
the value that will be returned by the function will be constant but There is no substantial issue to pass const or non-const variable to the function
#### For const return type and const parameter:
```
const int foo(const int y)
{
    // y = 9; it'll give CTE error as
    // y is const var its value can't be change
    return y;
}
int main()
{
    int x = 9;
    const int z = 10;
    cout << foo(x) << '\n' << foo(z);
}
```
Note :
both const and non-const values can be passed as the const parameter to the function, but we are not allowed to then change the value of a passed variable because the parameter is const
## Ampersand &
This operation  & has a lot of meanings and in each meaning has an applications :
### Applications of & : 
#### & to get the address of a variable
When using & on the right-hand side of a variable, it's known as the "address-of operator". if you put it in front of a variable, it'll return its address in the memory instead of it's value .It is useful for pointer declarations.
```
string mrSamberg=”Maryam”;
string* theBoss;
theBoss = &mrSamberg;
```
####  & to declare a reference to a type

When we use & in the left-hand side of a variable declaration then  the variable is declared as a reference, it becomes an alternative name for an existing variable
It can be used in any type of declarations (local variables, class members, method parameters).
```
    int x = 10;
  // ref is a reference to x.
  int& ref = x;
  // Value of x is now changed to 20
  ref = 20;
  cout << "x = " << x << endl;//x = 20
```
####  & as a bit-wise operator
It is the bitwise AND. This operator takes two numbers as inputs and the output is true only if the two inputs is true

#### && in a logical expression
&& comparing between two things In the logical expression ,if the two things their values is true then the output of the logical expression is true 

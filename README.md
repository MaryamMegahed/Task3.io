# Task3.io
## const
 const keyword is attached with any method(), variable, pointer variable, and with the object of a class it prevents that specific object/method()/variable to modify its data items value.
### Constant Variables:
There are some rules for the declaration and initialization of the constant variables:
•	The const variable cannot be left un-initialized at the time of the assignment.
•	It cannot be assigned value anywhere in the program.
•	Explicit value needed to be provided to the constant variable at the time of declaration of the constant variable.
Example 
>
const int y = 10;
>

### Const Keyword With Pointer Variables:
there are three possible ways to use a const keyword with a pointer
#### . the pointer variable point to a const value
Example
>
int main()
{
    int x{ 10 };
    char y{ 'M' };
    const int* i = &x;
    const char* j = &y;
     x = 9;
     y = 'A';
 }
>

Note that i and j are pointing to a memory location const int-type and char-type, but the value stored at these locations can be changed 
#### . the const pointer variable point to the value
>
data_type* const var_name;
>

Note  The values that are stored in the pointer are modifiable, but the locations that are pointed out by const-pointer variables where the values are stored aren’t modifiable. 

#### .const pointer pointing to a const variable
>
const data_type* const var_name;
>

Here  you are neither allowed to change the const pointer variable nor the value stored at the location pointed by that pointer variable.

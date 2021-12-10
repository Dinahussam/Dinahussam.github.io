# Const
const is attached with any method and variable and pointer and class object it prevents to
modify its data items value.
## Constant variables:-
Rules of declaration and initialization of the constant variables:
* it cannot be assigned value anywhere in the program.
* The const variable cannot be left un-initialized at the time of the assignment.
* Explicit value needed to be provided to the constant variable at the time of declaration of the constant variable.

```
#include <iostream>
using namespace std;
int main(){
const int x = 10;
cout<<x; //output --> 10
return 0;
}
```
#### Errors:
```
const int x;
x = 1; //compile time error

const int y; //compile time error
```

## Const with pointer variables:-
We have 3 ways to use a const with a pointer.

### 1)Pointer variable point to a const value:
```
#include <iostream>
using namespace std;
int main(){
int x = 5;
const int *y = &x;
x = 1;
cout<< *y; //output --> 1
}
```
#### Errors:
```
*y = 10; //compile time error
```
### 2)Const pointer variable point to the value:
```
#include <iostream>
using namespace std;
int main(){
int x = 10;
int *const y = &x;
*y = 8;
cout<< *y << "and" << y //output --> 8 and 00BFFE90
return 0;
}
```
#### Errors:
in the previous example if we have also (int d=1)
```
*y = &d; //compile time error
```
### 3)Const pointer pointing to a const variable:
```
#include <iostream>
using namespace std;
int main(){
int x = 5;
const int *const y = &x;
cout<< *y; //output --> 5
return 0;
}
```
#### Errors:
```
*y = 1; //compile time error
```
## Constant methods:-
Member functions and member function arguments and the objects of a class can be declared as const.

We have 2 ways to declare the constant function.
### 1)Ordinary const-function declaration:
```
const void do(){}
int main(){
do(x);
}
```
### 2)A const member function of the class:
```
class{
void do()const{}
}
```
## Constant function parameters and return type:
```
#include <iostream>
using namespace std;
void do(const int x){
cout<< x;
}
void do1(int x){
x = 10;
cout<< "\n" << y;
}
int main(){
int y = 5;
const int i = 8;
do(i);
do1(y);
return 0;
}
```
-------------------------------------------
# &
## Bitwise AND:-
All true --> true

If any one of them is false and the rest are true --> false
```
#include <iostream>
using namespace std;
int main(){
int x = 5;
int y = 5;
int z = 10;
bool i;
i = (x==5) & (y==5);
cout<< i; //output -->1 (true)
cout<< endl;
i = (x==5) & (z==5);
cout<< i; //output -->0 (false)
}
```
## Address of operator:-
```
#include <iostream>
using namespace std;
int main(){
int var;
int value;
int *ptr;
var = 10;
ptr = &var;
value = *ptr;
cout<< "var=" << var << endl; //output --> var=10
cout<< "ptr=" << ptr << endl; //output --> ptr=007DFA14
cout<< "value=" << value << endl; //output --> value=10
return 0;
}
```

# DSA in C++ (Striver A-Z)
A repository containing all the detailed concepts of Data Structures and Algorithms in C++ 

----

## Step 1: Learn the Basics 
## Lec-1
----
### Imput/Output in C++
A short and simple summary of C++ I/O for beginners – inspired by takeUforward.


#### ✅ 1. Include Libraries
Start your code by adding:
```cpp
#include<iostream>
```
This lets you use cin and cout for input and output.

#### ✅ 2. Basic Program Structure
```cpp
#include<iostream>
int main() {
    // your code here
    return 0;
}
```

#### ✅ 3. Printing Output
Use cout to print:
```cpp
#include<iostream>
int main() {
    std::cout << "Hey, Striver!";
    return 0;
}
```
✅ Use \n or std::endl to print on a new line:
```cpp
std::cout << "Hello\nWorld";
```

#### ✅ 4. Skip std:: every time
Use this to make code shorter:
```cpp
using namespace std;
```
Now you can write cout and cin directly.

####  ✅ 5. Taking Input
Use cin to take input from the user:
```cpp
int x;
cin >> x;
cout << "Value: " << x;
```
✔️ For two inputs:
```cpp
int x, y;
cin >> x >> y;
cout << "x: " << x << " y: " << y;
```

#### ✅ 6. Shortcut to include all libraries
use:
```cpp
#include<bits/stdc++.h>
```
⚠️ Not official C++ standard, but common in coding contests.

----
### DataTypes in C++
#### 1. Built-in Data Types in C++
| Type      | Keyword | Size (Typical) | Example Value         |
|-----------|---------|----------------|------------------------|
| Integer   | `int`   | 4 bytes        | `int x = 10;`          |
| Character | `char`  | 1 byte         | `char c = 'A';`        |
| Float     | `float` | 4 bytes        | `float pi = 3.14;`     |
| Double    | `double`| 8 bytes        | `double d = 3.14159;`  |
| Boolean   | `bool`  | 1 byte         | `bool isOn = true;`    |

#### 2. Type Modifiers
| Modifier   | Use                 | Example                 |
|------------|---------------------|--------------------------|
| `short`    | Smaller int         | `short s = 100;`         |
| `long`     | Larger int          | `long l = 100000;`       |
| `unsigned` | Only positive values| `unsigned int u = 50;`   |

#### 3. Example Code Snippet
```cpp
#include<iostream>
using namespace std;

int main() {
    int age = 21;
    char grade = 'A';
    float temp = 36.5;
    double pi = 3.141592;
    bool passed = true;
    
    cout << "Age: " << age << "\n";
    cout << "Grade: " << grade << "\n";
    cout << "Temperature: " << temp << "\n";
    cout << "Pi: " << pi << "\n";
    cout << "Passed? " << passed << "\n";  // prints 1 for true
    return 0;
}
```

-----

### DataTypes in C++













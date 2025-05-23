# DSA in C++ (Striver A-Z)
A repository containing all the detailed concepts of Data Structures and Algorithms in C++

----

## Step 1: Learn the Basics 
## Lec-1 : Basic Things to Know in C++
----
### Imput/Output in C++
A short and simple summary of C++ I/O for beginners – inspired by takeUforward


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

### Conditional Statements in C++
#### ✅ if-else Statement
- if checks a condition.
- If it's true, code inside runs.
- else runs if the condition is false.
 🧪 Example:
```cpp
int age = 10;
if (age >= 18)
    cout << "You are an adult.";
else
    cout << "You are not an adult.";
```
🧾 Output: You are not an adult.

#### ✅ else if Statement
Used when you want to check multiple conditions one after another.
 🧪 Example:
```cpp
int marks = 54;

if (marks < 25)
    cout << "Grade: F";
else if (marks <= 44)
    cout << "Grade: E";
else if (marks <= 49)
    cout << "Grade: D";
else if (marks <= 59)
    cout << "Grade: C";
else if (marks <= 69)
    cout << "Grade: B";
else
    cout << "Grade: A";

```
🧾 Output: Grade: C
👉 Instead of checking both >= and <=, you can just check <= because previous conditions already filter the lower values.

----

### Switch Statement
- Used when you have one variable and want to compare it to many exact values.
- Cleaner and easier to read for multiple fixed-value cases.
- Only works with integer or char values.
- Each case represents one possible value.
- Use break after each case to stop checking further cases.
- default handles any value not matched by cases.

**Example:** Switch Statement
```cpp
int day = 4;

switch(day) {
    case 1: cout << "Monday"; break;
    case 2: cout << "Tuesday"; break;
    case 3: cout << "Wednesday"; break;
    case 4: cout << "Thursday"; break;
    case 5: cout << "Friday"; break;
    case 6: cout << "Saturday"; break;
    case 7: cout << "Sunday"; break;
    default: cout << "Invalid"; 
}
```
Output: Thursday

**Important Points About Switch**
- The expression must be a constant or result in a constant value.
- Works only with int or char types.
- The break keyword is essential to stop fall-through to other cases.
- default case is optional but useful for unexpected values.
- Duplicate case values are not allowed.
- You can nest switch statements but it’s usually discouraged for readability.

----

### Arrays and Strings in C++
**What is an Array?**
An array is a collection of elements of the same data type stored in contiguous memory locations.
- It allows you to store multiple values under one variable name.
- Each element can be accessed using an index starting from 0.

**Why use arrays?**
- To manage and organize multiple related values easily.
- Instead of creating many separate variables, use one array.

**How to declare an array?**
```cpp
type arrayName[size];
```

**Example:**
```cpp
int numbers[5]; // Declares an array of 5 integers
```

**How to initialize an array?**
```cpp
int numbers[5] = {10, 20, 30, 40, 50};
```
**Accessing elements**
- Use the index (starting at 0) to get or set values.
```cpp
cout << numbers[2];  // Output: 30 (3rd element)
numbers[0] = 100;    // Changes 1st element to 100
```

**Example: Array to print 5 numbers**
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {1, 2, 3, 4, 5};

    for (int i = 0; i < 5; i++) {
        cout << arr[i] << " ";
    }

    return 0;
}
```
Output: 1 2 3 4 5

**What is a String?**
A string is a sequence of characters.
In C++, there are two main ways to use strings:
- C-style strings (character arrays ending with '\0' null character)
- The C++ string class from the standard library (<string>), which is easier and safer.

**1. C-Style Strings (Character Arrays)**
A string is stored as an array of characters ending with a special '\0' (null) character that marks the end.

- Declared like this:
```cpp
char name[20] = "Arya";  // array of chars with a string
```

**Example: Print a C-style string**
```cpp
#include <iostream>
using namespace std;

int main() {
    char name[] = "Arya";
    cout << name << endl;  // Output: Arya
    return 0;
}
```
**Important:** Always make sure there is enough space for the characters + the null '\0' character.

**2. C++ string Class**
- More powerful and easier to work with than C-style strings.
- Automatically manages memory and size.
- Include the string library: #include <string>

Declared like this:
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name = "Arya";
    cout << name << endl;  // Output: Arya

    // You can also concatenate strings easily:
    string greeting = "Hello, " + name + "!";
    cout << greeting << endl;  // Output: Hello, Arya!

    return 0;
}
```
**Summary**
| Concept       | Description                                   | Example                  |
|---------------|-----------------------------------------------|--------------------------|
| Array         | Collection of same-type elements accessed by index | `int arr[3] = {1,2,3};` |
| C-Style String| Array of characters ending with '\0'           | `char str[] = "Hi";`     |
| C++ String    | Class that stores and manages text easily       | `string s = "Hello";`    |

----
### For-Loop
🧠 What is a For Loop?
A for loop is used when you want to repeat a task multiple times.

It has 3 main parts:

- Initialization – start a counter
- Condition – keep looping while this is true
- Increment/Decrement – change counter each time

#### ✅ Basic Syntax:
```cpp
for (initialization; condition; update) {
    // code to repeat
}
```
**🔁 Example 1: Print 1 to 10**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        cout << "i = " << i << endl;
    }
    return 0;
}
```
📤 Output: 
```cpp
i = 1
i = 2
...
i = 10
```

**🔁 Example 2: Nested For Loop**
- Used when we need loops inside loops (like rows & columns):
```cpp
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        cout << "i = " << i << ", j = " << j << endl;
    }
}
```

**🔁 Example 3: For Loop with If-Else**
- Print if a number is even or odd:
```cpp
for (int i = 1; i <= 5; i++) {
    if (i % 2 == 0)
        cout << i << " is Even" << endl;
    else
        cout << i << " is Odd" << endl;
}
```

**🔁 Example 4: Custom Increment**
- Increase by 5 instead of 1:
```cpp
for (int i = 1; i <= 25; i += 5) {
    cout << "i = " << i << endl;
}
```

**📤 Output:**
```cpp
i = 1
i = 6
i = 11
i = 16
i = 21
```

----

### While Loop
🌀 What is a while loop?A while loop is used to repeat code as long as a condition is true.

#### ✅ How it works:
- Check the condition.
- If it's true, run the loop body.
- Repeat until the condition becomes false.

**Basic Syntax**
```cpp
while (condition) {
    // code to repeat
}
```

**📌 Example 1: Print numbers from 1 to 5**
```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 1;
    while (i <= 5) {
        cout << i << " ";
        i++;
    }
    return 0;
}
```
**Output:**
```cpp
1 2 3 4 5
```

**📌 Example 2: Factorial of a number**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    int fact = 1;

    while (n > 0) {
        fact *= n;
        n--;
    }

    cout << "Factorial is: " << fact << endl;
    return 0;
}

```
**Output:**
```cpp
Factorial is: 120
```

#### 🛑 break - Exit loop early
```cpp
int i = 1;
while (i <= 10) {
    if (i == 4) break;
    cout << i << " ";
    i++;
}
```
**Output:**
```cpp
1 2 3
```

#### 🔄 continue - Skip current loop iteration
```cpp
int i = 0;
while (i < 6) {
    i++;
    if (i % 2 == 0) continue; // skip even numbers
    cout << i << " ";
}
```
**Output:**
```cpp
1 3 5
```

#### ⚠️ Warning: Infinite loop
If the condition never becomes false, the loop runs forever.
```cpp
while (true) {
    // runs forever unless we use break
}
```
#### ✅ Use while when:
- You don't know in advance how many times to repeat.
- You want to keep running until a condition is false.

----

### Functions (Pass by Values and Reference)
#### 🧠 What is a Function?
A function is a reusable block of code that performs a specific task.

#### ✅ Why use functions?
- To avoid repeating code.
- To divide big programs into small, manageable pieces.

**📌 Function Syntax:**
```cpp
returnType functionName(parameters) {
    // function body
    return value; // if needed
}
```

#### 🎯 Two Ways to Pass Data to Functions:
1. Pass by Value (copy is sent)
2. Pass by Reference (actual variable is sent)

**🔹 1. Pass by Value**
👉 A copy of the variable is passed.
👉 Changes made inside the function don’t affect the original variable.

**🧪 Example:**
```cpp
#include <iostream>
using namespace std;

void changeValue(int x) {
    x = 100;
    cout << "Inside function: " << x << endl;
}

int main() {
    int a = 5;
    changeValue(a);
    cout << "Outside function: " << a << endl;
    return 0;
}
```
**🔎 Output:**
```cpp
Inside function: 100  
Outside function: 5
```
🎯 Even though x is changed to 100 inside the function, the original a remains 5 because only a copy was passed.

**🔹 2. Pass by Reference**
👉 The actual variable is passed using &.
👉 Changes inside the function affect the original variable.

**🧪 Example:**
```cpp
#include <iostream>
using namespace std;

void changeValue(int &x) {
    x = 100;
    cout << "Inside function: " << x << endl;
}

int main() {
    int a = 5;
    changeValue(a);
    cout << "Outside function: " << a << endl;
    return 0;
}

```
**🔎 Output:**
```cpp
Inside function: 100  
Outside function: 100
```
🎯 Now the change reflects outside the function too, because the actual variable was modified.


#### 🧪 Quick Comparison Table

| Feature           | Pass by Value                     | Pass by Reference                  |
|-------------------|------------------------------------|-------------------------------------|
| What is passed?   | A copy of the variable             | The actual variable                 |
| Changes reflect?  | ❌ No                              | ✅ Yes                              |
| Use case          | When you don't want original data to change | When you want to modify original data |

#### 💡 Extra Tip: Use const with reference for safety
If you want to pass large data (like arrays or strings) efficiently but don’t want to change them, use:
```cpp
void showData(const int &x) {
    cout << x;
}
```
This avoids copying and also protects the original value.

#### 🧠 Summary:
- Pass by Value: Makes a copy; original remains safe.
- Pass by Reference: Direct access; can modify original.
- Use & in parameter to pass by reference.
- Use const & when passing by reference without changing value.

----

### ✅ Time and Space Complexity 
#### 📌 What is Time Complexity?
- Time complexity measures how the time to run an algorithm increases with input size.
- It does not refer to actual time taken on a machine (as that varies with hardware).
- Big O notation is used to express time complexity, e.g., O(N), O(N²), O(log N).

#### 💡 Why Not Use Actual Time?
- Time differs on different machines (e.g., old PC vs. modern MacBook).
- So we measure how steps increase with input size N, rather than seconds or milliseconds.

#### 🧠 How to Represent Time Complexity?
We follow:
Use Big O notation to describe the upper bound of steps.
**For example**, a loop running 3N steps:
✅ O(3N) → simplifies to ✅ O(N) (drop constant).

#### ⚙️ Rules for Calculating Time Complexity
- Always use the worst-case scenario:
**Best case:** Fewest steps
**Worst case:** Maximum steps → use this
**Average case:** Middle ground, not usually considered unless explicitly asked

**Ignore constants:**
O(4N³ + 3N² + 8) → becomes O(N³) as N grows large

**Ignore lower-order terms:**
Same example: N² and constant 8 become negligible as N increases

#### ⚖️ Other Notations (Less Used in Interviews)

| Notation | Meaning                    |
|----------|----------------------------|
| **Big O (O)** | Worst-case time complexity     |
| **Theta (θ)** | Average-case (tight bound)     |
| **Omega (Ω)** | Best-case time complexity      |

👉 These are less important in interviews – Big O is the key focus.

**✅ Example Questions**

📘 Q1: Nested loop (both run N times)
```cpp
for (int i = 0; i < N; i++)
    for (int j = 0; j < N; j++)
        cout << i << " " << j;
```
- Outer loop → N times
- Inner loop → N times
- Total → N * N = N²
- ✅ Time Complexity: O(N²)

📘 Q2: Inner loop runs from 0 to i
```cpp
for (int i = 0; i < N; i++)
    for (int j = 0; j <= i; j++)
        cout << i << " " << j;
```
- Steps: 1 + 2 + 3 + ... + N = N(N+1)/2
- ✅ Time Complexity: O(N²) (drop constants)

#### 🧠 What is Space Complexity?
- Measures how much memory is used.
Includes:
- Auxiliary space: Extra memory for variables, arrays, stacks
- Input space: Memory for storing input data

**📘 Example:**
```cpp
int a, b; // input space
int c = a + b; // auxiliary space
```
- Total space = 3 units → Space Complexity = O(1)
📘 If you use an array of size N → Space Complexity = O(N)

#### 🚫 Avoiding Bad Practice
- Don’t overwrite inputs (e.g., b = a + b) just to save space
- In interviews, NEVER manipulate given data unless told to do so

#### ✅ Key Takeaways
- Use Big O notation for both time and space.
- Always analyze the worst-case scenario.
- Ignore constants and lower-order terms.
- Don’t manipulate inputs for better space complexity unless allowed.

----

## Lec-2 : Build-Up Logical Thinking 
----
### Must Do Patterns

#### Pattern-1
![Star Pattern](pattern_img/pattern_1.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; ++i) {
        cout << "*****" << endl;
    }
    return 0;
}
```
#### Pattern-2
![Star Pattern](pattern_img/pattern_2.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        for(int j=1; j<=i; j++){
            cout<<"*";
        }
        cout<<endl;
    }
}
```
#### Pattern-3
![Star Pattern](pattern_img/pattern_3.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        for(int j=1; j<=i; j++){
            cout<<j;
        }
        cout<<endl;
    }

}
```
#### Pattern-4
![Star Pattern](pattern_img/pattern_4.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        for(int j=1; j<=i; j++){
            cout<<i;
        }
        cout<<endl;
    }

}
```
#### Pattern-5
![Star Pattern](pattern_img/pattern_5.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 5; i >=1; i--) {
        for(int j=i; j>=1; j--){
            cout<<"*";
        }
        cout<<endl;
    }

}
```
#### Pattern-6
![Star Pattern](pattern_img/pattern_6.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    
    for (int i = 5; i >=1; i--) {
        for(int j=1; j<=i; j++){
            cout<<j;
        }
        
        cout<<endl;
    }

}
```
#### Pattern-7
![Star Pattern](pattern_img/pattern_7.png)

**Code**
```cpp

#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 1; i <= n; i++) {
        // Print spaces
        for(int j = 1; j <= n - i; j++)
            cout << " ";
        // Print stars
        for(int j = 1; j <= 2*i - 1; j++)
            cout << "*";
        cout << endl;
    }
    return 0;
}
```
#### Pattern-8
![Star Pattern](pattern_img/pattern_8.png)

**Code**
```cpp

#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = n; i >= 1; i--) {
        // Print spaces
        for(int j = 1; j <= n - i; j++)
            cout << " ";
        // Print stars
        for(int j = 1; j <= 2*i - 1; j++)
            cout << "*";
        cout << endl;
    }
    return 0;
}
```
#### Pattern-9
![Star Pattern](pattern_img/pattern_9.png)

**Code**
```cpp

#include <iostream>
using namespace std;

int main() {
    int n = 5;

    // Upper part
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= n - i; j++) cout << " ";
        for(int j = 1; j <= 2*i - 1; j++) cout << "*";
        cout << endl;
    }

    // Lower part
    for(int i = n - 1; i >= 1; i--) {
        for(int j = 1; j <= n - i; j++) cout << " ";
        for(int j = 1; j <= 2*i - 1; j++) cout << "*";
        cout << endl;
    }

    return 0;
}
```
#### Pattern-10
![Star Pattern](pattern_img/pattern_10.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;

    // Upper part
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= i; j++) cout << "*";
        cout << endl;
    }

    // Lower part
    for(int i = n - 1; i >= 1; i--) {
        for(int j = 1; j <= i; j++) cout << "*";
        cout << endl;
    }

    return 0;
}
```
#### Pattern-11
![Star Pattern](pattern_img/pattern_11.png)


**Code**
```cpp

#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= i; j++) {
            cout << ((i + j) % 2) << " ";
        }
        cout << endl;
    }
    return 0;
}
```

#### Pattern-12
![Star Pattern](pattern_img/pattern_12.png)
**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 1; i <= n; i++) {
        // Increasing numbers
        for(int j = 1; j <= i; j++) cout << j;
        // Spaces
        for(int j = 1; j <= 2*(n - i); j++) cout << " ";
        // Decreasing numbers
        for(int j = i; j >= 1; j--) cout << j;
        cout << endl;
    }
    return 0;
}
```
#### Pattern-13
![Star Pattern](pattern_img/pattern_13.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5, count = 1;
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= i; j++) {
            cout << count++ << " ";
        }
        cout << endl;
    }
    return 0;
}

```
#### Pattern-14
![Star Pattern](pattern_img/pattern_14.png)


**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 1; i <= n; i++) {
        for(char ch = 'A'; ch < 'A' + i; ch++) {
            cout << ch;
        }
        cout << endl;
    }
    return 0;
}


```

#### Pattern-15
![Star Pattern](pattern_img/pattern_15.png)


**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = n; i >= 1; i--) {
        for(char ch = 'A'; ch < 'A' + i; ch++) {
            cout << ch;
        }
        cout << endl;
    }
    return 0;
}


```
#### Pattern-16
![Star Pattern](pattern_img/pattern_16.png)


**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 0; i < n; i++) {
        char ch = 'A' + i;
        for(int j = 0; j <= i; j++) {
            cout << ch;
        }
        cout << endl;
    }
    return 0;
}

```
#### Pattern-17
![Star Pattern](pattern_img/pattern_17.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 1; i <= n; i++) {
        // Spaces
        for(int j = 1; j <= n - i; j++) cout << " ";
        // Increasing characters
        for(char ch = 'A'; ch < 'A' + i; ch++) cout << ch;
        // Decreasing characters
        for(char ch = 'A' + i - 2; ch >= 'A'; ch--) cout << ch;
        cout << endl;
    }
    return 0;
}

```
#### Pattern-18
![Star Pattern](pattern_img/pattern_18.png)


**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    for(int i = 0; i < n; i++) {
        char ch = 'E' - i;
        for(int j = 0; j <= i; j++) {
            cout << (char)(ch + j) << " ";
        }
        cout << endl;
    }
    return 0;
}

```

#### Pattern-19
![Star Pattern](pattern_img/pattern_19.png)


**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;

    // Upper Half
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < i; j++) cout << " ";
        for(int j = 0; j < 2*(n - i) - 1; j++) cout << "*";
        cout << endl;
    }

    // Lower Half
    for(int i = 1; i < n; i++) {
        for(int j = 0; j < n - i - 1; j++) cout << " ";
        for(int j = 0; j < 2*i + 1; j++) cout << "*";
        cout << endl;
    }

    return 0;
}

```
#### Pattern-20
![Star Pattern](pattern_img/pattern_20.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;

    // Upper Half
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= n - i; j++) cout << " ";
        for(int j = 1; j <= i; j++) cout << "* ";
        cout << endl;
    }

    // Lower Half
    for(int i = n - 1; i >= 1; i--) {
        for(int j = 1; j <= n - i; j++) cout << " ";
        for(int j = 1; j <= i; j++) cout << "* ";
        cout << endl;
    }

    return 0;
}
```
#### Pattern-21
![Star Pattern](pattern_img/pattern_21.png)

**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;

    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n; j++) {
            if(i == 0 || i == n - 1 || j == 0 || j == n - 1)
                cout << "* ";
            else
                cout << "  ";
        }
        cout << endl;
    }

    return 0;
}

```
#### Pattern-22
![Star Pattern](pattern_img/pattern_22.png)


**Code**
```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 4;

    int size = 2 * n - 1;
    for(int i = 0; i < size; i++) {
        for(int j = 0; j < size; j++) {
            int top = i;
            int left = j;
            int right = (2 * n - 2) - j;
            int bottom = (2 * n - 2) - i;
            int min_dist = min(min(top, bottom), min(left, right));
            cout << n - min_dist << " ";
        }
        cout << endl;
    }

    return 0;
}


```
-----
## Lec 3: C++ STL
-----
### What is STL?
C++ STL (Standard Template Library) is a collection of pre-written code that helps you use data structures (like vectors, stacks, queues, maps) and algorithms (like sort, binary search) easily and quickly without writing them from scratch.It's super useful in coding, especially in DSA and competitive programming, because it saves time and makes your code faster and cleaner.

### What is an unordered_set?
- It stores unique elements (no duplicates).
- The elements are not stored in any order.
- Most operations (like insert, find) take O(1) time on average.

**🔹 Syntax:**
```cpp
unordered_set<int> s;
```
### 🔹 Common Functions of `unordered_set`

| Function     | Description                     |
|--------------|---------------------------------|
| `insert(x)`  | Adds element `x` to the set     |
| `erase(x)`   | Removes element `x` from the set|
| `find(x)`    | Checks if `x` is present        |
| `count(x)`   | Returns 1 if `x` exists, else 0 |
| `size()`     | Returns the number of elements  |
| `clear()`    | Removes all elements            |
| `empty()`    | Returns `true` if set is empty  |

**Example**
```cpp
#include <iostream>
#include <unordered_set>
using namespace std;

int main() {
    unordered_set<int> s;

    s.insert(10);
    s.insert(20);
    s.insert(30);

    // Print all elements
    for (int x : s) {
        cout << x << " ";
    }
    cout << endl;

    // Check if 20 is present
    if (s.find(20) != s.end())
        cout << "20 is present\n";

    s.erase(10);  // Remove 10

    cout << "Size: " << s.size() << endl;

    s.clear();  // Remove all
    cout << "Is empty? " << s.empty() << endl;

    return 0;
}
```

**Output**
```cpp
30 20 10 
20 is present
Size: 2
Is empty? 1

```
----
### ✅ What is a Vector in C++?
A vector is like a resizable array. It can grow or shrink in size when you add or remove elements. It stores data in contiguous memory, just like an array.
**📌 Syntax:**
```cpp
vector<int> v;       // Vector of integers
vector<string> names; // Vector of strings
```
### 🔹 Common Functions (C++ STL Vector)

| Function         | Purpose                              |
|------------------|---------------------------------------|
| `push_back(x)`   | Adds `x` at the end                   |
| `pop_back()`     | Removes the last element              |
| `insert(pos, x)` | Inserts `x` at position `pos`         |
| `erase(pos)`     | Removes element at position `pos`     |
| `front()`        | Returns the first element             |
| `back()`         | Returns the last element              |
| `clear()`        | Deletes all elements                  |
| `empty()`        | Checks if the vector is empty         |
| `size()`         | Returns the number of elements        |
| `begin()/end()`  | Iterators for start and end positions |

**Example**
```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> v;

    // Add elements
    v.push_back(10);
    v.push_back(20);

    // Show elements
    cout << "Vector: ";
    for (int i : v)
        cout << i << " ";

    // Remove last element
    v.pop_back();

    cout << "\nAfter pop_back: ";
    for (int i : v)
        cout << i << " ";

    return 0;
}

```

**Output**
```cpp
Vector: 10 20 
After pop_back: 10

```
----
### 🔹 What is a set in C++?
A set is a container in C++ STL that:
- Stores only unique elements
- Stores elements in sorted order
- Allows fast insert, search, and delete (average case: O(log n))
- Internally uses balanced binary search trees (like Red-Black tree)
**Syntax**
```cpp
set<int> s;
set<string> names;
```

### 🧮 C++ STL `set` – Common Functions

| Function            | Purpose                                   |
|---------------------|-------------------------------------------|
| `insert(x)`         | Adds element `x` to the set               |
| `find(x)`           | Returns iterator to `x` if present        |
| `erase(x)`          | Removes element `x`                       |
| `begin()` / `end()` | Iterators to first and after-last element |
| `count(x)`          | Checks if `x` exists (returns 1 or 0)     |
| `clear()`           | Deletes all elements                      |
| `size()`            | Returns number of elements                |
| `empty()`           | Checks if set is empty                    |

  
**Example**
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    set<int> s;

    // Insert elements
    s.insert(10);
    s.insert(20);
    s.insert(30);
    s.insert(20); // duplicate, will be ignored

    cout << "Elements in set: ";
    for (auto x : s) {
        cout << x << " ";
    }

    // Check if element exists
    if (s.find(20) != s.end())
        cout << "\n20 is present in set.";

    // Erase an element
    s.erase(10);

    cout << "\nSet after deleting 10: ";
    for (auto x : s) {
        cout << x << " ";
    }

    cout << "\nSize: " << s.size();

    // Clear all elements
    s.clear();

    cout << "\nIs set empty? " << (s.empty() ? "Yes" : "No") << endl;

    return 0;
}

```

**Output**
```cpp
Elements in set: 10 20 30
20 is present in set.
Set after deleting 10: 20 30
Size: 2
Is set empty? Yes

```
----

###  📍 unordered_multiset

- 🔹 Stores duplicate values (like multiset), but in no particular order.
- 🔹 Fast for lookup and insertion.


### 🧮 C++ STL unordered_multicast

| Operation   | Purpose                                          |
| ----------- | ------------------------------------------------ |
| `insert(x)` | Adds element `x` (duplicates allowed, unordered) |
| `count(x)`  | Count of `x`                                     |
| `erase(x)`  | Removes all `x`                                  |
| `find(x)`   | Iterator to any `x`                              |
| `clear()`   | Remove all elements                              |
| `size()`    | Number of elements                               |

  
**Example**
```cpp
#include <iostream>
#include <unordered_multiset>
using namespace std;

int main() {
    unordered_multiset<int> ums = {2, 3, 2, 5};
    for (int x : ums) cout << x << " ";
    return 0;
}

```
------
###  📍 multiset
- 🔹 Stores elements in sorted order.
- 🔹 Allows duplicate elements.

### 🧮 C++ STL multiset
| Operation           | Purpose                          |
| ------------------- | -------------------------------- |
| `insert(x)`         | Adds `x` (keeps elements sorted) |
| `count(x)`          | Count of `x`                     |
| `erase(x)`          | Removes all `x`                  |
| `find(x)`           | Iterator to first `x`            |
| `begin()` / `end()` | Iterators for traversal          |

  
**Example**
```cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    multiset<int> ms = {3, 1, 2, 2};
    for (int x : ms) cout << x << " "; // Output: 1 2 2 3
    return 0;
}


```
------

###  📍 unordered_map
- 🔹 Stores key-value pairs.
- 🔹 No particular order. Fast access.
- 🔹 Keys are unique.

### 🧮 C++ STL unordered_map

| Operation      | Purpose                 |
| -------------- | ----------------------- |
| `m[key] = val` | Insert/update key-value |
| `find(key)`    | Iterator to key         |
| `erase(key)`   | Removes key             |
| `count(key)`   | 1 if exists, else 0     |
| `clear()`      | Remove all entries      |

  
**Example**
```cpp
#include <unordered_map>
using namespace std;

unordered_map<string, int> umap;
umap["apple"] = 10;
umap["banana"] = 5;


```
------

###  📍 unordered_multimap
🔹 Stores key-value pairs like unordered_map, but allows duplicate keys.

### 🧮 C++ STL unordered_multimap

| Operation        | Purpose                             |
| ---------------- | ----------------------------------- |
| `insert({k,v})`  | Insert duplicate keys (unordered)   |
| `equal_range(k)` | Range of values for key             |
| `find(k)`        | Iterator to one of the key’s values |

  
**Example**
```cpp
#include <unordered_map>
using namespace std;

unordered_multimap<string, int> ump;
ump.insert({"apple", 10});
ump.insert({"apple", 20});


```
------

###  📍 queue
🔹 FIFO (First In First Out) structure.

🔹 Insert at the back, remove from the front.

### 🧮 C++ STL queue

| Operation | Purpose                 |
| --------- | ----------------------- |
| `push(x)` | Add to back             |
| `pop()`   | Remove front            |
| `front()` | Access front            |
| `empty()` | Check if queue is empty |

**Example**
```cpp
#include <queue>
using namespace std;

queue<int> q;
q.push(1);
q.push(2);
q.pop();  // Removes 1


```
------

###  📍 stack
🔹 LIFO (Last In First Out) structure.

🔹 Insert and remove at the top.

### 🧮 C++ STL stack

| Operation | Purpose                 |
| --------- | ----------------------- |
| `push(x)` | Push on top             |
| `pop()`   | Remove top              |
| `top()`   | View top                |
| `empty()` | Check if stack is empty |


  
**Example**
```cpp
#include <stack>
using namespace std;

stack<int> s;
s.push(10);
s.pop(); // Removes 10



```
------

###  📍 deque
🔹 Double-ended queue.

🔹 Insert and remove from both front and back.

| Operation            | Purpose         |
| -------------------- | --------------- |
| `push_front(x)`      | Insert at front |
| `push_back(x)`       | Insert at back  |
| `pop_front()`        | Remove front    |
| `pop_back()`         | Remove back     |
| `front()` / `back()` | Access ends     |

  
**Example**
```cpp
#include <deque>
using namespace std;

deque<int> dq;
dq.push_front(1);
dq.push_back(2);
dq.pop_back();  // Removes 2



```
------

###  📍 priority_queue
🔹 A max-heap by default (largest element on top).

🔹 Used for getting max elements efficiently.

| Operation | Purpose                           |
| --------- | --------------------------------- |
| `push(x)` | Add to queue                      |
| `top()`   | View top element (max by default) |
| `pop()`   | Remove top                        |
| `empty()` | Check if empty                    |


  
**Example**
```cpp
#include <queue>
using namespace std;

priority_queue<int> pq;
pq.push(5);
pq.push(10);
cout << pq.top(); // 10

```
------


###  📍 multimap
🔹 Like a map but allows duplicate keys.

🔹 Sorted based on keys.

| Operation        | Purpose                               |
| ---------------- | ------------------------------------- |
| `insert({k,v})`  | Duplicate keys allowed, sorted by key |
| `equal_range(k)` | Returns all pairs with key `k`        |

**Example**
```cpp
#include <map>
using namespace std;

multimap<string, int> mm;
mm.insert({"apple", 1});
mm.insert({"apple", 2});




```
------

###  📍 list
🔹 Doubly linked list.

🔹 Fast insertion and deletion from anywhere.

| Operation        | Purpose            |
| ---------------- | ------------------ |
| `push_back(x)`   | Add to end         |
| `push_front(x)`  | Add to front       |
| `insert(pos, x)` | Insert at position |
| `remove(x)`      | Remove all `x`     |

  
**Example**
```cpp
#include <list>
using namespace std;

list<int> l;
l.push_back(1);
l.push_front(2);

```
------

###  📍 next_permutation()
🔹 Changes array to the next lexicographic permutation.
 
**Example**
```cpp
#include <algorithm>
using namespace std;

vector<int> v = {1, 2, 3};
next_permutation(v.begin(), v.end());  // v = {1, 3, 2}


```
------

###  📍 __builtin_popcount()
🔹 Counts the number of 1s in binary representation of a number.

🔹 Very useful in bit manipulation problems.
  
**Example**
```cpp
#include <iostream>
using namespace std;

int x = 7; // 111 in binary
cout << __builtin_popcount(x); // Output: 3



```
------


### 📍 sort()
🔹 Sorts a container in ascending order.

🔹 Can pass custom comparator for descending.

  
**Example**
```cpp
#include <algorithm>
vector<int> v = {3, 1, 2};
sort(v.begin(), v.end()); // v = {1, 2, 3}

```
------


### 📍 min_element()
🔹 Returns iterator to the minimum element in the range.                

  
**Example**
```cpp
#include <algorithm>
vector<int> v = {5, 1, 3};
cout << *min_element(v.begin(), v.end()); // 1


```
------

### 📍 max_element()
🔹 Returns iterator to the maximum element in the range.             

  
**Example**
```cpp
#include <algorithm>
vector<int> v = {5, 1, 3};
cout << *max_element(v.begin(), v.end()); // 5



```
### 🧠 STL Utility Functions
| Function                | Description                       | Example                                |
| ----------------------- | --------------------------------- | -------------------------------------- |
| `next_permutation()`    | Next lexicographic permutation    | `next_permutation(v.begin(), v.end())` |
| `__builtin_popcount(x)` | Counts set bits in binary of `x`  | `__builtin_popcount(7)` → `3`          |
| `sort()`                | Sorts elements in ascending order | `sort(v.begin(), v.end())`             |
| `min_element()`         | Iterator to smallest element      | `*min_element(v.begin(), v.end())`     |
| `max_element()`         | Iterator to largest element       | `*max_element(v.begin(), v.end())`     |


-----

## Lec-4 : Know the Basic Maths 
-----

### Count digits in a number
🔢 Problem Statement
- Given an integer N, count how many digits it has.

**✅ Examples:**
- Input: 12345 → Output: 5 (since it has 5 digits)
- Input: 7789 → Output: 4 (since it has 4 digits)

**💡 Approach 1: Brute Force (Using Loop)**
🧠 Intuition:
- We can repeatedly divide the number by 10, and each time we do that, we remove one digit from the end.
- We keep doing this until the number becomes 0 and count how many times this happens.

**🧮 Steps:**
- Initialize a counter = 0.
- While N > 0:
- Increment counter by 1.
- Remove last digit of N by doing N = N / 10.
- Return the counter.

**🧾 C++ Code:**
```cpp
#include <iostream>
using namespace std;

int countDigits(int n) {
    int cnt = 0;
    while(n > 0) {
        cnt++;         // count this digit
        n = n / 10;     // remove the last digit
    }
    return cnt;
}

int main() {
    int N = 12345;
    cout << "Number: " << N << endl;
    cout << "Digit count: " << countDigits(N) << endl;
    return 0;
}
```
**✅ Output:**
```cpp
Number: 12345
Digit count: 5
```

**⏱️ Time Complexity: O(log N)**
Because each time we divide by 10, the number reduces significantly.

**🧠 Space Complexity: O(1)**
Just one counter variable is used.

**💡 Optimal (Using Logarithm)**
🧠 Intuition:
- Mathematically, the number of digits in a number N is:
- 📌 digits = floor(log10(N)) + 1

**🧮 Why?**

- log10(N) gives us how many digits fit into powers of 10.
- Adding 1 accounts for the total number of digits.
- We take floor by converting it to an int in C++.
'⚠️ Important: This only works for positive numbers (N > 0). For N = 0, you can return 1 manually.'

**🧾 C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

int countDigits(int n) {
    if (n == 0) return 1;  // Special case
    return (int)(log10(n) + 1);
}

int main() {
    int N = 12345;
    cout << "Number: " << N << endl;
    cout << "Digit count: " << countDigits(N) << endl;
    return 0;
}

```
**✅ Output:**
```cpp
Number: 12345
Digit count: 5

```

**⏱️ Time Complexity: O(log N)**
Time Complexity: O(1) (since log is a direct operation)

**🧠 Space Complexity: O(1)**
Space Complexity: O(1)

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

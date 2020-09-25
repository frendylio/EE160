# LAB 4
# Announcements
HKN Tutoring

Please Email me with the subject "[EE 160] - Your_Question" or "EE 160 - Your questions"

Example
```c
[EE 160] - Lab 4, advice/help with temptbl.c
```

# What to submit
Submit an algorithms.txt and 5 .c files
- countup.c 
- countdown.c 
- temperature.c 
- temptbl.c
- account.c

Remember to have proper documentation (Comments).

# Countup.c
No warnings when compiling.

Expected output
```c
1
2
.
.
.
19
20
```

# Countdown.c
No warning when compiling.

- Be careful with infinity while loops.
    - Do Ctrl + Z to stop the command
    - Or just kill the terminal.

Expected output
```c
10
9
.
.
.
1
BLASTOFF!
```

# Temperature.c
Copy temperature.c from Lab 3.

If the input Temperature <= -500, terminate the loop.

## Function Prototypes
- A function prototype or function interface is a declaration of a function that specifies the function's name and type signature (arity, data types of parameters, and return type), but omits the function body.

- Example:
```c
//  Working Example
#include <stdio.h>

//  Function Prototype
void printHelloWorld();

void main() {
    printHelloWorld();
    return;
}

// Error if you do this
// This because your code should be inside a function
// With this, I mean it should be inside a {  }
void printHelloWorld();
    printf("Hello Word\n");
    return;


// Creating function
void printHelloWorld() {
    printf("Hello Word\n");
    return;
}
```

```c
// Error Example, will either not compile or give warnings.
#include <stdio.h>

void main() {
    printHelloWorld();
    return;
}

void printHelloWorld(){
    printf("Hello Word\n");
    return;
}
```
```c
// Working, without function prototype
#include <stdio.h>

// If you put the function before being called by other function (In this case main()), it will still work.
void printHelloWorld(){
    printf("Hello Word\n");
    return;
}

void main() {
    printHelloWorld();
    return;
}

```

```c
// More examples:
#include <stdio.h>
// Function Prototype
void printHelloWorld(int how_many_times_to_print);
void CustomPrint(int what_number_to_Print);
// Main function
void main() {
    int count = 0;

    // Example of a while loop
    // Will call the function printHelloWorld 5 times
    // Thus, it will print Hello World 5 times.
    printHelloWorld(5);

    // CustomPrint
    CustomPrint(160);
    return;
}
// Function 1
void printHelloWorld(int how_many_times_to_print){
    // int how_many_times_to_print;  
    while (how_many_times_to_print > 0){
        printf("Hello Word\n");
        how_many_times_to_print --;
    }
    return;
}
// Function 2
void CustomPrint(int what_number_to_Print){

    // Variable not in the parameters, so It doesn't give error of duplication.
    int how_many_times_to_print = 5;   
    while (how_many_times_to_print > 0){
        printf("%d\n", what_number_to_Print);
        how_many_times_to_print --;
    }
    return;
}

// Output
// This is from printHelloWorld(5);
Hello Word
Hello Word
Hello Word
Hello Word
Hello Word

// This is from CustomPrint(160);
160
160
160
160
160
```

My Temperature.c if you need it. 
```c

#include <stdio.h>

void main() {

    float f, c;

    printf("Enter a temperature in degrees Fahrenheit: ");
    scanf("%f", &f);

    c = (f - 32) * 5/9;

    printf("Degrees in Celsius: %.2f \n", c);

    return;
}
```

Example Output
```c
Enter a temperature in degrees Fahrenheit: 400
Degrees in Celsius: 204.44 
Enter a temperature in degrees Fahrenheit: 200
Degrees in Celsius: 93.33 
Enter a temperature in degrees Fahrenheit: 32
Degrees in Celsius: 0.00 
Enter a temperature in degrees Fahrenheit: -100
Degrees in Celsius: -73.33 
Enter a temperature in degrees Fahrenheit: -500
Invalid Temperature 
```

# temptable.c
## Write your algorithm first! Save this in an algorithms file
    - You can use vi to do this or just use a .txt file

## CheckList
    - Your code should know if you are incrementing positively (+5) or incrementing negatively (-5)
    - If the user enters the same value for start and stop. The program should terminate.
    - Print the temperatures and the number of temperature lines printed
    - temptable() function should return the number of table lines printed and your main() function should print the number of table lines.
    - Should Covert Celsius from start to at most stop.
    - Have a check for invalid temperatures (-500 F), similar to temperature.c 
Example:
```c
// Should Covert Celsius from start to at most stop.
// As you can observe, the stopping temperature is 33
// Thus, when it tries to do 35.00 - 5 = 30.00, it checks that 30 < 33; therefore not printing 30 Celsius.
Enter a temperature to start in degrees Fahrenheit: 50
Enter a temperature to stop in degrees Fahrenheit: 33
===C===|===F===
50.00  | 10.00
45.00  | 7.22
40.00  | 4.44
35.00  | 1.67
Computed 4 temperatures
// Example of positive increment
Enter a temperature to start in degrees Fahrenheit: 30
Enter a temperature to stop in degrees Fahrenheit: 60
===C===|===F===
30.00  | -1.11
35.00  | 1.67
40.00  | 4.44
45.00  | 7.22
50.00  | 10.00
55.00  | 12.78
60.00  | 15.56
Computed 7 temperatures
// Exiting the code by putting the same temperature for start and stop.
Enter a temperature to start in degrees Fahrenheit: 30
Enter a temperature to stop in degrees Fahrenheit: 30
... Exiting Program ...
```

# account.c
## Write your algorithm first! Save this in the same algorithm file used for temptbl.c
    - You can use vi to do this or just use a .txt file

## CheckList
    - If the user types 0, the program should terminate.
    - Have your function working:
        - float calc_acc_amt(float acc_amount, float annual_interest, int years);

Example
```c
// Remeber the formula should be 
// acc_amount = acc_amount + acc_amount * annual_interest
// Thus, every year, it increases by that amount.


// acc_amount  = 20
// annual_interest = 20
// Number of years = 2
// First Year, acc_amount = 20 + 20 * 20 = 420
// Second Tear, acc_amount = 420 + 420 * 20 = 8820

Enter initial amount (0 to exit): 20
Enter annual interest rate (in decimals): 20
Enter number of years of compounding: 2
Accumulated Value: $8820.00 

// Same logic as above
Enter initial amount (0 to exit): 100
Enter annual interest rate (in decimals): 3.3
Enter number of years of compounding: 5
Accumulated Value: $147008.44 

Enter initial amount (0 to exit): 0
... Exiting Program ...
```

# Extra
When you do printf what does %4.2f mean?

It has precision 4 and 2 decimal places.

Basically 
```c
% (Precision) . (How_Many_decimals) (Data type)
```

Example
# Lab 2 

```c
If you have a % in the print statement, you need to add a variable!
Check the data type of your variable

int use &d or &i
    -- Extra %d for decimal only, if not decimal, gives a random value (Garbage value)
    -- %i can be used for hexadecimal, octadecimal and binary, will print the equivalent as decimal
float use %f
char use %c  // single character
char string[] use %s // a word, sentence etc.


    float distance, time;

    // Correct
    printf("An object falling %f feet in %f seconds ", distance, time);

    // Wrong (No enough variables)
    printf("An object falling %f feet in %f seconds ", distance, time);

    // Wrong (Data type)
    printf("An object falling %d feet in %d seconds ", distance, time);       
```

# Lab 3
We assume that the user times a number. Don't worry about error checking.

Example, if you are asking for time. You don't need to worry that the user will type "five" as input. 

Fix all warnings.

## scanf

``` c
%data_type, f, d, c, etc.
&variable_name

scanf("%f", &time);
```

```c
scanf("%f\n", &time);

It will scanf ("%s\n", &time) it will scan for time followed by optional white space
```

## Gravity.c

In case you need a Gravity.c fixed from Lab 2. (You can just re-use your gravity.c code)
```c
#include <stdio.h>

void main(){  

        float velocity, distance, time;

        /*  set the time  */
        time = 10;

        /*  compute the velocity */
        velocity = 32.0 * time;

        /*  compute the distance  */
        distance = (32 * time * time) / 2;

        /*  print the result  */
        printf("An object falling %4.2f feet in %4.2f seconds ", distance, time);
        printf("is traveling %4.2f ft/sec\n",velocity);

        return;
}
```

## seconds.c
Test for 3600, 7210, 3660. Any other number you want.

Hint: % (Mod operator) gets the remainder. 

```
Example:
    5 % 2 = 1 (2*2 + 1 = 5)
    4 % 2 = 0 (2*2 + 0 = 4)
```

## cars.c
```
cp ~ee160/Labs/Lab3/cars.c cars.c
```

## gas.c
Create a new file and make gas.c

## temperature.c
Create a new file and make temperature.c

# Five step process

- 1 - Understand the problem
    - What is this program supposed to do?
    - What kind of information is it given? (What is the input?)
    - What kind of results is it to produce? (What is the output?)
    - What formulas or techniques will be needed?
- 2 - Do a small example by hand
    - Create a small example(s) of what the program should do
    - Solve these examples and keep in mind the questions from step 1.
- 3 - Write an algorithm for solving the problem
    - Remember that each line of code is sequentially executed
    - Your algorithm must include all the steps sequentially to arrive at a solution
    - Algorithm Design Example
- 4 - Translate the algorithm into a programming language (like C)
- 5 - Test the program

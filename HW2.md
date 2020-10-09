# Lab 7
Lab 6 Due next week.

## Homework 2
- You will only be working on Homework 2 today.
- If you have questions on Lab 6, ask now before the end of lab.
- If you have questions on the homework, I guess you can ask, but I won't be grading them.


## Makefiles
- Used to compile easier instead of typing really long "cc file1.c file2.c file3.c file4.c file5.c ....." 
- To create a makefile:
```bash
vi makefile
```

Example makefile:
```makefile

# Below are the commands you can type to compile mass files. i.e. "make driver1", "make driver2", etc.
# If you simply type "make" it will only run the very first command in this makefile. 
# To compile ALL your driver files at once, your first line must be somewhat like the first line shown below then type "make" or "make all"
all: driver1 driver2 driver3

driver1: test.o
  cc test.o driver1.c -o driver1
  
driver2: test2.o
  cc test2.o driver2.c -o driver2
  
driver3: test.o test2.o
  cc test.o test2.o driver3.c -o driver3
  
  
# Below are the object files (.o) that compiles the .h and .c files (except the driver.c files)
test.o: test.h

test2.o: test2.h 


# Clean, this can be useful when your code doesn't work as intended and you want to change stuff.
# So all you have to do is type "make clean" first and then recompile with "make driver1" or "make driver2" or "make" or "make all" or you get the idea...
clean:
  rm *.o
  rm driver1
  rm driver2
  rm driver3
```

## driver1
Files Included:
- leap

Example Output:
```
Enter the year you want to check (0 to exit): 4
Year 4 is a leap year
Enter the year you want to check (0 to exit): 40
Year 40 is a leap year
Enter the year you want to check (0 to exit): 100
Year 100 is NOT a leap year
Enter the year you want to check (0 to exit): 400
Year 400 is a leap year
Enter the year you want to check (0 to exit): 1000
Year 1000 is NOT a leap year
Enter the year you want to check (0 to exit): 2000
Year 2000 is a leap year
Enter the year you want to check (0 to exit): 2019
Year 2019 is NOT a leap year
Enter the year you want to check (0 to exit): 2020
Year 2020 is a leap year
Enter the year you want to check (0 to exit): 0
... Exiting Program ...
```

## driver2
Files Included:
- leap
- days

Example Output:
```
Please input a month(1-12) and year (CTRL+D to exit): 2 2015
2-2015 has 28 days

Please input a month(1-12) and year (CTRL+D to exit): 2 2016
2-2016 has 29 days

Please input a month(1-12) and year (CTRL+D to exit): 12 2020
12-2020 has 31 days

Please input a month(1-12) and year (CTRL+D to exit): [CTRL+D]
... Exiting Program ...
```

## driver3
Files Included:
- leap
- days
- julian

Example Output:
```
Enter the Day, Month, and Year to find Julian Date (EOF to exit): 1 1 2019
Julian Date: 1 
Enter the Day, Month, and Year to find Julian Date (EOF to exit): 31 12 2019
Julian Date: 365 
Enter the Day, Month, and Year to find Julian Date (EOF to exit): 31 12 2020
Julian Date: 366 
Enter the Day, Month, and Year to find Julian Date (EOF to exit): [CTRL+D]
... Exiting Program ...
```

## datediff
Files Included:
- leap
- days
- julian

Notes:
- There is a slight error in the example code. If your starting date is after the ending date, the output will be incorrect.
- It's up to you if you want to code it so it will work for the case above, but since it's not implemented in the example code, you won't get deducted points for it (probably, idk I'm not grading this)
- Note that this is the DIFFERENCE in days. Therefore, it excludes the starting date.

Example Output:
```
Enter a start date (dd mm yy) (EOF to quit): 1 1 2020  
Enter a end date (dd mm yy) (EOF to quit): 31 1 2020
        From     1  1 2020 
        To      31  1 2020
                 There are 30 days
Enter a start date (dd mm yy) (EOF to quit): 1 1 2020 
Enter a end date (dd mm yy) (EOF to quit): 31 12 2020
        From     1  1 2020 
        To      31 12 2020
                 There are 365 days
Enter a start date (dd mm yy) (EOF to quit): 1 1 2021
Enter a end date (dd mm yy) (EOF to quit): 31 12 2021
        From     1  1 2021 
        To      31 12 2021
                 There are 364 days
Enter a start date (dd mm yy) (EOF to quit): 1 1 2020
Enter a end date (dd mm yy) (EOF to quit): 1 1 2020
        From     1  1 2020 
        To       1  1 2020
                 There are 0 days
Enter a start date (dd mm yy) (EOF to quit): 1 1 2020
Enter a end date (dd mm yy) (EOF to quit): 31 12 2019
        From    31 12 2019 
        To       1  1 2020
                 There are 1 days
Enter a start date (dd mm yy) (EOF to quit): 14 3 1879
Enter a end date (dd mm yy) (EOF to quit): 18 4 1955
        From    14  3 1879 
        To      18  4 1955
                 There are 27793 days
Enter a start date (dd mm yy) (EOF to quit): [CTRL+D]
... Exiting Program ...
```


## Code Included in this Homework
| .c Files | .h Files |
| :---: | :---: |
| days.c | days.h |
| leap.c | leap.h |
| julian.c | julian.h |
| driver1.c |  |
| driver2.c |  |
| driver3.c |  |
| datediff.c |  |

## Made By Ethan chee
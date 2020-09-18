~ee160/Labs/Lab2/gravity.c


# Lab Task (Due next week before lab!)

(All this information is on the ee160 webstie)

## Team Formation (Obmitted as Google meet doesn't allow break out rooms)
- Do Team Exercise (10 min)
    - Team Task
    - 5 to 10 goals addressing issues.
    - Team name
- Email to frendy@hawaii.edu
    - Only one person per team should email
    - Team goals and expectation
    - Team Name
        - And the name of your memebers

## Explore C Program Creation & Compilation
- Create 5 C Programs
    - Be sure that they compile and work
- This should be done individually
    - You can ask your teammates and me for help (Don't be afraid of asking questions).
- Everyone should submit all 5 files at the end of this lab.
- How to compile and run it (be sure to be in the same folder as your c file)
    ``` bash
        gcc name_of_your_file.c && ./a.out

        Notes:
        gcc basically means to compile your c file
        ./a.out is to run your file
        && means "AND"

        Thus, the code above means:
            Compile a.c file and run it.
    ```

# The file files you need to submit

## welcome.c
- What does it produce as output?

## myname.c
- Copy myname.c file:
    - Modify it so it prints your full name
    - Compile it and check that it works
        - Do not have any warnings when compiling

## myinfo.c
- Copy myname.c file:
    - Add a new line that outputs your email in a new line

## pay0.c
- You can get the code from the ee160 website
    - Code From Text -> Chapter 2
    - Change it to compute the pay for working 32 hours at a pay rate of $9.75. 

## gravity.c
- Copy the file from ~ee160/Labs/Lab2/gravity.c
- Fix it so it can compile

## Submition
- To submit:
    ```
        grade -lab2s3,ee160 welcome.c myname.c myinfo.c pay0.c gravity.c
    ```
- To verify:
    ```
        grade -lab2s3,ee160
    ```
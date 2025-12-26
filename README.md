# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int num = 44;
    int result;

    // Left shift by 3 positions
    result = num << 3;

    printf("Result after left shift = %d", result);

    return 0;
}
```

## OUTPUT
<img width="460" height="265" alt="image" src="https://github.com/user-attachments/assets/3218f352-80fd-4027-a78e-2e41e1c5deab" />









## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM

```
#include <stdio.h>

int main() {
    int a, b;

    // Read two numbers
    scanf("%d %d", &a, &b);

    // Check equality
    if (a == b) {
        printf("Numbers are equal");
    }

    return 0;
}
```


## OUTPUT

<img width="455" height="326" alt="image" src="https://github.com/user-attachments/assets/a80ab791-b3f9-4532-ab52-14d8188831d1" />

           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    char str[100];
    int i;

    // Read the string
    scanf("%s", str);

    // Convert to lowercase
    for (i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'A' && str[i] <= 'Z') {
            str[i] = str[i] + 32; // ASCII conversion
        }
    }

    // Print the lowercase string
    printf("%s", str);

    return 0;
}
```
## OUTPUT

<img width="466" height="205" alt="image" src="https://github.com/user-attachments/assets/0ad0cc78-20b4-4314-a16e-70e59b837a84" />





## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    char str[100];
    int i = 0, wordCount = 0;

    // Read the string (with spaces)
    fgets(str, sizeof(str), stdin);

    // Count words using do-while loop
    do {
        // Skip leading spaces
        while (str[i] == ' ' || str[i] == '\n' || str[i] == '\t') {
            i++;
        }

        // If not end of string, it is a word
        if (str[i] != '\0') {
            wordCount++;
        }

        // Skip the current word
        while (str[i] != ' ' && str[i] != '\n' && str[i] != '\t' && str[i] != '\0') {
            i++;
        }

    } while (str[i] != '\0');

    printf("Total words = %d", wordCount);

    return 0;
}
```

## OUTPUT
<img width="530" height="197" alt="image" src="https://github.com/user-attachments/assets/ec721527-8698-49b5-9712-ccce51d7ea79" />






## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    char c1[100], c2[100];
    int i = 0, flag = 0;

    // Read the first string (can include spaces)
    scanf("%[^\n]", c1);
    getchar(); // consume the newline left by previous input

    // Read the second string (no spaces)
    scanf("%s", c2);

    // Compare characters of both strings
    while (c1[i] != '\0' && c2[i] != '\0') {
        if (c1[i] != c2[i]) {
            flag = 1;
            break;
        }
        i++;
    }

    // If one string is longer than the other
    if (c1[i] != '\0' || c2[i] != '\0') {
        flag = 1;
    }

    // Print result
    if (flag == 0) {
        printf("strings are same");
    } else {
        printf("strings are not same");
    }

    return 0;
}
```


## OUTPUT

<img width="388" height="237" alt="image" src="https://github.com/user-attachments/assets/1958dfec-3d9c-4f50-8905-b2f3aae20f40" />

 

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.


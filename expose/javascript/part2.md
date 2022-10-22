# Data Types
A. student.name
B. student['Grad Year']
C. student.greeting() 
D. student['Favorite Teacher'].name
E. student.courseLoad[0]

# Basic Operators & Type Conversion
13. Arithmetic
    A. '3' + 2 = '32' since 2 is an integer and integers map to their exact string representation
    B. '3' - 2 = 1 because '3' is a string that can map to its exact numerical representation
    C. 3 + null = 3 since `null` converts to `0` 
    D. '3' + null = '3null' since adding a string with `null` converts `null` to a string and so the two strings concatenate
    E. true + 3 = 4 since `true` converts to 1
    F. false + null = 0 since `false` converts to 0 and `null` also converts to 0 
    G. '3' + undefined = '3undefined' since `undefined` gets converted to the exact string representation when concatenating with a string
    H. '3' - undefined = NaN since `undefined` does not get converted to a numerical value and becomes `NaN`, which stands for Not-A-Number, so subtracting a string with a NaN ultimately results in NaN

14. Comparison
    A. '2' > 1 = true since JavaScript converts the string to a number when comparing a string with a number, so '2' converts to the exact representation of its number
    B. '2' < '12' = false since both are strings and will be compared alphabetically, so because '1' is less than '2', '2' is greater than '12'
    C. 2 == '2' = true since the number `2` gets converted to its string representation, which is the same as `2`
    D. 2 === '2' = false since `===` compares the data types between the two first before comparing its value, so it returns a false as one is a string and the other is a number
    E. true == 2 = false since `true` maps to its numerical value of 1 and is therefore unequal to 2
    F. true === Boolean(2) = true since Boolean() returns true to anything that has a value, so Boolean(2) evaluates to true and the strict equality passes with both boolean data types

15. The `==` operator is a non-strict equality check that compares the values of two different variables regardless of their data types while `===` compares both the equality of variables and their data types.

17. The result is [2, 4, 6] because inside the `modifyArray` function, it loops through each element inside `array`, which is [1, 2, 3], and each of those elements are passed into the callback function `doSomething`, which multiplies each of those elements by 2. The doubled value of each element in `array` is then added into `newArr`, the variable returned by the function. 


19. 1
    4
    3
    2
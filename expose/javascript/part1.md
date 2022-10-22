# Part 1. A Quick Introduction
1. values added: 20
2. final result: 20
3. values added: 20
4. Code returns an error because `result` is defined as a `let` scope, meaning that `result` can only be accessed within the `if` block that it is defined in. So since line 13 logs `result` outside of the `if`, there will be an undefined reference error.
5. The code returns a type error because `result` is defined with the `const` scope so it can't change after its initial value.
6. Since the code returns an error at line 9, line 13 will not be printed. But even if line 9 did not have an error, line 13 will still lead to a reference error since `result` is defined within the `if` block and has the same scope as a variable defined with `let` keyword, so there will be the same issue as explained in question #4.

# Part 2. A Little More of a Challenge
1. Line 12 prints out the last variable that `i` will increment to in the for loop, which is 3, because it starts at 0 and loops over each item in the `prices` array, which has a length of 3.
2. Line 13 will print out the last `discountedPrice` value, which is defined in the for loop, so it'll print out 150. There will be no errors because it is defined with a `var` scope, meaning the entire function will have access to it.
3. Line 14 will print out the same result as line 13, which is 150, because `finalPrice` is also defined with a `var` scope at the top of the function and last changed inside the for loop. 
4. This function returns an array of all the discounted prices: [ 50, 100, 150 ]. Since the discount value is essentially 50% of each price and the `discounted` array is defined at the top of the function with a `var` scope, each element inside the original `prices` array will be halved inside the for loop and stored inside `discounted`, the variable that's returned. 
5. Line 12 will run into a reference error since it prints out `i` outside of the for loop when `i` is defined with a `let` keyword _inside_ the for loop. Hence, `i` will not be accessible nor defined outside of the `for` block that it is declared in.
6. Line 13 will also run into a reference error due to the same error as #5: `discountedPrice` is only defined inside the for loop with a `let` scope, so it can only be accessed within the for loop block that it is first declared in. Outside of the for loop, there is no variable defined as `discountedPrice`, so it'll lead to an error.
7. Line 14 will print out 150 since `finalPrice` is a variable defined at the top of the function with a `let` scope, so it is accessible anywhere within the function. It was last changed inside the for loop, so its value is teh final price of the last element in the `prices` array.
8. This function still returns the discounted price of each element in the `prices` array: [ 50, 100, 150 ]. Even though the variables are changed to a `let` scope as opposed to `var`, there is no impact on the variable that's returned, `discounted`, since it is defined on the first line of the function and can be accessed and changed anywhere inside the function.
9. Line 11 will also run into a reference error like #6 since `i` is a `let` variable defined inside the for loop, so there will be no such variable that could be accessed outside of the `for` block. Hence, `i` will not be defined nor printed.
10. Line 12 will print out 3 since that is the length of the variable `prices` and there will be no errors since `length` is defined at the top of the function and accessed in the same scope.
11. The function will return the same result as the previous changes: [ 50, 100, 150 ]. Even though the variable that prints out the final discount, `discounted` is changed to a `const` scope, it is still accessible at the time of the return statement since it is within the block scope that it is declared in, which is bascially the entire function. Even though `const` variables can't be changed, the array itself is not getting reassigned so elements inside the array are still able to be added/changed.
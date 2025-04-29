1. At line 12, the number "3" will be printed to the console. It is taking the variable `i`, which has been declared as a `var` and had been incremented to 3 fro the for-loop. The print statement on line 12 has scope access to `i` as it is a `var`.
2. At line 13, "150" will be printed to the console. Since the print statement is after the for-loop, the last piece of data in `discountedPrice` was `300 * (1 - 0.5)` = `150`. As mentioned previously, the `var` scope of discountedPrice allows the print statement on line 13 to access it. 
3. Line 14 also prints out "150" for the same reasons as question #2 since `finalPrice` is a `var`. While the math in `finalPrice` does rounding work, the value is still the same as `discountedPrice`.
4. The function will return an array of `[50, 100, 150]`. The `discountPrices` function takes a list of prices and applies a reduction based on `discount`. Since the provided `discount` is 0.5, all of the prices are halved.
5. An error occurs at line 12 because the print statement tries to access a variable that is not within its scope (`i` is only accessible in the for-loop from lines 6-10).
6. Another error occurs at line 13 because the print statement attempts to access `discountedPrice`, which has been defined with `let` and thus is only accessible within the for-loop.
7. "150" is successfully printed. `let` + `finalPrice` and the print statement are within the same scope (the function scope), so the print statement has access to `finalPrice`.
8. The same array as #4 (`[50, 100, 150]`) is returned for the same reasons as #7- `discounted` is in function scope so the return has access to it.
9. Attempting to print on line 11 produces an error as it tries to access a variable `i` that is defined to only have for-loop scope, which the print statement does not have.
10. "3" is printed out. `length` and the print statement are in the same scope, so it is successful.
11. It is the same as #4 and #8- the array `[50, 100, 150]` is returned. While `discounted` is declared as a `const`, it is important to note that arrays are pointers to memory addresses, so we can change what data is at that memory location, but we cannot change the memory address itself. 
12. `student` Object 
    - A. `student.name`
    - B. `student['Grad Year']`
    - C. `student.greeting();`
    - D. `student['Favorite Teacher'].name`
    - E. `student.courseLoad[0]`
13. Arithmetic
    - A. `'32'`: '3' is read so 2 is converted into a string to concatenate (`+`) the two. 
    - B. `1`: the subtraction operation doesn't work on strings, so it sees the 2 then converts
    - C. `3`: null is like "nothing", so 3 stays the same.
    - D. `'3null'`: JavaScript sees a string '3' and it converts null to a string.
    - E. `4`: true is really a 1 in the binary sense, so the numeric values 1 and 3 are added.
    - F. `false + null`: false is really a 0 in the binary sense, so this is a similar case with C that null is "like nothing."
    - G. `'3undefined'`: this is a similar case to D where '3' is a string and undefined to converted to a string.
    - H. `NaN`: the subtraction operator is attempted with 3, but undefined is not a number (NaN).
14. Comparison
    - A. `true`: the string '2' becomes a number.
    - B. `false`: two *strings* are compared and '2' is greater than '12' (starts with '1') lexicographically.
    - C. `true`: '2' becomes numeric 2.
    - D. `false`: no type conversion is done so a string is not equal to a numeric value.
    - E. `false`: the boolean true becomes numeric 1, which is not equal to 2.
    - F. `true`: any numeric value greater than or equal to 1 is considered true... so the type conversion makes `Boolean(2)` true.
15. `==` does type conversion in its equality therefore it does not differentiate between different data types. `===` compares the values "as-is" (i.e. no type conversion).
16. See [part2-question16.js](./part2-question16.js)
17. We know our two parameters: an array and a function. When we call `modifyArray` with our parameters, we create a blank `newArr` and enter in the for-loop. Each iteration pushes a value to the array... but that value the return value from `doSomething`, taking each i-th element from the `array` paramter as an input. As per the definition of `doSomething`, each value is multiplied by two, so the resulting array is `[2, 4, 6]`.
18. See [part2-question18.js](./part2-question18.js)
19. `1`, `4`, `3`, `2` (where the commas should be new lines): the timeout on printing 2 is one second while printing 4 is run immediately, note that the print of 3 is placed on a stack rather than getting to run immediately.
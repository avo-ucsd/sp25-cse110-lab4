1. The number "20" is printed by line 9.
2. "20" is also printed by line 13.
3. `var` does not limit the variable scope to the current block. In this example program, the consequences are trivial, but issues can arise when variable names are reused in larger programs for example.
4. By line 9, "20" is printed.
5. An error occurs because the print statement on line 11 tries to access `result`, which is in an if-block and the print statement is outside of it. Because `let` is used, the print statement does not have scope access.
6. Trying to add the sum of `num1` and `num2` to result, a constant, results in an error as `const` variables cannot have their data changed. Thus, an error is printed at line 7, and the print statement on line 9 is never reached. 
7. Line 13 is not reached as it is stopped by the error from line 7 (see above).
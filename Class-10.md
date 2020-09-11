# Error Handling & Debugging

## JS Chapter 10 pg. 449-487

In JavaScript the execution order is line by line, but keep in mind that functions don't read until called, 
and when called in line it stops to execute that function line by line before continuing with the rest of the script

Any time the script enters a new context it goes through two processes, prepare and execute.
In preparation the new scope is created, variables, functions, and arguments are created, and the __this__ keyword is given value
In execute values are assigned to variables, functions are referenced and ran, and statements are ran

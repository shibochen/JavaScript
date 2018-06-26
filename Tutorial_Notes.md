# Notes

1. `var` has no block scope: variables either function-wide or global, they are visible through blocks;
2. if a code block is inside a function, then `var` become function-level variable.
3. variable declarations are processed at funciton start, but assignments are not.


# global object
1. global object provides all global variables and functions
    -Provides access to built-in functions and values, defined by the specification and the environment.
    -Provides access to global Function Declarations and `var` variables.
2. In non-strict mode, the value of `this` in global area is window. In strict mode, it is `undefined`. 

# Function Object, NFE(named Function Expression)
1. Function is an object with two properties: `name` and `length`;
2. It is possible to add properties to function, but property is not a variable;
3. If the function is declared as a Function Expression, and it carries the name, then it is called a Named Function Expression. The name does two things as shown in following: 1. It allows the function to reference itself internally. 2. It is not visible outside of the function.

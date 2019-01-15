# Code Review Checklist
The following code review checklist gives an idea about the various aspects you need to consider while reviewing the code.

## General

  - [ ] Does the code work? Does it perform its intended function, the logic is correct etc.
  - [ ] Is all the code easily understood?
  - [ ] Does it conform to your agreed coding conventions? These will usually cover location of braces, variable and function names, line length, indentations, formatting, and comments.
  - [ ] Is there any redundant or duplicate code?
  - [ ] Enums are used instead of int constants where applicable
  - [ ] There are no usages of 'magic numbers'
  - [ ] All variables are in the smallest scope possible
  - [ ] All class, variable, and method modifiers are correct.
  - [ ] There is no commented out code
  - [ ] Do the names used in the program convey intent?
  - [ ] There is no dead code (inaccessible at Runtime)
  - [ ] Is the code as modular as possible?
  - [ ] No code can be replaced with library functions
  - [ ] Required logs are present
  - [ ] No System.out.println or similar calls exist
  - [ ] No stack traces are printed
  - [ ] Variables are immutable where possible
  - [ ] No complex/long boolean expressions
  - [ ] No negatively named boolean variables
  - [ ] No empty blocks of code
  - [ ] Ideal data structures are used
  - [ ] Constructors do not accept null/none values
  - [ ] Collections are initialised with a specific estimated capacity
  - [ ] Arrays are checked for out of bound conditions
  - [ ] Catch clauses are fine grained and catch specific exceptions
  - [ ] Exceptions are not eaten if caught, unless explicitly documented otherwise
  - [ ] Files/Sockets/Cursors and other resources are properly closed even when an exception occurs in using them
  - [ ] StringBuilder is used to concatenate strings
  - [ ] Null/None are not returned from any method
  - [ ] Floating point numbers are not compared for equality
  - [ ] Loops have a set length and correct termination conditions
  - [ ] Blocks of code inside loops are as small as possible
  - [ ] Order/index of a collection is not modified when it is being looped over
  - [ ] No object exists longer than necessary
  - [ ] Design patterns if used are correctly applied
  - [ ] No memory leaks
  - [ ] Methods return early without compromising code readability

## Performance
  - [ ] Are there any obvious optimizations that will improve performance?
  - [ ] Can any of the code be replaced with library or built-in functions?
  - [ ] Can any logging or debugging code be removed?

## Documentation
  - [ ] All methods are commented in clear language.
  - [ ] All public methods/interfaces/contracts are commented describing usage
  - [ ] All edge cases are described in comments
  - [ ] Data structures and units of measurement are explained

## Threading
  - [ ] Objects accessed by multiple threads are accessed only through a lock, or synchronized methods.
  - [ ] Race conditions have been handled
  - [ ] Locks are acquired and released in the right order to prevent deadlocks, even in error handling code.
  - [ ] StringBuffer is used to concatenate strings in multi-threaded code

## Security
  - [ ] All data inputs are checked (for the correct type, length/size, format, and range)
  - [ ] Invalid parameter values handled such that exceptions are not thrown
  - [ ] No sensitive information is logged or visible in a stacktrace

## Testing
  - [ ] Is the code testable? The code should be structured so that it doesn’t add too many or hide dependencies, is unable to initialize objects, test frameworks can use methods etc.
  - [ ] Do tests exist, and are they comprehensive?
  - [ ] Could any test code be replaced with the use of an existing API?

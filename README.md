# Universal Coding Rules
Set of rules which can be used as a guideline in any software project.

## Classes
### Layout
* Put your publics above and privates below.
* Organize class members in the following order:
  1. Constructors.
  2. Destructors.
  3. Public attributes.
  4. Public methods.
  5. Private attributes.
  6. Private methods.
  7. Constants (keep private).
  8. Fields (keep private).
  
## Code flow
* Tell, don’t ask. You shouldn’t ask state of an object and make decisions based on that state in outer scope. Instead tell object to do the job because it already knows its state (which should be not exposed, btw).
  
## Conditions
### Switch statements
* Avoid switch statements at all costs. Replace them with polymorphism. Switch statement indicates your function does more than one thing.
* Multiple if/then/else is essentially a switch statement and should be avoided.

## Functions, methods and procedures
I’ll be using the word *function*, but the rules below apply to methods, procedures and even constructors.

### General
* Keep your function’s body as small as possible. Break it into smaller functions or classes until further division is impossible.
* Function must do only one thing.
* Use if/switch statements carefully, because they usually indicade that your function does more than one thing.
* Avoid temporal coupling. A function shouldn’t expect to be called in a certain order, after or before another function.
* Avoid changing state and creating side effects. Like in functional programming a function must always produce the same result for the same input.
* If a function has side effects—it shouldn’t return anything. Such function can be called a command or procedure.
* If a function doesn’t have side effects—it should return value.

### Arguments
* Don’t pass arguments which indicate state. Usually it’s boolean or enum, but integers or even strings are used sometimes. Remember: if you pass state indicator into a function it means your function does more than one thing.
* Keep number of arguments no more than 3 (this rule might be avoid in constructors).
* Don’t pass null/nil. In fact avoid using them at all. As a function argument they’re usually a hidden form of boolean.
* Don’t output via arguments. Always use return statement.

## Acknowledgments & Thanks

This set of rules is based on some personal experience and is mostly influenced by these great authors:
* Robert C. Martin (Uncle Bob) and his book [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882).
* Steve McConnell and [Code Complete: A Practical Handbook of Software Construction](https://www.amazon.com/Code-Complete-Practical-Handbook-Construction/dp/0735619670/).

Thanks for making our code better!

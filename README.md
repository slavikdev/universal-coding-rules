# Universal Coding Rules
Set of rules which can be used as a guideline in any software project.

## Functions, methods and procedures
I’ll be using the word *function*, but the rules below apply to methods, procedures and even constructors.

### General
* Keep your function’s body as small as possible. Break it into smaller functions or classes until further division is impossible.
* Function must do only one thing.
* Use if/switch statements carefully, because they usually indicade that your function does more than one thing.

### Arguments
* Don’t pass arguments which indicate state. Usually it’s boolean or enum, but integers or even strings are used sometimes. Remember: if you pass state indicator into a function it means your function does more than one thing.
* Keep number of arguments no more than 3 (this rule might be avoid in constructors).
* Don’t pass null/nil. In fact avoid using them at all. As a function argument they’re usually a hidden form of boolean.

## Acknowledgments & Thanks

This set of rules is based on some personal experience but it’s mostly influenced by these great authors:
* Robert C. Martin (Uncle Bob) and his book [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882).
* Steve McConnell and [Code Complete: A Practical Handbook of Software Construction](https://www.amazon.com/Code-Complete-Practical-Handbook-Construction/dp/0735619670/).

Thanks for making our code better!

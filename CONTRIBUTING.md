# CONTRIBUTING

- **Gold standard:** Submit a PR.
- **Honorable mention:** Create an issue.
- **Lazy fallback:** [Email Michael](mailto:michael@philomathsoftware.com)

The issue tracker is for bug reports and feature requests. If you'd like help with a usage question, please [email Michael](mailto:michael@philomathsoftware.com) or look for `seemikehack` on Freenode.

# Contributing to blessed-curl

1. [Directory structure](#directory-structure)
2. [Style guide](#style-guide)
3. [Testing](#testing)

## Directory structure

- `/tools` contains building and testing tools and scripts

- `/src` contains the source code

- `/test` contains test code

## Style guide

Use the same style as is used in the surrounding code.

###Whitespace

- 4 space indentation
- No trailing whitespace
- LF at end of files
- Curly braces can be left out of single statement `if/else/else if`s when it is obvious there will never be multiple statements, such as a null check at the top of a function for an early return.
- Add an additional new line between logical sections of code.

###Variables

- Use multiple `var` statements instead of a single one with comma separator. Do not declare variables until you need them.

###Equality and type checks

- Always use `===` except when checking for null or undefined. To check for null or undefined, use `x == null`.
- For checks that can be done with `typeof`: do not make helper functions, save results of `typeof` to a variable, or make the type string a non-constant. Always write the check in the form `typeof expression === "constant string"` even if it feels like repeating yourself.

## Testing

Make sure that all the tests run before and after you make your additions. Look in the [testing section in README.md](https://github.com/seemikehack/blessed-curl#testing) for how to run the tests. Add relevant new tests.

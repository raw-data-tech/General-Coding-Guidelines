# General Coding Guide


## Table of Contents
1. [DRY](#dry)
1. [Comments](#comments)
1. [Functions](#Functions)
1. Classes
1. Think about data than code
1. Clear variable names

## DRY
> DRY stands for Don't Repeat Yourself. Also known as DIE: Duplication is Evil.
"Every piece of knowledge must have a single, unambiguous, authoritative representation within a system."


You are violating of DRY
  1. If you are copying and pasting blocks of code from one method, function or block of code to another or
  1. you make mutiple similar code changes for a requirement change

## Comments

- **DO NOT** use comments to convey what the code does.

  > Refactor code and replace comments with better variable/function name. 

  Instead of
  ```python
    # convert to cents
    a = x * 100
  
    # avg cents per customer 
    avg = a / n
  
    # add to list
    avgs < avg
    t += 1
  ```
  use
  
  ```python
    total_cents = total * 100
    average_per_customer = total_cents / customer_count
    track_average(average_per_customer)
  ```
- Use comment to explain why. 
  
    > If you take an approach that might not be obvious to others, you should have a comment that explains why you made the decisions that you did.

## Functions

- Scope
  > Be clear on what the function does
  1. What are the inputs?
  2. What are the ouputs?
  3. Is there any side effects or actions(update DB or send email notification)? 

- Name 
  Based on the scope give a sensible name to the function.

- Measure complexity
  One metric for code complexity of a function [cyclometric complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity#Implications_for_software_testing) of the function

  > Cyclomatic complexity is one measure of code quality. It helps us know exactly how complex a particular routine is, and helps us refactor that routine as necessary. 
  
  For most functions, a cyclomatic complexity 
    1. below 4 is considered good
    1. between 5 and 7 is considered medium complexity
    1. between 8 and 10 is high complexity, and above that is extreme complexity

# RawData Technologies General Coding Guide


## Table of Contents
1. [DRY](#dry)
1. [comments](#comments)
1. [Functions](#Functions)
1. Classes
1. Think about data than code
1. Clear variable names

## DRY
What?
Why?
1. for a requirement change similar code change at mutiple places
2. copy pase of code

## Comments

- **DO NOT** use comments to convey what the code does. 
	>Instead refactor and convery it via better code. So instead of
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

Before implementing a function you should have
1. What are the inputs
2. What are the ouputs

Reduce [cyclometric complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity#Implications_for_software_testing) of the function


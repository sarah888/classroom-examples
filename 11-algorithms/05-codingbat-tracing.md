# Codingbat Solution Tracing - Recursion-1
This is a collection of [Codingbat](http://codingbat.com) solutions that may or may not work. 
The idea is to trace the code to discover the errors or to determine if the solution is infact correct.

## Adding a post
Simply edit this document and add your code as shown below with the following rules:
1. Ensure your code is within triple backticks like below. 
2. Add [type annotations](https://docs.python.org/3/library/typing.html) for the function header so we know what type of data the function recieves and returns.
3. Ensure that the name of the function is under an appropriate `###` header.
4. Ensure that the problem's explanation text is above all the "solutions". 
5. Keep the problems in alpha order.

## Example:
### double
Create a function that will double the given integer.
```
double(5) -> 10
double(3) -> 6
double(0) -> 0
```
Solutions:

```python
def double(n: int) -> int:
    return n * 2
```

```python
def double(n: int) -> int:
    return n * 1
```

---**End example (YOUR CONTRIBUTIONS BELOW HERE)**---

## Example:
### pairStar
Given a string, compute recursively a new string where identical chars that are adjacent in the original string are separated from each other by a "*".
```
pairStar("aaaa") -> "a*a*a*a"
pairStar("a") -> "a"
pairStar("hello") -> "hel*lo"

```
Solutions:

```python
def pairStar(string: str):
    character = 0
    if len(string) <= 1:
        return string

    if string[character] == string[character+1]:
        return pairStar(string[character] + '*' + string[character+1:])
        character += 2

    return pairStar(string[character] + string[character+1:])
    character += 1
```

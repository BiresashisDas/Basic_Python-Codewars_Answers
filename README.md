# Basic Python

**1. We need a function that can transform a number (integer) into a string.**

**What ways of achieving this do you know?**
   
***Examples (input --> output):***

> ***123  --> "123"***
> 
>***999  --> "999"***
> 
>***-100 --> "-100"***


<b><u>*Ans:-*<u></b>

```python
def number_to_string(num):
    # Return a string of the number here!
    return str(num)
```

**2. Jenny has written a function that returns a greeting for a user. However, she's in love with Johnny, and would like to greet him slightly different. She added a special case to her function, but she made a mistake.**

**Can you help her?**

***Ans:-*** Below is the correct code.

```python
def greet(name):
   if name == "Johnny":
      return "Hello, my love!"
   else:
      return "Hello, {name}!".format(name=name)
```

**3. Complete the method that takes a boolean value and return a <code>"Yes"</code> string for <code>true</code>, or a <code>"No"</code> string <code>for</code> false.**

***Ans:-***

`````python
def bool_to_word(boolean):
   # TODO
   if boolean == True:
      return "Yes"
   else:
      return "No"
`````


**4. Create a function which answers the question "Are you playing banjo?".**
**If your name starts with the letter "R" or lower case "r", you are playing banjo!**

**The function takes a name as its only argument, and returns one of the following strings:**

>***name + " plays banjo"***
>
>***name + " does not play banjo"***

***Ans:-***

```python
def are_you_playing_banjo(name):
   # Implement me!
   if name.startswith("R") or name.startswith("r"):
      return name + " plays banjo"
   else:
      return name + " does not play banjo"
```

**5. Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).**

***For example,***

`````
[True,  True,  True,  False,
   True,  True,  True,  True ,
   True,  False, True,  False,
   True,  False, False, True ,
   True,  True,  True,  True ,
   False, False, True,  True]
`````

***Ans:-***

`````python
def count_sheeps(sheep):
  # TODO May the force be with you
    return sheep.count(True)
`````

## *Convert number to reversed array of digits*

**6. Given a random non-negative number, you have to return the digits of this number within an array in reverse order.**

***Example(Input => Output):***
>35231 => [1,3,2,5,3]
>
>0 => [0]

***Ans:-***

```python
def digitize(n):
    
    n = list(str(n))
    n.reverse()
    return [int(x) for x in n]
```

## *A Needle in the Haystack*

**7. Can you find the needle in the haystack?**

**Write a function <code>findNeedle()</code> that takes an <code>array</code> full of junk but containing one <code>"needle"</code>**

**After your function finds the needle it should return a message (as a string) that says:**

**<code>"found the needle at position "</code> plus the <code>index</code> it found the needle, so:**

***Example(Input --> Output)***

<code>["hay", "junk", "hay", "hay", "moreJunk", "needle", "randomJunk"] --> "found the needle at position 5" </code>

***Ans:-***

```python
def find_needle(haystack):
    # your code here
    haystack = haystack.index("needle")
    return f"found the needle at position {haystack}"
```

## *A function within a function*

**8. Given an input n, write a function always that returns a function which returns n. Ruby should return a lambda or a proc.**

>***three = always(3)***
>
>****three() /\* returns 3 \*/****

***Ans:-***

```python

def always(n=0):
    # ...
    return lambda: n

```

## *Sum Arrays*

**9. Write a function that takes an array of numbers and returns the sum of the numbers. The numbers can be negative or non-integer. If the array does not contain any numbers then you should return 0.**

***Examples***

Input: <code>[1, 5.2, 4, 0, -1]</code>  
Output: <code>9.2</code>

Input: <code>[]</code>  
Output: </code>0</code>

Input: <code>[-2.398]</code>  
Output: <code>-2.398</code>


**Assumptions**

- You can assume that you are only given numbers.
- You cannot assume the size of the array.
- You can assume that you do get an array and if the array is empty, return 0.

***Ans:-***

```python
def sum_array(a):
    return sum(a)
```

## *Multiply*

**10. This code does not execute properly. Try to figure out why.**

***Ans:-*** Below is the correct code ⬇️

```python
def multiply(a, b):
    return a * b
```

## *Surface Area and Volume of a Box*

**11. Write a function that returns the total surface area and volume of a box as an array: <code>[area, volume]**</code>

***Ans:-***

```python
def get_size(w,h,d):
    #your code here
    area = (2*(w*h)) + (2*(w*d)) + (2*(h*d))
    volume = d * w * h
    result = [area, volume]
    return result
```

## *Rock Paper Scissors*

**12. Let's play! You have to return which player won! In case of a draw return Draw!.**

***Examples(Input1, Input2 --> Output):***

```box
"scissors", "paper" --> "Player 1 won!"
"scissors", "rock" --> "Player 2 won!"
"paper", "paper" --> "Draw!"
```

***Ans:-***

```python
def rps(p1, p2):
    #your code here
    
    r = "rock"
    p = "paper"
    s = "scissors"
    
    if (p1 == r and p2 == r) or (p1 == p and p2 == p) or (p1 == s and p2 == s):
        return "Draw!"
    elif (p1 == r and p2 == p) or (p1 == s and p2 == r) or (p1 == p and p2 == s):
        return "Player 2 won!"
    elif (p1 == r and p2 == s) or (p1 == s and p2 == p) or (p1 == p and p2 == r):
        return "Player 1 won!"
```

## Formatting decimal places \#0

**13. Each number should be formatted that it is rounded to two decimal places. You don't need to check whether the input is a valid number because only valid numbers are used in the tests.**

> <code>Example:     
>5.5589 is rounded 5.56   
> 3.3424 is rounded 3.34</code>

***Ans:-***

```python
def two_decimal_places(n):
    return round(n,2)
```

## Formatting decimal places \#1

**14. Each floating-point number should be formatted that only the first two decimal places are returned. You don't need to check whether the input is a valid number because only valid numbers are used in the tests.**

**Don't round the numbers! Just cut them after two decimal places!**

*Right examples:*    
<code>32.8493 is 32.84</code>  
<code>14.3286 is 14.32</code>

*Incorrect examples (e.g. if you round the numbers):*  
<code>32.8493 is 32.85</code>  
<code>14.3286 is 14.33</code>

```python
import math
def two_decimal_places(number):
    res = math.trunc(number * 100) / 100
    return res
```

## Stringy Strings

**15. write me a function <code>stringy</code> that takes a <code>size</code> and returns a string of alternating <code>1</code>s and <code>0</code>s.**

- *the string should start with a <code>1</code>.*

- *a string with <code>size</code> 6 should return :<code>'101010'</code>.*

- *with <code>size</code> 4 should return : <code>'1010'</code>.*

- *with <code>size</code> 12 should return : <code>'101010101010'</code>.*

- *The size will always be positive and will only use whole numbers.*

  ***Ans:-***

  ```python
  def stringy(size):
    # Good Luck!
    return ('10' * size)[:size]
  ```

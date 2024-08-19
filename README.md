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

```bash
def number_to_string(num):
    # Return a string of the number here!
    return str(num)
```

**2. Jenny has written a function that returns a greeting for a user. However, she's in love with Johnny, and would like to greet him slightly different. She added a special case to her function, but she made a mistake.**

**Can you help her?**

***Ans:-*** Below is the correct code.

    def greet(name):
    
    if name == "Johnny":
        return "Hello, my love!"
    else:
        return "Hello, {name}!".format(name=name)


**3. Complete the method that takes a boolean value and return a <code>"Yes"</code> string for <code>true</code>, or a <code>"No"</code> string <code>for</code> false.**

***Ans:-***

    def bool_to_word(boolean):
    # TODO
    if boolean == True:
        return "Yes"
    else:
        return "No"


**4. Create a function which answers the question "Are you playing banjo?".**
**If your name starts with the letter "R" or lower case "r", you are playing banjo!**

**The function takes a name as its only argument, and returns one of the following strings:**

>name + " plays banjo"
>
>name + " does not play banjo"

***Ans:-***

        def are_you_playing_banjo(name):
            # Implement me!
            if name.startswith("R") or name.startswith("r"):
                return name + " plays banjo"
            else:
                return name + " does not play banjo"

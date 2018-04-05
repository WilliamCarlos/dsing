### Functions in math
In math, functions are things that take the form:
```
function(input) = [do something to the input and give that back] 
```

For example, the function
f(x) = x^2

1. Takes an input (x)
2. Does something to the input (squares it, x -> x*x)
3. and "gives back" that new thing (x*x)

Let's say our input is 2.
1. we give the function our input, 2: f(2)
2. The function, f, does something to our input: 2*2
3. The function, f, gives us back our modified input (2*2 -> 4). 

### Python functions do the same thing

1. We specify what we want to give our function, our inputs, in the function header
```
def some_function(input1, input2, input3): # this line is the function header
    [body of function]
```

2. We do stuff in the body of the function. We "modify our input". 
```
def some_function(input1, input2, input3): # this line is the function header
    # Body of function
    new_variable1 = input2 + input3
    new_variable2 = input1 * input2 * input3
    new_variable3 = 5
    # WhatEVER computation you want the world is your oyester
```

3. Our function "gives back" our modified input. But ONLY what you tell it to. You tell a function what to "give back" by using the "return" keyword. 
```
def some_function(input1, input2, input3): # this line is the function header
    # Body of function
    new_variable1 = input2 + input3
    new_variable2 = input1 * input2 * input3
    new_variable3 = 5
    # WhatEVER you want the world is your oyester

    return new_variable1
```
So in this case, some_function() will "give back" new_variable1 because we wrote
"return new_variable1"

**All the calculations you do in your function that you do not return WILL DISAPPEAR**

**So you MUST "return" all variables you want to keep!**
(except for mutable variables, which are pass by ref in python, but ignore this for now)


Now, Dsing. You might be wondering. What does it mean for a function to "return" something?
Well now, that's a darn 'n dandy good question as old as time.

If you call a function, the variables it returns will be assigned to the left hand side of the function call.
```
	[stuff random_function() returns] = random_function()
```
In relation to the above example, some_function():
```
	[new_variable1] = some_function(3, 5, 7)
```
some_function() "returned" or "gave back" new_variable1, so the left hand side of the = will be assigned whatever new_variable1 was storing.

```
	# In this case, what_func_gives_back = new_variable1 since that's what some_function() returns
	what_func_gives_back = some_function(3, 5, 7) 
```


### A concrete example
Suppose we have a function that squares a number.
```
def square_this_number(input_num): # we take in some input, num_input (i.e. the number we want to square)

    # We do whatever calculations we want to do here. For example, we can square it like f(x) = x^2
    square = input_num * input_num # equivalent to x*x

    # We can also do random stuff like print the input
    print(input_num)

    # Or compute the cube of the number
    cube = input_num * input_num * input_num

    # Or even more random stuff
    print('borgey borge')

    # At this exact line in the code, you can access variables like "square" and "cube"
    # BUT, as soon as this function finishes running, all the variables in this function
    # will disappear. So, if you want to use/save any of these variables (like square),
    # You have to save them somehow/get them out of this function. You can do this by
    # having your function "return" a value. Just like how in the square function in math,
    # f(2) -> 2 * 2 -> gives us 4, we can have our function "give us back" something. 
   
    # In this case, we want to "give back" input_num^2, so we return the variable square
    return square    
```
    
So now, if we call the function:

```
returned_number = square_this_number(5)
```
The returned_number will store what you returned: the variable square. All the variables you
computed in square_this_number(5) are destroyed after the function finishes, BUT since we
"returned" the variable square, we have it stored in returned_number and can still use it. 


Likewise, you can return more than one thing. For example, change the line:
```
return square
```
to
```
return square, cube
```
and the function call will look like this:
```
returned_square, returned_cube = square_this_number(5)
```
So now, the function gives back two things. The variable square, and the variable cube (in that order).


TLDR after you do calculations in a function and have them stored in variables in the function,
return [var1], [var2], ... , [varn] will make the function "give back" or "return" those variables to the place where you called the function:
```
var1, var2, ... varn = function_call(input_vars)
```



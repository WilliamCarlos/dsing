
In math, functions are things that take the form:
```
function(input) = [do something to the input]
```

For example, the function
f(x) = x^2
Takes an input (x), does something to the input (squares it, x -> x*x), and "gives back" that new thing (x*x)

Let's say our input is 2.
f(2) -> 2*2 (does something to our input) -> gives us back our modified input (4). 


Python functions do the same thing
```
def square_this_number(input_num): # we take in some input, num_input

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



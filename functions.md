
In math, functions are things that take the form:
```
function(input) = [do something to the input]
```

For example, the function
f(x) = x^2
Takes an input (x), does something to the input (squared it, x -> x*x), and "gives back" that new thing (x*x)



Python functions do the same thing
```
def square_this_number(input_num): # we take in some input, num_input

    # We do whatever calculations we want to do here.

    # Compute the square of the number
    square = input_num * input_num # equivalent to x*x

    # Compute the cube of the number
    cube = input_num * input_num * input_num

    print('borgey borge')

    # After doing any/all computations we want, we still need to specify what to "give back"
    # In this case, we want to give back input_num^2 so we return square
    return square
    
```
    
So now, if we call the function:

```
returned_number = square_this_number(5)
```
The returned_number will store what you returned: the variable square.
If you don't have any "return" in the function, it will not "give back" anything and returned_number will be "None".

Likewise, you can return more than one thing. For example, change:
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



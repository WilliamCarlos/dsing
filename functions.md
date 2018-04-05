
In math, functions are things that take the form
function(input) = [do something to the input]

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
    
    
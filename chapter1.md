---
title       : Basic Programming
description : See how DataCamp handles variables
attachments :


--- type:NormalExercise lang:python xp:100 skills:1 key:f2b3238ea0
## Set your Variables

We'll start with the most basic of programming tasks, storing a value in a variable.

*** =instructions
- Create three variables, `foo`, `bar`, and `baz`.
- Set `foo` to 1 and `bar` to the string "Quantum"
- Set `baz` to a list with the numbers 1, 2, and 3 in it, in that order.

*** =hint
- Remember that you don't need to initialize variables in Python (unlike in C++ or Javascript). You can just declare them with their values right away.

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
# Set variable foo to 1 and variable bar to "Quantum"
# Set variable baz to a list with 1, 2, and 3 in that order.

```

*** =solution
```{python}
# Set variable foo to 1 and variable bar to "Quantum"
# Set variable baz to a list with 1, 2, and 3 in that order.
foo = 1
bar = "Quantum"
baz = [1,2,3]

```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

test_object("foo")
test_object("bar")
test_object("baz")

success_msg("Great! Let's move on to the next one.")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:8ae1a9a8fc
## Write a Loop

Next we'll use a loop to create a bigger list.

*** =instructions

Create a variable `foo`, and use a `for` loop to store a list of the numbers 0 to 99 in it, in ascending order.

Note that you MUST use a `for` loop in this example. We've included some other ways to create the list as examples below. In general we will let you use whatever method you want, but the `for` loop is so important that we are forcing you to use it in this exercise.

*** =hint
- A for loop in Python starts like this: `for x in list_name:`
- You can use the `range(a,b)` function to create a list of numbers from a to b-1.

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
# Write your for loop below.
foo = []


# This section creates the list using a while loop.
# Uncomment the lines below to test it out,
# Or just leave it commented out when you run your own code.
# foo = []
# count = 0
# while count < 100:
#     foo.append(count)
#     count = count + 1

# This section creates the list by typing it all in.
# As before, uncomment the code to test it out.
# foo = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 
#    28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 
#    54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 
#    80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]

# Here is a super-simple third way to do it!
# foo = list(range(0,100))

```

*** =solution
```{python}
foo = []
for x in range(0,100):
    foo.append(x)

# There are other ways to do this in Python as well: "List Comprehensions", that are more powerful but a little harder to read.

```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

test_object("foo")

test_for_loop(index=1,
              for_iter=None,
              body=None,
              orelse=None,
              expand_message=True)

success_msg("Great! Let's move on to the last stage.")

```

--- type:NormalExercise lang:python xp:100 skills:2 key:133eefc173
## A Simple Function

Finally, let's make and use a simple function.

*** =instructions

Here's your last programming task for today: 
- Create a simple function named `square` that takes a number, squares it, and returns it.
- Use your function to square the number 37.
- Print the result.

A note: DataCamp uses Python 3, not Python 2. The proper use of `print` is as a function: `print(variable_name)`.

*** =hint

- function declarations in Python start with `def function_name(argument):`

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}

```

*** =solution
```{python}
def square(x):
    return x*x

y = square(37)
print(y)
```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

test_function_v2("square",
              index=1,
              eq_condition="equal",
              do_eval=True,
              not_called_msg="You did not call your square() function.",
              incorrect_msg=None)

test_output_contains("1369",
                     pattern=True,
                     no_output_msg="You did not print the result of your function.")

success_msg("You're done! You can continue with the rest of The Quantum World.")

```

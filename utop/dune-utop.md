# How to use utop - An example with P3

## Getting Setup - How to Access the Sets Module

The purpose of this short tutorial is to teach you how to use utop, 
in particular with Project 3 - NFA to DFA.

The first thing you need to do is navigate to the project3 directory, and type ```dune utop src``` like so:

![Opening Utop](img/dune_utop_src.png)

Once we have opened utop we can start interactively testing our code.

Recall that we made available a Sets module for you to use when implementingall your functions. Again, we strongly encourage you to use it as it'll make implementing them much easier.

First, we suggest you try some of the functions in it. However, you'll notice that you're not able to access them directly. You might've tried to do something like this:

![Can't Open Sets Module](img/cant_open_sets.png)

The reason why is because the Sets module is not simply available from the top level, but rather it is nested within the general P3 module that we're using for this project. It doesn't necesarilly make a difference, but it is the way it is implemented.

Thus, instead of opening Sets, try opening "P3", like so:

![Opening P3](img/open_p3.png)

You'll notice you'll get no errors, and we can actually see what's available under P3, like so:

![What's Available in P3](img/whats_available_p3.png)

Aha! There it is. Notice that you have access to the Nfa, Regexp and Sets module via P3. **However**, the Nfa and Regexp where already "opened" when you loaded our src when calling ```dune utop src```, which means that we don't need to preface their calls in any way. Further as we look at some examples we'll see different ways to call them.

In the case of the Sets module however, we must preface it with Sets.something in order to use its functions, like so:

![Sets Examples](img/sets_example.png)

We encourage you to try the different functions available in the sets.ml file to get a sense for how they work and where you might use them.

## Interactively Testing your Code

Now let's look at some examples of how you might want to interactively test your code. First, I'll make an nfa example record we'll use. I'll use the same one from the project README, which is this one:

![Nfa Pic](img/nfa_drawn.png)

Now, let's actually write it out:

![Making the NFA](img/making_the_nfa.png)

Now let's run e-closure on it:

![E-Closure on NFA](img/eclosure_example.png)

Now other functions:

![Other functions on NFA](img/new_stuff_examples.png)

Now let's convert it to a DFA!

![Converting to DFA](img/converting_to_dfa.png)

## Regex Portion

Now that should have given you a sense of how you can interactively make examples and test your code. Let's look at how you'd do this with the regex module as well. Let's create a regex:

![Creating the Regex](img/creating_regex.png)

Let's turn it into an NFA:

![Regex to NFA](img/regex_to_nfa.png)

And now let's test it!

![Testing the Regex](testing_regex.png)

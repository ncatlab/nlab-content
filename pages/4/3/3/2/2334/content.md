This entry is about the inner workings of a web-based program that generates componentwise illustrations of simple [[limit]]s and [[colimit]]s in [[Set]] as developed at

* J. Paine, [Category Theory Demonstrations](http://www.j-paine.org/cgi-bin/webcats/webcats.php)

***

In this section, I'll explain coproducts by showing you a program that implements the categorical coproduct of sets. We programmers live our working lives surrounded by data structures and subroutines, entities that become as concrete to us &#8212; as "thing-like", as "manipulable" &#8212; as teacups and bricks. So if I can implement some categorical calculations as programs, I hope it will give them a sense of reality that the maths alone might lack. This way of explaining category theory isn't new, actually: it's the idea behind the following book, which implements categorical constructions in the programming language ML:

* [_Computational Category Theory_ (dead link)]( http://www.cs.manchester.ac.uk/~david/categories/book/book.pdf), by [David Rydeheard](http://www.cs.manchester.ac.uk/~david/) and [Rod Burstall](http://www.dcs.ed.ac.uk/home/rb/).

## Preliminaries: functional programming in Python 3.0 ##

I'll implement my categorical coproduct in the programming language [Python 3.0](http://www.python.org/download/releases/3.0/). This is because: its syntax makes it easy to read; many programmers already know it; and it's free, so you can download it from the above link and try the examples yourself. 

But most importantly, Python supports [functional programming] (http://en.wikipedia.org/wiki/Functional_programming). That is, functions are [first-class citizens](http://en.wikipedia.org/wiki/First-class_object), meaning that one can assign them to variables and store them in datatypes, pass them into other functions as arguments and back from other functions as results, and construct them at runtime. 

In the next few paragraphs, I'll introduce Python 3.0 and then functional programming in Python. I'll do so by using it as a desk calculator, where I type commands &#8212; usually, expressions to be evaluated &#8212; and get back a result. If you want to try this, you can type them either into the Python command-line window, or into Python's IDLE graphical user-interface window.

As a start, this shows Python evaluating simple arithmetic expressions. What I type is after the three greater-than signs; Python's reply is on a line by itself:

    >>> 1
    1
    >>> 1+3
    4
    >>> 1+2*5
    11

I can store a result in a variable, and then use the variable as all or part of an expression. I'm showing you this because although the example below only stores numbers in variables, I shall later want to store functions. Please note that <code>eleven = 1+2*5</code> means "put the result of evaluating <code>1+2*5</code> into the variable <code>eleven</code>". Like many languages, Python uses the equals sign for assignment, which may be confusing if you're not a programmer:

    >>> eleven = 1+2*5
    >>> eleven
    11
    >>> eleven * 2
    22

I can call a function. The <code>from math import *</code> below merely gets me the built-in arithmetic functions, including <code>exp</code>, and isn't really very interesting:

    >>> from math import *
    >>> exp(1)
    2.7182818284590451

This is where it begins getting interesting. Below, I put the _function_ <code>exp</code> into the variable <code>myfunc</code>. I can then apply <code>myfunc</code> in the same way I did <code>exp</code>:

    >>> myfunc = exp
    >>> myfunc(1)
    2.7182818284590451

Instead of using <code>exp</code> as a function value, I can write a "lambda expression":

    >>> identity = lambda x: x
    >>> identity(5)
    5
    >>> double = lambda x: 2*x
    >>> double(5)
    10

A lambda expression denotes a function without naming it or hiving it off into a separate definition. Then, in the same way that 1 denotes an integer and can be used as a constant in a language of arithmetic expressions, a lambda expression can be used in a language of expressions over functions. You can see this in the interaction below, where I have applied a lambda expression to 5. The syntax is the same as for <code>double(5)</code>, except that in place of <code>double</code>, we have the lambda expression:

    >>> (lambda x: 2*x)(5)
    10

By the way, lambda expressions arose as part of the lambda calculus. \[ Possibly put some of this on a new lambda calculus page \] This is a mathematical model of computation,  invented by the logician [Alonzo Church](http://en.wikipedia.org/wiki/Alonzo_Church) as a foundation for logic. (One topic he wanted to investigate was G&ouml;del's incompleteness theorem, hoping it might not apply to logic founded on the lambda calculus.) It consists of a language of expressions over values which include functions, and a set of transformation rules for evaluating these expressions. His notation for functions used Greek lambda to signal a function's argument: in it, the identity function is written $\lambda x.x$. Python's <code>lambda x: x</code>, and lambda expressions in other programming languages, are keyboard approximations to this notation. I should note that the phrase "lambda expression" seems to be ambiguous: some people use it only for functions written using lambda notation, while others use it to mean any expression in the lambda calculus. I suspect, though I haven't yet looked at Church's original paper, that he used it in the first sense. You'll find some online references about the lambda calculus at the n-Category Caf&eacute; thread [_Classical vs Quantum Computation (Week 1)_](http://golem.ph.utexas.edu/category/2006/10/classical_vs_quantum_computati.html), and a history of it at:

* [_History of Lambda-calculus and
Combinatory Logic_](http://www-maths.swan.ac.uk/staff/jrh/papers/JRHHislamWeb.pdf), by Felice Cardone and J. Roger Hindley.

... I now have all the prerequisites needed for some functional programming....

    >>> compose = lambda f, g: lambda x: g(f(x))

    >>> double_then_exp = compose( double, exp )
    >>> double_then_exp(1)
    7.3890560989306504
    >>> exp(2)
    7.3890560989306504 


## Categorical definition of coproduct ##

I'll start with the definition of coproduct, which I've lightly edited from Section 3, _Coproducts and Colimits_ in Chapter III. _Universals and Limits_, of:

* [_Categories for the Working Mathematician_], by Saunders Mac Lane.

> For any [[category]] $C$, a _coproduct diagram_ consists of [[object|objects]] $a$, $b$ and $c$ of $C$, and a pair of [[morphism|arrows]] $i:a\to c$ and $j:b\to c$. This pair has the familiar [[universal property]]: For any pair of arrows $f:a\to d$ and $g:b\to d$, there is a unique arrow $h:c\to d$, such that $f = i;h$ and $g = j;h$.

Before going on to an example, I must just explain that I am using semicolon to denote composition, with the meaning that $(i;h)(x)$ = $h(i(x))$. That is, we apply $i$ first, then $h$. As the page on [[composition]] explains, this is an alternative to the standard mathematical notation $h \circ i$: computer scientists often prefer the semicolon notation, because it reflects the order in which the functions get applied.

To create an example of a coproduct diagram, I'll start by defining the sets $a$, $b$ and $c$:

    a = { 'dimanche', 'lundi', 'mardi' };
    b = { 'Mittwoch', 'Donnerstag', 'Freitag', 'Samstag' };
    c = { 'Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday' };

Python 3.0 has adopted mathematical notation for sets, enclosing them in curly brackets. Quotes enclose string constants, which I'm using to create arbitrary set elements.

Now I need the pair of arrows $i$ and $j$. I'll define these as functions:

    # Maps a to c.
    def i( x ): 
      if x == 'dimanche':
        return 'Sunday';
      elif x == 'lundi':
        return 'Monday';
      elif x == 'mardi':
        return 'Tuesday'; 

    # Maps b to c.
    def j( x ): 
      if x == 'Mittwoch':
        return 'Wednesday';
      elif x == 'Donnerstag':
        return 'Thursday';
      elif x == 'Freitag':
        return 'Friday';
      elif x == 'Samstag':
        return 'Saturday';

...\[Explain somewhere why I have made a and b not subsets of c. In examples where they are, perhaps readers don't see the purpose of the injections, so I want to make that explicit. Also, I shall later use this \[but maybe not appropriate topic for nLab? Though relevant to HDA&N\] to talk about "glueing data" (database merging, sensor fusion.)\]

One important point is that, to keep my program simple, I'm cheating a little bit. In category theory, essential parts of every arrow are its [[source]] and its [[target]]. Thus, the arrow $i$ that maps $a$ to $c$ is _different_ from an arrow that maps $a$ into &mdash; say &mdash; the set $\{'Sunday','Monday','Tuesday'\}$, or the set $\{'Sunday','Monday','Tuesday','Friday'\}$. This is so even if their mappings are the same. In computing terminology, we would say that essential parts of every arrow are its argument type and its result type. 

If I represent $i$ and $j$ by functions as above, I can't represent that in my code. But I shall do so by writing the source and target in a comment above every function. \[Perhaps I'll show a version later that does represent arrows. Use a dict with source, target, and body fields.\]

Now I'll show the definition of coproduct again: 

> For any category $C$, a _coproduct diagram_ consists of objects $a$, $b$ and $c$ of $C$, and a pair of arrows $i:a\to c$ and $j:b\to c$. This pair has the familiar universal property: For any pair of arrows $f:a\to d$ and $g:b\to d$, there is a unique arrow $h:c\to d$, such that $f = i;h$ and $g = j;h$. 

I have created the objects $a$, $b$ and $c$ and the arrows $i$ and $j$: \[insert diagram a<--i--c--j-->b. It would be really nice to (a) be able to click on the objects and arrows and see their content; (b) drag them around and manipulate them.\]. Now look at the sentence following "universal property". I'm going to change the wording slightly:

> You give me any pair of arrows $f:a\to d$ and $g:b\to d$, and I will give you a unique arrow $h:c\to d$, such that $f = i;h$ and $g = j;h$. 

But this sounds like a function talking! "You give me these arrows $f$ and $g$," it commands me, "and I will give you a new arrow $h$." \[ link in: CftWM 63, after (2), and the phrase "uniquely determined" \] So I am now going to implement a function that takes arrows $f$ and $g$ and returns our $h$. In fact, I want you to see the coproduct diagram \[a<--i--c--j-->b\] as such a function, so I am first going to implement another function that turns it into one. 

...\[To be continued\]

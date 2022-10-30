
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# The &#955;-calculus
* table of contents
{: toc}

## Idea

The **lambda calculus** is:

* a simple [[programming language]];

* a *model of computation* (akin to [[Turing machine]]s and [[recursive function]]s), through which we can study the computability and complexity of [[functions]] and predicates; and

* an [[internal language]] for [[cartesian closed categories]].

It comes in both *typed* and *untyped* (or, more correctly, *single-typed*) versions.


## Concepts

### Abstraction and application

The basic constructs of lambda calculus are *[[lambda abstractions]]* and *applications*.  If $t$ is an expression of some sort involving a free variable $x$ (possibly vacuously), then the lambda abstraction

$$ \lambda x. t $$

is intended to represent the function which takes one input and returns the result of substituting that input for $x$ in $t$.  Thus, for instance, $(\lambda x. (x+1))$ is the function which adds one to its argument.  Lambda expressions are often convenient, even outside lambda calculus proper, for referring to a function without giving it a name.

Application is how we "undo" abstraction, by applying a function to an argument.  The application of the function $f$ to the argument $t$ is generally denoted simply by $f t$.  Applications can be parenthesized, so for instance $f(t)$ and $(f)t$ and $(f t)$ all denote the same thing as $f t$.

Application is generally considered to associate to the left.  Thus $u v w$ denotes the application of $u$ to $v$, followed by application of the result (assumed to again be a function) to $w$.  This allows the representation of functions of multiple variables in terms of functions of one variable via "currying" (named for Haskell Curry, although it was invented by Moses Sch&#246;nfinkel): after being applied to the first argument, we return a function which, applied to the next argument, returns a function which, when applied to the next argument, ... , returns a value.  For instance, the "addition" function of two variables can be denoted $(\lambda x. (\lambda y. x+y))$: when applied to an argument $x$, it returns a function which, when applied to an argument $y$, returns $x+y$.  This is so common that it is generally abbreviated $(\lambda x y. x+y)$.

### Evaluation and Reduction

*Evaluation* or *reduction* is the process of "computing" the "value" of a lambda term.  The most basic operation is called *[[beta reduction]]* and consists in taking a lambda abstraction at its word about what it is supposed to do when applied to an input.  For instance, the application $(\lambda x. x+1) 3$ reduces to $3+1$ (and thereby, presuming appropriate rules for $+$, to $4$).  Terms which can be connected by a [[zigzag]] of beta reductions (in either direction) are said to be *beta-equivalent*.

Another basic operation often assumed in the lambda calculus is *[[eta reduction]]/expansion*, which consists of identifying a function, $f$ with the lambda abstraction $(\lambda x. f x)$ which does nothing other than apply $f$ to its argument.  (It is called "reduction" or "expansion" depending on which "direction" it goes in, from $(\lambda x. f x)$ to $f$ or vice versa.)

A more basic operation than either of these, which is often not even mentioned at all, is *alpha equivalence*; this consists of the renaming of bound variables, e.g. $(\lambda x. f x) \to (\lambda y. f y)$.

More complicated systems that build on the lambda calculus, such as various [[type theories]], will often have other rules of evaluation as well.

In good situations, lambda-calculus reduction is *[[confluent category|confluent]]* and *terminating* (the [[Church-Rosser theorem]]), so that every term has a *[[normal form]]*, and two terms are equivalent precisely when they have the same normal form.

## Variants

### Pure lambda calculus

In the pure "untyped" lambda calculus, there is only one kind of variable and one kind of term, and the only construction used to form expressions is *application* of a function $f$ to an argument $t$, generally denoted simply $f t$.  In particular, all variables and terms "represent functions", and can be applied to any other variable or term.

From the point of view of [[type theory]], it is more appropriate to call this "single-typed" or "unityped" lambda-calculus rather than "untyped" --- there is a single type which all terms belong to.

As an example of the sort of freedom this allows, any term can always be applied to itself.  We can then form the term $\lambda x. x x$ which applies its argument to itself.  The self-application of this term:

$$ (\lambda x. x x) (\lambda x. x x) $$

is a classic example of a term which admits an infinite sequence of beta-reductions (each of which leads back to itself).

In pure untyped lambda calculus, we can define [[natural numbers]] using the [[Church numerals]]: the number $n$ is represented by the operation of $n$-fold iteration.  Thus for instance we have $2 = \lambda f. (\lambda x.f (f x))$, the function which takes a function $f$ as input and returns a function that applies $f$ twice.  Similarly $1 = \lambda f. (\lambda x.f x)$ is the identity on functions, while $0 = \lambda f. (\lambda x . x)$ takes any function $f$ to the identity function (the 0th iterate of $f$).  We can then construct (very inefficiently) all of arithmetic, and prove that the arithmetic functions expressible by lambda terms are exactly the same as those computable by Turing machines or (total) recursive functions.

The most natural sort of *model* of pure lambda calculus is a set or other object $D$ which is equivalent to its own [[exponential]] $D^D$.  Of course there are no nontrivial such models in sets, but they do exist in other categories, such as [[domain]]s. It is worth remarking that a necessary condition on such $D$ is that every term $f \colon D^D$ have a fixed-point; see [[fixed-point combinator]]. 


### Simply typed lambda calculus

In simply typed lambda calculus, each variable and term has a [[type theory|type]], and we can only form the application $f t$ if $t$ is of some type $A$ while $f$ is of a function type $A \to B = B^A$ whose domain is $A$; the type of $f t$ is then $B$.  Similarly, if $x$ is a variable of type $A$ and $t$ is a term of type $B$ involving $x$, then $\lambda x. t$ has type $A\to B$.

Without some further type and term constructors, there is not much that can be done, but if we add a [[natural numbers object]] (that is, a type $N$ with constants $0$ of type $N$ and $s$ of type $N\to N$, along with a "definition-by-recursion" operator), then we can express many recursive functions.  (We cannot by this means express *all* computable functions, although we can go beyond [[primitive recursive function]]s; for instance we can define the [[Ackermann function]].  One way to increase the expressiveness to all [[partial recursive function]]s is to add a [[fixpoint]] [[combinator]], or an unbounded search operator).

Simply typed lambda calculus is the natural [[internal language]] of [[cartesian closed categories]].  This means that

* Every cartesian closed category gives rise to a simply typed lambda calculus whose basic types are its objects, and whose basic terms are its morphisms, while

* Every simply typed lambda calculus "generates" a cartesian closed category whose objects are its types and whose morphisms are its equivalence classes of terms.

These two operations are adjoint in an appropriate sense.

### Functional programming

Most [[functional programming|functional]] [[programming language|programming languages]], such as Lisp, ML, and Haskell, are at least loosely based on lambda calculus.


## Related entries

* [[combinator]], [[combinatory logic]]

  * [[fixed-point combinator]]

* [[type theory]]

## References

Please add...


[[!redirects lambda calculus]]
[[!redirects lambda calculi]]
[[!redirects lambda-calculus]]
[[!redirects lambda-calculi]]
[[!redirects ∞-calculus]]
[[!redirects ∞-calculi]]

[[!redirects pure lambda calculus]]
[[!redirects pure lambda-calculus]]
[[!redirects pure ∞-calculus]]

[[!redirects untyped lambda calculus]]
[[!redirects untyped lambda-calculus]]
[[!redirects untyped ∞-calculus]]


[[!redirects unityped lambda calculus]]
[[!redirects unityped lambda-calculus]]
[[!redirects unityped ∞-calculus]]

[[!redirects typed lambda calculus]]
[[!redirects typed lambda-calculus]]
[[!redirects typed ∞-calculus]]

[[!redirects simply typed lambda calculus]]
[[!redirects simply typed lambda-calculus]]
[[!redirects simply typed ∞-calculus]]

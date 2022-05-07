
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

* an [[internal language]] for [[cartesian closed categories]] (for more on this see at _[[relation between type theory and category theory]]_).

It comes in both *typed* and *untyped* versions.

## Concepts

### Abstraction and application

The basic constructs of lambda calculus are *[[lambda abstractions]]* and *applications*.  If $t$ is an expression of some sort involving a free variable $x$ (possibly vacuously), then the lambda abstraction

$$ \lambda x. t $$

is intended to represent the function which takes one input and returns the result of substituting that input for $x$ in $t$.  Thus, for instance, $(\lambda x. (x+1))$ is the function which adds one to its argument.  Lambda expressions are often convenient, even outside lambda calculus proper, for referring to a function without giving it a name.

Application is how we "undo" abstraction, by applying a function to an argument.  The application of the function $f$ to the argument $t$ is generally denoted simply by $f t$.  Applications can be parenthesized, so for instance $f(t)$ and $(f)t$ and $(f t)$ all denote the same thing as $f t$.

Application is generally considered to associate to the left.  Thus $u v w$ denotes the application of $u$ to $v$, followed by application of the result (assumed to again be a function) to $w$.  This allows the representation of functions of multiple variables in terms of functions of one variable via "currying" (named for Haskell Curry, although it was invented by Moses Sch&#246;nfinkel): after being applied to the first argument, we return a function which, applied to the next argument, returns a function which, when applied to the next argument, ... , returns a value.  For instance, the "addition" function of two variables can be denoted $(\lambda x. (\lambda y. x+y))$: when applied to an argument $x$, it returns a function which, when applied to an argument $y$, returns $x+y$.  This is so common that it is generally abbreviated $(\lambda x y. x+y)$.

### Evaluation and Reduction

*Evaluation* or *reduction* is the process of "computing" the "value" of a lambda term.  The most basic operation is called *[[beta reduction]]* and consists in taking a lambda abstraction at its word about what it is supposed to do when applied to an input.  For instance, the application $(\lambda x. x+1) 3$ reduces to $3+1$ (and thereby, presuming appropriate rules for $+$, to $4$).  In general, the beta reduction of a term $(\lambda x.t)(u)$ is defined as the [[substitution#avoiding variable capture|capture-avoiding substitution]] of $u$ for $x$ in $t$,

$$(\lambda x.t)(u) \to_\beta t[u/x].$$

Terms which can be connected by a [[zigzag]] of beta reductions (in either direction) are said to be *beta-equivalent*.

Another basic operation often assumed in the lambda calculus is *[[eta reduction]]/expansion*, which consists of identifying a function, $f$ with the lambda abstraction $(\lambda x. f x)$ which does nothing other than apply $f$ to its argument.  (It is called "reduction" or "expansion" depending on which "direction" it goes in, from $(\lambda x. f x)$ to $f$ or vice versa.)

A more basic operation than either of these, which is often not even mentioned at all, is *alpha equivalence*; this consists of the renaming of bound variables, e.g. $(\lambda x. f x) \to (\lambda y. f y)$.

More complicated systems that build on the lambda calculus, such as various [[type theories]], will often have other rules of evaluation as well.

In good situations, lambda calculus reduction is *[[confluent category|confluent]]* (the [[Church-Rosser theorem]]), so that every term has at most one *[[normal form]]*, and two terms are equivalent precisely when they have the same normal form.  A term is said to be _normalizing_ if its reduction is also terminating---more precisely, $t$ is said to be *weakly-normalizing* if there exists a finite sequence of reductions

$$ t \to t_1 \to t_2 \to \dots \to t_n \nrightarrow $$

terminating in a normal form $t_n$, and *strongly-normalizing* if _all_ sequences of reductions lead to a (by confluence, necessarily unique) normal form.  In general, there exist terms which do not normalize by any reduction sequence, although simply-typed lambda calculus and many other typed variants of lambda calculus are strongly-normalizing.

## Variants

### Pure lambda calculus

In the untyped (or "pure") lambda calculus, every term can be applied to any other term.  As an example of the sort of freedom this allows, we can form the term $u = \lambda x. x x$ which applies its argument to itself, and then define

$$ \omega = u(u) $$

as the self-application of $u$.  Performing beta-reduction on $\omega$ yields

$$ \omega \to_\beta x x[u/x] = u(u) = \omega \to_\beta \omega \to_\beta \dots$$

thus giving the classic example of a non-terminating program.

In pure untyped lambda calculus, we can define [[natural numbers]] using the [[Church numerals]]: the number $n$ is represented by the operation of $n$-fold iteration.  Thus for instance we have $2 = \lambda f. (\lambda x.f (f x))$, the function which takes a function $f$ as input and returns a function that applies $f$ twice.  Similarly $1 = \lambda f. (\lambda x.f x)$ is the identity on functions, while $0 = \lambda f. (\lambda x . x)$ takes any function $f$ to the identity function (the 0th iterate of $f$).  We can then construct (very inefficiently) all of arithmetic, and prove that the arithmetic functions expressible by lambda terms are exactly the same as those computable by Turing machines or (total) recursive functions.

The most natural sort of *model* of pure lambda calculus is a [[reflexive object]] in a cartesian closed category, that is, an object $U$ together with a pair of maps

$$
\array{U & \overset{a}{\underset{\ell}{\rightleftarrows}} & U^U} 
$$

representing $a$pplication and $\ell$ambda, such that $a \circ \ell = 1$ (to validate the $\beta$ equation).  Such data thereby witnesses the [[exponential object]] $U^U$ as a [[retract]] of $U$.  Of course there are no nontrivial such models in sets, but they do exist in other categories, such as [[domain]]s. It is worth remarking that a necessary condition on such $U$ is that every term $f \colon U^U$ have a fixed-point; see [[fixed-point combinator]]. 

From the point of view of [[type theory]] and in particular the "types &#224; la Church" perspective, such a reflexive object $U$ can also be seen as the intrinsic type of _every_ lambda term, and so the untyped lambda calculus is sometimes referred to (a bit cheekily) as really being "uni-typed".  On the other hand, from the "types &#224; la Curry" perspective, it is also possible to begin with the pure lambda calculus as a foundation, and then try to ascribe individual terms more precise types.  For example, the normalizing terms of pure lambda calculus can be characterized precisely as those which are typable in an [[intersection type]] system.

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

* [[relation between type theory and category theory]]

## References

The idea that untyped lambda calculus can be modeled internally to a cartesian closed category as a [[reflexive object]] (an object $U$ such that the exponential $U^U$ is a [[retract]] of $U$) was formulated explicitly by [[Dana Scott]] in

* Dana Scott. Relating theories of the $\lambda$-calculus. In _To H.B. Curry: Essays on Combinatory Logic, Lambda-Calculus and Formalism_ (eds. Hindley and Seldin), Academic Press, 403--450, 1980.

This followed his earlier work constructing an explicit such model in the category of domains:

* Dana Scott. Outline of a Mathematical Theory of Computation. _Proc. 4th Princeton Conf. on Information Sciences and Systems_, 169--176, 1970. [pdf](http://ropas.snu.ac.kr/~kwang/520/readings/sco70.pdf)

* Dana Scott. Data types as lattices. _SIAM Journal of Computing_, 5(3):522--587, September 1976.

Another, more recent take on pure lambda calculus as a certain kind of [[algebraic theory]] (called a "[[lambda theory]]") can be found in

* [[Martin Hyland]]. Classical lambda calculus in modern dress. To appear in _Mathematical Structures in Computer Science_, 2013. [arxiv](http://arxiv.org/abs/1211.5762)

[[!redirects lambda calculus]]
[[!redirects lambda calculi]]
[[!redirects lambda-calculus]]
[[!redirects lambda-calculi]]
[[!redirects λ-calculus]]
[[!redirects λ-calculi]]

[[!redirects pure lambda calculus]]
[[!redirects pure lambda-calculus]]
[[!redirects pure λ-calculus]]

[[!redirects untyped lambda calculus]]
[[!redirects untyped lambda-calculus]]
[[!redirects untyped λ-calculus]]


[[!redirects unityped lambda calculus]]
[[!redirects unityped lambda-calculus]]
[[!redirects unityped λ-calculus]]

[[!redirects typed lambda calculus]]
[[!redirects typed lambda-calculus]]
[[!redirects typed λ-calculus]]

[[!redirects simply typed lambda calculus]]
[[!redirects simply typed lambda-calculus]]
[[!redirects simply typed λ-calculus]]

[[!redirects simply-typed lambda calculus]]

[[!redirects λ-term]]
[[!redirects λ-terms]]
[[!redirects lambda-term]]
[[!redirects lambda-terms]]



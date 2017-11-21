
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In a strict sense of the term, a **function** is a [[homomorphism]] $f : S \to T$ of [[sets]].  We may also speak of a __[[map]]__ or __mapping__, but those terms are used in other ways in other contexts. 

A function from a [[set]] $A$ to a set $B$ is determined by giving, for each element of $A$, a specified element of $B$.  The process of passing from elements of $A$ to elements of $B$ is called [[function application]].  The set $A$ is called the [[domain]] of $f$, and $B$ is called its [[codomain]].

A function is sometimes called a __total function__ to distinguish it from a [[partial function]].


More generally, every [[morphism]] between [[objects]] in a [[category]] may be thought of as a function in a generalized sense. This generalized use of the word is wide spread (and justified) in [[type theory]], where for $S$ and $T$ two [[types]], there is a [[function type]] denoted $S \to T$ and then the expression $f : S \to T$ means that $f$ is a [[term]] of [[function type]], hence is a function. 

In this generalized sense, functions between sets are the [[morphisms]] in the [[category]] [[Set]].  This is [[cartesian closed category|cartesian closed]], and the [[function type]] $S \to T$ is then the [[function set]].

For more on this more general use of "function" see at _[[function type]]_.


## Foundations

The formal definition of a function depends on the [[foundations]] chosen.

* In [[material set theory]], a function $f$ is often defined to be a set of [[ordered pairs]] such that for every $x$, there is at most one $y$ such that $(x,y)\in f$.  The [[domain]] of $f$ is then the set of all $x$ for which there exists some such $y$.  This definition is not entirely satisfactory since it does not determine the codomain (since not every element of the codomain may be in the [[image]]); thus to be completely precise it is better to define a function to be an ordered triple $(f,A,B)$ where $A$ is the domain and $B$ the codomain.

* In [[structural set theory]], the role of functions depends on the particular axiomatization chosen.  In [[ETCS]], functions are among the undefined things, whereas in [[SEAR]], functions are defined to be particular relations (which in turn are undefined things).

* In [[type theory]], functions are simply [[terms]] belonging to [[function types]].

See [[set theory]] and [[type theory]] for more details.


## As morphisms of discrete categories

If we regard sets as [[discrete categories]], then a **function** is a [[functor]] between [[sets]]. The functoriality structure becomes the property that a function preserves [[equality]]:

\[ x = y \Rightarrow f(x) = f(y) .\]


## For classes

One can also speak of functions between proper [[classes]], although the precise details may vary depending on the status of classes with respect to the formal theory. 

In [[ZFC]] for example, proper classes are by design not formal objects in the theory; rather they are proxied by a formula in the language (for instance, the class $V$ of all sets is proxied by the formula $x = x$; intuitively we may think of $V$ as consisting of all $x$ satisfying that formula). Then functions $f: A \to B$ between classes are again classes given by suitable formulas; see for example the MathOverflow discussion [what-are-maps-between-proper-classes](http://mathoverflow.net/questions/63265/what-are-maps-between-proper-classes). If (as described above for material set theory) one wants to describe a function as an ordered triple $(A, f, B)$, then this too can be accommodated if one defines ordered triples/pairs of classes appropriately; see [here](/nlab/show/ordered+pair#class) for one possibility. Thus functors between categories whose objects and morphisms form proper classes can similarly be described in the language. 

Such technical hacks can be avoided by choosing a different foundations. For example, Mac Lane in his [[Categories for the Working Mathematician]] assumes ZFC with a [[universe]] in which some sets are considered large, such as the set of small sets, so that a category like $Set$ (the category of small sets) is again a formal object of the theory. 

## Alternative terms 

Useful terms, more or less synonymous with *function*, are *assignment*, _assignation_ or more specifically *assignation on objects*. These do not have standard meanings but are useful to signal to readers that the domain of the 'function' under consideration is large, or that one is more interested in [[functorial]] extensions of this partial assignation (cf. e.g. Richard Garner, Homomorphisms of higher categories, Adv. Math. 224 (2010) 2269-2311 for many examples). In mathematical writing "assignment" is usually synonymous with _[[function]]_ or _[[map]]_ or "mapping". For example one might speak of "assigning to each positive number its square root" to refer to the function $\sqrt{(-)} \colon \mathbb{R}_{\geq 0} \to \mathbb{R}$. 

Authors may resort to verb forms such as "assigns" or "associates" or "sends" in informal writing, perhaps to avoid the bother of specifying an axiomatic framework in which a formal notion like "function" is ensconced. For example, according to Wikipedia, Jacobson defines a functor $F: C \to D$ between categories as a "mapping" that "associates" to each object $X$ in $C$ an object $F(X)$ in $D$, etc. No clarity would be gained by making this any more formal (which as we saw in the case of functions between classes, such as classes of objects of categories, may involve annoyingly technical hacks). 

Sometimes the word "assignment" is understood more generally as _[[relation]]_, often when authors define a function to be something that "assigns unique values" (for instance  [here](https://books.google.de/books?id=jYniBQAAQBAJ&pg=PA27&lpg=PA27&dq=function+map+assignment+mathematics&source=bl&ots=2aHFjcZ3c9&sig=1HkugZIeSQdnV70U5gjSx_H21ug&hl=en&sa=X&ved=0ahUKEwjpxuPey6nUAhWIfhoKHe9BDy0Q6AEIVTAJ#v=onepage&q=function%20map%20assignment%20mathematics&f=false)). 


## Examples

* [[empty function]]

* [[constant function]]

Many functions that carry special names map some [[ring]] or [[field]] like the [[real numbers]] or [[complex numbers]] to itself:

* [[polynomial]]

* [[exponential]]

* [[step function]]

* [[trigonometric function]]

* [[hypergeometric function]]

* [[special function]]

* ...

Special properties these may have:

* [[continuous function]], [[analytic function]], [[smooth function]]

...

## Related concepts

* [[map]], [[operation]]

* [[partial function]], [[partial recursive function]]

* [[anafunction]]


* [[function set]]

* [[function algebra]], [[pullback of functions]]

* [[continuous function]], [[differentiable function]], [[smooth function]]

* [[bounded function]]

* [[fixed point]]

* [[motivic function]]

* [[functor]]

* [[2-functor]] / [[pseudofunctor]]

  * [[monoidal functor]]

* [[n-functor]]

* [[(∞,1)-functor]]

* [[(∞,n)-functor]]


[[!redirects function]]
[[!redirects functions]]

[[!redirects total function]]
[[!redirects total functions]]
[[!redirects assignation]]
[[!redirects assignment]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In a strict sense of the term, a **function** is a [[homomorphism]] $f \colon S \to T$ of [[sets]]: a prescription which takes any [[element]] $s \in S$ to a unique element $f(s) \in T$, this also called the *[[value]]* of the function at $s$.


Instead of "function" one also speaks of _[[map]]_ or _mapping_, but those terms are used in other ways in other contexts. 

A function from a [[set]] $A$ to a set $B$ is determined by giving, for each element of $A$, a specified element of $B$.  The process of passing from elements of $A$ to elements of $B$ is called [[function application]].  The set $A$ is called the [[domain]] of $f$, and $B$ is called its [[codomain]].

A function is sometimes called a __total function__ to distinguish it from a [[partial function]].


More generally, every [[morphism]] between [[objects]] in a [[category]] may be thought of as a function in a generalized sense. This generalized use of the word is wide spread (and justified) in [[type theory]], where for $S$ and $T$ two [[types]], there is a [[function type]] denoted $S \to T$ and then the expression $f : S \to T$ means that $f$ is a [[term]] of [[function type]], hence is a function. 

In this generalized sense, functions between sets are the [[morphisms]] in the [[category]] [[Set]].  This is [[cartesian closed category|cartesian closed]], and the [[function type]] $S \to T$ is then the [[function set]].

For more on this more general use of "function" see at _[[function type]]_.


## Foundations

The formal definition of a function depends on the [[foundations]] chosen.

### In set theory

* In [[material set theory]], a function $f$ is often defined to be a set of [[ordered pairs]] such that for every $x$, there is at most one $y$ such that $(x,y)\in f$.  The [[domain]] of $f$ is then the set of all $x$ for which there exists some such $y$.  This definition is not entirely satisfactory since it does not determine the codomain (since not every element of the codomain may be in the [[image]]); thus to be completely precise it is better to define a function to be an ordered triple $(f,A,B)$ where $A$ is the domain and $B$ the codomain.

* In [[structural set theory]], the role of functions depends on the particular axiomatization chosen.  In [[ETCS]], functions are among the undefined things, whereas in [[SEAR]], functions are defined to be particular relations (which in turn are undefined things).

### In dependent type theory

In [[dependent type theory]], a [[type]] $A$ is a [[contractible type]] if it comes with an element $a:A$ and a family of identities $x:A \vdash c(x):a =_A x$ indicating that $a$ is a [[center of contraction]]. A **function** between types $A$ and $B$ could be defined as

* a family of elements $x:A \vdash f(x):B$
* a [[span]] $(C; z:C \vdash g(z):A; z:C \vdash h(z):B)$ for which the dependent type $\sum_{z:C} g(z) =_A x$ is a [[contractible type]] for all $x:A$
* a [[multivalued partial function]] $(x:A \vdash P(x); x:A, p:P(x) \vdash f(x, p):B)$ for which the dependent type $P(x)$ is a [[contractible type]] for all $x:A$
* a [[correspondence]] $x:A, y:B \vdash R(x, y)$ for which the dependent type $\sum_{y:B} R(x, y)$ is a [[contractible type]] for all $x:A$. 
* an element of the [[function type]] $f:A \to B$, in dependent type theories with function types. 

The first four definitions are interdefinable with each other in [[dependent type theories]] with [[identity types]] and [[dependent sum types]]: 

* From every family of elements $x:A \vdash f(x):B$, one could define a [[span]] by defining the type $C$ to be a [[copy]] of $A$, $C \coloneqq \mathrm{Copy}(A)$, the family of elements $z:C \vdash g(z):A$ to be $g(z) \coloneqq \pi_1(\alpha(x))$ since for all elements $z:C$, the dependent type $\sum_{x:A} \mathrm{copy}(x) =_C z$ is contractible and with [[center of contraction]] $z:C \vdash \alpha(z):\sum_{x:A} \mathrm{copy}(x) =_C z$, and the family of elements $x:C \vdash h(x):B$ to be $h(x) \coloneqq f(g(x))$. For every element $x:A$, the dependent type $\sum_{z:C} g(z) =_A x$ is always a [[contractible type]]. 

* From every [[span]] $(C; z:C \vdash g(z):A; z:C \vdash h(z):B)$ for which the dependent type $\sum_{z:C} g(z) =_A x$ is a [[contractible type]] for all $x:A$, one can define a family of elements $x:A \vdash f(x):B$ as $f(x) \coloneqq h(\pi_1(\alpha(x)))$ for all [[centers of contraction]] $x:A \vdash \alpha(x):\sum_{z:C} g(z) =_A x$.

* From every family of elements $x:A \vdash f(x):B$, one could define a [[multivalued partial function]] by defining $x:A \vdash P(x)$ to be $P(x) \coloneqq \sum_{y:A} x =_A y$ and $x:A, p:P(x) \vdash f'(x, p):B$ to be $f'(x, p) \coloneqq f(x)$. For every element $x:A$, the dependent type $\sum_{y:A} x =_A y$ is always a [[contractible type]]. 

* From every [[multivalued partial function]] $(x:A \vdash P(x); x:A, p:P(x) \vdash f(x, p):B)$ for which the dependent type $P(x)$ is a [[contractible type]] for all $x:A$, one could define a family of elements $x:A \vdash f'(x):B$ as $f'(x) \coloneqq f(x, \alpha(x))$ for all [[centers of contraction]] $x:A \vdash \alpha(x):P(x)$. 

* From every family of elements $x:A \vdash f(x):B$, one could define a [[correspondence]] by defining $x:A, y:B \vdash R(x, y)$ to be $R(x, y) \coloneqq f(x) =_B y$. For every element $x:A$, the dependent type $\sum_{y:B} f(x) =_B y$ is always a [[contractible type]]. 

* From every [[correspondence]] $x:A, y:B \vdash R(x, y)$ for which the dependent type $\sum_{y:B} R(x, y)$ is a [[contractible type]] for all $x:A$, one could define a family of elements $x:A \vdash f(x):B$ as $f(x) \coloneqq \pi_1(\alpha(x))$ for all [[centers of contraction]] $x:A \vdash \alpha(x):\sum_{y:B} R(x, y)$. 

* The second, third, and fourth definitions of a function are interdefinable via the following relations between [[spans]], [[multivalued partial functions]], and [[correspondences]]:

  * From every span one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:C} g(y) =_A x$ and the family of elements $x:A, p:P(x) \vdash f(x, p):B$ as $f(x, p) \coloneqq h(\pi_1(x))$. 

  * From every multivalued partial function one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} P(x)$ and the family of elements $x:C \vdash g(x):A$ as $g(x) \coloneqq \pi_1(x)$. 

  * From every multivalued partial function one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$. 

  * From every correspondence one could get a multivalued partial function by defining the type family $x:A \vdash P(x)$ as $P(x) \coloneqq \sum_{y:B} R(x, y)$, and the family of elements $x:A, p:P(x) \vdash h(x, p):B$ as $h(x, p) \coloneqq \pi_1(p)$

  * From every span one could get a correspondence by defining the type family $x:A, y:B \vdash R(x, y)$ as $R(x, y) \coloneqq \sum_{z:C} (g(z) =_A x) \times (h(z) =_B y)$. 

  * From every correspondence one could get a span by defining the type $C$ as $C \coloneqq \sum_{x:A} \sum_{y:B} R(x, y)$, the family of elements $z:C \vdash g(z):A$ as $g(z) \coloneqq \pi_1(z)$, and the function $z:C \vdash h(z):B$ as $h(z) \coloneqq \pi_1(\pi_2(z))$ 

If the dependent type theory has [[function types]], then 

* From every element of the function type $f:A \to B$, one could define a family of elements $x:A \vdash f'(x):B$ as $f'(x) \coloneqq \mathrm{ev}(f, x)$, where $f:A \to B, x:A \vdash \mathrm{ev}(f, x):B$ appears in the [[elimination rules]] for function types. 

* From every family of elements $x:A \vdash f(x):B$, one could define an element of the function type $f':A \to B$ as $f' \coloneqq x \mapsto f(x)$, where $x:A, f(x):B \vdash x \mapsto f(x):A \to B$ appears in the [[introduction rules]] for function types.  

### In formal category theory

In [[formal category theory]], sets are [[discrete categories]], and a **function** is a [[functor]] between [[sets]]. The functoriality structure becomes the property that a function preserves [[equality]]:

\[ x = y \Rightarrow f(x) = f(y) .\]

### For classes

One can also speak of functions between proper [[classes]], although the precise details may vary depending on the status of classes with respect to the formal theory. 

In [[ZFC]] for example, proper classes are by design not formal objects in the theory; rather they are proxied by a formula in the language (for instance, the class $V$ of all sets is proxied by the formula $x = x$; intuitively we may think of $V$ as consisting of all $x$ satisfying that formula). Then functions $f: A \to B$ between classes are again classes given by suitable formulas; see for example the MathOverflow discussion [what-are-maps-between-proper-classes](http://mathoverflow.net/questions/63265/what-are-maps-between-proper-classes). If (as described above for material set theory) one wants to describe a function as an ordered triple $(f, A, B)$, then this too can be accommodated if one defines ordered triples/pairs of classes appropriately; see [here](/nlab/show/ordered+pair#class) for one possibility. Thus functors between categories whose objects and morphisms form proper classes can similarly be described in the language. 

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

* [[periodic function]]

## Related concepts

* [[map]], [[operation]]

* [[partial function]], [[partial recursive function]]

* [[anafunction]]


* [[function set]]

* [[function algebra]], [[pullback of functions]]

* [[continuous function]], [[differentiable function]], [[smooth function]]

* [[periodic function]]

* [[linear function]], [[quadratic function]], [[polynomial function]]

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

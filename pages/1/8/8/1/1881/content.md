
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Finite lists and free monoids
* table of contents
{: toc}

## Idea

Given a [[set]] $S$, the __free [[monoid]]__ on $S$ is the set $S^*$ of all __lists__ (finite [[sequences]]) of elements of $S$, made into a monoid using __concatenation__.  The [[free functor]] from [[Set]] to [[Mon]] takes $S$ to $S^*$.


## Definitions

We will give three definitions, which can all be shown equivalent.


### As functions

An element of $S^*$ consists of a [[natural number]] $n$ (possibly $n = 0$) and function from $[n]$ to $S$, where $[n]$ is the [[subset]] $\{i\colon \mathbf{N} \;|\; i \lt n\}$ of $\mathbf{N} = \{0, 1, 2, \ldots\}$.  Such an element is called a __list__ or (to specify $n$) __$n$-tuple__ of elements of $S$.  The number $n$ is called the __length__ of the list.

The __[[empty list]]__ is the unique list of length $0$.  It may be written $()$, $*$, or $\epsilon$, perhaps with a subscript $S$ if desired.

If $n \gt 0$, then the list which assigns $0, \ldots, n - 1$ to $a_0, a_1, \ldots, a_{n-1}$ may be written $(a_0, a_1, \ldots, a_{n-1})$.  For example, if $a,b,c$ are elements of $S$, then $(a,b,c)$ is an element of $S^*$.

Given two lists $x$ and $y$, the former of length $m$ and the latter of length $n$, their __concatenation__ $x * y$ is a list of length $m + n$, given as follows:
$$ i \mapsto \left\{ \array { x_i     & if\; i \lt m \\
                              y_{i-m} & if\; i \geq m } \right. $$

One can now show that concatenation is associative with the empty list as identity; hence $S^*$ is a monoid.


### Recursively

The (underlying) set $S^*$ may be defined as an [[inductive type]] as follows.  There are two basic constructors, one with no arguments, and one with two arguments, of which one is an element of $S$ and the other is an element of $S^*$.  By the yoga of inductive types, that is a complete definition, but we spell it out in more detail while also giving terminology and notation.

So, a __list__ is either the __[[empty list]]__ or the __cons__ (short for 'constructor' and deriving from Lisp) of an element $a$ of $S$ and a (previously constructed) list $x$.  The empty list may may be written $()$, $*$, or $nil$, perhaps with a subscript $S$ if desired; the cons of $a$ and $x$ may be written $a : x$, $(a) * x$, or $cons(a,x)$.  We interpret the definition [[recursion|recursively]], so we can list the elements of $S^*$ in the order in which they appear:

*  $()$,
*  $a : ()$,
*  $a : b : ()$,
*  $a : b : c : ()$,
*  etc.

Here, $a, b, c, \ldots$ are elements of $S$.  We may continue the 'etc' as far as we like, but no farther; while there are lists of arbitrarily long finite length, there are no lists of infinite length.  (We would get such lists, however, if we interpreted the definition [[corecursion|corecursively]], known in computer science as a [[stream]].)  We normally abbreviate the lists above as follows:

*  $()$,
*  $(a)$,
*  $(a,b)$,
*  $(a,b,c)$,
*  etc.

We still must define the monoidal structure on $S^*$; we define the __concatenation__ $x * y$ of $x$ and $y$ recursively in $x$.  To be explicit:

*  $() * y = y$;
*  $(a : x) * y = a : (x * y)$ (with parentheses for grouping, but the parentheses can be dropped now that have this definition).

One can now show that concatenation is associative with the empty list as identity; hence $S^*$ is a monoid.


### By general abstract nonsense

To prove that the category [[Mon]] of monoids is a [[complete category]], one normally shows that the [[forgetful functor]] $U$ (from $Mon$ to the category [[Set]] of sets) preserves all [[limits]].  Then, the [[adjoint functor theorem]] defines a [[left adjoint]] to $U$ if a size condition is met; this adjoint is the functor $*$ that takes a set to its free monoid $S^*$.

To be sure, meeting the solution set condition basically requires starting the constructions in one of the other definitions above; but the proofs may all be thrown onto the adjoint functor theorem. 

Another abstract approach is given in the following general theorem, which applies to more general [[monoid in a monoidal category|monoids in a monoidal category]]: 

+-- {: .num_theorem #monoid_in_monoidal}
###### Theorem 
Suppose $C$ is a monoidal category with countable coproducts for which the tensor product distributes over countable coproducts (for example, a [[cocomplete category|cocomplete]] [[monoidal biclosed category]]). Then a left adjoint to the forgetful functor $Mon(C) \to C$ exists, taking an object $c$ to 
$$\sum_{n \geq 0} c^{\otimes n},$$ 
which thereby becomes the free monoid on $c$. 
=-- 

This applies immediately to $C = Set$, as this is a cocomplete [[cartesian closed category]]. 


## Examples

*  If $S$ is the [[empty set]], then $S^*$ consists only of the empty list; it is the trivial monoid, one manifestation of the [[point]].
*  If $S$ is the point, then $S^*$ is $\mathbf{N}$; the only information in a list of indistinguishable points is the length of the list.  The monoid operation on $\mathbf{N}$ is addition.
*  If $S$ is $\mathbf{N}$, then $\mathbf{N}^*$ is still a [[denumerable set]].  But note that $\mathbf{N} \cong \mathbf{N}^*$ only as sets (that is, ${|\mathbf{N}^*|} = {|\mathbf{N}|} = \aleph_0$ as [[cardinal numbers]]); they are quite different as monoids.
*  Generalising the above, ${|S^*|} = {|S|}$ is $S$ is an [[infinite set]], or more generally ${|S^*|} = max(\aleph_0,S)$ if $S$ is an [[inhabited set]].  (These theorems probably require the [[axiom of choice]], but I haven\'t checked thoroughly.)


## The free monoid monad

If the free monoid functor $F\colon Set \to Mon$ is followed by the forgetful functor $U\colon Mon \to Set$, then we get a [[monad]] on $Set$.  This monad is very important in [[computer science]], where it is known as the __list monad__.

The list monad bears the same relation to [[multicategories]] as the [[identity monad]] on $Set$ bears to ordinary [[categories]].  This relation should be explained at [[generalized multicategory]].


## Foundational relevance

Every definition of free monoid makes use of some form of [[axiom of infinity]], either $\mathbf{N}$ directly or the ability to form general inductive types.  Indeed, as $\mathbf{N} = pt^*$, the axiom of infinity follows from the existence of free monoids.

In [[topos theory]] the equivalent of the above theorem \ref{monoid_in_monoidal} is due to C. J. Mikkelsen:

+-- {: .num_prop #free_monoids_in_topos}
###### Proposition
Let $\mathcal{S}$ be a topos and $\mathbf{mon}(\mathcal{S})$ its category of internal monoids. Then $\mathcal{S}$ has a NNO precisely if the forgetful functor $U:\mathbf{mon}(\mathcal{S})\to \mathcal{S}$ has a left adjoint.
=--

For a proof see Johnstone ([1977](#JT77),p.190).

Furthermore then it is a theorem due to [[Andreas Blass]] ([1989](#Blass)) that $\mathcal{S}$ has a NNO precisely if $\mathcal{S}$ has an [[classifying topos for the theory of objects|object classifier]] $\mathcal{S}[\mathbb{O}]$.

A consequence of this, discussed in sec. B4.2 of (Johnstone 2002,I p.431), is that [[classifying topos|classifying toposes]] for [[geometric theories]] over $\mathcal{S}$ exist precisely if $\mathcal{S}$ has a NNO.

From a different perspective then, in a topos the existence of free objects over various gadgets like e.g. [[algebraic theory|algebraic theories]] or [[geometric theory|geometric theories]] often hinge on the existence of free monoids, the intuition being that the free monoids permit to construct a free model _syntactically_ by providing for the (syntactic) building blocks needed for this process.

Notice that algebraic theories can nevertheless have free algebras even if the ambient topos lacks a NNO. This may happen for algebraic theories that have the property that the free algebra on a finite set of generators has a finite carrier e.g. in the topos $FinSet$ of finite sets [[graphic category|free graphic monoids]] exist.

## Stacks and queues

In [[computer science]], lists often appear as _stacks_ (not to be confused with the [[stacks]] from higher sheaf theory) and _queues_.

Fix a [[monoidal category]] that has [[coproducts]] with the [[unit object]] $I$.  Given an [[object]] $A$, an object of __stacks__ on $A$ is an object $S_A$ equipped with [[morphisms]] $push_A\colon S_A \otimes A \to S_A$ and $pop_A\colon S_A \to S_A \otimes A + I$ such that these diagrams commute:
$$ \array {
   S_A \otimes A &                     & \overset{\iota_{S_A \otimes A,I}}\to &                  & S_A \otimes A + I \\
                 & {}_{push_A}\searrow &                                      & \nearrow_{pop_A} &                                       & \searrow^{push_A + id_I} \\
                 &                     & S_A                                  &                  & \underset{\iota_{S_A \otimes A,I}}\to &                          & S_A + I
   } $$
The idea is that $push_A$ and $pop_A$ are as close to [[inverse morphism|inverses]] as reasonably possible, but $pop_A$ takes us to $S_A \otimes A + I$ rather than to $S_A \otimes A$, because of the empty stack.

Queues are a little more complicated.  An object of __queues__ on $A$ is an object $Q_A$ equipped with morphisms $ins_A\colon A \otimes Q_A \to Q_A$ ('insert') and $rem_A\colon Q_A \to Q_A \otimes A + I$ ('remove').  These operations are far from inverses; whereas popping a stack returns the last item to be pushed onto it, removing an item from a queue returns the *first* item to have been inserted into it.

+-- {: .query}
What are the diagrams for this?  I seem to recall that we need a [[distributive category]]; in particular, we need a [[cartesian monoidal category]], so that $\otimes$ is $\times$.  But perhaps a [[2-rig]] will be sufficient?
=--


## Related concepts

* [[classifying topos for the theory of objects]]

* [[natural numbers object]]

* [[arithmetic pretopos]]

* [[tensor algebra]]

* [[cofree coalgebra]]

## References

* {#Ben91}[[Jean Bénabou]], _Some Remarks on Free Monoids in a Topos_ , pp.20-29 in LNM **1488** Springer Heidelberg 1991.

* {#Blass} [[Andreas Blass]], _Classifying topoi and the axiom of infinity_ , Algebra Universalis **26** (1989) pp.341-345.

* {#JT77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint Minneola 2014, chap. 6)

[[!redirects list]]
[[!redirects lists]]
[[!redirects finite list]]
[[!redirects finite lists]]
[[!redirects finite sequence]]
[[!redirects finite sequences]]

[[!redirects concatenation]]
[[!redirects cons]]

[[!redirects free monoid]]
[[!redirects free monoid functor]]
[[!redirects free monoid monad]]
[[!redirects list monad]]

[[!redirects queue]]
[[!redirects queues]]

[[!redirects list object]]
[[!redirects list objects]]
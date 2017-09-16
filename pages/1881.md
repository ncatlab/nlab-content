Given a [[set]] $S$, the __free monoid__ on $S$ is the set $S^*$ of all __lists__ (finite [[sequences]]) of elements of $S$, made into a monoid using __concatenation__.  The [[free functor]] from [[Set]] to [[Mon]] takes $S$ to $S^*$.


## Definitions ##

We will give three definitions, which can all be shown equivalent.


### As functions

An element of $S^*$ consists of a [[natural number]] $n$ (possibly $n = 0$) and function from $[n]$ to $S$, where $[n]$ is the [[subset]] $\{i: \mathbf{N} \;|\; i \lt n\}$ of $\mathbf{N} = \{0, 1, 2, \ldots\}$.  Such an element is called a __list__ or (to specify $n$) __$n$-tuple__ of elements of $S$.  The number $n$ is called the __length__ of the list.

The __empty list__ is the unique list of length $0$.  It may be written $()$, $*$, or $\epsilon$, perhaps with a subscript $S$ if desired.

If $n \gt 0$, then the list which assigns $0, \ldots, n - 1$ to $a_0, a_1, \ldots, a_{n-1}$ may be written $(a_0, a_1, \ldots, a_{n-1})$.  For example, if $a,b,c$ are elements of $S$, then $(a,b,c)$ is an element of $S^*$.

Given two lists $x$ and $y$, the former of length $m$ and the latter of length $n$, their __concatenation__ $x * y$ is a list of length $m + n$, given as follows:
$$ i \mapsto \left\{ \array { x_i     & if\; i \lt m \\
                              x_{i-m} & if\; i \geq m } \right. $$

One can now show that concatenation is associative with the empty list as identity; hence $S^*$ is a monoid.


### Recursively

The (underlying) set $S^*$ may be defined as an [[inductive type]] as follows.  There are two basic constructors, one with no arguments, and one with two arguments, of which one is an element of $S$ and the other is an element of $S^*$.  By the yoga of inductive types, that is a complete definition, but we spell it out in more detail while also giving terminology and notation.

So, a __list__ is either the __empty list__ or the __cons__ (short for 'constructor' and deriving from Lisp) of an element $a$ of $S$ and a (previously constructed) list $x$.  The empty list may may be written $()$, $*$, or $nil$, perhaps with a subscript $S$ if desired; the cons of $a$ and $x$ may be written $s:x$, $(a) * x$, or $cons(a,x)$.  We interpret the definition [[recursion|recursively]], so we can list the elements of $S^*$ in the order in which they appear:

*  $()$,
*  $a:()$,
*  $a:b:()$,
*  $a:b:c:()$,
*  etc.

Here, $a, b, c, \ldots$ are elements of $S$.  We may continue the 'etc' as far as we like, but no farther; while there are lists of arbitrarily long finite length, there are no lists of infinite length.  (We would get such lists, however, if we interpreted the definition [[corecursion|corecursively]].)  We normally abbreviate the lists above as follows:
*  $()$,
*  $(a)$,
*  $(a,b)$,
*  $(a,b,c)$,
*  etc.

We still must define the monoidal structure on $S^*$; we define the __concatenation__ $x * y$ of $x$ and $y$ recursively in $x$.  To be explicit:
*  $() * y = y$;
*  $(a:x) * y = a:(x * y)$ (with parentheses for grouping, but the parentheses can be dropped now that have this definition).

One can now show that concatenation is associative with the empty list as identity; hence $S^*$ is a monoid.


### By general abstract nonsense

In the course of proving that the category [[Mon]] of monoids is a [[complete category]], one normally shows that the [[forgetful functor]] $U$ (from $Mon$ to the category [[Set]] of sets) preserves all [[limit]]s.  Thus, the [[adjoint functor theorem]] defines a [[left adjoint]] to $U$ if a size condition is met; this adjoint is the functor $*$ that takes a set to its free monoid $S^*$.

To be sure, meeting the solution set condition basically requires starting the constructions in one of the other definitions above; but the proofs may all be thrown onto the adjoint functor theorem.


## Examples

*  If $S$ is the [[empty set]], then $S^*$ consists only of the empty list; it is the trivial monoid, one manifestation of the [[point]].
*  If $S$ is the point, then $S^*$ is $\mathbf{N}$; the only information in a list of indistinguishable points is the length of the list.  The monoid operation on $\mathbf{N}$ is addition.
*  If $S$ is $\mathbf{N}$, then $\mathbf{N}^*$ is still a [[denumerable set]].  But note that $\mathbf{N} \cong \mathbf{N}^*$ only as sets (that is, $|\mathbf{N}^*| = |\mathbf{N}| = \aleph_0$ as [[cardinal numbers]]); they are quite different as monoids.
*  Generalising the above, $|S^*| = |S|$ is $S$ is an [[infinite set]], or more generally $|S^*| = max(\aleph_0,S)$ if $S$ is an [[inhabited set]].  (These theorems probably require the [[axiom of choice]], but I haven\'t checked thoroughly.)


## The free monoid monad

If the free moniod functor $F: Set \to Mon$ is followed by the forgetful functor $U: Mon \to Set$, then we get a [[monad]] on $Set$.  This monad is very important in [[computer science]], where it is known as the __list monad__.

The list monad bears the same relation to [[multicategories]] as the [[identity monad]] on $Set$ bears to ordinary [[categories]].  This relation should be explained at [[generalized multicategory]].


## Foundational relevance

Every definition of free monoid makes use of some form of [[axiom of infinity]], either $\mathbf{N}$ directly or the ability form general inductive types.  Indeed, as $\mathbf{N} = pt^*$, the axiom of infnity follows from the existence of free monoids.


[[!redirects list]]
[[!redirects empty list]]
[[!redirects concatenation]]
[[!redirects cons]]
[[!redirects free monoid functor]]
[[!redirects free monoid monad]]
[[!redirects list monad]]
[[!redirects lists]]
A multiset is like a [[set]], just allowing that the elements have multiplicities. Thus the multiset $\{1,1,2\}$ differs from the multiset $\{1,2\}$, while $\{1,2,1\}$ is the same as $\{1,1,2\}$. Multisets are useful in [[combinatorics]]. See [wikipedia](http://en.wikipedia.org/wiki/Multiset).


## Definitions 

While it is possible to take multisets as a fundamental concept in [[foundations]], it is more common to define them in terms of [[sets]] and [[functions]].


A **multiset** $\mathcal{X} = \langle X,\mu_X\rangle$,can be defined as a set $X$ (its __underlying set__) together with a function $\mu_X$ (giving each element its __multiplicity__) from $X$ to a class of nonzero [[cardinal numbers]].  A multiset is **locally finite** if multiplicity takes values in the [[natural numbers]].  Many authors take all multisets to be locally finite; that is the default in combinatorics.  The multiset is **finite** if it is locally finite and $X$ is a [[finite set]].  We can also define a multiset to be a function from the [[proper class]] of all objects to the class of all cardinal numbers, with the proviso that the objects whose multiplicity is nonzero form a set (the set $X$ above).


If we are only interested in multisets with elements drawn from a given set $U$ (as is common in combinatorics), then an alternative definition is very useful: a __multisubset__ of $U$ is a function $f\colon B \to U$, where two multisubsets $f\colon B \to U$ and $f'\colon B' \to U$ are considered _equal_ if there is a [[bijection]] $g\colon B \to B'$ that makes a commutative triangle.  In other words, a multisubset of $U$ is an isomorphism class in the [[slice category]] $Set/U$.  (Compare this to the structural definition of _[[subset]]_ of $U$ as an [[injective function]] to $U$.)


A multisubset of $U$ is locally finite if every [[fibre]] is finite; it is finite if additionally the [[image]] of $f$ (which corresponds to $A$ in the original definition) is finite.  A locally finite multisubset can also be described as a function from $U$ to the set of natural numbers; this is just the multiplicity function $\mu$ again, now with $U$ (rather than $X$) specified as the domain and allowing the value $0$ to be taken.


## Operations on multisets

The operations on cardinal numbers induce operations on multisets (or on multisubsets of any given set $U$).

In the following, let $\mathcal{X} = \langle X,\mu_X\rangle$ and $\mathcal{Y} = \langle Y,\mu_Y\rangle$ be multisets.

*  The [[cardinality]] of a multiset is given by

   $$|\mathcal{X}| = \sum_{e\in X} \mu_X(e).$$

*  The __[[intersection]]__ of multisets is the multiset whose cardinality is given by the [[infimum]] operation on cardinal numbers.

   $$\mathcal{X}\cap\mathcal{Y} = \langle X\cap Y, \min(\mu_X,\mu_Y)\rangle.$$

*  The __[[union]]__ of multisets is the multiset whose cardinality is given by the [[supremum]] operation on cardinal numbers.

   $$\mathcal{X}\cup\mathcal{Y} = \langle X\cup Y, \max(\mu_X,\mu_Y)\rangle.$$

*  The __sum__ of multisets is the multiset whose cardinality is given by addition of cardinal numbers; this has no analogue for ordinary sets.

   $$\mathcal{X}+\mathcal{Y} = \langle X\cup Y, \mu_X+\mu_Y\rangle.$$

*  The __product__ of multisets (turning them into a [[rig]]) is the multiset whose cardinality is given by the product of cardinal numbers

   $$\mathcal{X}\mathcal{Y} = \langle X\cap Y, \mu_X\mu_Y\rangle.$$

   Note that if $\mathcal{X}$ is a set, then $\mathcal{X}\mathcal{X} = \mathcal{X}.$

*  The [[inner product of multisets]] is given by

   $$\langle\mathcal{X},\mathcal{Y}\rangle = \sum_{e\in{X\cap Y}} \mu_X(e) \mu_Y(e).$$

   Note that the inner product corresponds to the cardinality of the product

   $$\langle\mathcal{X},\mathcal{Y}\rangle = |\mathcal{X}\mathcal{Y}|.$$

+--{.query}
[[Eric]]: What would a colimit over an MSet-valued functor $F:A\to MSet$ look like?

_Toby_:  That depends on what the morphisms are.
=--

## Morphisms

What is a function between multisets?  I would be inclined to say that for multisubsets of an ambient universe $U$ considered as objects of $Set/U$, a function from $B\to U$ to $B'\to U$ would be an arbitrary function $B\to B'$ (not necessarily commuting with the projections to $U$).  But this doesn't work if a multisubset of $U$ is an *isomorphism class* in $Set/U$ rather than merely an object of it.  -- [[Mike Shulman]]

[[Eric]]: This definition is taken from Syropoulos:

+-- {: .un_defn}
###### Definition
Category $\mathbf{MSet}$ is a category of all possible multisets.

1. The objects of the category consist of pairs $(A, P)$, where $A$ is a set and $P:A\to Set$ a presheaf on $A$.
1. If $(A,P)$ and $(B,Q)$ are two objects of the category, an arrow between these objects is a pair $(f,\lambda)$, where $f:A\to B$ is a function and $\lambda:P\to Q\circ f$ is a natural transformation, i.e., a family of functions.
1. Arrows compose as follows: suppose that $(A,P)\stackrel{(f,\lambda)}{\to}(B,Q)$ and $(B,Q) \stackrel{(g,\mu)}{\to}(C,R)$ are arrows of the category, then $(f,\lambda)\circ (g,\mu) = (g\circ f, \mu\times\lambda)$, where $g\circ f$ is the usual function composition and $\mu\times\lambda:P\to R\circ (g\circ f)$.
4. Given an object $(A,P)$, the identity arrow is $(id_A, id_P)$.
=--

The last part of the definition is a kind of wreath product (see [4]). However, it is not clear at the moment how this definition fits into the general theory of
wreath products.

[[Mike Shulman]]: Huh.  So his definition takes a multiset to assign a *set* to every element, rather than a *cardinality* to every element, so that the multisubsets of $U$ are exactly objects of $Set/U$.  I'm surprised, though, that with his definition the only functions $\{1,1\} \to \{2,3\}$ are constant; why can't I send the two copies of $1$ to different places?

_Toby_:  If you could, then $\{1,1\}$ and $\{2,3\}$ would be isomorphic in this category, and we\'d just have $Set$ back again.

I find _Mathematics of Multisets_ especially interesting for its distinction between multisets with *distinguishable* objects and 'pure' multisets with *indistinguishable* objects.  The definition above involving cardinal numbers gives us 'pure' multisets, unlike the objects of the category $MSet$ above.

Normally, one only needs multisubsets of a given set, and one is not interested in functions between them.  But if one wants to make a category of abstract multisets, then the pure and impure versions are different!

[[Mike Shulman]]: Whereas his definition makes the category of multisets equivalent to $Set^{\mathbf{2}}$.  Is that better?

I don't find it wrong that the category of multisets would be equivalent to $Set$, since $Set$ only sees "structural" properties of sets, and the fact that two elements of a set are "the same" (which is what distinguishes $\{1,1\}$ from $\{2,3\}$) is a nonstructural property that only makes sense in the context of sub-multisets of some ambient set.

_Toby_:  At least $Set^{\mathbf{2}}$ is *different* from $Set$.  And how do you decide whether being 'the same' is a structural property of a *multi*set?  We\'re trying to take an idea that originally applied only to collections of elements from a fixed universe and move it to a more abstract settings; there are (at least) two ways to do that, and Syropoulos has chosen the more interesting one.  (Anyway, if somebody asked me to come up with a structural notion of abstract multiset, the first thing that I would think of ---and did think of, before this discussion started--- is an object of $Set^{\mathbf{2}}$.)  Asking which notion is correct is not really a fair question.

[[Eric]]: The paper [Mathematics of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/MathMSet.pdf) is worth having a look. I might have pasted a suboptimal piece. He talks about two types of multisets (and more actually): 1.) real multisets and 2. multisets. Here is another quote:

>Real multisets and multisets are associated with a (ordinary) set and an equivalence relation or a function, respectively. Here are the formal definitions:

>**Definition 1**. A real multiset $\mathcal{X}$ is a pair $(X,\rho)$, where $X$ is a set and $\rho$ an equivalence relation on $X$. The set $X$ is called the field of the real multiset. Elements of $X$ in the same equivalence class will be said to be of the same sort; elements in different equivalence classes will be said to be of different sorts.

>Given two real multisets $\mathcal{X} = (X,\rho)$ and $\mathcal{Y} = (Y,\sigma)$, a morphism of real multisets is a function $f:X\to Y$ which respects sorts; that is, if $x,x'\in X$ and $x \rho x'$, then $f(x)\sigma f(x')$.

>**Definition 2**. Let $D$ be a set. A multiset over $D$ is just a pair $\langle D, f\rangle$, where $D$ is a set and $f:D\to\mathbb{N}$ is a function.

>The previous definition is the characteristic function definition method for multisets.

>**Remark 1**. Any ordinary set $A$ is actually a multiset $\langle A,\chi_A\rangle$, where $\chi_A$ is its characteristic function.

## Examples

...


* See also [[inner product of multisets]].

## References

* [Mathematics of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/MathMSet.pdf), Apostolos Syropoulos

* [Categorical Models of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/mset.pdf), Apostolos Syropoulos


+--{.query}

[[Eric]]: Given $X = \{1,1,2\}$ and $Y = \{1,1,3\}$, is $X\cap Y = \{1,1\}$ or is $X\cap Y = \{1\}$?

[[Todd Trimble|Todd]]: It's $\{1, 1\}$. (To make the question structural, we should think of $X$ and $Y$ as multisubsets of some other multiset, but never mind.) 

As a writer (perhaps Toby) was saying above, a locally finite multiset $M$ can be thought of as an ordinary set $X$ equipped with a multiplicity function $\mu: X \to \mathbb{N}$. A multisubset of $M$ can then be reckoned as
$X$ equipped with a function $\nu: X \to \mathbb{N}$ which is bounded above by $\mu$. To take the intersection of two multisubsets $\nu, \nu': X \to \mathbb{N}$, you take the minimum or inf of $\nu, \nu'$. Your question can then be translated to one where $X = \{1, 2, 3\}$, where $\nu(1) = 2, \nu(2) = 1, \nu(3) = 0$ and $\nu'(1) = 2, \nu'(2) = 0, \nu'(3) = 1$. 

[[Eric]]: Thanks Todd! The reference [Mathematics of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/MathMSet.pdf) explains this nicely too.

=--


+--{.query}
[[Eric]]: What is the difference (aside from negatives) between multisets and abelian groups freely generate by some set $U$? It seems like a multiset $\langle X,\mu\rangle$ ($X$ s a set and $\mu:X\to\mathbb{N}$) can be thought of as a _vector_ with $\mu$ providing the coefficients. 

For example, we could express the multiset $\mathcal{X} = \{1,1,1,2,3,3,3,3,3\}$ as

$$\mathcal{X} = 3\{1\} + 1\{2\} + 4\{3\}.$$

_Toby_:  The only difference is notation; see the note at the end of [[inner product of multisets]].

[[Mike Shulman]]: At least, if all your multisets are locally finite.

_Toby_:  Right; which they are for Eric, who specified $\mu\colon X \to \mathbb{N}$.  If you allow arbitrary cardinalities, then it\'s the free module on $U$ over the rig of cardinal numbers.
=--


[[!redirects multisubset]]

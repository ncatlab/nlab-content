
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Quotient spaces
* table of contents
{: toc}

## Idea

A *quotient space* is a [[quotient object]] in some [[category]] of [[spaces]], such as [[Top]] (of [[topological spaces]]), or [[Loc]] (of [[locales]]), etc.

Quotient objects in the category $Vect$ of [[vector spaces]] also traditionally use the term 'quotient space', but they are really just a special case of [[quotient module]]s, very different from the other kinds of quotient space.  Quotient [[TVSes]], however, combine both aspects.


## Definitions

### In $Top$

Let $X$ be a [[topological space]] and $\sim$ an [[equivalence relation]] on (the underlying set of) $X$.  (Since [[monomorphisms]] in [[Top]] are just [[injection|injective]] [[continuous maps]], to give an equivalence relation on the underlying set of a topological space is the same as to give a [[congruence]] on that space in $Top$.)  Let $Y = X/{\sim}$ be the [[quotient set]] and $q\colon X\to Y$ the quotient map.

The **quotient topology**, or **identification topology**, induced on $Y$ from $X$ says that a subset $U\subseteq Y$ is [[open subset|open]] if and only if $q^{-1}(U)\subseteq X$ is open.  With this topology $Y$ is a **quotient space** or **identification space** of $X$.

Obviously, up to [[homeomorphism]], all that matters is the surjective function $X\to Y$.  For the above definition, we don't even need it to be surjective, and we could generalize to a [[sink]] instead of a single map; in such a case one generally says *[[final topology]]* or *[[strong topology]]*.  See [[topological concrete category]].


### In $Loc$

A quotient space in $Loc$ is given by a [[regular subobject]] in [[Frm]].

(More details needed.)


## Related pages

* [[image]]

* [[subspace]]

* [[subframe]]


[[!redirects quotient space]]
[[!redirects quotient spaces]]
[[!redirects identification space]]
[[!redirects identification spaces]]

[[!redirects quotient topology]]
[[!redirects quotient topologies]]
[[!redirects identification topology]]
[[!redirects identification topologies]]

[[!redirects quotient locale]]
[[!redirects quotient locales]]

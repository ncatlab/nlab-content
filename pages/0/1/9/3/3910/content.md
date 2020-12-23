
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--
# Contents
* table of contents
{: toc}

## Idea

An __integer__ is a [[number]] that is a [[natural number]] or the [[negative number|negative]] of one.

The [[ring]] $\mathbb{Z}$ of all integers may defined as the [[free group]] on one generator or as the [[initial object|initial]] [[ring]]. 

In keeping with a historical point of view in which integers are natural numbers with a sign attached, one may write 

$$
  \mathbb{Z} = \{n, -n | n \in \mathbb{N}, 0 = -0\} = \{ \ldots, -3, -2, -1, 0, 1, 2, 3, \ldots \}
  \,.
$$

From an [[nPOV]], one may consider this as follows: $\mathbb{Z}$ is a [[filtered colimit]] of sets 

$$\mathbb{N} \stackrel{1 + (-)}{\to} \mathbb{N} \stackrel{1 + (-)}{\to} \mathbb{N} \stackrel{1 + (-)}{\to} \ldots$$ 

whereby $-n \in \mathbb{Z}$ is represented by the element $0$ in the $n^{th}$ copy of $\mathbb{N}$ appearing in this diagram (starting the count at the $0^{th}$ copy). The resulting induced map to the colimit 

$$\mathbb{N} \times \mathbb{N} \cong \sum_{m \in \mathbb{N}} \mathbb{N} \to \mathbb{Z}: (m, n) \mapsto n-m$$ 

imparts a monoid (in fact a group) structure on $\mathbb{Z}$ descended from the monoid structure on $\mathbb{N} \times \mathbb{N}$; compare double-entry bookkeeping in medieval mathematics (*[partita doppia](http://rfcwalters.blogspot.com/2011/02/mathematical-economics-double-entry.html)*). 

As a group, $\mathbb{Z}$ is [[abelian group|abelian]] and is the [[Grothendieck group]] of the [[monoid]] (or [[semigroup]]) $\mathbb{N}$ of [[natural numbers]].

The monoid of natural numbers is naturally even a [[rig]] -- in fact the [[initial object|initial]] rig -- and this multiplicative structure extends to $\mathbb{Z}$ to make it a [[ring]] -- in fact the initial ring.


## Terminology

The underlying [[sets]] $\mathbb{Z}$ and $\mathbb{N}$ are [[isomorphic]]. Some subcultures of mathematics (and not only [[set theory|set theorists]]) use the term 'integer' synonymously for a natural number.  Computer scientists distinguish between 'unsigned integers' (natural numbers) and 'signed integers' (integers as described here).  Translations can also cause confusion with the term 'whole number'.

In [[number theory]], one generalises integers to [[algebraic integers]], an instance of the [[red herring principle]].  Accordingly, some number theorists will call the integers '[[rational integers]]' to clarify; $\mathbb{Z}$ is the [[ring of integers]] in the [[number field]] $\mathbb{Q}$ of [[rational numbers]].  (Compare, for example, [[Gaussian integers]] and [[Gaussian numbers]].)

The symbol '$\mathbb{Z}$' derives from the German word 'Zahlen', which is a generic word for 'numbers'.  (Compare [[Richard Dedekind|Dedekind]]\'s use of that word in the title of his famous book on the [[foundations]] of [[real numbers]].)

## Related concepts

* [[infinite cyclic group]]

* [[even number]], [[odd number]]

* [[natural number]], [[rational number]], [[real number]]

* [[algebraic integer]]

* [[ring of integers]]

* [[cyclotomic integer]]

* [[geometry]] modeled on the [[formal duality|formal dual]], [[Spec(Z)]], of the ring of integers is [[arithmetic geometry]]

* [[integers object]] in a [[topos]]

## References

A formalization in terms of [[homotopy type theory]], using a unary notation, is in 

* [[Mike Shulman]], _[Integers.v](https://github.com/HoTT/HoTT/blob/master/Coq/HIT/Integers.v)_

(A different common formalization of integers in type theory is in a binary notation, as in the [Coq standard library](http://coq.inria.fr/stdlib/Coq.ZArith.BinInt.html).  Binary notation is exponentially more efficient for performing computations, but the unary notation was convenient for calculating $\pi_1(S^1)$.)


[[!redirects integer]]
[[!redirects integers]]


[[!redirects integer number]]
[[!redirects integer numbers]]

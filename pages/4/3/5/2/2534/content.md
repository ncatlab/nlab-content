
# Multisets
* table of contents
{: toc}

## Idea

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

*  The _[[set difference]]_ of multisets is the multiset given by

   $$ \mathcal{X} \backslash \mathcal{Y} = \langle \{ a \in X \cup Y \;|\; mu_X(a) \gt \mu_Y(a) \}, \mu_X - \mu_Y \rangle .$$

*  The __sum__ of multisets is the multiset whose cardinality is given by addition of cardinal numbers; this has no analogue for ordinary sets.

   $$\mathcal{X}+\mathcal{Y} = \langle X\cup Y, \mu_X+\mu_Y\rangle.$$

*  The __product__ of multisets (turning them into a [[rig]]) is the multiset whose cardinality is given by the product of cardinal numbers

   $$\mathcal{X}\mathcal{Y} = \langle X\cap Y, \mu_X\mu_Y\rangle.$$

   Note that if $\mathcal{X}$ is a set, then $\mathcal{X}\mathcal{X} = \mathcal{X}.$

*  The [[inner product of multisets]] is given by

   $$\langle\mathcal{X},\mathcal{Y}\rangle = \sum_{e\in{X\cap Y}} \mu_X(e) \mu_Y(e).$$

   Note that the inner product corresponds to the cardinality of the product

   $$\langle\mathcal{X},\mathcal{Y}\rangle = |\mathcal{X}\mathcal{Y}|.$$


## Examples

...


* See also [[inner product of multisets]].


## References

* [Mathematics of Multisets](http://asyropoulos.eu/papers/PDF/MathMSet.pdf), Apostolos Syropoulos

* [Categorical Models of Multisets](http://asyropoulos.eu/papers/PDF/mset.pdf), Apostolos Syropoulos

* [An Overview of the Applications of
Multisets](http://www.emis.de/journals/NSJOM/Papers/37_2/NSJOM_37_2_073_092.pdf), D. Singh, A. M. Ibrahim, T. Yohanna and J. N. Singh

[[!redirects multiset]]
[[!redirects multisets]]

[[!redirects multisubset]]
[[!redirects multisubsets]]

[[!redirects bag]]
[[!redirects bags]]

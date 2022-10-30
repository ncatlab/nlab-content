
> This entry is about the general notion of localization of a possible noncommutative ring. For the more restrictive but more traditional notion of [[localization of a commutative ring]] see there.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General

Given a (possibly noncommutative) unital [[ring]] $R$ there are many situations when certain elements or matrices can be inverted in a universal way obtaining a new "localized" ring $S^{-1}R$ equipped with a localization [[homomorphism]] $R\to S^{-1}R$ under which all elements in $S$ are mapped to multiplicatively invertible elements ([[units]]). The latter property must be modified for Cohn localization at multiplicative set of matrices. 

We can typically invert elements in a left or right Ore subset $S\subset R$ or much more generally some multiplicative set or matrices ([[Cohn localization]]) etc. There are also some specific localizations like Martindale localizations in ring theory. 

### Localization "at" and "away from"
 {#Terminology}

The common terminology in algebra is as follows.

For $S$ a set of [[primes]], "localize at $S$" means "invert what is not divisible by $S$"; so for $p$ prime, localizing "at $p$" means considering only $p$-[[torsion subgroup|torsion]].

Adjoining inverses $[S^{-1}]$ is pronounced "localized away from $S$". Inverting a [[prime]] $p$ is localizing away from $p$, which means ignoring $p$-torsion.

Evidently, this conflicts with more-categorial uses of "localized"; "inverting weak equivalences" is called localization, by obvious analogy, and is written as "localizing at weak equivalences". This is confusing! It's also weird: since a ring is a one-object Ab-enriched category with morphisms "multiply-by", the localization-of-the-category $R$ "at $p$" (or its Ab-enriched version, if saying that is necessary) really means the localization-of-the-ring R "away from p".

## Definition

+-- {: .num_defn }
###### Definition

The localization of a [[ring]] $R$ at a [[multiplicative subset]] $S$ is the [[commutative ring]] whose underlying  [[set]] is the set of [[equivalence classes]] on $R \times S$ under the [[equivalence relation]]

$$
  (r_1, s_1) \sim (r_2, s_2) 
  \;\;\Leftrightarrow\;\;
  \exists u \in S
  \;
  (r_1 s_2- r_2 s_1) u = 0 \;\in R
  \,.
$$

Write $r s^{-1}$ for the [[equivalence class]] of $(r,s)$. On this set, addition and multiplication is defined by

$$
  r_1 s_1^{-1} + r_2 s_2^{-1} \coloneqq (r_1 s_2 + r_2 s_1) (s_1 s_2)^{-1}
$$

$$
  (r_1 s_1^{-1})(r_2 s_2^{-1}) \coloneqq r_1 r_2 (s_1 s_2)^{-1}
  \,.
$$


=--

(e.g. [[The Stacks Project|Stacks Project, def. 10.9.1]])


## Related concepts

* [[localization]], 

* [[localization of a commutative ring]]

* [[localization of a module]]

* [[Cohn localization]], [[Ore localization]].


## References


* [[Zoran Škoda]], _Noncommutative localization in noncommutative geometry_,  London Math. Society Lecture Note Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed.  A. Ranicki; pp. 220--313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276).

[[!redirects localizations of a ring]]

#Contents#
* table of contents
{:toc}

##Motivation

[[Solomon Lefschetz]] wanted to count the [[fixed point]] set of a 
[[continuous map]]. 

## Lefschetz number

Fix a ground [[field]] $k$.
Given a [[continuous map]] $f \colon X\to X$ of [[topological space]], its **Lefschetz number** $\Lambda(X,f)$ is the alternating [[sum]] of the [[traces]] 

$$
  \sum_i (-1)^i Tr (H^i(f) \colon H^i(X,k)\to H^i(X,k)
  \,,
$$

of the [[endomorphisms]]  of the [[ordinary cohomology|ordinary]] [[cohomology groups]] with [[coefficients]] in the ground [[field]] $k$. 

One sometimes also talks of the _Lefschetz number_ of the induced [[endomorphism]] of the [[chain complex|chain/cochain complexes]], see [[algebraic Lefschetz formula]]. 

For $f = id$ the [[identity]] map, the Lefschetz trace reduces to the _[[Euler characteristic]]_. 


## Lefschetz fixed point theorem

### Statement

The _Lefschetz fixed point theorem_ says that if $X$ is a compact polyhedron and if the Lefschetz number is non-zero, then $f$ has at least one [[fixed point]]. In particular, if $X$ is a contractible compact polyhedron, then every $f \colon X\to X$ has a fixed point, so the theorem is a vast generalization of Brower fixed point theorem.


The existence of a Lefschetz formula holds more general in [[Weil cohomology]] theories (by definition) and hence notably in [[ℓ-adic cohomology|ℓ-adic]] [[étale cohomology]]. This fact serves to prove the [[Weil conjectures]].


### Proof

(...)

follows from existence of 

* good [[cycle map]]

* [[Künneth formula]]

* [[Poincaré duality]]

([Milne, section 25](#Milne))

(...)


## Related concepts

* [[Reidemeister trace]]

* [[Weil conjecture]]

* [[Grothendieck-Lefschetz trace formula]]

## References

### For ordinary cohomology

The original article is

* [[Solomon Lefschetz]], _On the fixed point formula_, Ann. of Math. (2), **38**  (1937) 819&#8211;822

Reviews include

* Online Springer Enc. of Math. ([[eom]]): [Lefschetz number](http://eom.springer.de/l/l057990.htm) (Rudyak), [Lefschetz formula](http://eom.springer.de/L/l057980.htm) (Iskovskikh)
 {#eom}

See also

* Minhyong Kim, _A Lefschetz trace formula for equivariant cohomology_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 28 no. 6 (1995), p. 669-688, [numdam](http://www.numdam.org/item?id=ASENS_1995_4_28_6_669_0), [MR97d:55012](http://www.ams.org/mathscinet-getitem?mr=97d:55012)

* Atiyah, Bott, ... (cf. [[Atiyah-Bott fixed point formula]])

### For &#233;tale cohomology

For [[étale cohomology]] of [[schemes]]:

* [[James Milne]], section 25 of _[[Lectures on Étale Cohomology]]_

For [[algebraic stacks]]:


* [[Kai Behrend]], _The Lefschetz trace formula for algebraic stacks_, 	Invent. Math. **112**, 1 (1993), 127-149, [doi](http://dx.doi.org/10.1007/BF01232427)

[[!redirects Lefschetz number]]
[[!redirects Lefschetz formula]]
[[!redirects Lefschetz numbers]]

[[!redirects Lefschetz fixed point theorem]]

[[!redirects Lefschetz fixed point formula]]
[[!redirects Lefschetz fixed-point formula]]
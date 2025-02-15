


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


> See also *[[Bousfield--Kan formula]]*


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The Bousfield--Kan map(s) are comparison morphisms in a [[simplicial model category]] between two different "puffed up" versions of (co)limits over (co-)simplicial objects: one close to a [[homotopy limit|homotopy (co)limit]] and the other a version of nerve/geometric realization.


## Definition


Let $C$ be an ([[SimpSet|SSet]],$\otimes = \times$)-[[enriched category]] and write 

$$
  \Delta : \Delta \to Set^{\Delta^{op}}
$$

for the canonical cosimplicial [[simplicial set]] (the [[adjunct]] of the [[hom-functor]] $\Delta^{op} \times \Delta \to Set$).

Write furthermore $N(\Delta/-) : \Delta \to Set^{\Delta^{op}}$ for the [[fat simplex]], the  [[cosimplicial object|cosimplicial]] [[simplicial set]] which assigns to $[n]$ the [[nerve]] of the [[overcategory]] $\Delta / [n]$.

The **Bousfield--Kan map of cosimplicial simplicial maps** is a canonical morphism

$$
  \varphi 
  \,\colon\, 
  N\big(\Delta/(-)\big) 
   \longrightarrow 
  \Delta
$$

of cosimplicial simplicial sets.

This can also be regarded as a morphism

$$
  \varphi 
    \,\colon\, 
  N\big(
    (-)/\Delta^{op}
  \big)^{op} 
    \longrightarrow 
  \Delta
  \,.
$$


This morphism induces the following morphisms between (co)[[simplicial objects]] in $C$.


### Bousfield--Kan for simplicial objects

For $X \,\colon\, \Delta^\op \to C$ any [[simplicial object]] in $C$, the **realization** of $X$ is the [[end|coend]]

$$
  {|X|} 
    \;\coloneqq\; 
  X \otimes_{\Delta^{op}} \Delta 
    \;\coloneqq\; 
  \int^{[n] \in \Delta} 
    X_n \otimes \Delta^n
  \,,
$$

where in the integrand we have the *[[copower]]* (or *[[tensoring]]*) of $C$ by [[sSet]].

Here the **Bousfield--Kan** map is the morphism

$$
  X \otimes_{\Delta^{op}} 
   N\big((-)/\Delta^{op}\big)^{op}
  \stackrel
    {Id_X \otimes_{\Delta^{op}} \phi }
    {\longrightarrow}
  X \otimes_{\Delta^{op}} \Delta
  \,.
$$


### Bousfield--Kan for cosimplicial objects


For $X \,\colon\, \Delta \to C$ any cosimplicial object, its **totalization** is the $\Delta$-[[weighted limit]]

$$
  Tot X 
    \;\coloneqq\; 
  lim^\Delta X 
    \;\simeq\; 
  \int_{[n \in \Delta]} X_n^{\Delta^n}
  \,,
$$

where in the integrand we have the [[power]] or cotensor $X_n^{\Delta^n} = \pitchfork(\Delta, X_n)$ of $C$ by [[SimpSet|SSet]].


Here the **Bousfield--Kan** morphism is the morphism

$$
  Tot X \simeq hom(\Delta,X) 
    \stackrel
      {hom(\phi,Id_X)} 
      {\longrightarrow}  
  hom\Big(
    N\big(\Delta/(-)\ig)
    ,\, 
    X
    \Big)
  \,.
$$


## Properties


+-- {: .un_theorem}
###### Theorem

If the [[simplicial object]] $X$ is [[Reedy category|Reedy]]-[[cofibrant objects|cofibrant]] then its Bousfield--Kan map is a natural [[weak equivalence]].

If the co-[[simplicial object]] $X$ is [[Reedy category|Reedy fibrant]] then its Bousfield--Kan map is a natural weak equivalence.


=--

+-- {: .proof}
###### Proof

This can be proven for instance using [[homotopy colimits]] in the [[Reedy model structure]]. Details are at *[Reedy model structure -- over the simplex category](Reedy+model+structure#SimplexCategory)*.

=--


## Relation to homotopy limits

When the co[[simplicial object]]  $X$ is degreewise fibrant,  then 

$$
  lim^{N(\Delta/(-))} X
  \simeq holim X
$$

computes the [[homotopy limit]] of $X$ as a [[weighted limit]] (as explained there). Then the above theorem says that the homotopy limit is already computed by the totalization

$$
  holim X \simeq lim^\Delta X
  \,.
$$


## References

The original article: 
 
* {#BousfieldKan} [[Aldridge K. Bousfield]] and [[Daniel M. Kan]], Chapter IX in: *[[Homotopy Limits, Completions and Localizations]]*, Lecture Notes in Mathematics 304 (1972; 1987), Springer ([doi:10.1007/978-3-540-38117-4](https://link.springer.com/book/10.1007/978-3-540-38117-4))


Review:

* {#Hirschhorn} [[Philip Hirschhorn]], Chapter 9 in: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

The Bousfield--Kan map(s) are on p. 397, def. 18.7.1 and def. 18.7.3.

_Realization_ and _totalization_ are defs 18.6.2 and 18.6.3 on p. 395.

Notice that this book writes $B$ for the nerve!

[[!redirects Bousfield-Kan formula]]


<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The Bousfield--Kan map(s) are comparison morphisms in a [[simplicial model category]] between two different "puffed up" versions of (co)limits over (co-)simplicial objects: one close to a [[homotopy limit|homotopy (co)limit]] and the other a version of nerve/geometric realization.

#Definition#


Let $C$ be an ([[SimpSet|SSet]],$\otimes = \times$)-[[enriched category]] and write 

$$
  \Delta : \Delta \to Set^{\Delta^{op}}
$$

for the canonical cosimplicial [[simplicial set]] (the [[adjunct]] of the [[hom-functor]] $\Delta^{op} \times \Delta \to Set$).

Write furthermore $N(\Delta/-) : \Delta \to Set^{\Delta^{op}}$ for the cosimplicial simplicial set which assigns to $[n]$ the [[nerve]] of the [[over category]] $\Delta / [n]$.

The **Bousfield--Kan map of cosimplicial simplicial maps** is a canonical morphism

$$
  \varphi : N(\Delta/(-)) \to \Delta
$$

of cosimplicial simplicial sets.

This can also be regarded as a morphism

$$
  \varphi : N((-)/\Delta^{op})^{op} \to \Delta
  \,.
$$


This morphism induces the following morphisms between (co)[[simplicial object]]s in $C$.

##Bousfield--Kan for simplicial objects##

For $X : \Delta^\op \to C$ any [[simplicial object]] in $C$, the **realization** of $X$ is the [[end|coend]]

$$
  |X| := X \otimes_{\Delta^{op}} \Delta := 
  \int^{[n] \in \Delta} X_n \otimes \Delta^n
  \,,
$$

where in the integrand we have the [[copower]] or tensor of $C$ by [[SimpSet|SSet]].

Here the **Bousfield--Kan** map is the morphism

$$
  X \otimes_{\Delta^{op}} N((-)/\Delta^{op})^{op}
  \stackrel{Id_X \otimes_{\Delta^{op}} \phi }{\to}
  X \otimes_{\Delta^{op}} \Delta
  \,.
$$


##Bousfield--Kan for cosimplicial objects##



For $X : \Delta \to C$ any cosimplicial object, its **totalization** is the $\Delta$-[[weighted limit]]

$$
  Tot X := lim^\Delta X \simeq \int_{[n \in \Delta]} X_n^{\Delta^n}
  \,,
$$

where in the integrand we have the [[power]] or cotensor $X_n^{\Delta^n} = \pitchfork(\Delta, X_n)$ of $C$ by [[SimpSet|SSet]].


Here the **Bousfield--Kan** morphism is the morphism

$$
  Tot X \simeq hom(\Delta,X) \stackrel{hom(\phi,Id_X)}{\to}  
  hom(N(\Delta/(-)), X)
  \,.
$$


##Properties##


**Theorem**

If the [[simplicial object]] $X$ is [[Reedy category|Reedy cofibrant]] then its Bousfield--Kan map is a natural weak equivalence.

If the co[[simplicial object]] $X$ is [[Reedy category|Reedy fibrant]] then its Bousfield--Kan map is a natural weak equivalence.


#Relation to homotopy limits#

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


#References#

* Hirschhorn, _Simplicial model categories and their localization_.

The Bousfield--Kan map(s) are on p. 397, def. 18.7.1 and def. 18.7.3.

 _Realization_ and _totalization_ are defs 18.6.2 and 18.6.3 on p. 395.

Notice that this book writes $B$ for the nerve!
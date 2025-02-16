
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


\tableofcontents

## Idea

The *Bousfield-Kan formula* ([BK72](#BousfieldKan)) is a presentation of [[colimits]] (or [[formal duality|dually]], [[limits]]) in [[(infinity,1)-categories|$(\infty,1)$-categories]] (i.e., [[homotopy colimits]]) in terms of [[coproducts]] and [[colimits]] of [[simplicial objects]].

In ordinary [[category theory]], the [[colimit]] of a [[diagram]] $F \colon I\to C$ may be computed as a [[coequalizer]] of the [[parallel pair]]
$$
  \coprod_{c_{0}\to c_{1}}F c_{0}
    \rightrightarrows
  \coprod_{c}F c
  \,.
$$
When $C$ is an $(\infty,1)$-category, we need to take "higher
data" into account. So we take the [[geometric realization]] (i.e., $\Delta^{op}$-[[indexed colimit]]) of the [[simplicial object]]
$$
  B_{\bullet}(\ast,I,F)
  \;=\;
  \left(
      \cdots
    \coprod_{c_{0}\to c_{1}\to c_{2}} F c_{0}
      \Rrightarrow
    \coprod_{c_{0}\to c_{1}} F c_{0}
      \rightrightarrows
    \coprod_{c\in C} F c
  \right)
  \,.
$$
This can be formalized as follows: There is an "initial vertex" functor $\mathrm{init} \colon (\Delta_{/I})^{op}\to I$ from the [[opposite category|opposite]] of the [[category of simplices]] of $I$, which is [[homotopy final functor|homotopy final]]. Thus,
$$
  \mathrm{colim}_{I} F
  \;\simeq\;
  \mathrm{colim}_{(\Delta_{/I})^{op}}(F\circ\mathrm{init})
  \,.
$$
The simplicial object $B_{\bullet}(\ast,I,F)$ is just the [[left Kan extension]] of $F\circ\mathrm{init}$ along the projection $(\Delta_{/I})^{op}\to\Delta^{op}$,
so we have
$$
  \mathrm{colim}_{(\Delta_{/I})^{op}}  (F\circ\mathrm{init})
    \simeq
  \mathrm{colim}_{\Delta^{op}}B_{\bullet}(\ast,I,F)
  \,.
$$


## Particular Implementations in Model Categories

### Via Geometric Realizations

In a [[simplicial model category]] $C$, [[homotopy colimits]] indexed by $\Delta^{op}$ are modeled by [[geometric realization]] (see [there](geometric+realization+of+simplicial+topological+spaces#RelationToHomotopyColimit)). Therefore, the Bousfield-Kan formula for the [[homotopy colimit]] of a (pointwise [[cofibrant]]) diagram $F \colom I\to C$ is computed by
$$
  {\mathrm {hocolim}}_{I}F
    \simeq
  {\big|B_{\bullet}(\ast,I,F)\big|}
  \,.
$$
Textbook account includes [Rie14, Chapter 5](#Riehl14).

### Via Functor Tensor Product

Let $F \colon I\to C$ be a (pointwise cofibrant) diagram in a [[simplicial model category]]. Some [[coend]] calculus shows [Rie14, 6.6.1](#Riehl14)
that 
$$
  \big\vert
    B_{\bullet}(\ast,I,F)
  \big\vert
   \;\cong\;
  \int^{i\in I}N(I_{/i})\otimes F(i)
    \;\eqqcolon\;
  N(I_{/-})\otimes_{I}F
  \,.
$$
The right hand side is also called the *Bousfield-Kan formula*. 

### In Model Categories with Framings {#framed}

A cosimplicial [framing](derived+hom-space#Framings) on a [[model category]] is roughly a functorial choice of cosimplicial [[resolutions]] [Hir03, Chapter 16](#Hir03). With this data, we can formally mimic the Bousfield-Kan formula, and this is adopted as the definition of homotopy colimits in [Hir03, Chapter19](#Hir03); that this approach is equivalent to the ordinary notion of homotopy colimits is established in [AO23](#AO23) (for combinatorial model
categories) and [Ara23, Theorem 1.16](#Ara23) (for general model categories).

## Bousfield--Kan map

In a [[simplicial model category]] (this can be generalized, as discussed [above](#framed)), there are two formulas for [[homotopy colimits]] of [[simplicial objects]]: The Bousfield--Kan formula, and geometric realization. The Bousfield--Kan map(s) compare these formulas.

More precisely, let $C$ be an ([[SimpSet|SSet]],$\otimes = \times$)-[[enriched category]] and write 

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
There is also the Bousfield--Kan map for cosimplicial objects:


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

+-- {: .un_theorem}
###### Theorem

If the [[simplicial object]] $X$ is [[Reedy category|Reedy]]-[[cofibrant objects|cofibrant]] then its Bousfield--Kan map is a natural [[weak equivalence]].

If the co-[[simplicial object]] $X$ is [[Reedy category|Reedy fibrant]] then its Bousfield--Kan map is a natural weak equivalence.


=--

+-- {: .proof}
###### Proof

This can be proven for instance using [[homotopy colimits]] in the [[Reedy model structure]]. Details are at *[Reedy model structure -- over the simplex category](Reedy+model+structure#SimplexCategory)*.

=--




+-- {: .un_example}
###### Example

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


=--

## References

The Bousfield-Kan formula was introduced in:

* {#BK72} [[Aldridge K. Bousfield]] and [[Daniel M. Kan]], Chapter IX in: *[[Homotopy Limits, Completions and Localizations]]*, Lecture Notes in Mathematics 304 (1972; 1987), Springer ([doi:10.1007/978-3-540-38117-4](https://link.springer.com/book/10.1007/978-3-540-38117-4))

Discussion in [[model categories]]:

* {#Hir03} [[Philip Hirschhorn]], _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs **99** (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/pshmain.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;

  > The Bousfield--Kan map(s) are on p. 397, def. 18.7.1 and def. 18.7.3.

  > _Realization_ and _totalization_ are defs 18.6.2 and 18.6.3 on p. 395.

  > Beware that this book writes $B$ for the nerve!

Discussions in [[simplicial model categories]]:

* {#Rie16} [[Emily Riehl]], Chapter 5 in: *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;

See also:

* {#AO23} [[Sergey Arkhipov]], [[Sebastian Ørsted]]: _Homotopy (co)limits via homotopy (co)ends in general combinatorial model categories_, Appl. Categ. Structures **31** 6 (2023) &lbrack;[doi:10.1007/s10485-023-09747-8](https://doi.org/10.1007/s10485-023-09747-8)&rbrack;

* {#Ara23} [[Kensuke Arakawa]], Section 1 of: _Homotopy Limits and Homotopy Colimits of Chain Complexes_, (2023)  &lbrack;[arXiv:2310.00201](https://arxiv.org/abs/2310.00201)&rbrack;

[[!redirects Bousfield-Kan formulas]]

[[!redirects Bousfield--Kan formula]]
[[!redirects Bousfield--Kan formulas]]


[[!redirects Bousfield-Kan map]]
[[!redirects Bousfield-Kan maps]]

[[!redirects Bousfield--Kan map]]
[[!redirects Bousfield--Kan maps]]

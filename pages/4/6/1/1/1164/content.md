
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _orbit category_ of a [[group]] $G$ is the category of "all kinds" of  [[orbits]] of $G$, namely of all suitable [[coset spaces]] regarded as [[G-spaces]]. 

## Definition

+-- {: .num_defn #TheOrbitCategory}
###### Definition

Given a [[topological group]] $G$ the __orbit category__ $\operatorname{Orb}_G$ (denoted also $\mathcal{O}_G$) is the [[category]] whose 

* [[objects]] are the [[homogeneous spaces]]  ([[coset spaces]], $G$-[[orbit types]]) $G/H$, where $H$ is a [[closed subgroup]] of $G$, 

* [[morphisms]] are the $G$-[[equivariant function|equivariant]] [[continuous functions]].  

=--

+-- {: .num_remark }
###### Remark

For suitable [[continuous function|continuous]] [[actions]] of $G$ on a [[topological space]] $X$, every [[orbit]] of the action is [[isomorphism|isomorphic]] to one of the [[coset spaces]] $G/H$ (the [[stabilizer group]] of any point in the orbit is conjugate to $H$). This is the sense in which def. \ref{TheOrbitCategory} gives "the category of all $G$-orbits".

=--

+-- {: .num_remark }
###### Remark

Def. \ref{TheOrbitCategory} yields a [[small category|small]] [[enriched category|topologically enriched]] category (though of course if $G$ is a [[discrete group]], the enrichment of $\operatorname{Orb}_G$ is likewise discrete).  

Of course, like any category, it has a [[skeleton]], but as usually defined it is not itself skeletal, since there can exist distinct subgroups $H$ and $K$ such that $G/H \cong G/K$.

=--



\begin{remark}\label{GActionsAndGOrbits}
**([[G-set|$G$-sets]] are the [[free coproduct completion]] of [[orbit category|$G$-orbits]])**
\linebreak
  Let $G \,\in\, Grp(Set)$ be a [[discrete group]]. 
Since every [[G-set]] $X$ decomposes as a [[disjoint union]] of [[transitive actions]], namely of [[orbits]] of [[elements]] of $X$, the defining inclusion of the orbit category into [[G-set|$G Set$]] exhibits the latter as its [[free coproduct completion]] (see also [this Prop.](free+coproduct+completion#CategoriesOfCoproductsOfConnectedObjects)). 
\end{remark}


+-- {: .num_remark }
###### Remark

Warning: This should not be confused with the situation where a group $G$ acts on a groupoid $\Gamma$ so that one obtains the  [[orbit groupoid]].   

=--

More generally, given a family $F$ of subgroups of $G$ which is closed under conjugation and taking subgroups one looks at the full subcategory $\mathrm{Orb}_F\,G \subset \operatorname{Orb}_G$ whose objects are those $G/H$ for which $H\in F$.


## Variants

### Families of subgroups

Sometimes a family, $\mathcal{W} \subset Sub_{Grp}(G)$, of [[subgroups]] is specified, and then a subcategory of $Orb_G$ consisting of the $G/H$ where $H\in \mathcal{W}$ will be considered. If the trivial subgroup is in $\mathcal{W}$ then many of the considerations of results such as [[Elmendorf's theorem]] will still hold.



### Equivariant fundamental groupoid
 {#FundamentalCategoryOfAGSpace}


\begin{definition}\label{EquivariantFundamentalGroupoid}
For $G \curvearrowright X \,\in\, G Act(TopSp)$ a [[topological G-space]], its *fundamental category* ([tom Dieck 1987 (10.7)](#tomDieck87), [Lück 1989, 8.15](#Lueck89)) or *equivariant fundamental groupoid* ([Pronk & Scull 2021, Def. 3.1](#PronkScull21))

is the [[small category]] whose

- [[objects]] are [[pairs]] consisting of a [[subgroup]] $H \subset G$ and a  $G$-[[equivariant functions]] $x_X \,\colon\, G/H \to X$, hence, equivalently a points in the [[fixed locus]] $X^H$;

- [[morphisms]] $x_H \xrightarrow{ (\phi,[\gamma]) } x'_{H'}$  are [[pairs]] consisting of a $G$-[[equivariant function]] $G/H \xrightarrow{ \phi } G/H'$ and a relative $G$-homotopy class $[\gamma]$ of a continuous path $\gamma \,\colon\,  G/H \times [0,1] \xrightarrow{\;} X$ from $\gamma(0) = x_H$ to $\gamma_1 = \phi^\ast x'_X'$.

\end{definition}

\begin{example}
  For $G \curvearrowright X \,=\, G \curvearrowright \ast$ the point, its fundamental category (equivariant fundamental groupoid) according to Def. \ref{EquivariantFundamentalGroupoid} is the plain [[orbit category]] $G Orbts$ (Def. \ref{TheOrbitCategory}).
\end{example}

\begin{proposition}
If we write 
$$
  \tau_1 \esh \big( X^{(-)}\big)
  \;\in\;
  PSh\big( G Orbt \big)
$$
for the [[fundamental groupoid]] of $X$ in its incarnation as a [[presheaf]] of [[fixed loci]] over the [[orbit category]], hence for the [[(2,1)-functor]]

\[
  \label{FundamentalGroupoidOfAPresheafOfFixedLoci}
  \array{
    G Orbt^{op}
    &\xrightarrow{ \tau_1 \esh \big( X^{(-)}\big) }&
    Grpd_1
    \\
    G/H
    &\mapsto&
    \tau_1 \esh (X^H)
  }
\]
which sends $G/H$ to the ordinary [[fundamental groupoid]] of the [[fixed locus]] $X^H$, then the equivariant fundamental groupoid of $G \curvearrowright X$ (Def. \ref{EquivariantFundamentalGroupoid}) is equivalently the [[Grothendieck construction]] on (eq:FundamentalGroupoidOfAPresheafOfFixedLoci).
\end{proposition}

This follows by direct unwinding of the definitions; see also [Pronk & Scull 2021, below Def. 3.1](#PronkScull21).


## Examples
 {#Examples}

+-- {: .num_example #OrbitCategoryOfCyclicGroupOfOrder2} 
###### Example
**([[orbit category]] of [[cyclic group of order 2|Z/2Z]])**

For equivariance group the [[cyclic group of order 2]]:

$$
  G \;\coloneqq\;  \mathbb{Z}_2 \;\coloneqq\; \mathbb{Z}/2\mathbb{Z}
  \,.
$$

the [[orbit category]] looks like this:

\[
  \label{OrbitCategoryOfZMod2}
  \mathbb{Z}_2
  Orbits
  \;=\;
  \left\{
  \array{
    \mathbb{Z}_2/1
    &
      \overset{
        \phantom{AAAAA}
      }{ 
        \longrightarrow
      }
    &
    \mathbb{Z}_2/\mathbb{Z}_2
    \\
    Aut = \mathbb{Z}_2
    &&
    Aut = 1
  }
  \right\}
\]

i.e.:

$$
  \begin{aligned}
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/\mathbb{Z}_2
      \,,\,
      \mathbb{Z}_2/\mathbb{Z}_2
    \big)
    \;\simeq\;
    1
    \\
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/1
      \,,\,
      \mathbb{Z}_2/\mathbb{Z}_2
    \big)
    \;\simeq\;
    \ast
    \\
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/\mathbb{Z}_2
      \,,\,
      \mathbb{Z}_2/1
    \big)
    \;\simeq\;
    \varnothing
    \\
    \mathbb{Z}_2 Orbits
    \big(
      \mathbb{Z}_2/1
      \,,\,
      \mathbb{Z}_2/1
    \big)
    \;\simeq\;
    \mathbb{Z}_2
  \end{aligned}
$$

=--


\begin{imagefromfile}
  "file_name": "OrbitCategoriesOfSmallCyclicGroups.jpg",
  "width": 600,
  "margin": {
    "top": 0,
    "right": 10,
    "bottom": 10,
    "left": 0,
    "unit": "px"
  } 
\end{imagefromfile}

## Properties

### General properties

* Orbit categories as well as fundamental categories of $G$-spaces are [[EI-categories]].

### Relation to $G$-spaces and Elmendorf's theorem

[[Elmendorf's theorem]] (see there for details) states that the [[(∞,1)-category of (∞,1)-presheaves]] on the orbit category $Orb_G$ are [[equivalence of (∞,1)-categories|equivalent]] to the [[localization of an (∞,1)-category|localization]] of [[topological spaces]] with $G$-[[action]] at the _[[weak homotopy equivalences]] on [[fixed point spaces]]_.

$$
  L_{we} G Top \simeq PSh_\infty(Orb_G)
  \,.
$$


### Relation to global equivariant homotopy theory
 {#RelationToGlobalHomotopyTheory}

The $G$-orbit category is the [[slice (∞,1)-category]] of the [[global orbit category]] $Orb$ (the version with [[faithful functors]] as morphisms) over the [[delooping]] $\mathbf{B}G$:

$$
  Orb_G \simeq Orb_{/\mathbf{B}G}
  \,.
$$

This means that in the general context of [[global equivariant homotopy theory]], the orbit category appears as follows.

For more on this see also at *[[cohesion of global- over G-equivariant homotopy theory]]* the section *[the adjunction of sites](cohesion+of+global-+over+G-equivariant+homotopy+theory#TheAdjunctionOfSites)*.

[[!include equivariant homotopy theory -- table]]


### Relation to Mackey functors

Orbit categories are used often in the treatment of [[Mackey functor]]s from the theory of [[locally compact group]]s and in the definition of [[Bredon cohomology]]. 

### Relation to Bredon equivariant cohomology

It appears in [[equivariant stable homotopy theory]], where the $H$-fixed [[homotopy groups]] of a space form a [[presheaf]] on the [[homotopy category]] of the orbit category (e.g. [page 8, 9 here](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf#page=8)).



### Base change of equivariance groups
 {#BaseChangeOfEquivarianceGroups}

\begin{example}\label{LeftBaseChangeAlongCoveringOfEquivarianceGroup}
**(left base change along covering of equivariance group)**
\linebreak
Let $\widehat{G} \overset{p}{\twoheadrightarrow} G $ be a surjective homomorphism of discrete groups. For $H \subset G$ a [[subgroup]], write $\widehat{H} \subset \widehat{G}$ for its [[pullback]]

\begin{tikzcd}
  \widehat{H}
  \ar[r, hook]
  \ar[d,->>]
  \ar[dr, phantom, "\mbox{\tiny(pb)}"]
  &
  \widehat{G}
  \ar[d,->>]
  \\
  H
  \ar[r, hook]
  &
  G
  \mathrlap{\,.}
\end{tikzcd}


Then there is a [[reflective subcategory]]-inclusion of orbit categories

\begin{tikzcd}
  \widehat{G}\mathrm{Orbt}
  \ar[from=r, hook', shift left=7pt, "R"]
  \ar[r, shift left=7pt, "L"]
  \ar[r, phantom, "\scalebox{.7}{$\bot$}"]
  &
  G\mathrm{Orbt}
\end{tikzcd}

where

* $R(G/H) \,=\, \widehat{G}/\widehat{H}$

* $L(\widehat{G}/K) \,=\, G/p(K)$.

A transparent way to see this is to identify (as [above](#RelationToGlobalHomotopyTheory))
$G$-orbits with the [[n-truncated object of an (infinity,1)-category|0-truncated objects]] in the $B G$-slice of $Singlrt \,\coloneqq\, Grpd_1^{cn} $: 

$$
  G Orbt \;\simeq\; \left( (Grpd_1^{cn})_{/ B G} \right)_0
  \,.
$$

Under this identification, the adjunction is the canonical left [[base change]] on [[slice (infinity,1)-category|slices]] composed with the [[n-truncated object of an (infinity,1)-category|0-truncation]] reflection ([here](n-truncated+object+of+an+infinity1-category#nTruncationReflection)):

\begin{tikzcd}
  (\mathrm{Grpd}_1^{\mathrm{cn}})_{/ B \widehat{G}}
  \ar[from=r, shift left=7pt, "(B p)^\ast"]
  \ar[r, shift left=7pt, "(B p)_!"]
  \ar[r, phantom, "\scalebox{.7}{$\bot$}"]
  &
  (\mathrm{Grpd}_1^{\mathrm{cn}})_{/ B G}
  \ar[from=r, hook', shift left=7pt]
  \ar[r, shift left=7pt, "\tau_0"]
  \ar[r, phantom, "\scalebox{.7}{$\bot$}"]
  &
  \left( (\mathrm{Grpd}_1^{\mathrm{cn}})_{/ B G} \right)_0
\end{tikzcd}

That the right adjoint $R$ is fully faithful is most readily seen by direct inspection: A map between $\widehat{G}$-sets on both of which $\widehat{G}$ acts only through $G$ is evidently $\widehat{G}$-equivariant if and only if it is $G$-equivariant.
\end{example}

\linebreak


## Related concepts

* [[orbit]], [[orbit type]]

* [[equivariant homotopy theory]]

* [[global orbit category]], [[global equivariant stable homotopy theory]]

* [[Bredon cohomology]], [[equivariant cohomology]]

* [[topological G-space]]

* [[vector G-space]]

* [[equivariant dgc-algebra]]

* [[equivariant rational homotopy theory]]




## References

The notion of the orbit category (for use in [[equivariant cohomology]]/[[Bredon cohomology]]) is due to

* {#Bredon67b} [[Glen Bredon]], Section I.3. of _[[Equivariant cohomology theories]]_, Springer Lecture Notes in Mathematics Vol. 34. 1967 ([doi:10.1007/BFb0082690](https://link.springer.com/book/10.1007/BFb0082690))

announced in

* {#Bredon67a} [[Glen Bredon]], _Equivariant cohomology theories_, Bull. Amer. Math. Soc. Volume 73, Number 2 (1967), 266-268. ([educlid:1183528794](https://projecteuclid.org/euclid.bams/1183528794))

and there considered specifically for [[finite groups]].

Discussion for any [[topological group]] (and further generalization)  is considered (together with the [[model category|model category theoretic]] proof of [[Elmendorf's theorem]]) in:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]], Sec. 2.1 and Thm. 3.1 of: _Singular functors and realization functors_, Indagationes Mathematicae (Proceedings) Volume 87, Issue 2, 1984, Pages 147-153 (<a href="https://doi.org/10.1016/1385-7258(84)90016-7">doi:10.1016/1385-7258(84)90016-7</a>)

Textbook accounts:

* {#tomDieck87} [[Tammo tom Dieck]], Section I.10 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

* {#Lueck89} [[Wolfgang Lück]], (8.16) in _Transformation Groups and Algebraic K-Theory_, Lecture Notes in Mathematics **1408** (Springer 1989) ([doi:10.1007/BFb0083681](https://doi.org/10.1007/BFb0083681))

* {#May96} [[Peter May]], Section I.4 of: _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996 ([ISBN:978-0-8218-0319-6](https://bookstore.ams.org/cbms-91), [pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf), [pdf](https://ncatlab.org/nlab/files/MayEtAlEquivariant96.pdf))

Lecture notes:

* {#tomDieck09} [[Tammo tom Dieck]], Section 1.3 of: _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

For more in relation to [[global equivariant homotopy theory]] see 

* [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_

The notion of fundamental category of a $G$-space is due to 

* [tom Dieck 1987](#tomDieck87)

* [Lück 1989, 8.15](#Lueck89)

with further discussion in

* {#PronkScull21} [[Dorette Pronk]], [[Laura Scull]], *The Equivariant Fundamental Groupoid as an Orbifold Invariant*, Homology, Homotopy and Applications **23** 1 (2021) ([arXiv:1908.01201](https://arxiv.org/abs/1908.01201), [doi:10.4310/HHA.2021.v23.n1.a3](https://dx.doi.org/10.4310/HHA.2021.v23.n1.a3))


[[!redirects orbit categories]]

[[!redirects equivariant fundamental groupoid]]
[[!redirects equivariant fundamental groupoids]]


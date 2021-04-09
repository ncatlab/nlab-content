
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

Of course, like any category, it has a [[skeleton]], but as usually defined it is not itself skeletal, since there can exist distinct subgroups $H$ and $K$ such that $G/H\cong G/K$.


=--

+-- {: .num_remark }
###### Remark

Warning: This should not be confused with the situation where a group $G$ acts on a groupoid $\Gamma$ so that one obtains the  [[orbit groupoid]].   

=--

More generally, given a family $F$ of subgroups of $G$ which is closed under conjugation and taking subgroups one looks at the full subcategory $\mathrm{Orb}_F\,G \subset \operatorname{Orb}_G$ whose objects are those $G/H$ for which $H\in F$.


## Variants

Sometimes a family, $\mathcal{W}$, of subgroups is specified, and then a subcategory of $\operatorname{Orb}_G$ consisting of the $G/H$ where $H\in \mathcal{W}$ will be considered. If the trivial subgroup is in $\mathcal{W}$ then many of the considerations of results such as [[Elmendorf's theorem]] will go across to the restricted setting.

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

### Relation to $G$-spaces and Elmendorf's theorem

[[Elmendorf's theorem]] (see there for details) states that the [[(∞,1)-category of (∞,1)-presheaves]] on the orbit category $Orb_G$ are [[equivalence of (∞,1)-categories|equivalent]] to the [[localization of an (∞,1)-category|localization]] of [[topological spaces]] with $G$-[[action]] at the _[[weak homotopy equivalences]] on [[fixed point spaces]]_.

$$
  L_{we} G Top \simeq PSh_\infty(Orb_G)
  \,.
$$


### Relation to equivariant homotopy theory

The $G$-orbit category is the [[slice (∞,1)-category]] of the [[global orbit category]] $Orb$ over the [[delooping]] $\mathbf{B}G$:

$$
  Orb_G \simeq Orb_{/\mathbf{B}G}
  \,.
$$

This means that in the general context of [[global equivariant homotopy theory]], the orbit category appears as follows.

[[!include equivariant homotopy theory -- table]]


### Relation to Mackey functors

Orbit categories are used often in the treatment of [[Mackey functor]]s from the theory of [[locally compact group]]s and in the definition of [[Bredon cohomology]]. 

### Relation to Bredon equivariant cohomology

It appears in [[equivariant stable homotopy theory]], where the $H$-fixed [[homotopy groups]] of a space form a [[presheaf]] on the [[homotopy category]] of the orbit category (e.g. [page 8, 9 here](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf#page=8)).


### Relation to the category of groups, homomorphisms and conjugations

See at _[[global equivariant homotopy theory]]_.

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

* {#May96} [[Peter May]], Section I.4 of: _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996 ([ISBN:978-0-8218-0319-6](https://bookstore.ams.org/cbms-91), [pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf), [pdf](https://ncatlab.org/nlab/files/MayEtAlEquivariant96.pdf))

Lecture notes:

* {#tomDieck09} [[Tammo tom Dieck]], Section 1.3 of: _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

For more on the relation to [[global equivariant homotopy theory]] see 

* [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_

[[!redirects orbit categories]]

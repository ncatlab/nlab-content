
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

### Pure Hodge structure

A _Hodge structure_ (or _pure Hodge structure_, for emphasis) is a (bi-)[[graded object|grading]] structure on [[cohomology groups]] -- called a _Hodge decomposition_ -- of the kind that is exhibited by the [[de Rham cohomology]]/complex-[[ordinary cohomology]] of [[compact topological space|compact]] [[Kähler manifolds]], according to the [[Hodge theorem]]. A Hodge structure is said to be _of weight $d$_ if it behaves like the cohomology of a K&#228;hler manifold of [[dimension]] $d$.

If instead of considering a single [[cohomology group]] one considers the cohomology groups of a parameterized collection of spaces -- hence the cohomology _[[sheaves]]/[[stacks]]_ -- then one speaks of _variation of Hodge structure_ (of a given weight).

By a central theorem of Hodge theory (recalled as theorem \ref{HodgeFiltrationForComplexSpaceReproducesKaehlerHodgeStructure} below) the traditional (and original) [[filtered complex|filtration]] on the complex cohomology of a [[Kähler manifold]] induced by the [[harmonic differential forms]] generalizes to a [[filtered complex|filtration]] of the complex-valued [[ordinary cohomology]] of any [[complex analytic space]] which is simply given by the canonical degree-filtration of the [[holomorphic de Rham complex]].

This means that [[ordinary differential cohomology]] in the guise of [[Deligne cohomology]] is nothing but the [[homotopy pullback]] of a stage of the Hodge filtration along the "[[Chern character]]" map from integral to complex cohomology. (A point of view highlighted for instance in [Peters-Steenbrink 08, section 7.2](#PetersSteenbrink08)). Viewed this way Hodge structures are filtrations of stages of differential form cycle refinements of [[Chern characters]] that appear in the general definition/characterization of [[differential cohomology]], as discussed at  _[[differential cohomology hexagon]]_ starting around the section _[de Rham coefficients](differential+cohomology+diagram#DeRhamCoefficients)_

This modern point of view is also crucial for instance in the characterization of an [[intermediate Jacobian]] (see there) as the subgroup of [[Deligne cohomology]] that is in the [[kernel]] of the map to Hodge-filtering stage of ordinary cohomology. See at _[intermediate Jacobian -- characterization as Hodge-trivial Deligne cohomology](intermediate+Jacobian#CharacterizationAsHodgeTrivialDeligneCohomology)_.

### Mixed Hodge structure

A _mixed Hodge structure_ is a [[filtration]] on [[cohomology groups]] -- called a _[[Hodge filtration]]_ -- such that the [[associated graded object]] has pure Hodge structure of weight $k$ in each degree $k$. The archetypical example exhibiting this is the cohomology of  [[complex varieties]] that have singularities ([Deligne 71](#Deligne71) [Deligne 74](#Deligne74)).


## Definition

### For a K&#228;hler manifold

(...)

For a [[Kähler manifold]], the Hodge filtering of its complex cohomology is that induced by its [[harmonic differential forms]] (...)

### For a complex analytic space
 {#ForAComplexAnalyticSpace}

For $X$ a [[complex analytic space]], write 

$$
  \Omega^\bullet_X
  \coloneqq
  (\mathcal{O}_X \stackrel{\partial}{\longrightarrow} \Omega^1_X \stackrel{\partial}{\longrightarrow} \Omega^2(X) \stackrel{\partial}{\longrightarrow} \cdots)
$$

for its [[holomorphic de Rham complex]]. Notice its [relation to complex cohomology](holomorphic+de+Rham+complex#RelationToComplexCohomology) given by

$$
  H^k(X,\mathbb{C}) \simeq H^k(X,\Omega^\bullet_X)
  \,.
$$


The [[holomorphic de Rham complex]] is naturally [[filtered object|filtered]] by degree with the $p$th filtering stage being

$$
  F^p \Omega^\bullet_X
  \coloneqq
  (0 \to \cdots \to \Omega^p_X \stackrel{\partial}{\longrightarrow}
   \Omega^{p+1} \stackrel{\partial}{\longrightarrow} \cdots)
  \,.
$$

Notice that here $\Omega^p$ is still regarded as sitting in degree $-p$, one just replaces by 0 in the holomorphic de Rham complex the groups of differential forms of degree less than $p$.

+-- {: .num_defn #HodgeFiltrationForComplexSpace}
###### Definition

The _Hodge filtration_ on $H^\bullet(X,\mathbb{C})$ is defined to be the [[filtration]] with $p$th stage the [[image]] of the [[hypercohomology|hyper]]-[[abelian sheaf cohomology]] with coefficients in the $p$th filtering stage of the holomorphic de Rham complex inside that with coefficients the full de Rham complex:

$$
  F^p H^k(X,\mathbb{C})
  \coloneqq
  im
  \left(
    H^k(X, F^p \Omega^\bullet_X)
    \to 
    H^k(X, \Omega^\bullet_X)
  \right)
$$

=--

(e.g. [Voisin 02, def. 8.2](#Voisin02), [Peters-Steenbrink 08, def. 2.21](#PetersSteenbrink08)).

+-- {: .num_theorem #HodgeFiltrationForComplexSpaceReproducesKaehlerHodgeStructure}
###### Theorem

When the [[complex manifold]] $X$ happens to be a [[Kähler manifold]] then the [[Frölicher spectral sequence]]/[[Hodge–de Rham spectral sequence]]  gives that def. \ref{HodgeFiltrationForComplexSpace} coincides with the more traditional definition via [[harmonic differential forms]]. 

=--

(e.g. [Voisin 02, remark 8.29](#Voisin02), [Peters-Steenbrink 08, prop 2.22](#PetersSteenbrink08)).


## Related concepts

* [[Hodge theory]], 

  [[nonabelian Hodge theory]], [[noncommutative Hodge theory]]

* [[Hodge cohomology]]

* [[intermediate Jacobian]]

## References

Textbook accounts include

* {#Voisin02} [[Claire Voisin]], section 7 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

* {#PetersSteenbrink08} [[Chris Peters]], [[Jozef Steenbrink]], _[[Mixed Hodge Structures]]_, Ergebisse der Mathematik (2008) ([pdf](http://www.arithgeo.ethz.ch/alpbach2012/Peters_Steenbrinck))

The notion of mixed Hodge structures was introduced in 

* {#Deligne71} [[Pierre Deligne]], _Th&#233;orie de Hodge II_, Publ. Math. I.H.E.S, 40, 5&#8211;58 (1971)
 

* {#Deligne74} [[Pierre Deligne]], _Th&#233;orie de Hodge III_, Publ. Math., I. H. E. S, 44, 5-77 (1974)


A review is in section 8.4 of 

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_

 

See also

* [[Jozef Steenbrink]], S. Zucker, _Variation of mixed Hodge structure I_, Invent. Math. __80__ (1985), 489-542.


* Wikipedia, _[Hodge structure](http://en.wikipedia.org/wiki/Hodge_structure), 

* [[Donu Arapura]], _Mixed Hodge Structures Associated to
Geometric Variations_ ([pdf](http://www.math.purdue.edu/~dvb/preprints/tifr.pdf))


*  [[eom]], 

   A.I. Ovseevich _[Hodge structure](http://eom.springer.de/H/h047470.htm)_, _[Period mapping](http://eom.springer.de/p/p072140.htm)_, 

   [[Jozef Steenbrink]], _[Variation of Hodge structure](http://eom.springer.de/v/v096170.htm)_

* [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_ ([arXiv:1212.2173](http://arxiv.org/abs/1212.2173))


[[!redirects Hodge structures]]

[[!redirects pure Hodge structure]]
[[!redirects pure Hodge structures]]

[[!redirects mixed Hodge structure]]
[[!redirects mixed Hodge structures]]

[[!redirects Hodge filtration]]
[[!redirects Hodge filtrations]]
[[!redirects Hodge decomposition]]
[[!redirects Hodge decompositions]]

[[!redirects variation of Hodge structure]]
[[!redirects variation of Hodge structures]]
[[!redirects variations of Hodge structure]]
[[!redirects variations of Hodge structures]]
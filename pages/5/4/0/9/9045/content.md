
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

This means that [[ordinary differential cohomology]] in the guise of [[Deligne cohomology]] is nothing but the [[homotopy pullback]] of a stage of the Hodge filtration along the " [[Chern character]] " map from integral to complex cohomology. (A point of view highlighted for instance in [Peters-Steenbrink 08, section 7.2](#PetersSteenbrink08)). Viewed this way Hodge structures are filtrations of stages of differential form cycle refinements of [[Chern characters]] that appear in the general definition/characterization of [[differential cohomology]], as discussed at  _[[differential cohomology hexagon]]_ starting around the section _[de Rham coefficients](differential+cohomology+diagram#DeRhamCoefficients)_

This modern point of view is also crucial for instance in the characterization of an [[intermediate Jacobian]] (see there) as the subgroup of [[Deligne cohomology]] that is in the [[kernel]] of the map to Hodge-filtering stage of ordinary cohomology. See at _[intermediate Jacobian -- characterization as Hodge-trivial Deligne cohomology](intermediate+Jacobian#CharacterizationAsHodgeTrivialDeligneCohomology)_.

### Mixed Hodge structure

A _mixed Hodge structure_ is a [[filtration]] on [[cohomology groups]] -- called a _[[Hodge filtration]]_ -- such that the [[associated graded object]] has pure Hodge structure of weight $k$ in each degree $k$. The archetypical example exhibiting this is the cohomology of  [[complex varieties]] that have singularities ([Deligne 71](#Deligne71) [Deligne 74](#Deligne74)).


## Definition

Historically, Hodge structures originate in the special structure induced on the [[de Rham cohomology|de Rham]] [[cohomology groups]] of a compact [[Kähler manifold]] by the existence of [[harmonic differential forms]]. Below we first discuss this canonical Hodge structure

* [on the cohomology of a K&#228;hler manifold](#ForAKaehlerManifold)

But it turns out that this Hodge structure only depends on the natural degree-[[filtration]] on the [[holomorphic de Rham complex]] and hence more generally there is canonical Hodge structure

* [on the cohomology of a complex analytic space](#ForAComplexAnalyticSpace).

Abstracting from here one defines Hodges structures 

* [generally on abelian groups](#OnAnAbelianGroup).

### On the cohomology of a K&#228;hler manifold
 {#ForAKaehlerManifold}

Let $X$ be a [[compact topological space|compact]] [[Kähler manifold]] and write $H^{p,q}(X)$ for its space of [[harmonic differential forms]], equivalently, via the [[Hodge isomorphism]], its [[Dolbeault cohomology]] in bidegree $(p,q)$.

Notice that by the [[de Rham theorem]] there are canonical maps

$$
  H^{p,q}(X)\to H^{p+q}(X,\mathbb{C})
$$

to [[ordinary cohomology]] of $X$ with complex [[coefficients]].

+-- {: .num_defn #TraditionalHodgeFiltration}
###### Definition

The _Hodge filtration_ on the cohomology of $X$ is the [[filtered complex]] structure given by the [[direct sum]]


$$
  F^p H^k(X, \mathbb{C})
   \coloneqq
  \underset{k-q \geq p}{\oplus}
  H^{k-q,q}(X)
  \,.
$$

=--

+-- {: .num_example}
###### Example

The full Hodge filtration of degree-2 cohomology is

$$
  \begin{aligned}
    F^0 H^2(X,\mathbb{C})
    & =
    H^{0,2}(X) \oplus H^{1,1}(X) \oplus H^{2,0}(X)
    \\
    F^1 H^2(X,\mathbb{C})
    & =
    \;\;\;\;\;\;\;
    H^{1,1}(X)
    \oplus
    H^{2,0}(X)
    \\
    F^2 H^2(X,\mathbb{C})
    & = 
    \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
    H^{2,0}(X)
 \end{aligned}
$$

=--

+-- {: .num_example}
###### Example

For all $p$ the mid-dimensional Hodge filtration stage in even total degree is

$$
  F^p H^{2p}
  = 
  H^{p,p}(X)
  \oplus
  H^{p+1,p-1}(X)
  \oplus 
  \cdots
  \oplus
  H^{2p,0}(X)
  \,.
$$



=--

### On the cohomology of a complex analytic space
 {#ForAComplexAnalyticSpace}

+-- {: .num_defn }
###### Definition


For $X$ a [[complex analytic space]], write 

$$
  \Omega^\bullet_X
  \coloneqq
  (\mathcal{O}_X \stackrel{\partial}{\longrightarrow} \Omega^1_X \stackrel{\partial}{\longrightarrow} \Omega^2(X) \stackrel{\partial}{\longrightarrow} \cdots)
$$

for its [[holomorphic de Rham complex]]. 

=--

+-- {: .num_remark }
###### Remark

Notice the [relation to complex cohomology](holomorphic+de+Rham+complex#RelationToComplexCohomology) given by

$$
  H^k(X,\mathbb{C}) \simeq H^k(X,\Omega^\bullet_X)
  \,.
$$

=--

+-- {: .num_remark }
###### Remark


The [[holomorphic de Rham complex]] is naturally [[filtered object|filtered]] by degree with the $p$th filtering stage being

$$
  F^p \Omega^\bullet_X
  \coloneqq
  (0 \to \cdots \to \Omega^p_X \stackrel{\partial}{\longrightarrow}
   \Omega^{p+1} \stackrel{\partial}{\longrightarrow} \cdots)
  \,.
$$

Notice that here $\Omega^p$ is still regarded as sitting in degree $-p$, one just replaces by 0 in the holomorphic de Rham complex the groups of differential forms of degree less than $p$.

=--

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

When the compact [[complex manifold]] $X$ happens to have the structure of a [[Kähler manifold]] then the [[Frölicher spectral sequence]] degenerates at the $E_1$ page which implies that def. \ref{HodgeFiltrationForComplexSpace} coincides with the traditional definition via [[harmonic differential forms]], def. \ref{TraditionalHodgeFiltration}:

$$
  \underset{k-q \geq p}{\oplus}
  H^{k-q,q}(X)
  \simeq
  im
  \left(
    H^k(X, F^p \Omega^\bullet_X)
    \to 
    H^k(X, \Omega^\bullet_X)
  \right)
  \,.
$$

=--

(e.g. [Voisin 02, remark 8.29](#Voisin02), [Voisin, 1.1.2](#Voisin) [Peters-Steenbrink 08, prop 2.22](#PetersSteenbrink08)).

+-- {: .num_remark #FrolicherEquivalenceInComponents}
###### Remark

The equivalence in theorem \ref{HodgeFiltrationForComplexSpaceReproducesKaehlerHodgeStructure} is exhibited by the following morphism.

Write  

$$
  tot(\Omega^{\bullet \geq p, \bullet}, \mathbf{d}= \partial + \bar \partial)
$$ 

for the holomorphically truncated [[de Rham complex]], as indicated, thought of as the [[total complex]] of the [[Dolbeault complex|Dolbeault]] [[double complex]]

$$
  \array{
    \Omega^{p,0} &\stackrel{\bar \partial}{\to}& \Omega^{p-1,1} &\stackrel{\bar \partial}{\to}& \cdots
    \\
    \downarrow^{\mathrlap{\partial }}
    &&
    \downarrow^{\mathrlap{\partial }}
    \\
    \Omega^{p+1,0} &\stackrel{\bar \partial}{\to}& \Omega^{p,1} &\stackrel{\bar \partial}{\to}& \cdots
    \\
    \downarrow^{\mathrlap{\partial }}
    &&
    \downarrow^{\mathrlap{\partial }}
    \\
    \vdots && \vdots
  }
  \,.
$$

Since this is in each row the [[Dolbeault resolution]] of the given sheaf of [[holomorphic differential forms]], this total complex is indeed [[quasi-isomorphism|quasi-isomorphic]] to the (truncated) [[holomorphic de Rham complex]]. 

The total complex is in degree $-k$ given by
$\underset{k-q \geq p}{\oplus} \Omega^{k-q, q}$
and hence globally defined closed $(k-q \geq p,q)$-forms naturally inject into

$$
  H^k(X, tot(\Omega^{\bullet\geq p, \bullet}, \mathbf{d} = \partial + \bar \partial) )
  \simeq
  H^0(X,tot(\Omega^{\bullet\geq p, \bullet}, \mathbf{d} = \partial + \bar \partial)[-k])
  \,.
$$

Therefore given a representative $\alpha \in \Omega^{p,q}_{cl}(X)$ of $[\alpha] \in H^{p,q}(X)$ it is canonically sent along

$$
  \underset{k-q\geq p}{\oplus} \Omega^{p,q}_{cl}(X)
  \simeq
  \underset{k-q\geq p}{\oplus} 
   H^0(X, \Omega^{p,q}_{cl})
  \to
  H^0(X,tot(\Omega^{\bullet\geq p, \bullet}, \mathbf{d} = \partial + \bar \partial)[-k])
  \,.
$$

This map exhibits the equivalence in theorem \ref{HodgeFiltrationForComplexSpaceReproducesKaehlerHodgeStructure} (e.g. [Voisin, section 1.1.2](#Voisin)).

Dually, 

$$
  \Omega_{hol}^{\leq k}
  \simeq
  tot(  \Omega^{\bullet \leq k, \bullet})
  \,.
$$

This plays a role in the discussion of [[intermediate Jacobians]], 
where for $dim_{\mathbb{C}}(X)= k+1$ we have

$$
  H^{2k+1}(X,\mathbb{R})
  \simeq
  H^{2k+1}(X,\mathbb{C}) / F^{k+1} H^{2k+1}(X,\mathbb{C})
  \simeq
  H^{2k+1}(X, \Omega_{hol}^{\bullet \leq k})
  \,.
$$

Here a real differential $(2k+1)$-form

$$
  \alpha 
  = 
  \overline{\alpha^{0,2k+1}}
  +
  \overline{\alpha^{1, 2k}}
  + 
  \cdots
  +
  \alpha^{1, 2k}
  + 
  \alpha^{0,2k+1}
$$

injects via its pieces in 

$$
  \Omega^{p \leq k, 2k+1-p}(X)
  \simeq
  H^0(X, \Omega^{p \leq k, 2k+1-p})
  \to
  H^0(X, tot(\Omega^{\bullet \leq k, \bullet})[-k])
  \simeq
  H^k(\Omega_{hol}^{\bullet\leq k})
  \,.
$$


=--

### Generally on an abelian group
 {#OnAnAbelianGroup}

+-- {: .num_defn #HodgeStructureOfWeightk}
###### Definition

For $H_{\mathbb{Z}}$ an [[abelian group]], a _Hodge structure_ 
of _weight_ $k \in \mathbb{Z}$ on $H_{\mathbb{Z}}$ is a [[direct sum]] decomposition of its [[complexification]]

$$
  H_{\mathbb{C}}\coloneqq H_{\mathbb{Z}} \otimes_{\mathbb{Z}} \mathbb{C}
$$

into [[complex vector spaces]] $H^{p,q}$ with $p +q = k$ of the form

$$
  H_{\mathbb{C}} \simeq \underset{p+q = k}{\oplus} H^{p,q}
$$

such that $H^{q,p}$ is the [[complex conjugation|complex conjugate]] of $H^{p,q}$:

$$
  H^{p,q} = \overline{H^{q,p}}
  \,.
$$
This is an equality of the underlying sets of the complex vector spaces.
=--

With this the above def. \ref{TraditionalHodgeFiltration} has the following verbatim generalization

+-- {: .num_defn #GeneralHodgeFiltration}
###### Definition

Given a Hodge structure $H_{\mathbb{Z}}, \{H^{p,q}\}$ of weight $k$, def. \ref{HodgeStructureOfWeightk}, then  the associated _Hodge filtration_ on $H_{\mathbb{C}}$ is the [[filtered complex]] structure given by the [[direct sum]]


$$
  F^p H_{\mathbb{C}}
   \coloneqq
  \underset{k-q \geq p}{\oplus}
  H^{k-q,q}
  \,.
$$

=--



## Related concepts

* [[Hodge theory]], 

  [[nonabelian Hodge theory]], [[noncommutative Hodge theory]]

* [[Hodge symmetry]]

* [[Hodge cycle]]

* [[Hodge cohomology]]

* [[intermediate Jacobian]]

* [[Lefschetz decomposition]]

## References

Textbook accounts include

* {#Voisin02} [[Claire Voisin]], section 7 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

* {#Voisin} [[Claire Voisin]], _Hodge theory and the topology of compact K&#228;hler and complex projective manifolds_ ([pdf](http://www.math.columbia.edu/~thaddeus/seattle/voisin.pdf))


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

[[!redirects Hodge filtering]]
[[!redirects Hodge filterings]]

[[!redirects variation of Hodge structure]]
[[!redirects variation of Hodge structures]]
[[!redirects variations of Hodge structure]]
[[!redirects variations of Hodge structures]]

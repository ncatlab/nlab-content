
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _$G_2$-structure_ on a [[manifold]] of [[dimension]] 7 is a choice of [[reduction of the structure group]] of the [[tangent bundle]] along the inclusion of [[G2]] into $GL(7)$.

Given that $G_2$ is the [[subgroup]] of the [[general linear group]] on the [[Cartesian space]] $\mathbb{R}^7$ which preserves the [[associative 3-form]] on $\mathbb{R}^7$, a $G_2$ structre is a higher analog of an  [[almost symplectic structure]] under lifting from [[symplectic geometry]] to [[2-plectic geometry]] ([Ibort](#Ibort)).

A _$G_2$-manifold_ is a manifold equipped with an "integrable" or "parallel" $G_2$-structure. This is equivalently a [[Riemannian manifold]] of [[dimension]] 7 with [[special holonomy]] group being the [[exceptional Lie group]] [[G2]]. 

$G_2$-manifolds may be understood as 7-dimensional analogs of real 6-dimensional [[Calabi-Yau manifolds]].

## Definition

### $G_2$-structure

+-- {: .num_defn #G2Structure}
###### Definition

For $X$ a [[smooth manifold]] of [[dimension]] $7$ a **$G_2$-structure** on $X$ is a [[G-structure]] for $G = $ [[G2]] $\hookrightarrow GL(7)$.

=--

+-- {: .num_remark #CanonicalRiemannianMetric}
###### Remark

A $G_2$-structure in particular implies an [[orthogonal structure]], hence a [[Riemannian metric]].


=--

### $G_2$-holonomy

+-- {: .num_defn #G2manifold}
###### Definition

A manifold equipped with a $G_2$-structure $\omega$, def. \ref{G2Structure}, is called a **$G_2$-manifold** if $\omega$ is "parallel" or "integrable" in that 

1. $d \omega = 0$ 

1. $d \star \omega = 0$

(where $d$ is the [[de Rham differential]] and $\star$ is the [[Hodge star operator]] of the canonical [[Riemannian metric]] of remark \ref{CanonicalRiemannianMetric}).

=--

For instance ([Joyce, p. 4](#Joyce)).


The [[holonomy]] of the [[Levi-Civita connection]] on a $G_2$-manifold is contained in $G_2$.

### Weak $G_2$-holonomy
 {#WeakG2Holonomy}

There is a useful weakened notion of $G_2$-holonomy. 

+-- {: .num_defn #WeakG2Holonomy}
###### Definition

A 7-dimensional manifold is said to be of _weak $G_2$-holonomy_ if it carries a 3-form $\omega$ with the relation of def. \ref{G2manifold} generalized to

$$
  d \omega = \lambda \star \omega
$$

and hence

$$
  d \star \omega = 0
$$

for $\lambda \in \mathbb{R}$. For $\lambda = 0$ this reduces to strict $G_2$-holonomy, by \ref{G2manifold}. 

=--

(See for instance ([Bilal-Derendinger-Sfetsos 02](#BilalDerendingerSfetsos), [Bilal-Metzger 03](#BilalMetzger03)).)



## Properties

### Existence

+-- {: .num_prop }
###### Proposition

A 7-manifold admits a $G_2$-structure, def. \ref{G2Structure}, precisely if it admits a [[spin structure]].

=--

### Metric structure

The canonical [[Riemannian metric]] $G_2$ manifold is [[Ricci tensor|Ricci flat]]. More generally a manifold of weak $G_2$-holonomy, def. \ref{WeakG2Holonomy}, with weakness parameter $\lambda$ is an [[Einstein manifold]] with [[cosmological constant]] $\lambda$. 

## Applications

### In supergravity 

In [[string phenomenology]] [[model (in particle phyiscs)|models]] obtained from [[Kaluza-Klein mechanism|compactification]] of [[11-dimensional supergravity]]/[[M-theory on G2-manifolds]] (see for instance [Duff](#Duff)) can have attractive [[phenomenology|phenomenological]] properties, see for instance the _[[G2-MSSM]]_. 

## Related concepts

[[!include special holonomy table]]

* [[Hitchin functional]]

* [[M-theory on G2-manifolds]], [[G2-MSSM]]

* [[topological M-theory]], [[topological membrane]]

* [[generalized G2-manifold]]

* [[Calabi-Yau manifold]]

* [[exceptional generalized geometry]]

## References

### General

The concept goes back to 

* E. Bonan, (1966), _Sur les vari&#233;t&#233;s riemanniennes &#224; groupe d'holonomie G2 ou Spin(7)_, C. R. Acad. Sci. Paris 262: 127&#8211;129.

Non-compact $G_2$-manifolds were constructed in

* [[Robert Bryant]], ; S.M. Salamon,  (1989), _On the construction of some complete metrics with exceptional holonomy_, Duke Mathematical Journal 58: 829&#8211;850.

[[compact topological space|Compact]] $G_2$-manifolds were first found in 

* {#Joyce}[[Dominic Joyce]], _Compact Riemannian 7-manifolds with holonomy $G_2$_, Journal of Differential Geometry vol 43, no 2 ([Euclid](https://projecteuclid.org/euclid.jdg/1214458109))
 
* [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford Mathematical Monographs, Oxford University Press (2000)

Surveys include

* Spiro Karigiannis, _What is... a $G_2$-manifold_ ([pdf](http://www.ams.org/notices/201104/rtx110400580p.pdf))

* Spiro Karigiannis, _$G_2$-manifolds -- Exceptional structures in geometry arising from exceptional algebra_ ([pdf](http://www.math.uwaterloo.ca/~karigian/talks/waterloo.pdf)) 


* [[Robert Bryant]], _Some remarks on $G_2$-structures_, Proceedings of the 12th G&#246;kova Geometry-Topology Conference pp. 75-109 [pdf](http://gokovagt.org/proceedings/2005/ggt05-bryant.pdf)


The relation to [[multisymplectic geometry]]/[[2-plectic geometry]] is mentioned explicitly in 

* {#Ibort} Alberto Ibort, _Multisymplectic geometry: generic and exceptional_, _[Proceedings of the IX Fall workshop on geometry and physics](http://rsme.es/public/publi3.htm)_ ([[IbortMultisymplectic.pdf:file]])
 

(but beware of some mistakes in that article...)

For more see the references at _[[exceptional geometry]]_.
 


### Application in supergravity

The following references discuss the role of $G_2$-manifolds in [[M-theory on G2-manifolds]]:

* [[Mike Duff]], _M-theory on manifolds of G2 holonomy: the first twenty years_ ([arXiv:hep-th/0201062](http://arxiv.org/abs/hep-th/0201062))
 {#Duff}

A survey of the corresponding [[string phenomenology]] for [[M-theory on G2-manifolds]] (see there for more) is in

* [[Bobby Acharya]], _$G_2$-manifolds at the CERN Large Hadron collider and in the Galaxy_, talk at _$G_2$-days_ (2012) ([pdf](http://www.mth.kcl.ac.uk/~tbmadsen/acharya.pdf))

Weak $G_2$-holonomy is discussed in

* [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 {#BilalDerendingerSfetsos}

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger, _Compact weak $G_2$-manifolds with conical singularities_ ([arXiv:hep-th/0302021](http://arxiv.org/abs/hep-th/0302021))

* {#HouseMicu04} Thomas House, Andrei Micu, _M-theory Compactifications on Manifolds with $G_2$ Structure_ ([arXiv:hep-th/0412006](http://arxiv.org/abs/hep-th/0412006))

For more on this see at _[[M-theory on G2-manifolds]]_

[[!redirects G2 manifolds]]
[[!redirects G2-manifold]]
[[!redirects G2-manifolds]]

[[!redirects G2 structure]]
[[!redirects G2-structure]]
[[!redirects G2 structures]]
[[!redirects G2-structures]]

[[!redirects weak G2-holonomy]]
[[!redirects weak G2 holonomy]]
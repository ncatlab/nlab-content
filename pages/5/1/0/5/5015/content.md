

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #PlainDefinition}
###### Definition

A [[topological groupoid]] or [[Lie groupoid]] $C$ is called an **&#233;tale groupoid** if the [[domain|source]]-map $s : Mor C \to Obj C$ is a [[local homeomorphism]] or [[local diffeomorphism]], respectively, and hence exhibits the space of morphisms as an [[étale space]] over the space of objects.

=--

+-- {: .num_remark}
###### Remark

In the situation of def. \ref{PlainDefinition} it follows that all the other structure maps ([[codomain|target]], [[identity]], [[composition]]) are also local homeomorphisms, resp. local diffeomorphisms.

This means that an &#233;tale groupoid is equivakentlly [[internal groupoid]] in the [[category]] whose objects are [[topological spaces]]/[[smooth manifold]]s and whose [[morphisms]] are local homeomorphisms/diffeomorphisms.

=--

+-- {: .num_remark}
###### Remark

Definition \ref{PlainDefinition} is not invariant under the general notion of [[equivalence]] of Lie groupoids, the equivalence between them regarded as [[smooth groupoids]], specifically as [[differentiable stacks]] ("[[Morita equivalence]]"). 

But it does make sense to take an **&#233;tale smooth groupoid** to be a [[smooth groupoid]]/[[differentiable stack]] which is equivalent, as such, to, hence is presented by an &#233;tale Lie groupoid as in def. \ref{PlainDefinition}. 
This notion has been called **folitation groupoid** in ([Crainic-Moerdijk 00](#CrainicMoerdijk)).
    
=--

The following characterizes foliation groupoids

+-- {: .num_theorem}
###### Theorem

For a [[Lie groupoid]] $\mathcal{G}_\bullet$ the following are equivalent

1. $\mathcal{G}$ is a foliation groupoid, hence is equivalent, as a [[differentiable stack]] to an &#233;tale groupoid as in def. \ref{PlainDefinition};

1. The [[Lie algebroid]] $(\mathfrak{g},\mathcal{G}_0)$ which corresponds to $\mathcal{G}$ under [[Lie differentiation]] has an [[injection|injective]] [[anchor map]];

   hence the [[orbits]] of $\mathcal{G}$ form the [[leaves]] of a [[foliation]], the foliation whose leaves are tangent to the vectors in the image of this anchor map;

1. All [[isotropy groups]] of $\mathcal{G}_\bullet$ are [[discrete groups]].

=--

This is ([Crainic-Moerdijk 00, theorem 1](#CrainicMoerdijk)).

## Properties

### Cohomology and homology

In the literature one finds, roughly speaking, two different approaches to the study of &#233;tale groupoids. One approach is based on the construction of the convolution algebras associated to an &#233;tale groupoid, in the spirit of Connes' [[noncommutative geometry]], and involves the study of [[cyclic homology|cyclic]] and [[Hochschild homology]] and [[Hochschild cohomology|cohomology]] of these algebras. The other approach uses methods of algebraic topology such as the construction of the [[classifying space]] of an
&#233;tale groupoid and its [[abelian sheaf cohomology|(sheaf) cohomology groups]].

### Characterization by convolution Hopf algebroids (Gelfand duality)
 {#GelfandDuality}

The [[groupoid convolution algebra]] $C^\ast(\mathcal{G}_\bullet)$ of a [[Lie groupoid]] with its canonical [[atlas]] remembered has the structure of a [[Hopf algebroid]]. 
In ([Mr&#269;un 99](#Mrcun99), [Kali&#353;nik-Mr&#269;un 07](#KalisnikMrcun07)) &#233;tale Lie groupoids are characterized dually by their Hopf algebroids  (a refinement of [[Gelfand duality]] to [[noncommutative topology]]).

### Characterization by site of manifolds and &#233;tale maps

+-- {: .num_prop}
###### Proposition

The [[2-category]] of [[étale stacks]] with [[étale maps]] between them is equivalent to the [[2-topos]] over the [[site]] of [[smooth manifolds]] with [[local diffeomorphisms]] between them

=--

([Carchedi 12, therem 3.4, corollary 3.3](Carchedi12))

+-- {: .num_prop}
###### Proposition

A [[smooth stack]] is an &#233;tale stack precisely if it is in the [[essential image]] of the [[left Kan extension]] along the non-full inclusion of [[sites]]

$$
  SmthMfd^{et} \to SmthMfd
$$

of [[smooth manifolds]], with [[local diffeomorphisms]] on the left and all [[smooth functions]] on the right.

=--

([Carchedi 12, therem 3.5, corollary 3.4](Carchedi12))



## Examples

&#201;tale groupoids arise naturally as models for [[leaf spaces]] of [[foliations]], for [[orbifold]]s, and for [[orbit spaces]] of [[discrete group]] [[actions]].


* Every [[topological space]] may be regarded as an &#233;tale groupoid with only identity morphisms.

* For $X$ a [[topological space]] and $\Gamma$ a [[discrete group]] with a continuous [[action]] $X \times \Gamma \to X$ on $X$, the [[action groupoid]] $X//\Gamma$ is &#233;tale.

* The [[Haefliger groupoid]] $\Gamma^q$ has the [[Cartesian space]] $\mathbb{R}^q$ as its space of objects. A [[morphism]] $x \to y$ is a [[germ]] of a [[diffeomorphism]] $(\mathbb{R}^q,x) \to (\mathbb{R}^q, y)$.

  This groupoid, and its [[geometric realization]] play a central role in [[foliation theory]].

* Every [[orbifold]] is an &#233;tale [[Lie groupoid]].

## Related concepts

* [[étale space]]

* [[orbifold]], [[Deligne-Mumford stack]]

* [[étale ∞-groupoid]]

* [[proper Lie groupoid]], [[effective Lie groupoid]]

## References

A standard textbook account is section 5.5. of 

* [[Ieke Moerdijk]], [[Janez Mr?un]], _[[Introduction to foliations and Lie groupoids]]_, Cambridge (2003)

The relation between &#233;tale groupoid and [[foliations]] is analyzed in detail in 

* [[Marius Crainic]], [[Ieke Moerdijk]], _Foliation groupoids and their cyclic homology_ ([arXiv:math/0003119](http://arxiv.org/abs/math/0003119))
 {#CrainicMoerdijk}
  

See also at _[[orbifold]]_ for basic and introductory literature. 

Further discussion of &#233;tale groupoids and their properties includes

* [[Marius Crainic]], [[Ieke Moerdijk]], _A Homology Theory for &#201;tale groupoids_ ([journal](http://www.math.uiuc.edu/K-theory/0284/))

* [[David Carchedi]], _Sheaf Theory for &#201;tale Geometric Stacks_ ([arXiv:1011.6070](http://arxiv.org/abs/1011.6070))

* {#Carchedi12} [[David Carchedi]], section 2.2, section 3 of _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))

  

The [[groupoid convolution algebra|convolution]]-[[Hopf algebroids]] of &#233;tale Lie groupoids have been characterized in

* [[Janez Mr?un]], _On spectral representation of coalgebras and Hopf algebroids_ ([arXiv:math/0208199](http://arxiv.org/abs/math/0208199))  
 {#Mrcun99}

* [[Jure Kali?nik]], [[Janez Mr?un]], _Equivalence between the Morita categories of etale Lie groupoids and of locally grouplike Hopf algebroids_ ([arXiv:math/0703374](http://arxiv.org/abs/math/0703374))
 {#KalisnikMrcun07}



[[!redirects étale groupoids]]

[[!redirects etale groupoid]]
[[!redirects etale groupoids]]

[[!redirects étale Lie groupoid]]
[[!redirects étale Lie groupoids]]

[[!redirects etale Lie groupoid]]
[[!redirects etale Lie groupoids]]

[[!redirects foliation groupoid]]
[[!redirects foliation groupoids]]

[[!redirects étale stack]]
[[!redirects étale stacks]]

[[!redirects etale stack]]
[[!redirects etale stacks]]




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial Quantum Field Theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

_Extended quantum field theory_ (or _multi-tiered quantum field theory_) is the fully [[local quantum field theory|local]] formulation of [[functorial quantum field theory]], stated using [[higher category theory]]

Whereas a

* [[category theory|1-categorical]] [[functorial field theory]] may be regarded as a rule that allows one to compute invariants $Z(\Sigma)$ assigned to $d$-dimensional [[manifold]]s by cutting these manifolds into a sequence $\{\Sigma_i\}$ of $d$-dimensional composable [[cobordism]]s with $(d-1)$-dimensional boundaries $\partial \Sigma_i$, e.g.  $\Sigma = \Sigma_2 \coprod_{\partial \Sigma_1 = \partial \Sigma_2} \Sigma_1$, then assigning quantities $Z(\Sigma_i)$ to each of these and then composing these quantities in some way, e.g. as $Z(\Sigma) = Z(\Sigma_2)\circ Z(\Sigma_1)$;

we have that

* in extended [[functorial field theory]] $Z(\Sigma)$ may be computed by decomposing $\Sigma$ into $d$-dimensional pieces with piecewise smooth boundaries, whose boundary strata are of arbitrary codimension $k$.

For that reason extended functorial field theory is also sometimes called **local** or **localized** functorial field theory. In fact, the notion of locality in [[quantum field theory]] is precisely this notion of locality. And, as also discussed at [[FQFT]], this higher dimensional version of locality is naturally encoded in terms of [[higher category theory|n-functoriality]] of $Z$ regarded as a functor on a [[higher category theory|higher category]] of [[cobordism]]s.



##  Definition

### The category of extended cobordisms

The definition of a $j$-cobordism is recursive. A $(j+1)$-cobordism between $j$-cobordisms is a [[compact space|compact]] [[orientation|oriented]] $(j+1)$-dimensional [[smooth manifold]] with corners whose the boundary is the [[disjoint union]] of the target $j$-cobordism and the orientation reversal of the source $j$-cobordism.  (The base case of the recursion is the [[empty set]], thought of as a $(-1)$-dimensional manifold.)

$n Cob_d$ is an $n$-category with smooth compact oriented $(d-n)$-manifolds as objects and cobordisms of cobordisms up to $n$-cobordisms, up to diffeomorphism, as morphisms.

There are various suggestions with more or less detail for a precise definition of a higher category $n Cob_n$ of fully extended $n$-dimensional cobordisms. 

A very general (and very natural) one consists in taking a further step in categorification: one takes $n$-cobordisms as $n$-morphisms and smooth homotopy classes of diffeomorphisms beween them as $(n+1)$-morphisms. Next one iterates this; see details at [[(∞,n)-category of cobordisms]].

See 

* [[extended cobordism]].

### Extended functorial field theory

Fix a [[base ring]] $R$, and let $C$ be the [[symmetric monoidal category|symmetric monoidal]] $n$-category of $n$-$R$-modules.

An $n$-extended $C$-valued functorial field theory of dimension $d$ is a symmetric $n$-tensor functor $Z: n Cob_d \rightarrow C$ that maps

* smooth compact oriented $d$-manifolds to elements of $R$

* smooth compact oriented $(d-1)$-manifolds to $R$-modules

* cobordisms of smooth compact oriented $(d-1)$-manifolds to $R$-linear maps between $R$-modules

* smooth compact oriented $(d-2)$-manifolds to $R$-linear [[additive categories]]

* cobordisms of smooth compact oriented $(d-2)$-manifolds to functors between $R$-linear categories

* etc ...

* smooth compact oriented $(d-n)$-manifolds to $R$-linear $(n-1)$-categories

* cobordisms of smooth compact oriented $(d-n)$-manifolds to $(n-1)$-functors between $R$-linear $(n-1)$-categories

with compatibility conditions and gluing formulas that must be satisfied... For instance, since the functor $Z$ is required to be monoidal, it sends monoidal units to monoidal units. Therefore, the $d$-dimensional [[vacuum]] is mapped to the unit element of $R$, the $(d-1)$-dimensional vacuum to the $R$-module $R$, the $(d-2)$-dimensional vacuum to the category of $R$-modules, etc.

Here $n$ can range between $0$ and $d$. This generalizes to an arbitrary symmetric monoidal category $C$ as codomain category.





## Examples

### Classes of examples by dimension

$n=1$ gives ordinary [[TQFT]].

The most common case is when $R = \mathbb{C}$ (the [[complex numbers]]), giving unitary ETQFT.

The most common cases for $C$ are

*  $C = n Hilb(R)$, the category of $n$-[[n-Hilbert space|Hilbert spaces]] over a topological field $R$. As far as we know this is only defined up to $n=2$.

*  $C = n Vect(R)$, the category of $n$-[[n-vector space|vector spaces]] over a field $R$.

*  $C = n Mod(R)$, the (conjectured?) category of $n$-[[n-module|modules]] over a commutative ring $R$.

3d: [[Turaev-Viro model]]

### Generic examples

By the [[cobordism hypothesis]]-theorem every [[fully dualizable object]] in a symmetric monoidal $(\infty,n)$-category with duals provides an example.

### Specific examples

* [[Levin-Wen model]]

* [Chern-Simons theory as a fully extended TQFT](Topological+Quantum+Field+Theories+from+Compact+Lie+Groups#3dCSFullyExtended)

* ...many more...

See also at _[[TCFT]]_.


## Properties

### Construction of ETQFT's

* By generators and relations

* By path integrals (this is Daniel Freed's approach)

* By modular tensor n-categories?

### Classification of ETQFT's

Assume $Z: n Cob_d \rightarrow n Vect(R)$ is an extended TQFT. Since $Z$ maps the $(d-1)$-dimensional vacuum to $R$ as an $R$-vector space, by functoriality $Z$ is forced to map a $d$-dimensional closed manifold to an element of $R$. 
Iterating this argument, one is naturally led to conjecture that, under the correct categorical hypothesis, the behaviour of $Z$ is entirely determined by its behaviour on $(d-n)$-dimensional manifolds. See details at [[cobordism hypothesis]].

### Relation of ETQFT to AQFT

See 

* [[topological chiral homology]].

also

* _[AQFT from n-functorial QFT](http://arxiv.org/abs/0806.1079)_.

## Related concepts

* [[local quantum field theory]]

* [[extended Lagrangian]]

* [[twisted functorial field theory]]

More on extended QFTs is also at:

* [[FQFT]]

[[!include Isbell duality - table]]


## References

### General

* Ruth J. Lawrence, _Triangulations, categories and extended topological field theories_. Quantum topology, 191–208, Ser. Knots Everything, 3, World Sci. Publ., River Edge, NJ, 1993.  [doi](https://doi.org/10.1142/9789812796387_0011).
Presented at the AMS Meeting 876, held in Dayton, Ohio, on October 31, 1992.

* [[Daniel S. Freed]], _Higher Algebraic Structures and Quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

* [[Daniel S. Freed]], _Quantum Groups from Path Integrals_ ([arXiv:q-alg/9501025](http://arxiv.org/abs/q-alg/9501025))

* [[John Baez]] and [[James Dolan]], _Higher-dimensional Algebra and Topological Quantum Field Theory_  ([arXiv:q-alg/9503002](http://arxiv.org/abs/q-alg/9503002))

* [[Daniel S. Freed]], _Remarks on Chern-Simons theory_, [arXiv:0808.2507](https://arxiv.org/abs/0808.2507).

* [[Jacob Lurie]],  _[[On the Classification of Topological Field Theories]]_. [arXiv](http://arxiv.org/abs/0905.0465)

* [[Shawn X. Cui]], *Higher Categories and Topological Quantum Field Theories*, Quantum Topology **10** 4 (2019) 593-676 &lbrack;[arXiv:1610.07628] (https://arxiv.org/abs/1610.07628), [doi:10.4171/QT/128](https://doi.org/10.4171/QT/128)&rbrack;


With an eye towards the full extension of [[Chern-Simons theory]]:

* [[Daniel S. Freed]], _Remarks on Fully Extended 3-Dimensional Topological Field Theories_ (2011) ([pdf](http://www.ma.utexas.edu/users/dafr/stringsmath_np.pdf))

* [[Daniel S. Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]],  _[[Topological Quantum Field Theories from Compact Lie Groups]]_ , in P. R. Kotiuga (ed.) _A celebration of the mathematical legacy of Raoul Bott_ AMS (2010) ([arXiv](http://arxiv.org/abs/0905.0731))

Review:

* [[Luigi Alfonsi]], §6 in: *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;


For TQFTs appearing in [[solid state physics]] in the context of [[topological order]] (see also at *[[K-theory classification of topological phases of matter]]*):

* {#FreedMoore12} [[Daniel S. Freed]], [[Gregory Moore]], _Twisted equivariant matter_ ([arxiv/1208.5055](http://arxiv.org/abs/1208.5055))

  > (uses [[equivariant K-theory]] to classify free fermion gapped phases with symmetry)

* {#Freed14} [[Daniel S. Freed]], _Short-range entanglement and invertible field theories_ ([arXiv:1406.7278](http://arxiv.org/abs/1406.7278))

* [[Daniel Freed]], [[Michael Hopkins]], *Reflection positivity and invertible topological phases*, Geometry & Topology ([arXiv:1604.06527](https://arxiv.org/abs/1604.06527))

* [[Davide Gaiotto]], [[Theo Johnson-Freyd]], *Condensations in higher categories* ([arXiv:1905.09566](https://arxiv.org/abs/1905.09566))

For its relation to the notion of [[generalized symmetries]]: 

* [[Daniel S. Freed]], [[Gregory W. Moore]], [[Constantin Teleman]], *Topological symmetry in quantum field theory* &lbrack;[arXiv:2209.07471](https://arxiv.org/abs/2209.07471)&rbrack;

The case of [[Rozansky-Witten theory]]:

* [[Lorenzo Riva]], *Higher categories of push-pull spans, I: Construction and applications* &lbrack;[arXiv:2404.14597](https://arxiv.org/abs/2404.14597)&rbrack;

* [[Germán Stefanich]]: *Categorification of sheaf theory* &lbrack;[arXiv:2511.09553](https://arxiv.org/abs/2511.09553)&rbrack;

For *geometric* (non-topological) extended field theory:

* {#GradyPavlov20} [[Daniel Grady]], [[Dmitri Pavlov]], *Extended field theories are local and have classifying spaces* &lbrack;[arXiv:2011.01208](https://arxiv.org/abs/2011.01208)&rbrack;


* {#GradyPavlov21} [[Daniel Grady]], [[Dmitri Pavlov]], *The geometric cobordism hypothesis* &lbrack;[arXiv:2111.01095](https://arxiv.org/abs/2111.01095)&rbrack;

Review:

* [[Dmitri Pavlov]], *The geometric cobordism hypothesis*, talk at *[QFT and Cobordism](https://nyuad.nyu.edu/en/events/2023/march/quantum-field-theories-and-cobordisms.html)*, [[CQTS]] (Mar 2023) &lbrack;[pdf](https://dmitripavlov.org/nyuad.pdf), [[Pavlov-GCHatCQTS.pdf:file]], [web](Center+for+Quantum+and+Topological+Systems#PavlovMar2023), video: [YT](https://www.youtube.com/watch?v=n6Eog_z82eA)&rbrack;

* Alexander Zahrer: *Smooth Functorial Field Theory and the Geometric Cobordism Hypothesis*, MSc thesis, Vienna (2023) &lbrack;[utheses:67464](https://utheses.univie.ac.at/detail/67464#), <a href="https://alexanderzahrer.github.io/maths/Notes_GCH%20(1).pdf">pdf</a>&rbrack;




[[!include D=6 N=(2,0) SCFT as an extended functorial field theory -- references]]



[[!redirects extended topological quantum field theory]]

[[!redirects EQFT]]
[[!redirects extended TQFT]]

[[!redirects extended quantum field theory]]
[[!redirects extended QFT]]

[[!redirects extended quantum field theories]]
[[!redirects extended topological quantum field theories]]
[[!redirects extended QFTs]]

[[!redirects extended topological field theory]]
[[!redirects extended topological field theories]]
[[!redirects extended field theory]]
[[!redirects extended field theories]]

[[!redirects multi-tiered field theory]]
[[!redirects multi-tiered field theories]]

[[!redirects multi-tiered quantum field theory]]
[[!redirects multi-tiered quantum field theories]]

[[!redirects extended TQFTs]]

[[!redirects extended TFT]]
[[!redirects extended TFTs]]

[[!redirects extended functorial field theory]]
[[!redirects extended functorial field theories]]

[[!redirects fully extended TQFT]]
[[!redirects fully extended TQFTs]]


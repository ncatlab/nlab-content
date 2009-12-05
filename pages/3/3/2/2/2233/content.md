<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>

#Idea#

_Extended quantum field theory_ (or _many-tiered quantum field theory_) is the [[higher category theory|higher categorical]] version of [[FQFT|functorial quantum field theory]]:

whereas 

* [[category theory|1-categorical]] [[TQFT]] may be regarded as a rule that allows one to compute topological invariants $Z(\Sigma)$ assigned to $d$-dimensional [[manifold]]s by cutting these manifolds into a sequence $\{\Sigma_i\}$ of $d$-dimensional composable [[cobordism]]s with $(d-1)$-dimensional boundaries $\partial \Sigma_i$, e.g.  $\Sigma = \Sigma_2 \coprod_{\partial \Sigma_1 = \partial \Sigma_2} \Sigma_1$, then assigning quantities $Z(\Sigma_i)$ to each of these and then composing these quantities in some way, e.g. as $Z(\Sigma) = Z(\Sigma_2)\circ Z(\Sigma_1)$;

we have that

* in extended [[TQFT]] $Z(\Sigma)$ may be computed by decomposing $\Sigma$ into $d$-dimensional pieces with piecewise smooth boundaries, whose boundary strata are of arbitrary codimension $k$.



For that reason extended QFT is also sometimes called **local** or **localized** QFT. In fact, the notion of locality in [[quantum field theory]] is precisely this notion of locality. And, as also discussed at [[FQFT]], this higher dimensional version of locality is naturally encoded in terms of [[higher category theory|n-functoriality]] of $Z$ regarded as a functor on a [[higher category theory|higher category]] of [[cobordism]]s.

#The category of extended cobordisms#

The definition of a $j$-cobordism is recursive. A $(j+1)$-cobordism between $j$-cobordisms is a [[compact space|compact]] [[orientation|oriented]] $(j+1)$-dimensional [[smooth manifold]] with corners whose the boundary is the [[disjoint union]] of the target $j$-cobordism and the orientation reversal of the source $j$-cobordism.  (The base case of the recursion is the [[empty set]], thought of as a $(-1)$-dimensional manifold.)

$n Cob_d$ is an $n$-category with smooth compact oriented $(d-n)$-manifolds as objects and cobordisms of cobordisms up to $n$-cobordisms, up to diffeomorphism, as morphisms.

There are various suggestions with more or less detail for a precise definition of a higher category $n Cob_n$ of fully extended $n$-dimensional cobordisms. 

A very general (and very natural) one consists in taking a further step in categorification: one takes $n$-cobordisms as $n$-morphisms and smooth homotopy classes of diffeomorphisms beween them as $(n+1)$-morphisms. Next one iterates this; see details at [[(∞,n)-category of cobordisms]].

See 

* [[extended cobordism]].


#Definition#

Fix a [[base ring]] $R$, and let $C$ be the [[symmetric monoidal category|symmetric monoidal]] $n$-category of $n$-$R$-modules.

An $n$-extended $C$-valued TQFT of dimension $d$ is a symmetric $n$-tensor functor $Z: n Cob_d \rightarrow C$ that maps
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





#Examples#

$n=1$ gives ordinary [[TQFT]].

The most common case is when $R = \mathbb{C}$ (the [[complex numbers]]), giving unitary ETQFT.

The most common cases for $C$ are
*  $C = n Hilb(R)$, the category of $n$-[[n-Hilbert space|Hilbert spaces]] over a topological field $R$. As far as we know this is only defined up to $n=2$.
*  $C = n Vect(R)$, the category of $n$-[[n-vector space|vector spaces]] over a field $R$.
*  $C = n Mod(R)$, the (conjectured?) category of $n$-[[n-module|modules]] over a commutative ring $R$.

#Construction of ETQFT's#

* By generators and relations

* By path integrals (this is Daniel Freed's approach)

* By modular tensor n-categories?

#Classification of ETQFT's#

Assume $Z: n Cob_d \rightarrow n Vect(R)$ is an extended TQFT. Since $Z$ maps the $(d-1)$-dimensional vacuum to $R$ as an $R$-vector space, by functoriality $Z$ is forced to map a $d$-dimensional closed manifold to an element of $R$. 
Iterating this argument, one is naturally led to conjecture that, under the correct categorical hypothesis, the behaviour of $Z$ is enterely determined by its behaviour on $(d-n)$-dimensional manifolds. See details at [[cobordism hypothesis]].

#Relation of ETQFT to AQFT#

See Urs Schreiber, [AQFT from n-functorial QFT](http://arxiv.org/abs/0806.1079).

#Related entries#

More on extended QFTs is also at 

* [[FQFT]]

#References#

* Daniel Freed, Remarks on Chern-Simons theory

* Daniel Freed, Quantum Groups from Path Integrals 

* Daniel Freed, Higher Algebraic Structures and Quantization 

* John Baez and James Dolan, Higher-dimensional Algebra and Topological Quantum Field Theory.  [arXiv](http://arxiv.org/abs/q-alg/9503002)

* [[Jacob Lurie]],  [[On the Classification of Topological Field Theories]]  


+-- {: .query}
I changed references to bordism here into references to [[cobordisms]], since there\'s also a notion of bordism (a back-formation) as dual to cobordism, which is not what we want.  (Also Wikipedia implies that 'bordism' is a mass noun while 'cobordism' is a count noun, and these are count nouns, for what that\'s worth.)  ---Toby
=--
+-- {: .query}
_Rafael_: I obviously used a linear category in the definition as C instead of a general C. Do anyone know how to generalize it? Neither do i know the compatibility conditions and gluing formulas, any good explicit references?
=--

+-- {: .query}
_Rafael_: I am very tired because it is very late.
Please check and expand this page, i am not counting very good with my eyes half closed neither am i an expert on ETQFT.

[[Urs Schreiber]]: notice that I had a bit on extended QFT over at [[FQFT]]. Maybe some of the material needs to be merged. i have now at least added links back and forth.

_Rafael_: Yes, for the merge. I think of a subsection here **construction of ETQFTs** and a pointer to the relation between ETQFT to AQFT. I also think you are much better to include the construction of ETQFTs in **Nonabelian cocycles and their sigma model QFTs** than me.

=--


[[!redirects EQFT]]
[[!redirects extended TQFT]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An abstractly defined $n$-dimensional [[quantum field theory]] is a consistent assignment of [[state]]-space and correlators to $n$-dimensional [[cobordism]]s with certain structure (topological structure, conformal structure, Riemannian structure, etc. see [[FQFT]]/[[AQFT]]). In an _open-closed QFT_ the cobordisms are allowed to have boundaries. 

In this abstract formulation of QFT a **D-brane** is a type of data assigned by the QFT to boundaries of cobordisms. 

### In $2d$ rational CFT

A well understood class of examples is this one: among all 2-dimensional [[conformal field theory]] that case of _full rational 2d CFT_ has been understood completely, using [[FFRS-formalism]]. It is then a theorem that full 2-rational CFTs are classified by 

1. a [[modular tensor category]] $\mathcal{C}$ (to be thought of as being the category of representaitons of the [[vertex operator algebra]] of the 2d CFT);

1. a special symmetric [[Frobenius algebra]] object $A$ [[internalization|internal]] to $\mathcal{C}$.

In this formulation a type of **brane** of the theory is precisely an $A$-[[module]] in $\mathcal{C}$ (an $A$-[[bimodule]] is a [[bi-brane]] or _defect line_ ):

the 2d cobordisms with boundary on which the theory defined by $A \in \mathcal{C}$ carry as extra structure on their connected boundary pieces a label given by an equivalence class of an $A$-module in $\mathcal{C}$. The assignment of the CFT to such a cobordism with boundary is obtained by

* triangulating the cobordism, 

* labeling all internal edges by $A$

* labelling all boundary pieces by the $A$-module

* all vertices where three internal edges meet by the multiplication operation 

* and all points where an internal edge hits a moundary by the corresponding [[action]] morphism 

* and finally evaluating the resulting [[string diagram]] in $\mathcal{C}$.

So in this abstract algebraic formulation of QFT on the worldvolume, a brane is just the datum assigned by the QFT to the boundary of a cobordism. But abstractly defined QFTs may arise from [[quantization]] of [[sigma model]]s. This gives these boundary data a geometric interpretation in some space. This we discuss in the next section.

### In $2d$ TFT

Another case where the branes of a QFT are under good mathematical control is [[TCFT]]: the [[(infinity,1)-category]]-version of a 2d [[TQFT]].

Particularly the [[A-model]] and the [[B-model]] are well understood.

* the branes of the B-model ("B-branes") form the the [[stable (infinity,1)-category]] of [[chain complex]]es of [[quasicoherent sheaves]] on the target space (often considered just in terms of its [[homotopy category of an (infinity,1)-category]], the [[derived category]] of quasicoherent sheaves);

*  the branes of the A-model form the [[Fukaya category]] of the target space.



* the category of D-branes of the A-model on a symplectic [[Landau-Ginzburg model]], is a [[Fukaya-Seidel category]];

* the category of D-branes of the B-model on a complex Landau-Ginzburg model is a category of [[matrix factorization]]s.



There is also a mathematical structure called _[[string topology]]_  with D-branes. At present this is more "string inspired" than actually derived from string theory, though.

### In terms of geometric data of the $\sigma$-model background 

An abstractly defined QFT (as a consistent assignment of state spaces and propagators to cobordisms as in [[FQFT]]) may be obtained by [[quantization]] from _geometric data_ :

Sich a _[[sigma-model]] QFT_ is the [[quantization]] of an [[action functional]] on a space of maps $\Sigma \to X$ from a cobordims ("worldvolume") $\Sigma$ to some target space $X$ that may carry further geoemtric data such as a [[Riemannian metric]],  or other background [[gauge field]]s.

One may therefore try to match the geometric data on $X$ that encodes the $\sigma$-model with the algebraic data of the [[FQFT]] that results after quantization. This gives a geometric interpretation to many of the otherwise purely abstract algebraic properties of the worldvolume QFT.

It turns out that if one checks which geometric data corresponds to the $A$-modules in the above discussion, one finds that these tend to come from structures that look at least roughly like _submanifolds_ of the target space $X$. And typically these submanifolds themselves carry their own background [[gauge field]] data.

A well-understood case is the [[Wess-Zumino-Witten model]]: for this the target space $X$ is a simple [[Lie group]] $X = G$ and the background field is a [[circle n-bundle with connection|circle 2-bundle with connection]] (a [[bundle gerbe]]) on $G$, representing the background field that is known as the [[Kalb-Ramond field]].

In this case it turns out that branes for the sigma model on $X$ are given in the smplest case by conjugacy classes $D \subset G$ inside the group, and that these carry [[twisted bundle|twisted vector bundle]] with the twist given by the Kalb-Ramond background bundle. These vector bundles are known in the [[string theory]] literature as _[[Chan-Paton vector bundles]]_ . The geometric intuition is that a QFT with certain boundary condition comes form a quantization of spaces of maps $\Sigma \to G$ that are restricted to take the boundary of $\Sigma$ to these submanifolds.

More generally, one finds that the geometric data that corresponds to the branes in the algebraically defined 2d QFT is given by cocycles in the twisted [[differential K-theory]] of $G$. These may be quite far from having a direct interpretation as submanifolds of $G$.

The case of rational 2d CFT considered so far is only the best understood of a long sequence of other examples. Here the collection of all [[D-branes]] -- identified with the colleciton of all internal modules over an internal frobenius algebra, forms an ordinary [[category]].

More generally, at least for 2-dimensional [[TQFT]]s analogous considerations yield not just categories but [[stable (∞,1)-categories]] of boundary condition objects. For instance for what is called the [[B-model]] 2-d [[TQFT]] the category of [[D-branes]] is the [[derived category]] of [[coherent sheaves]] on some Calabi-Yau space.

Starting with Kontsevich's [[homological algebra]] reformulation of [[homological mirror symmetry|mirror symmetry]] the study of (derived) D-brane categories has become a field in its own right in pure mathematics.

... lots of further things to say ...


## Examples

### Various dimensions

In [[type IIA supergravity]]

* [[D0-brane]], [[D2-brane]], [[D4-brane]].

In [[type IIB supergravity]]

* [[D1-brane]], [[D3-brane]], [[D5-brane]], [[D7-brane]]

### In the WZW model

For D-branes in the [[WZW-model]] see _[WZW-model -- D-branes](Wess-Zumino-Witten+model#DBranes)_.

## Characterizations

### In terms of Dirac structures

D-branes may be identified with [[Dirac structures]] on 
a [[Courant Lie 2-algebroid]] over spacetime related to the [[type II geometry]] ([Asakawa-Sasa-Watamura](#AsakawaSasaWatamura)). See at _[[Dirac structure]]_ for more on this.

## D-brane charge

## Related concepts

* [[Chan-Paton bundle]], [[twisted bundle]], [[twisted K-theory]], [[Chan-Paton gauge field]]

* [[Freed-Witten anomaly cancellation]]

* [[Dirac-Born-Infeld action]]

* [[black brane]], [[black hole in string theory]]

* [[K-homology]], [[KK-theory]]

[[!include table of branes]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

### General

A classical text describing how the physics way to think of D-branes leads to seeing that they are objects in derived categories is

* [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv](http://arxiv.org/abs/hep-th/0403166)) 

This can to a large extent be read as a dictionary from [[homological algebra]] terminology to that of D-brane physics.

More recent similar material with the emphasis on the [[K-theory]] aspects is

* [[Richard Szabo]], _[[Szabo09.pdf:file]]_

### KK-theoretic description

Discussion of D-branes in [[KK-theory]] is reviewed in

* [[Richard Szabo]], _D-branes and bivariant K-theory_ ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))
 {#Szabo}

based on

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], 

  _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))

  _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))

  _D-branes, KK-theory and duality on noncommutative spaces_, J. Phys. Conf. Ser. 103:012004,2008 ([arXiv:0709.2128](http://arxiv.org/abs/0709.2128))
### For rational CFT

For exhaustive details on D-branes in 2-dimensional rational [[CFT]] see the references given at 

* [[FFRS-formalism]].

### For topological strings

A discussion of topological D-branes in the context of [[higher category theory]] is in

* [[Anton Kapustin]], _Topological Field Theory, Higher Categories, and Their Applications_ ([arXiv:1004.2307](http://arxiv.org/abs/1004.2307))

### Open string worldsheet Anomaly cancellation

The need for [[twisted spin^c structures]] as [[quantum anomaly]]-cancellaton condition on the [[worldvolume]] of D-branes was first discussed in

* [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_ ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))

More details are in 

* [[Anton Kapustin]], _D-branes in a topologically nontrivial B-field_ , Adv. Theor. Math. Phys.
4, no. 1, pp. 127&#8211;154 (2000), ([arXiv:hep-th/9909089](http://arxiv.org/abs/hep-th/9909089))

A clean review is provided in

* Kim Laine, _Geometric and topological aspects of Type IIB D-branes_ ([arXiv:0912.0460](http://arxiv.org/abs/0912.0460))

For more see at _[[Freed-Witten anomaly cancellation]]_.


### Relation to Dirac structures

* Tsuguhiko Asakawa, Shuhei Sasa, Satoshi Watamura, _D-branes in Generalized Geometry and Dirac-Born-Infeld Action_ ([arXiv:1206.6964](http://arxiv.org/abs/1206.6964))
 {#AsakawaSasaWatamura}


### D-brane charge

* [[Peter Bouwknegt]], _A note on equality of algebraic and geometric D-brane charge charges in WZW models_ ([pdf](http://people.physics.anu.edu.au/~drt105/papers/BR0312259.pdf))

[[!redirects D-branes]]
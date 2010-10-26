+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The term _brane_ in formal high energy [[physics]], and in particular in [[string theory]], refers to entities that one thinks of as physical objects that generalize the notion _point particles_ to higher dimensional objects.

The term derives from the word _membrane_ that was originally used to describe 2-dimensional "particles". When the need was felt to speak also about 3-, 4- and higher dimensional such "particles" the usage "3-brane", "4-brane" etc. was introduced. Ordinary particles would be 0-branes in this counting, the strings in [[string theory]] would be 1-branes and membranes themselves 2-branes.

There are two fundamentally different concrete realizations of this somewhat vague notion.

1. **D-branes** and other boundary conditions

1. **fundamental** or $\sigma$-model branes


### Boundary conditions or D-branes

#### In terms of the abstract theory on the worldvolume

An abstractly defined $n$-dimensional [[quantum field theory]] is a consistent assignment of [[state]]-space and correlators to $n$-dimensional [[cobordism]]s with certain structure (topological structure, conformal structure, Riemannian structure, etc. see [[FQFT]]). In an _open-closed QFT_ the cobordisms are allowed to have boundaries. 

In this abstract formulation of QFT a **brane** is a type of data assigned by the QFT to boundaries of cobordisms. 

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


#### In terms of the $\sigma$-model background data

An abstractly defined QFT (as a consistent assignment of state spaces and propagators to cobordisms as in [[FQFT]]) may be obtained by [[quantization]] from _geometric data_ :

Sich a _[[sigma-model]] QFT_ is the [[quantization]] of an [[action functional]] on a space of maps $\Sigma \to X$ from a cobordims ("worldvolume") $\Sigma$ to some target space $X$ that may carry further geoemtric data such as a [[Riemannian metric]],  or other background [[gauge field]]s.

One may therefore try to match the geometric data on $X$ that encodes the $\sigma$-model with the algebraic data of the [[FQFT]] that results after quantization. This gives a geometric interpretation to many of the therwise purely abstract algebraic properties of the worldvolume QFT.

It turns out that if one checks which geometric data corresponds to the $A$-modules in the above discussion, one finds that these tend to come from structures that look at least roughly like _submanifolds_ of the target space $X$. And typically these submanifolds themselves carry their own background [[gauge field]] data.

A well-understood case is the [[Wess-Zumino-Witten model]]: for this the target space $X$ is a simple [[Lie group]] $X = G$ and the background field is a [[circle n-bundle with connection|circle 2-bundle with connection]] (a [[bundle gerbe]]) on $G$, representing the background field that is known as the [[Kalb-Ramond field]].

In this case it turns out that branes for the sigma model on $X$ are given in the smplest case by conjugacy classes $D \subset G$ inside the group, and that these carry [[twisted bundle|twisted vector bundle]] with the twist given by the Kalb-Ramond background bundle. These vector bundles are known in the [[string theory]] literature as _Chan-Paton vector bundles_ . The geometric intuition is that a QFT with certain boundary condition comes form a quantization of spaces of maps $\Sigma \to G$ that are restricted to take the boundary of $\Sigma$ to these submanifolds.

More generally, one finds that the geometric data that corresponds to the branes in the algebraically defined 2d QFT is given by cocycles in the twisted [[differential K-theory]] of $G$. These may be quite far from having a direct interpretation as submanifolds of $G$.

The case of rational 2d CFT considered so far is only the best understood of a long sequence of other examples. Here the collection of all D-branes -- identified with the colleciton of all intermal modules over an internal frobenius algebra, forms an ordinary [[category]].

More generally, at least for 2-dimensional [[TQFT]]s analogous considerations yield not just categories but [[stable (∞,1)-categories]] of boundary condition objects. For instance for what is called the [[B-model]] 2-d [[TQFT]] the category of D-branes is the [[derived category]] of [[coherent sheaves]] on some Calabi-Yau space.

Starting with Kontsevich's [[homological algebra]] reformulation of [[homological mirror symmetry|mirror symmetry]] the study of (derived) D-brane categories has become a field in its own right in pure mathematics.

... lots of further things to say ...


### Fundamental or $\sigma$-model branes

In string theory one speak apart from the D-branes alsso about _fundamental branes_ . These are the objects $\Sigma$ in the $n$-dimensional [[sigma model]] themselves.

* For $n=0$ this describes the ordinary quantum mechanics of a point particle on $X$. And such point particles are the _fundamental particles_ for instance of the [[standard model of particle physics]].

* For $n=1$ this describes the quantum propagation of a [[string theory|string]], and accordingly one speaks of the _fundamental string_ or F1-brane (fundamental 1-brane).

* For $n=2$ this describes the quantum propagation of a membrane. 

* There are good indications that there is a way to describe heterotic [[string theory]] not in terms of fundamental 1-branes but in terms of the [[sigma-model]] of a fundamental 5-brane -- the [[magnetic charge|magnetic dual]] of the 1-brane in 10-dimensions. 

* etc.

#### The super-brane scan

If the worldvolume QFT of the fundamental branes (for instance the worlsheet 2d[[CFT]] of the string) is required to be a [[supersymmetric QFT]], specifically if the [[Green-Schwarz action functional]] is used only particular combinations of the dimenion $dim \Sigma = p + 1$ of the worldvolume and $D = dim X$ of [[spacetime]] are possible.

The corresponding table has been called the **brane scan**

[[branescan.gif:pic]]


## References 

### Boundary conditions / D-branes

For exhaustive details on D-branes in 2-dimensional rational [[CFT]] see the references given at 

* [[FFRS-formalism]].


A classical text describing how the physics way to think of D-branes leads to seeing that they are objects in derived categories is

* [[Paul Aspinwall], _D-Branes on Calabi-Yau Manifolds_ ([arXiv](http://arxiv.org/abs/hep-th/0403166)) 

This can to a large extent be read as a dictionary from [[homological algebra]] terminology to that of D-brane physics.

More recent similar material with the emphasis on the [[K-theory]] aspects is

* [[Richard Szabo]], _[[Szabo09.pdf:file]]_

### Fundamental branes

The "brane scan" table showing the consistent dimension pairs for the [[Green-Schwarz action functional]] was depicted in

* [[Michael Duff]], _Supermembranes: the first fifteen weeks_ CERN-TH.4797/87 ([scan](http://ccdb4fs.kek.jp/cgi-bin/img/allpdf?198708425))
{#Duff}

going back to

* A. Ach&#250;carro, J. M. Evans, Pete Townsend and D. L. Wiltshire, _Super $p$-branes_ Physics Letters B Volume 198, Issue 4, 3 (1987)

Further developments are in

More along these lines is in

* [[Michael Duff]], S. Ferrara, _Four curious supergravities_ ([arXiv](http://arxiv.org/abs/1010.3173))

See also [[division algebras and supersymmetry]].

[[!redirects branes]]
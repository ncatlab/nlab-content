+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Phyics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

> This article is about the general concept of branes. For more specific details see also also at _[[super p-brane]]_, _[[black brane]]_ and _[[D-brane]]_.

***



#Contents#
* table of contents
{:toc}

## Idea 

The term _brane_ in formal high energy [[physics]], and in particular in [[string theory]], refers to entities that one thinks of as physical objects that generalize the notion _point particles_ to higher dimensional objects.

The term derives from the word _membrane_ that was originally used to describe 2-dimensional "particles". When the need was felt to speak also about 3-, 4- and higher dimensional such "particles" the usage "3-brane", "4-brane" etc. was introduced. Ordinary particles would be 0-branes in this counting, the strings in [[string theory]] would be 1-branes and membranes themselves 2-branes.

Generally, there are two different incarnations of branes

1. **fundamental $p$-branes** (as in "[[fundamental particle]]"): these are given by [[sigma-models]] on $(p+1)$-dimensional [[worldvolumes]] describing propagation of single $p$-dimensional objects on certain [[target spacetimes]]. If these sigma-models are required to exhibit manifest [[target spacetime]] [[supersymmetry]], then they are [[Green-Schwarz sigma models]], which are classified by a "[[brane scan]]" in [[super L-infinity algebra]] [[L-infinity algebra cohomology|cohomology]];

1. **[[black branes|black p-branes]]** (as in "[[black hole]]"): these are [[soliton|solitonic]] solutions to [[field theories]], typically [[supergravity]] theories, with [[singularities]] of [[dimension]] $(p+1)$. In analogy to how a [[charged black hole]] ($p = 0$) [[source|sources]] an [[electromagnetic field]] with [[field strength]] 2-form, so black $p$-branes source $(p+2)$-form [[higher gauge fields]] and hence appear in those [[supergravity]] theories where such exists.

The idea is that these two concepts match where a [[condensate]] of fundamental $p$-branes turns into a black $p$-branes.


 
Indeed, the classical [[no-hair theorem]] matches [[fundamental particles]] (i.e. 0-branes) characterized (via the [[Wigner classification]]) by just their [[mass]], electromagnetic [[charge]] and [[angular momentum]]  to [[black hole]] solutions of pure vacuum gravity. Accordingly, it is an old suggestion ([Einstein-Infeld-Hoffmann 39](#EinsteinInfeldHoffmann39)) that fundamental particles could be identified with singular solutions of vacuum gravity.

This matching generalizes to higher dimensional $p$-branes in higher dimensional [[supergravity]] and there is an exact correspondence between fundamental [[Green-Schwarz super p-branes]] and extremal [[BPS solutions|BPS]] black brane solutions.
 
In [[string theory]] there is a third incarnation of branes, known as 

* **[[D-branes]]**: these are the admissible [[boundary conditions]] for the 2-dimensional [[sigma models]] describing [[open strings]].  

One envisions that as one passes from [[perturbative string theory]] to the [[non-perturbative effect|non-perturbative]] version of the theory ("[[M-theory]]") these [[D-branes]] show [[back-reaction]] and turn into the [[UV-completion]] of the [[black branes]] seen in the [[supergravity]] [[effective field theory]]. This relation is key in the microscopic computation of [[black hole entropy]] for [[black holes in string theory]].
 



### Boundary conditions or D-branes
 {#Dbranes}

Some words on [[D-branes]]

#### In terms of the algebraic data of the QFT on the worldvolume

An abstractly defined $n$-dimensional [[quantum field theory]] is a consistent assignment of [[state]]-space and correlators to $n$-dimensional [[cobordisms]] with certain structure (topological structure, conformal structure, Riemannian structure, etc. see [[FQFT]]/[[AQFT]]). In an _open-closed QFT_ the cobordisms are allowed to have boundaries. See at _[[boundary field theory]]_ for more on this.

In this abstract formulation of QFT a **brane** is a type of data assigned by the QFT to boundaries of cobordisms. 

##### In $2d$ rational CFT

A well understood class of examples is this one: among all 2-dimensional [[conformal field theory]], the case of _full rational 2d CFT_ has been understood completely, using [[FFRS-formalism]]. It is then a theorem that full 2-rational CFTs are classified by 

1. a [[modular tensor category]] $\mathcal{C}$ (to be thought of as being the category of representations of the [[vertex operator algebra]] of the 2d CFT);

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

##### In $2d$ TFT

Another case where the branes of a QFT are under good mathematical control is [[TCFT]]: the [[(infinity,1)-category]]-version of a 2d [[TQFT]].

Particularly the [[A-model]] and the [[B-model]] are well understood.

* the branes of the B-model ("B-branes") form the the [[stable (infinity,1)-category]] of [[chain complex]]es of [[quasicoherent sheaves]] on the target space (often considered just in terms of its [[homotopy category of an (infinity,1)-category]], the [[derived category]] of quasicoherent sheaves);

*  the branes of the A-model form the [[Fukaya category]] of the target space.

(...)


#### In terms of geometric data of the $\sigma$-model background 

An abstractly defined QFT (as a consistent assignment of state spaces and propagators to cobordisms as in [[FQFT]]) may be obtained by [[quantization]] from _geometric data_ :

Sich a _[[sigma-model]] QFT_ is the [[quantization]] of an [[action functional]] on a space of maps $\Sigma \to X$ from a cobordims ("worldvolume") $\Sigma$ to some target space $X$ that may carry further geoemtric data such as a [[Riemannian metric]],  or other background [[gauge field]]s.

One may therefore try to match the geometric data on $X$ that encodes the $\sigma$-model with the algebraic data of the [[FQFT]] that results after quantization. This gives a geometric interpretation to many of the otherwise purely abstract algebraic properties of the worldvolume QFT.

It turns out that if one checks which geometric data corresponds to the $A$-modules in the above discussion, one finds that these tend to come from structures that look at least roughly like _submanifolds_ of the target space $X$. And typically these submanifolds themselves carry their own background [[gauge field]] data.

A well-understood case is the [[Wess-Zumino-Witten model]]: for this the target space $X$ is a simple [[Lie group]] $X = G$ and the background field is a [[circle n-bundle with connection|circle 2-bundle with connection]] (a [[bundle gerbe]]) on $G$, representing the background field that is known as the [[Kalb-Ramond field]].

In this case it turns out that branes for the sigma model on $X$ are given in the smplest case by conjugacy classes $D \subset G$ inside the group, and that these carry [[twisted bundle|twisted vector bundle]] with the twist given by the Kalb-Ramond background bundle. These vector bundles are known in the [[string theory]] literature as _Chan-Paton vector bundles_ . The geometric intuition is that a QFT with certain boundary condition comes form a quantization of spaces of maps $\Sigma \to G$ that are restricted to take the boundary of $\Sigma$ to these submanifolds.

More generally, one finds that the geometric data that corresponds to the branes in the algebraically defined 2d QFT is given by cocycles in the twisted [[differential K-theory]] of $G$. These may be quite far from having a direct interpretation as submanifolds of $G$.

The case of rational 2d CFT considered so far is only the best understood of a long sequence of other examples. Here the collection of all [[D-branes]] -- identified with the colleciton of all internal modules over an internal frobenius algebra, forms an ordinary [[category]].

More generally, at least for 2-dimensional [[TQFT]]s analogous considerations yield not just categories but [[stable (∞,1)-categories]] of boundary condition objects. For instance for what is called the [[B-model]] 2-d [[TQFT]] the category of [[D-branes]] is the [[derived category]] of [[coherent sheaves]] on some Calabi-Yau space.

Starting with Kontsevich's [[homological algebra]] reformulation of [[homological mirror symmetry|mirror symmetry]] the study of (derived) D-brane categories has become a field in its own right in pure mathematics.

... lots of further things to say ...


### Fundamental or $\sigma$-model branes

In [[string theory]] one speaks apart from the [[D-branes]] also about **fundamental branes** . These are the objects $\Sigma$ in the $n$-dimensional [[sigma model]] themselves.

* For $n=0$ this describes the ordinary quantum mechanics of a point particles on $X$. And such point particles are the _fundamental particles_ for instance of the [[standard model of particle physics]].

* For $n=1$ this describes the quantum propagation of a [[string theory|string]], and accordingly one speaks of the _fundamental string_ or F1-brane (fundamental 1-brane).

* For $n=2$ this describes the quantum propagation of a membrane. 

* There are good indications that there is a way to describe heterotic [[string theory]] not in terms of fundamental 1-branes but in terms of the [[sigma-model]] of a fundamental 5-brane -- the [[magnetic charge|magnetic dual]] of the 1-brane in 10-dimensions. 

* etc.

[[!include brane scan]]

### Black branes

See _[[black brane]]_ .


## Properties

### Worldvolume theories

[[!include table of branes]]

### The super-brane scan

If the worldvolume QFT of the fundamental branes (for instance the worlsheet 2d[[CFT]] of the string) is required to be a [[supersymmetric QFT]], specifically if the [[Green-Schwarz action functional]] is used only particular combinations of the dimenion $dim \Sigma = p + 1$ of the worldvolume and $D = dim X$ of [[spacetime]] are possible.

The corresponding table has been called the **[[brane scan]]**

[[branescan.gif:pic]]


## Related concepts

* [[wrapped brane]]

* [[brane intersection]]

* [[D-brane]], [[fractional D-brane]]

* [[sigma-model]]

* [[double dimensional reduction]]

* [[particle]], [[superparticle]]

* [[string]], [[superstring]] 

* [[membrane]], [[M2-brane]], [[M5-brane]]

* [[NS5-brane]]

* [[D-brane]]

* [[electric eigenbrane]]. [[magnetic eigenbrane]]

[[!include field theory with boundaries and defects - table]]


[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]



## References 

### Prehistory

* {#EinsteinInfeldHoffmann39} [[Albert Einstein]], [[Leopold Infeld]], B. Hoffmann, _The gravitational equations and the problem of motion_, Annals of Mathematics, Vol 39, No. 1, 1938

See also

* Wikipedia, _[Black hole electron](https://en.wikipedia.org/wiki/Black_hole_electron)_

The terminology "$p$-brane" originates in

* {#DuffInamiPopeSezginStelle88} [[Mike Duff]], T. Inami, [[Christopher Pope]], [[Ergin Sezgin]],  [[Kellogg Stelle]], _Semiclassical Quantization of the Supermembrane_, Nucl.Phys. B297 (1988) 515-538 ([spire:247064](http://inspirehep.net/record/247064))



### General
  

* [[Greg Moore]], _What is... a brane?_, Notices of the AMS vol 52, no. 2 ([pdf](http://www.ams.org/notices/200502/what-is.pdf))

* Joan Simon, _Brane Effective Actions, Kappa-Symmetry and Applications_ ([arXiv:1110.2422](http://arxiv.org/abs/1110.2422))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 6.2 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012


### Boundary conditions / D-branes

(...)

See [[D-brane]].

For exhaustive details on D-branes in 2-dimensional rational [[CFT]] see the references given at 

* [[FFRS-formalism]].


A classical text describing how the physics way to think of D-branes for the [[topological string]] leads to seeing that they are objects in [[derived categories]] (of [[coherent sheaves]] for the [[B-model]]) is reviewed in

* [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv](http://arxiv.org/abs/hep-th/0403166)) 

based on

* [[Michael Douglas]], _D-branes, Categories and $N=1$ Supersymmetry_, J.Math.Phys. 42 (2001) 2818-2843 ([arXiv:hep-th/0011017](https://arxiv.org/abs/hep-th/0011017))

* [[Paul Aspinwall]], Albion Lawrence, _Derived Categories and Zero-Brane Stability_ ([arXiv:hep-th/0104147](https://arxiv.org/abs/hep-th/0104147))

This can to a large extent be read as a dictionary from [[homological algebra]] terminology to that of D-brane physics.

More recent similar material with the emphasis on the [[K-theory]] aspects is

* [[Richard Szabo]], _[[Szabo09.pdf:file]]_

### Fundamental branes

The "[[brane scan]]" table showing the consistent dimension pairs for the [[Green-Schwarz action functional]] was depicted in

* [[Michael Duff]], _Supermembranes: the first fifteen weeks_ CERN-TH.4797/87 ([scan](http://ccdb4fs.kek.jp/cgi-bin/img/allpdf?198708425))
{#Duff}

going back to

* A. Ach&#250;carro, J. M. Evans, [[Paul Townsend]] and D. L. Wiltshire, _Super $p$-branes_ Physics Letters B Volume 198, Issue 4, 3 (1987)

Further developments are in

More along these lines is in

* [[Michael Duff]], S. Ferrara, _Four curious supergravities_ ([arXiv](http://arxiv.org/abs/1010.3173))

See also [[division algebras and supersymmetry]].


### Branes ending on branes

* [[Andrew Strominger]], _Open P-Branes_, Phys. Lett. B383:44-47,1996 ([arXiv:hep-th/9512059](http://arxiv.org/abs/hep-th/9512059))

[[!redirects branes]]

[[!redirects branes]]

[[!redirects fundamental brane]]
[[!redirects fundamental branes]]

[[!redirects NS-fivebrane]]
[[!redirects NS-fivebranes]]

[[!redirects p-brane]]
[[!redirects p-branes]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The [[action functional]] of [[gravity]] was originally conceived as a [[nonlinear functional|functional]] on the space of [[pseudo-Riemannian metrics]] of a [[manifold]] $X$. Later on it was realized that it may alternatively naturally be thought of as a functional on the space of [[connection on a bundle|connections]] with values in the [[Poincaré Lie algebra]] -- subject to the constraint that the component in the [[translation Lie algebra]] defines a [[vielbein field]]. 

Mathematically this means that the [[field (physics)|field]] of [[gravity]] is modeled as a _[[Cartan connection]]_ for the [[Lorentz group]] inside the [[Poincaré group]]. In [[physics]] this is known as the _first order formalism_ or the _Cartan moving frame method_. The translation part of the [[Poincaré Lie algebra]]-connection is called the _[[vielbein]]_ and the remainder the _[[spin connection]]_. The [[field strength]] of gravity -- the [[Riemann tensor]] -- is the [[curvature]].

The reformulation of [[pseudo-Riemannian geometry]] in terms of [[Cartan geometry]] is suggestive of also re-rewriting the form of the [[Lagrangian density]]/[[action functional]] of the theory of [[gravity]], even though this is logically an independent issue. In [[spacetime]] of [[dimension]] 3+1 one such alternative is known as the _Palatini-Cartan-Holst action_. That its [[phase space]] coincides with that induced by the [[Einstein-Hilbert action]] is due to [Cattaneo-Schiavina 17a](#CattaneoSchiavina17a)

Promoting the first-order formulation of gravity from the [[Poincaré group]] to the [[super Poincaré group]] yields _[[supergravity]]_ formulated in [[super Cartan geometry]]. Promoting it further to the [[L-infinity algebra cohomology|Lie n-algebra]] extensions of the [[super Poincaré group]] (from the [[brane scan]]/[[schreiber:The brane bouquet|brane bouquet]]) yields [[type II supergravity]], [[heterotic supergravity]] and [[11-dimensional supergravity]] in [[higher Cartan geometry]]-formulation ([[D'Auria-Fré formulation of supergravity]]).

[[!include local and global geometry - table]]

## Properties

### Local and global framing

Discussion in the physics literature traditionally tends to ignore the global structure of [[spacetime]] manifolds and pretends that a [[vielbein]] field may be chosen globally, hence that spacetime admits a [[framed manifold|framing]].

In general that is only valid locally, but it so happens that in the archetypical case of interest, namely for 4-dimensional [[globally hyperbolic spacetimes]] with [[orientation|orientable]] spatial slices, it is valid globally. See _[this remark](framed+manifold#In4dFirstOrderGravity)_ at _[[framed manifold]]_ for more.

See also at _[[teleparallel gravity]]_.

## Related concepts 

* [[Lorentzian geometry]]

* [[supergravity]]

* [[D'Auria-Fre formulation of supergravity]]

* [[gravity as a BF-theory]].

* [[teleparallel gravity]]


## References

Introductions:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section I.4 of: _[[Supergravity and Superstrings - A Geometric Perspective]]_ &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), ch I.4: [[CastellaniDAuriaFre-ChI4.pdf:file]]&rbrack;

* [[Jorge Zanelli]], sections 4 and 5 of: _Lecture notes on Chern-Simons (super-)gravities. Second edition (February 2008)_, lectures at *Geometric and topological methods for quantum field theory*, Villa de Leyva (2001) &lbrack;[arXiv:hep-th/0502193](http://arxiv.org/abs/hep-th/0502193), [inspire:677203](https://inspirehep.net/literature/677203)&rbrack;

* [[Pietro Fré]], §5 in: *Gravity, a Geometrical Course*, Volume 1: *Development of the Theory and Basic Physical Applications*, Spinger (2013) &lbrack;[doi:10.1007/978-94-007-5361-7](https://doi.org/10.1007/978-94-007-5361-7)&rbrack;

More explicitly understood via [[Cartan geometry]]:

* [[Gabriel Catren]], *Geometrical Foundations of Cartan Gauge Gravity*,  Int. J. Geom. Methods in Modern Physics **12** 04 (2015) 1530002  &lbrack;[arXiv:1407.7814](https://arxiv.org/abs/1407.7814), [doi:10.1142/S0219887815300020](https://doi.org/10.1142/S0219887815300020)&rbrack;

* [[Kirill Krasnov]], §3 in: *Formulations of General Relativity*, Cambridge Monographs on Mathematical Physics, Cambridge University Press (2020) &lbrack;[doi:10.1017/9781108674652](https://doi.org/10.1017/9781108674652), taster:[pdf](https://www.maths.nottingham.ac.uk/plp/pmzkk/book_taster.pdf)&rbrack;


and in view of [[supergravity]]:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section I.4.1 of _[[Supergravity and Superstrings - A Geometric Perspective]]_ &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), ch I.4: [[CastellaniDAuriaFre-ChI4.pdf:file]]&rbrack;

For more in the case of [[supergravity]]:

* [[Bernard Julia]], S. Silva, *On first order formulations of supergravities*, JHEP 0001 (2000) 026 &lbrack;[arXiv:hep-th/9911035](https://arxiv.org/abs/hep-th/9911035), [doi:10.1088/1126-6708/2000/01/026](https://doi.org/10.1088/1126-6708/2000/01/026)&rbrack;

Formulation via [[BV-formalism]] and [[L-infinity algebras|$L_\infty$-algebras]]:

* Marija Dimitrijević Ćirić, [[Grigorios Giotopoulos]], Voja Radovanović, [[Richard J. Szabo]], *$L_\infty$-Algebras of Einstein-Cartan-Palatini Gravity*, Journal of Mathematical Physics **61** (2020) 112502 &lbrack;[arXiv:2003.06173](https://arxiv.org/abs/2003.06173), [doi:10.1063/5.0011344](https://doi.org/10.1063/5.0011344)&rbrack;



The equivalence of the [[phase space]] of Palatini-Cartan-Holst [[Lagrangian  field theory]] with the [[Einstein-Hilbert action|Einstein-Hilbert version]] is established in

* {#CattaneoSchiavina17a} [[Alberto Cattaneo]], [[Michele Schiavina]], _The reduced phase space of Palatini-Cartan-Holst theory_, Ann. Henri Poincaré (2019) 20: 445 ([arXiv:1707.05351](https://arxiv.org/abs/1707.05351), [doi:10.1007/s00023-018-0733-z](https://doi.org/10.1007/s00023-018-0733-z))

Subtleties in extending this to a [[local field theory]] (gluing pieces of spacetimes along their boundaries) are discussed in

* {#CattaneoSchiavina17b} [[Alberto Cattaneo]], [[Michele Schiavina]], _BV-BFV approach to General Relativity: Palatini-Cartan-Holst action_ ([arXiv:1707.06328](https://arxiv.org/abs/1707.06328))

following

* {#CattaneoSchiavina15} [[Alberto Cattaneo]], [[Michele Schiavina]], _BV-BFV approach to General Relativity, Einstein-Hilbert action_, J. Math. Phys. 57, 023515 (2016) ([arXiv:1509.05762](https://arxiv.org/abs/1509.05762))

see also:

* Giovanni Canepa, [[Alberto Cattaneo]], *Corner Structure of Four-Dimensional General Relativity in the Coframe Formalism*, Annales Henri Poincaré **25** (2024) 2585–2639 &lbrack;[arXiv:2202.08684](https://arxiv.org/abs/2202.08684), [doi:10.1007/s00023-023-01360-8](https://doi.org/10.1007/s00023-023-01360-8)&rbrack;


Reviewed in:

* [[Alberto S. Cattaneo]], *Phase space for gravity with boundaries*,  Encyclopedia of Mathematical Physics (2023) &lbrack;[arXiv:2307.04666](https://arxiv.org/abs/2307.04666)&rbrack;

  > (following [Kijowski & Tulczyjew (2005)](phase+space#KijowskiTulczyjew05))


Relation to [[BF-theory]]:

* {#CattaneoMengerSchiavina23} [[Alberto S. Cattaneo]], [[Leon Menger]], [[Michele Schiavina]], *Gravity with torsion as deformed BF theory* &lbrack;[arXiv:2310.01877](https://arxiv.org/abs/2310.01877)&rbrack;


See also:

* J. Fernando Barbero G., Juan Margalef-Bentabol, Valle Varo, Eduardo J.S. Villaseñor, *Covariant phase space for gravity with boundaries: metric vs tetrad formulations* ([arXiv:2103.06362](https://arxiv.org/abs/2103.06362))


More towards [[quantization]] ([[quantum gravity]]):

* Fernando T. Brandt, J. Frenkel, S. Martins-Filho, D. G. C. McKeon, *Quantization of Einstein-Cartan theory in the first order form* &lbrack;[arXiv:2401.16343](https://arxiv.org/abs/2401.16343)&rbrack;

* Fernando T. Brandt, J. Frenkel, S. Martins-Filho, D. G. C. McKeon: *On the equivalence of first and second order formulations of the Einstein-Hilbert theory* &lbrack;[arXiv:2510.17615](https://arxiv.org/abs/2510.17615)&rbrack;



[[!redirects first-order formulations of gravity]]

[[!redirects first order formulation of gravity]]
[[!redirects first order formulations of gravity]]


[[!redirects Palatini action]]
[[!redirects Palatini actions]]

[[!redirects Palatini formulation]]
[[!redirects Palatini formulations]]

[[!redirects Palatini formalism]]
[[!redirects Palatini formalisms]]




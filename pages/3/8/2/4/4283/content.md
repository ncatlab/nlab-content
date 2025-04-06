
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea ##

In ([[algebraic quantum field theory|algebraic]]) [[quantum field theory]], superselection theory is concerned with identifying *superselection sectors*: Namely [[conservation laws]] imply that in an isolated system the total value of certain [[charges]] (e.g. [[electric charges]], [[magnetic charges]]) cannot change due to any interactions taking place in the system, and a superselection sector is specified by prescribing a number to each of these charges, it is the space of all [[quantum states]] of the system with these values for the charges.

There are two complementary viewpoints about superselection sectors: 

In the picture of [Wick, Wigner & Wightman 1952](#WickWignerWightman52), all possible [[quantum states]] of a system form one big [[Hilbert space]] and  superselection sectors are subspaces of this Hilbert space, and no measurement, that is no [[observable]], can map a state in one superselection sector to another. Further, [[superpositions]] of states in different sectors do not exist in physical reality. 

Mathematically speaking this means that superselection sectors are the *[[irreducible representations]]* of a given [[algebra of observables]] inside a possibly larger [[space of quantum states]].

An example would be a superposition of a state containing one electron with a state containing two electrons.

In the [[AQFT]] approach to [[quantum field theory]] the observables of the theory are [[self-adjoint elements]] of a [[C-star algebra|$C^\ast$-algebra]] [[algebra of quantum observables]]. A concrete physical system is a [[state on a star-algebra|state of]] this algebra, which is accompanied, via the [[GNS construction]], with a representation of the algebra. A superselection sector from this viewpoint is an [[equivalence class]] of unitarily equivalent representations, see at *[[representation of a C-star algebra]]*. 


## Examples ##

Usually, in [[AQFT]] not _all_ representations of the algebra of observables are considered to be _physically relevant_, so that superselection theory starts with the statement of conditions that representations have to fulfill in order to be **admissible**, and only those are considered. 
Example:

* [[DHR superselection theory]] 

## Related concepts

* [[quantum parallelism]]

* [[quantum superposition]]

* [[quantum interference]]

* [[entanglement]]
 
## References ##

The notion originates (in a context similar to the [[Wigner classification]] of [[fundamental particles]]) in:

* {#WickWignerWightman52} [[Gian-Carlo Wick]], [[Eugene Wigner]], [[Arthur Wightman]]: *The intrinsic parity of elementary particles*, Phys. Rev. **88** (1952) 101-105 &lbrack;[doi;10.1103/PhysRev.88.101](https://doi.org/10.1103/PhysRev.88.101), [pdf](http://dieumsnh.qfb.umich.mx/archivoshistoricosmq/ModernaHist/Wick.pdf)&rbrack;
 
Brief early survey:

* [[Raymond F. Streater]], section 2.3 of: *Outline of axiomatic relativistic quantum field theory*, Rep. Prog. Phys. **38** (1975) 771 &lbrack;[doi:10.1088/0034-4885/38/7/001](https://iopscience.iop.org/article/10.1088/0034-4885/38/7/001)&rbrack;

Lecture notes:

* [[Klaus Fredenhagen]]: *Superselection Sectors*, lecture notes, Hamburg (1994/5) &lbrack;[pdf](https://www.physik.uni-hamburg.de/th2/ag-fredenhagen/dokumente/superselect.pdf), [[Fredenhagen-Superselection.pdf:file]]&rbrack;

Seminar notes:

* Tadashi Fujimoto: *Outline of superselectionrule on Algebraic Quantum Field Theory* (2021) &lbrack;[pdf](https://www.eonet.ne.jp/~tfujimoto21/superselection2.pdf)&rbrack;

See also at *[[AQFT]]*, *[[QFT]]* and *[[Haag-Kastler axioms]]* and *[[DHR superselection theory]]*.

References that make explicit the identification of superselection sections with [[irreducible representations]] of the [[algebra of quantum observables]]:

* [[John E. Roberts]], p. 110 (5 of 14) in: *Local cohomology and superselection structure*,  Comm. Math. Phys. **51** 2 (1976) 107-119 &lbrack;[euclid:cmp/1103900345](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-51/issue-2/Local-cohomology-and-superselection-structure/cmp/1103900345.full)&rbrack;

* {#FroehlichGabbianiMarchetti90} [[Jürg Fröhlich]], [[Fabrizio Gabbiani]], [[Pieralberto Marchetti]], below Def. 2.1, p 16 of: *Braid statistics in three-dimensional local quantum field theory*, in: H.C. Lee (ed.) *Physics, Geometry and Topology*, NATO ASI Series **238**, Springer (1990)  &lbrack;[doi:10.1007/978-1-4615-3802-8_2](https://doi.org/10.1007/978-1-4615-3802-8_2), [[FroehlichGabbianiMarchetti-BraidStatistics.pdf:file]]&rbrack;
  > (in a context of [[braid group statistics]])

* [[Klaas Landsman]], p. 48 (4 of 28): *Quantization and Superselection Sectors I. Transformation Group $C^\ast$ Algebras*,  Reviews in Mathematical Physics **02** 01 (1990) 45-72 &lbrack;[doi:10.1142/S0129055X9000003X](https://doi.org/10.1142/S0129055X9000003X), [pdf](https://www.math.ru.nl/~landsman/landsman1.pdf)&rbrack;

* [[Klaas Landsman]], p. 73-4 (1-2 of 32) in: *Quantization and Superselection Sectors II. Dirac Monopole and Aharonov-Bohm effect*, Reviews in Mathematical Physics **02** 01 (1990) 73-104 &lbrack;[doi:10.1142/S0129055X90000041](https://doi.org/10.1142/S0129055X90000041), [pdf](http://www.math.ru.nl/~landsman/landsman2.pdf)&rbrack;

* David John Baker, p. 273 (12 of 24): *Identity, Superselection Theory, and the Statistical Properties of Quantum Fields*, Philosophy of Science **80**  2 (2013) 262-285 &lbrack;[doi:10.1086/670296](https://doi.org/10.1086/670296)&rbrack;


Discussion via [[vertex operator algebras]]:

* Haisheng Li: *The Physics Superselection Principle in Vertex Operator Algebra Theory*, Journal of Algebra *196** (1997) 436-457 &lbrack;[doi;10.1006/jabr.1997.7126](https://doi.org/10.1006/jabr.1997.7126)&rbrack;


Discussion in the context of [[holographic entanglement entropy]]:

* Horacio Casini, Marina Huerta, Javier M. Magan, Diego Pontello, _Entanglement entropy and superselection sectors I. Global symmetries_ &lbrack;[arXiv:1905.10487](https://arxiv.org/abs/1905.10487)&rbrack;

In the context of the [[Aharonov-Bohm effect]]:

* [[Claudio Dappiaggi]], [[Giuseppe Ruzzi]], Ezio Vasselli: *Aharonov-Bohm superselection sectors*, Lett Math Phys **110**  (2020) 3243–3278 &lbrack;[doi;10.1007/s11005-020-01335-4](https://doi.org/10.1007/s11005-020-01335-4), [arXiv:, 1912.05297](https://arxiv.org/abs/1912.05297)&rbrack;


Discussion in relation to [[asymptotic symmetries]] of [[gauge theories]]:

* [[A. P. Balachandran]],  [[V. P. Nair]], A. Pinzul, [[A. F. Reyes-Lega]], S. Vaidya: *Superselection, boundary algebras, and duality in gauge theories*, Phys. Rev. D **106** (2022) 025001 &lbrack;[doi:10.1103/PhysRevD.106.025001](https://doi.org/10.1103/PhysRevD.106.025001), [arXiv:2112.08631](https://arxiv.org/abs/2112.08631)&rbrack;




[[!redirects superselection theory]]
[[!redirects superselection sector]]
[[!redirects superselection sectors]]

[[!redirects superselection rule]]
[[!redirects superselection rules]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The traditional notion of *[[connection on a principal bundle]]* with given [[structure group|structure]] [[Lie algebra]] $\mathfrak{g}$ has a slick [[dg-algebra|dg-algebraic]]-formulation in terms of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ and the [[Weil algebra]] $W(\mathfrak{g})$ of $\mathfrak{g}$ (due to [Henri Cartan 1950](Weil+algebra#Cartan50)). 

These concepts of *[[Cartan connection]]* may be generalized to [[L-infinity algebras|$L_\infty$-algebras]] (originally so in [SSS09](#SSS09), [SSS12](#SSS12), [FSS12](#FSS12), which was the starting point for the more comprehensive development in [dcct12](#dcct12)) -- see at *[[connection on a smooth principal infinity-bundle|connection on a smooth principal $\infty$-bundle]]*. In fact, noticing (see [here](L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra)) that the [[Chevalley-Eilenberg algebra]]-construction $CE(-)$ constitutes a [[full subcategory]]-embedding of the 1-category of [[finite type]] [[L-infinity algebras|$L_\infty$-algebras]] into the [[opposite category|opposite 1-category]] of [[dgc-algebras]], there is an immediate $L_\infty$-analog of the notion of [[Weil algebra]] ([SSS09, Def. 16](#SSS09)).

However, this is a [[1-category|1-]][[category theory|category theoretic]] analog, hence is a particularly strict model, defined up to [[isomorphism]], of what the would-be $\infty$-Weil algebra of an $L_\infty$-algebra should be. The latter will only be well-defined up to compatible [[quasi-isomorphism]]. 

The need to pass to compatible deformations of $L_\infty$-Weil algebras for a satisfactory definition of [[string 2-connections]] ([[1-brane]] connections) and analogous higher notions ([[fivebrane structure|5-brane]]-connection, [[ninebrane structure|9-brane]], etc.) was first discussed around [SSS09, Prop. 21](#SSS09) (and used to exhibit the [[higher gauge theory|higher gauge-theoretic]] nature of the [[Green-Schwarz mechanism]] in [SSS12, §3.2](higher+gauge+theory+of+the+Green-Schwarz+mechanism+--+references#SatiSchreiberStasheff12)), and was justified there by the condition that the canonical [[invariant polynomial]] in that situation does lift as expected. 

A more general discussion of the necessary *adjustments* of $L_\infty$-Weil algebras was then given in [Saemann & Schmidt 20](#SaemannSchmidt20), who observe that a good general condition to impose is that the induced [[BRST complex|BRST complexes]] of $L_\infty$-connections ([SSS09, §9.3](#SSS09)) remain well-defined when the [[antifields]] and [[auxiliary fields]] are required to strictly vanish. 
These authors introduce the terminology *adjusted Weil algebras* ([Saemann & Schmidt 20, Def. 4.2](#SaemannSchmidt20)) and the resulting *adjusted $L_\infty$-connections* and *adjusted [[higher parallel transport]]* ([Kim & Saemann 2020](KimSaemann20)). 

Concretely, the choice of compatible deformation of the Weil algebra determines the [[Bianchi identities]] on the [[curvature characteristic forms]] of corresponding [[L-infinity algebra valued differential forms|$L_\infty$-algebra valued differential forms]] (these [[Bianchi identities]] are embodied by the [[differential]] in the Weil algebra restricted to shifted generators) and without adjustment the Bianchi identities are stronger than (i.e. just special cases of what) they ought to be.

Notice that, while the [[Weil algebra]] by itself is [[contractible homotopy type]], its *adjustments* along [[quasi-isomorphisms]] must satisfy [[horizontal differential form|horizontality]] constraints (such as the vanishing of those [[antifields]]) which makes this a non-trivial procedure. 

While the characterization of adjusted Weil algebras for $L_\infty$-algebra in [Saemann & Schmidt 20, Def. 4.2](#SaemannSchmidt20) clearly (generalizes and) conceptually improves on [SSS09, Prop. 21](#SSS09), and while in applications it clearly gives the right answers (the correct higher [[Bianchi identities]]), what is still missing is a purely [[homotopy theory|homotopy theoretic]] justification. Since in practice these adjusted Weil algebras behave and are used much like [[resolutions]] by [[minimal fibrations]] in [[model category]]-theory, it is natural to wonder if there is the structure of a [[homotopical category|homotopical]] [[fibration category]] on the Weil algebra choices for $L_\infty$-algebras, such that this is indeed the case. This question is open.

On the other hand, [Borsten, Kim & Saemann 2021](#BorstenKimSaemann21) argue that adjustment is naturally understood after embedding [[L-infinity algebras|$L_\infty$-algebras]] within [[EL-infinity algebra|$E L_\infty$-algebras]] (and that this is what exhibits [[tensor hierarchies]] as a [[higher gauge theory]]-phenomenon). 


## Related entries

* [[principal infinity-connection]]

* [[nonabelian differential cohomology]]

* [[supergravity Lie 6-algebra]]

## References
 {#References}

The original discussion for the special case of [[string 2-connections]] and their higher analogs (such as [[Fivebrane structure|fivebrane]] 6-connections, [[Ninebrane structure|Ninebrane]] 10-connections etc.):

* {#Schreiber07} [[Urs Schreiber]], *[Obstructions to $n$-Bundle Lifts Part II](https://golem.ph.utexas.edu/category/2007/10/obstructions_to_nbundle_lifts.html)* (Oct 2007) &lbrack;bottom right corner in this hand-drawn diagram: [[Schreiber-PrincipalInfinityConnections-2007.pdf:file]]&rbrack;

* {#SSS09} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], Def. 23 on  [p. 47](https://arxiv.org/pdf/0801.3480.pdf#page=47) with Prop. 21 on [p. 48](https://arxiv.org/pdf/0801.3480.pdf#page=48) in:  *[[schreiber:L-infinity algebra connections|$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport]]*, in *Quantum Field Theory*, Birkhäuser (2009) 303-424 &lbrack;[arXiv:0801.3480](https://arxiv.org/abs/0801.3480), [doi:10.1007/978-3-7643-8736-5_17](https://doi.org/10.1007/978-3-7643-8736-5_17)&rbrack;

* {#SSS12} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]]:  middle boxes on [p. 28](https://arxiv.org/pdf/0910.4001.pdf#page=28) and [p. 32](https://arxiv.org/pdf/0910.4001.pdf#page=32) of: *[[schreiber:Twisted Differential String and Fivebrane Structures]]*, Communications in Mathematical Physics **315** 1 (2012)  169-213 &lbrack;[arXiv:0910.4001](https://arxiv.org/abs/0910.4001), [doi:10.1007/s00220-012-1510-3)]([arXiv:](https://link.springer.com/article/10.1007/s00220-012-1510-3))&rbrack;

* {#FSS12} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], [p. 77](https://arxiv.org/pdf/1011.4735.pdf#page=77) and [p. 80](https://arxiv.org/pdf/1011.4735.pdf#page=80) of: _[[schreiber:Cech cocycles for differential characteristic classes|Čech cocycles for differential characteristic classes]]_, Advances in Theoretical and Mathematical Physics, **16** 1 (2012) 149-250 &lbrack;[arXiv:1011.4735](https://arxiv.org/abs/1011.4735), [doi:10.1007/BF02104916](https://doi.org/10.1007/BF02104916)&rbrack;

* {#dcct13} [[Urs Schreiber]], Def. 5.2.91 on [p. 645](https://arxiv.org/pdf/1310.7930v1.pdf#page=645) in: *[[schreiber:dcct|differential cohomology in a cohesive topos]]* (2013-)

{#WithHindsight} With hindsight, an early example of such adjustment (namely for the  "[[supergravity Lie 6-algebra]]", see [there](supergravity+Lie+6-algebra#ModifiedWeilAlgebra)), is given in:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], vol 2, III (8.24) of: *[[Supergravity and Superstrings - A Geometric Perspective]]*, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), [epdf](https://epdf.pub/supergravity-and-superstrings-a-geometric-perspective-vol-2-supergravity.html)&rbrack;

(recognized as a "modified Weil algebra" in [revision 8, 2011](https://ncatlab.org/nlab/revision/diff/supergravity+Lie+6-algebra/8), long before the "adjusted"-terminology was proposed).

Characterization of adjusted $\mathfrak{g}$-Weil algebras by requiring well-behaved [[BRST-complexes]] for [[L-infinity algebra valued differential forms|$L_\infty$-algebra valued differential forms]]:

* {#SaemannSchmidt20} [[Christian Saemann]], [[Lennart Schmidt]], *Towards an M5-Brane Model II: Metric String Structures*, Fortschr. Phys. **68** (2020) 2000051 &lbrack;[arXiv:1908.08086](https://arxiv.org/abs/1908.08086), [doi:10.1002/prop.202000051](https://doi.org/10.1002/prop.202000051)&rbrack;

Revisiting the special case of the [[string Lie 2-algebra]]:

* {#Schmidt19} [[Lennart Schmidt]], _Twisted Weil Algebras for the String Lie 2-Algebra_, in [[Christian Saemann]], [[Urs Schreiber]], [[Martin Wolf]] (eds.) _[Higher Structures in M-Theory](http://www.maths.dur.ac.uk/lms/109/index.html)_ [Durham Symposium](http://www.maths.dur.ac.uk/lms/) 2018, Fortschritte der Physik 2019 &lbrack;[arXiv:1903.02873](https://arxiv.org/abs/1903.02873), [doi:10.1002/prop.201910016](https://doi.org/10.1002/prop.201910016)&rbrack;


Application to [[higher parallel transport]]:

* {#KimSaemann20} [[Hyungrok Kim]], [[Christian Saemann]], *Adjusted Parallel Transport for Higher Gauge Theories*, J. Phys. A **52** (2020) 445206 &lbrack;[arXiv:1911.06390](https://arxiv.org/abs/1911.06390), [doi:10.1088/1751-8121/ab8ef2](https://doi.org/10.1088/1751-8121/ab8ef2)&rbrack;

Relation to [[EL-infinity algebras|$E L_\infty$-algebras]] and [[tensor hierarchies]]:

* {#BorstenKimSaemann21} [[Leron Borsten]], [[Hyungrok Kim]], [[Christian Saemann]].  *$E L_\infty$-algebras, Generalized Geometry, and Tensor Hierarchies* &lbrack;[arXiv:2106.00108](https://arxiv.org/abs/2106.00108)&rbrack;


Survey and review:

* [[Christian Saemann]], *Adjusted Higher Gauge Theory: Connections and Parallel Transport* Lisbon (2021) &lbrack;[pdf](https://math.tecnico.ulisboa.pt/seminars/download.php?fid=1485), [[Saemann-AdjustedHGT.pdf:file]]&rbrack;

* [[Christian Saemann]], *$E L_\infty$-algebras, Generalized Geometry, and Tensor Hierarchies*, talk at [SFT@Cloud 2021](https://indico.cern.ch/event/1042834/) (2021) &lbrack;[pdf](https://indico.cern.ch/event/1042834/contributions/4487418/attachments/2313514/3937748/saemann_generalized_geometry.pdf), [[Saemann-ELInfinityAndTensorHierarchies.pdf:file]]&rbrack;

* [[Christian Saemann]], *Atiyah Algebroids for Higher and Groupoid Gauge Theories*, [talk at](M-Theory+and+Mathematics#Saemann2024) *[[M-Theory and Mathematics]]*, [[CQTS]] (2024) &lbrack;[[Saemann-AtiyahAlgebroids.pdf:file]]&rbrack;

Application to geometric refinement of [[topological T-duality]]:

* [[Hyungrok Kim]], [[Christian Saemann]], *T-duality as Correspondences of Categorified Principal Bundles with Adjusted Connections* &lbrack;[arXiv:2303.16162](https://arxiv.org/abs/2303.16162)&rbrack;



[[!redirects adjusted Weil algebras]]



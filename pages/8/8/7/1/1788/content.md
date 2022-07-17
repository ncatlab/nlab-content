

## Idea

The traditional notion of *[[connection on a principal bundle]]* with given [[structure group|structure]] [[Lie algebra]] $\mathfrak{g}$ has a slick [[dg-algebra|dg-algebraic]]-formulation in terms of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ and the [[Weil algebra]] $W(\mathfrak{g})$ of $\mathfrak{g}$ (due to [Henri Cartan 1950](Weil+algebra#Cartan50) ). 

These concepts of *[[Cartan connection]]* may be generalized to [[L-infinity algebras|$L_\infty$-algebras]] (originally so in [SSS09](#SSS09), [SSS12](#SSS12), [FSS12](#FSS12), which was the starting point for the more comprehensive development in [dcct12](#dcct12)). In fact, noticing (see [here](L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra)) that the [[Chevalley-Eilenberg algebra]]-construction $CE(-)$ constitutes a [[full subcategory]]-embedding of the 1-category of [[finite type]] [[L-infinity algebras|$L_\infty$-algebras]] into the [[opposite category|opposite 1-category]] of [[dgc-algebras]], there is an immediate $L_\infty$-analog of the notion of [[Weil algebra]] ([SSS09, Def. 16](#SSS09)).

However, this is a [[1-category|1-]][[category theory|category theoretic]] analog, hence is a particularly strict model, defined up to [[isomorphism]], of what the would-be $\infty$-Weil algebra of an $L_\infty$-algebra should be. The latter will only be well-defined up to compatible [[quasi-isomorphism]]. 

The need to pass to compatibly [[quasi-isomorphism|quasi-isomorphic]] deformations of $L_\infty$-Weil algebras for a satisfactory definition of [[string 2-connections]] ([[1-brane]] connections) and analogous higher notions ([[fivebrane structure|5-brane]]-connection, [[ninebrane structure|9-brane]], etc.) was first discussed around [SSS09, Prop. 21](#SSS09) (and used to exhibit the [[higher gauge theory|higher gauge-theoretic]] nature of the [[Green-Schwarz mechanism]] in [SSS12, §3.2](higher+gauge+theory+of+the+Green-Schwarz+mechanism+--+references#SatiSchreiberStasheff12)), and was justified there by the condition that the canonical [[invariant polynomial]] in that situation does lift as expected. 

A more general discussion of the necessary *adjustments* of $L_\infty$-Weil algebras was then given in [Saemann & Schmidt 20](#SaemannSchmidt20), who observe that a good general condition to impose is that the induced [[BRST complex|BRST complexes]] of $L_\infty$-connections ([SSS09, §9.3](#SSS09)) remain well-defined when the [[antifields]] and [[auxiliary fields]] are required to strictly vanish. 
These authors introduce the terminology *adjusted Weil algebras* ([Saemann & Schmidt 20, Def. 4.2](#SaemannSchmidt20)) and the resulting *adjusted $L_\infty$-connections* and *adjusted [[higher parallel transport]]* ([Kim & Saemann 2020](KimSaemann20)). 

Notice that, while the [[Weil algebra]] by itself is [[contractible homotopy type]], its *adjustments* along [[quasi-isomorphisms]] must satisfy [[horizontal differential form|horizontality]] constraints (such as the vanishing of those [[antifields]]) which makes this a non-trivial procedure. 

While the characterization of adjusted Weil algebras for $L_\infty$-algebra in [Saemann & Schmidt 20, Def. 4.2](#SaemannSchmidt20) clearly (generalizes and) conceptually improves on [SSS09, Prop. 21](#SSS09), and while in applications it clearly gives the right answers (the correct higher [[Bianchi identities]]), what is still missing is a purely [[homotopy theory|homotopy theoretic]] justification. Since in practice, these adjusted Weil algebras behave and are used much like [[resolutions]] by [[minimal fibrations]] in [[model category]]-theory, it is natural to wonder if there is the structure of a [[homotopical category|homotopical]] [[fibration category]] on the weil algebra choices for $L_\infty$-algebras, such that this is indeed the case. This question is open.


## References

The original discussion for the special case of [[string 2-connections]] and their higher analogs:

* {#SSS09} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], *[[schreiber:L-infinity algebra connections|$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport]]*, in *Quantum Field Theory*, Birkhäuser (2009) 303-424 &lbrack;[arXiv:0801.3480](https://arxiv.org/abs/0801.3480), [doi:10.1007/978-3-7643-8736-5_17](https://doi.org/10.1007/978-3-7643-8736-5_17)&rbrack;

* {#SSS12} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]]:  *[[schreiber:Twisted Differential String and Fivebrane Structures]]*, Communications in Mathematical Physics **315** 1 (2012)  169-213 &lbrack;[arXiv:0910.4001](https://arxiv.org/abs/0910.4001), [doi:10.1007/s00220-012-1510-3)]([arXiv:](https://link.springer.com/article/10.1007/s00220-012-1510-3))&rbrack;


* {#FSS12} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech cocycles for differential characteristic classes|Čech cocycles for differential characteristic classes]]_, Advances in Theoretical and Mathematical Physics, **16** 1 (2012) 149-250 &lbrack;[arXiv:1011.4735](https://arxiv.org/abs/1011.4735), [doi:10.1007/BF02104916](https://doi.org/10.1007/BF02104916)&rbrack;

* {#dcct13} [[Urs Schreiber]], *[[schreiber:dcct|differential cohomology in a cohesive topos]]* (2013-)

The definition of adjusted $\mathfrak{g}$-Weil algebras by requiring well-behaved [[BRST-complexes]] for [[L-infinity algebra valued differential forms|$L_\infty$-algebra valued differential forms]]:

* {#SaemannSchmidt20} [[Christian Saemann]], [[Lennart Schmidt]], *Towards an M5-Brane Model II: Metric String Structures*, Fortschr. Phys. **68** (2020) 2000051 &lbrack;[arXiv:1908.08086](https://arxiv.org/abs/1908.08086), [doi:10.1002/prop.202000051](https://doi.org/10.1002/prop.202000051)&rbrack;

Application to [[higher parallel transport]]:

* {#KimSaemann20} [[Hyungrok Kim]], [[Christian Saemann]], *Adjusted Parallel Transport for Higher Gauge Theories*, J. Phys. A **52** (2020) 445206 &lbrack;[arXiv:1911.06390](https://arxiv.org/abs/1911.06390), [doi:10.1088/1751-8121/ab8ef2](https://doi.org/10.1088/1751-8121/ab8ef2)&rbrack;

Survey and review:

* [[Christian Saemann]], *Adjusted Higher Gauge Theory: Connections and Parallel Transport* Lisbon (2021) &lbrack;[pdf](https://math.tecnico.ulisboa.pt/seminars/download.php?fid=1485), [[Saemann-AdjustedHGT.pdf:file]]&rbrack;


<table>
<tr><th markdown="1" style="white-space: nowrap;">$n$&#8594;<br/>$r$&#8595;</th>
  <th markdown="1">$-2$</th>
  <th markdown="1">$-1$</th>
  <th markdown="1">$0$</th>
  <th markdown="1">$1$</th>
  <th markdown="1">$2$</th>
  <th markdown="1">...</th>
  <th markdown="1">$\infty$</th></tr>
<tr><th markdown="1">$0$</th>
  <td>[[point]]</td>
  <td>[[truth value]]</td>
  <td>[[set]]</td>
  <td>[[groupoid]]</td>
  <td>[[2-groupoid]]</td>
  <td>...</td>
  <td>[[∞-groupoid]]</td></tr>
<tr><th markdown="1">$1$</th>
  <td>"</td>
  <td>"</td>
  <td>[[partial order|poset]]</td>
  <td>[[category]]</td>
  <td>[[(2,1)-category]]</td>
  <td>...</td>
  <td>[[(∞,1)-category]]</td></tr>
<tr><th markdown="1">$2$</th>
  <td>"</td>
  <td>"</td>
  <td>"</td>
  <td>[[2-poset]]</td>
  <td>[[2-category]]</td>
  <td>...</td>
  <td>[[(∞,2)-category]]</td></tr>
<tr><th markdown="1">$3$</th>
  <td>"</td>
  <td>"</td>
  <td>"</td>
  <td>"</td>
  <td>[[3-poset]]</td>
  <td>...</td>
  <td>[[(∞,3)-category]]</td></tr>
<tr><th markdown="1">&#8942;</th>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8945;</td>
  <td>&#8942;</td></tr>
<tr><th markdown="1">$\infty$</th>
  <td>point</td>
  <td>truth value</td>
  <td>poset</td>
  <td>2-poset</td>
  <td>3-poset</td>
  <td>...</td>
  <td>[[(∞,∞)-category]]/[[∞-poset]]</td></tr>
</table>


$\max(1, x + 2)$

$\forall x. \; x = x$


$\phi \colon \Omega \;\;|\; (\!\triangleright \phi) \Rightarrow \phi \;\;\;\;\;\vdash\;\;\;\;\; \phi$


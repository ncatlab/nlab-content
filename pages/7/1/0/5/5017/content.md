+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, the **Haefliger groupoid** $\Gamma^n$ is the [[groupoid]] whose set of [[objects]] is the [[Cartesian space]] $\mathbb{R}^n$ and for which a [[morphism]] $x \to y$ is a [[germ]] of a [[diffeomorphism]] $(\mathbb{R}^n ,x) \to (\mathbb{R}^n ,y)$.

This is regarded as a [[topological groupoid|topological]] or [[Lie groupoid|Lie]] [[étale groupoid]] via the canonical [[topological space|topology]]/[[smooth structure]] on $(\Gamma^n)_0 = \mathbb{R}^n$ and taking $s \colon (\Gamma^n)_1 \to (\Gamma^n)_0$ to be the [[étale space]] [associated](etale+space#RelationToSheaves) to the [[sheaf]] on $\mathbb{R}^n$ (with its canonical [[open cover]] [[Grothendieck topology]]) which is the [[sheafification]] of the presheaf that sends $U \subset \mathbb{R}^n$ to the set of all open [[embedding of differentiable manifolds|embeddings]] of $U$ into $\mathbb{R}^n$.

The [[smooth stack]] represented by the smooth Haefliger groupoid is also called the _Haefliger stack_.

=--


## Variants and Generalizations 
 {#Variants}

+-- {: .num_remark}
###### Remark

There is also the full smooth structure on the space of germs of diffeomorphisms. This gives a Lie groupoid whose underlying bare groupoid is the same as that of the Haefliger groupoid, but whose smooth structure is different.

=--


+-- {: .num_remark}
###### Remark

More generally for a given [[integrable G-stucture]] there is a corresponding Haefliger groupoid, for instance for [[symplectic structures]].

=--

+-- {: .num_remark}
###### Remark

Instead of considering [[germs]] of local diffeomorphisms one may consider (just) order-$k$ [[jets]] of these. The resulting Lie groupoids are known as [[jet groupoids]] (see [Lorenz 09](#Lorenz09))

=--



## Properties

### Classification of foliations

The Haefliger groupoid classifies [[foliations]]. See at _[[Haefliger theorem]]_.

### Universal characterization

Consider in the following the union $\mathcal{H}$ of Haefliger groupoids over all $n$.

+-- {: .num_prop #HIsTerminalInEtaleEtale}
###### Proposition

The Haefliger stack is a [[terminal object]] in the [[2-category]] of [[étale stacks]] on the site of [[smooth manifolds]] with [[étale morphisms]] between them. 

=--

([Carchedi 12, theorem 3.3.](#Carchedi12))

This implies ([Carchedi 12, 3,2](#Carchedi12))

+-- {: .num_theorem #StacksOnEtaleSiteAndEtaleStacks}
###### Theorem

There is an equivalence 

$$
  \Theta \colon St(SmthMfd^{et}) \simeq EtSt(SmthMfd)^{et} 
$$

between [[stacks]] on the [[site]] of smooth manifolds with [[local diffeomorphisms]] between them and [[étale stacks]] with [[étale morphisms]] between them inside all [[smooth stacks]].

=--

([Carchedi 12, theorem 1.3](#Carchedi12))

+-- {: .num_remark}
###### Remark

This in turn implies for instance that the Haefliger groupoid for [[complex structures]] ([Carchedi 12, p. 38](#Carchedi12)) is simply the image under the equivalence $\Theta$ in theorem \ref{StacksOnEtaleSiteAndEtaleStacks} of the sheaf on $SmthMfd^{et}$ which sends each smooth manifold to its set of [[complex structures]]. (...)

=--

### Sheaves and stacks on the Haefliger groupoid.

Consider in the following the union $\mathcal{H}$ of Haefliger groupoids over all $n$.

+-- {: .num_prop #HIsTerminalInEtaleEtale}
###### Proposition

The [[category of sheaves]] over $\mathcal{H}$ is equivalently the category of sheaves on the [[site]] of [[smooth manifolds]] with [[local diffeomorphism]] between them. 

=--

([Carchedi 12, theorem 3.1](#Carchedi12)).

+-- {: .num_prop }
###### Proposition

The [[2-topos]] over the Haefliger stack is equivalent to the 2-topos over the site $SmthMfd^{et}$ of smooth manifolds with local diffeomorphisms between them:

$$
  St(\mathcal{H}) \simeq St(SmthMfd^{et})
$$

=--

([Carchedi 12, 3.2](#Carchedi12)).


## References

Original articles:

* [[André Haefliger]], _Homotopy and integrability_,  In: N.H. Kuiper (ed.) _Manifolds_ — Amsterdam 1970. Lecture Notes in Mathematics, vol 197. Springer 1971 ([doi:10.1007/BFb0068615](https://doi.org/10.1007/BFb0068615))

* [[André Haefliger]], _Groupo&#239;des d'holonomie et espaces classiants_ , Ast&#233;risque 116 (1984), 70-97 ([numdam:AST_1984__116__70_0](http://www.numdam.org/item/?id=AST_1984__116__70_0))

* [[Raoul Bott]], _Lectures on characteristic classes and foliations_, Springer LNM 279, 1-94 ([doi:10.1007/BFb0058509](https://doi.org/10.1007/BFb0058509))

A textbook account is in 

* [[Ieke Moerdijk]], [[Janez Mrčun]], _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0

See also

* Wikipedia, _[Haefliger structure](http://en.wikipedia.org/wiki/Haefliger_structure)_


Discussion in a broader context of [[étale stacks]] and [[étale ∞-stacks]]:

* {#Carchedi12} [[David Carchedi]], section 2.2, section 3 of: _&#201;tale Stacks as Prolongations_, Advances in Mathematics Volume 352, 20 August 2019, Pages 56-132 ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))

* [[David Carchedi]], p. 104-105 of: _Higher Orbifolds and Deligne-Mumford Stacks as Structured Infinity-Topoi_, Memoirs of the American Mathematical Society 2020; 120 ([arXiv:1312.2204](https://arxiv.org/abs/1312.2204), [ISBN:978-1-4704-5810-2](https://bookstore.ams.org/memo-264-1282))

* {#Carchedi15} [[David Carchedi]], _On The Homotopy Type of Higher Orbifolds and Haefliger Classifying Spaces_, Advances of Mathematics, Volume 294, 2016, Pages 756-818 ([arXiv:1504.02394](http://arxiv.org/abs/1504.02394))


Discussion of [[jet groupoids]] includes

* {#Lorenz09} Arne Lorenz, _Jet Groupoids, Natural Bundles
and the Vessiot Equivalence Method_, Thesis ([pdf](http://wwwb.math.rwth-aachen.de/~arne/Dissertation_Lorenz_Arne.pdf)) 2009

The [[geometric realization]]/[[shape modality]] for Haefliger-type groupoids is discussed in

* {#Carchedi15} [[David Carchedi]], _On The Homotopy Type of Higher Orbifolds and Haefliger Classifying Spaces_ ([arXiv:1504.02394](http://arxiv.org/abs/1504.02394))




[[!redirects Haefliger groupoids]]

[[!redirects Haefliger stack]]
[[!redirects Haefliger stacks]]
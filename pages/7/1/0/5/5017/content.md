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

For $n \in \mathbb{N}$, the **Haefliger groupoid** $\Gamma^n$ is the [[groupoid]] whose set of [[objects]] is the [[Cartesian space]] $\mathbb{R}^n$ and for which a [[morphism]] $x \to y$ is a [[germ]] of a [[diffeomorphism]] $(\mathbb{R}^n ,x) \to (\mathbb{R}^n ,y)$.

## Properties

### Geometric structure

The Haefliger groupoid is naturally a [[topological groupoid]]. As such it is an [[étale groupoid]].

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

Original articles include

* [[André Haefliger]], _Groupo&#239;des d'holonomie et espaces classiants_ , Ast&#233;risque 116 (1984), 70-97

* [[Raoul Bott]], _Lectures on characteristic classes and foliations_ , Springer LNM 279, 1-94

A textbook account is in 

* [[Ieke Moerdijk]], [[Janez Mrčun]], _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0

Discussion in a broader context of [[étale stacks]] is in

* {#Carchedi12} [[David Carchedi]], section 2.2, section 3 of _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))


See also

* Wikipedia, _[Haefliger structure](http://en.wikipedia.org/wiki/Haefliger_structure)_

Discussion of [[jet]]-restrictions of the Haefliger groupoid is in 

* Arne Lorenz, _Jet Groupoids, Natural Bundles
and the Vessiot Equivalence Method_, Thesis ([pdf](http://wwwb.math.rwth-aachen.de/~arne/Dissertation_Lorenz_Arne.pdf))


[[!redirects Haefliger groupoids]]
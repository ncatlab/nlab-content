
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]]. Then the [[(∞,1)-categories]] of non-negatively graded [[sequential diagram|sequences]] in $C$ is [[equivalence of (∞,1)-categories|equivalent]] to the [[(∞,1)-category]] of [[simplicial objects in an (∞,1)-category]] in $\mathcal{C}$

$$
  Fun(N(\mathbb{Z}_{\geq 0}), C)
  \simeq
  Fun(N(\Delta)^{op}, C)  
  \,.
$$

Under this equivalence, a [[simplicial object]] $X_\bullet$ is sent to the [[sequential diagram|sequence]] of [[geometric realizations]] ([[(∞,1)-colimits]]) of its [[simplicial skeleta]]

$$
  {\vert sk_0 X_\bullet \vert} \to {\vert sk_1 X_\bullet \vert} \to {\vert sk_2 X_\bullet \vert} \to \cdots
  \,.
$$

This constitutes a [[filtered object in an (infinity,1)-category|filtering]] on the [[geometric realization]] of $X_\bullet$ itself

$$
  {\vert X_\bullet \vert}
  \simeq
  \underset{\longrightarrow}{\lim}_n {\vert sk_n X_\bullet \vert}
  \,.
$$

=--

([[Higher Algebra|Higher Algebra, theorem 1.2.4.1]])

+-- {: .num_remark }
###### Remark

Given a [[simplicial objects in an (∞,1)-category|simplicial object]] $X_\bullet$ in a [[stable (∞,1)-category]] $\mathcal{C}$, its image in the [[triangulated category|triangulated]] [[homotopy category of an (∞,1)-category|homotopy category]] $Ho(\mathcal{C})$ is identified by the 
ordinary [[Dold-Kan correspondence]] with a [[chain complex]]. On the other hand, by the discussion at [[spectral sequence of a filtered stable homotopy type]] in the section _[Filtered objects and their chain complexes](spectral+sequence+of+a+filtered+stable+homotopy+type#FilteredObjectsAndTheirChainComplexes)_, the skelton sequence $sk_\bullet X_\bullet$ also induces a chain complex. These are [[natural isomorphism|naturally isomorphic]].

In particular therefore first page of the _[[spectral sequence of a filtered stable homotopy type]]_ associated with the [[simplicial skeleton]] filtration consists of the [[Moore complexes]] of the [[simplicial objects]] $\pi_q(X_\bullet) \in \mathcal{A}^{\Delta^{op}}$

$$
  E_1^{\bullet,q} \simeq N(\pi_q X_\bullet)
  \,.
$$


=--

([[Higher Algebra|Higher Algebra, remark 1.2.4.3, 1.2.4.4]])

## Applications

* [[J-homomorphism and chromatic homotopy]]

## Related concepts

* [[spectral sequence of a simplicial stable homotopy type]]

* [[stable Dold-Kan correspondence]]


## References

  This _infinity-Dold-Kan correspondence_ is [theorem 12.8, p. 50](http://www.math.harvard.edu/~lurie/topoibook/DAGI.pdf) of 

* [[Jacob Lurie]], _[[Stable ∞-Categories]]_

later absorbed in

* [[Jacob Lurie]], section 1.2.4 of _[[Higher Algebra]]_

[[!redirects ∞-Dold-Kan correspondence]]

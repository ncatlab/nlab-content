
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Generally, the _McKay correspondence_ concerns identifications between [[linear representations]] of [[finite subgroups of SU(2)]], $G \subset SU(2)$ with [[cohomology]] of the [[blow-up]] [[resolution of singularities|resolution]] $\tilde X$ of the corresponding [[ADE-singularity]] [[orbifold]] $X \sslash G \coloneqq \mathbb{C}^2\sslash G$.

A strong version of the McKay correspondence is obtained when the [[cohomology theory]] is taken to be ([[equivariant K-theory|equivariant]]) _[[K-theory]]_ ([Gonzalez-Sprinberg & Verdier 83](#GSV83)): 

Here the McKay correspondence becomes an [[isomorphism]] between the [[equivariant K-theory]] $K_{G_{ADE}}(\ast)$ of an [[ADE-singularity]] (equivalently the [[representation ring]] $R(G_{ADE})$) to the plain [[K-theory]] $K(\tilde X)$ of its [[blow-up]] [resolution](ADE+singularity#ResolutionBySpheresTouchingAlongADynkinDiagram) $\tilde X$. Much like in [[topological T-duality]], this isomorphism is given by [[integral transform]] ([[Fourier-Mukai transform]]) through the canonical [[correspondence]] that these spaces constitute:

$$
  \array{
     &&
     && K( X \times_{X/G} \tilde X )
     \\
     && 
     & {}^{\mathllap{ p_1^\ast }}\nearrow && \searrow^{\mathrlap{Inv \circ (p_2)_\ast}}
     \\
     R(G) \simeq K_G(\ast) &\simeq& K_G(X) && \overset{\simeq}{\longrightarrow}  && K(\tilde X)
  }
$$

In terms of [[physics]] ([[string theory]]), the [[K-theory]] classes appearing here may be interpreted as [[groups]] of [[fractional D-brane|fractional]] [[D-brane charges]] (see [there](fractional+D+brane#DBranesAtOrbifoldSingularities)).
In terms of the [[worldvolume]] [[Chan-Paton gauge field|Chan-Paton]]-[[Yang-Mills theory]] on the D-branes the McKay correspondence is then seen as passage from the [[Higgs branch]] to the [[Coulomb branch]] (see [there](fractional+D-brane#InTermsOfTheWorldvolumeGaugeTheories)).

The proof of these statemens generally proceeds by relating both sides of the equivalence to [[Dynkin diagrams]] of [[ADE-classification|ADE-type]].

The classical McKay correspondence, named after [[John McKay]], is a one-to-one correspondence between the [[McKay graphs]] of [[finite group|finite]] [[subgroups]] $G \subset \text{SL}_2(\mathbb{C})$ and the extended Dynkin diagrams of ADE type.

### Construction

Take $G\subset \text{SL}_2(\mathbb{C})$ finite. Then, let $\rho_0, ..., \rho_n$ denote the irreducible representations of $G$, with $\rho_0$ being the trivial representation. Then, set $\langle \rho_i \otimes \mathbb{C}^2, \rho_j \rangle = m_{i j}$. Since $\mathbb{C}^2$ is self-dual, as it admits an invariant non-degenerate skew-symmetric bilinear form, $m_{i j} = m_{j i}$. Finally, consider the vertices $v_0, ..., v_n$ with $m_{i j}$ vertices between each $v_i$ and $v_j$. Furthermore, for $m_{i j} = 1$, we do not need to write the weight of the corresponding arrow. The resulting graph is the [[McKay graph]] of $G$.


(...)

### Interpretation in K-theory

In ([Gonzalez-Sprinberg & Verdier 83](#GSV83)) the McKay correspondence is interpreted as an isomorphism on [[K-theory]], based on the observation that the [[representation ring]] of $G$ is equal to the $G$-[[equivariant K-theory]] of $\mathbb{C}^2$. This is isomorphic to the ordinary K-theory of the minimal resolution of the Kleinian singularity, $\mathbb{C}^2\sslash G$.




## Related concepts

* [[ADE classification]]

## References

Introductions and surveys include

* Graham Leuschke, _The McKay correspondence_ ([pdf](http://www.leuschke.org/uploads/McKay-total.pdf))

* Drew Armstrong, _Lectures on the McKay correspondence_, 2015 ([pdf scan of notes](http://www.math.miami.edu/~armstrong/Talks/McKay_Talca.pdf))

* [[John Baez]], _The Geometric McKay Correspondence_, ([Part I](https://golem.ph.utexas.edu/category/2017/06/the_geometric_mckay_correspond.html), [Part II](https://golem.ph.utexas.edu/category/2017/07/the_geometric_mckay_correspond_1.html))

Literature collection

* [[Miles Reid]], _[Links to papers on McKay correspondence](homepages.warwick.ac.uk/staff/Miles.Reid/McKay/)_

As an isomorphism between the [[equivariant K-theory]] of [[ADE-singularity]] and the plain [[topological K-theory]] of its [resolution](ADE singularity#ResolutionBySpheresTouchingAlongADynkinDiagram), the McKay correspondence is proven in:

* {#GSV85} [[Gérard Gonzalez-Sprinberg]], [[Jean-Louis Verdier]], _Construction géométrique de la correspondance de McKay_, Ann. Sci. ́École Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))

An analogous discussion for [[derived categories]] of coherent sheaves is in

* [[Tom Bridgeland]], [[Alastair King]], [[Miles Reid]], _The McKay correspondence as an equivalence of derived categories_ ([pdf](http://www.ams.org/journals/jams/2001-14-03/S0894-0347-01-00368-X/S0894-0347-01-00368-X.pdf))


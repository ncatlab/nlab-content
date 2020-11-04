
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
 {#Idea}

Generally, the _McKay correspondence_ is a subtle correspondence between the theory of [[finite subgroups of SU(2)]], the corresponding [[orbifold]] [[singularities]] ([[du Val singularities]]) and that of [[simple Lie groups]] falling into the [[ADE classification]].

[[!include ADE -- table]]

The correspondence may be understood at different levels:

1. **McKay quivers.** The original correspondence due to [McKay 80](#McKay80) is the observation that the [[McKay quiver]] associated to the [[orbifold]] [[singularity]] $\mathbb{C}^2 \sslash G$ of a [[finite subgroup of SU(2)]] $G \subset SU(2)$ happens to be an extended [[Dynkin quiver]], hence happens to be an extended [[Dynkin diagram]] of the kind that also arises in the [[ADE-classification]] of [[simple Lie groups]].

   More on this in _[McKay quivers](#McKayQuivers)_, below.

1. **Equivariant K-theory.** A more conceptual explanation for this correspondence comes from the classical fact that the [[blow up]] $\widehat{\mathbb{C}^2\sslash G}$ of the [[ADE singularity]] $\mathbb{C}^2\sslash G$ is given by a sequence of [[spheres]] that touch along the vertices of the corresponding [[Dynkin quiver]]. In [Gonzalez-Sprinberg & Verdier 83](#GSV83) it was shown that the $G$-[[equivariant K-theory]] $K_G(\mathbb{C}^2)$ of the singularity is isomorphic to the [[K-theory]] of the desingularization $\widehat {\mathbb{C}^2\sslash G}$ such that under this isomorphism the generators of $K_G(\mathbb{C}^2) \simeq R_\mathbb{C}(G)$, hence of the [[representation ring]], hence the [[irreducible representations]], map to K-theory classes supported on the [[exceptional divisors]] of this blowup. This gives a conceptual geometric/cohomological explanation for the identifications observed by [McKay 80](#McKay80).

   More on this in _[As an equivalence of K-theories](#AsAnEquivalenceOfKtheories)_


1. **Seiberg-Witten theory.** Under the interpretation of [[K-theory]]-classes as [[D-brane]] charges, the K-theoretic McKay correspondence of [Gonzalez-Sprinberg & Verdier 83](#GSV83) identifies [[wrapped brane]] charges of the desingularized space with [[fractional brane]] charges at the singularity.

   This leads to a further (currently non-rigorous) explanation of the McKay correspondence in terms of the [[AdS-CFT duality|dual]] [[worldvolume]] [[quantum field theories]] on these branes, which are [[N=2 D=4 super Yang-Mills theory|N=2]] [[quiver gauge theories]]: The [[moduli space]] of [[scalar fields]] of these theories has two "branches", called the _[[Higgs branch]]_ and the _[[Coulomb branch]]_, and the idea is that depending on which of the branches the [[vacuum state]] of the theory is in, it describes the brane as being either on the [[ADE singularity]] or on its [[resolution of singularities|resolution]], but since it's the same quantum field theory in both cases, these two situations are actually suitably equivalent.

  More on this in _[Via N=2 SYM theory](#ViaSuperYangMillsTheory)_ below.


### Via McKay quivers
 {#McKayQuivers}


Generally, for $G$ a [[finite group]] and $V$ a [[linear representation]] of $G$ on a [[finite dimensional vector space|finite dimensional]] [[complex vector space]], the _[[McKay quiver]]_ or _[[McKay graph]]_ associated with $V$ is the [[quiver]] whose [[vertices]] correspond to the [[irreducible representations]] $\rho_i$ of $G$ and which has $a_{i j} \in \mathbb{N}$ [[edges]] between the $i$th and the $j$th vertex, for $a_{i j}$ the [[coefficients]] in the expansion into [[irreps]] of the [[tensor product of representations]] of $V$ with these irreps:

$$
  V \otimes \rho_i
  \;\simeq\;
  \underset{j}{\bigoplus}
  a_{i j} \cdot \rho_j
  \,.
$$

Specifically this applies to the special case where $G \subset $ [[SU(2)]] a [[finite subgroup of SU(2)]] and $V$ its defining representation on $\mathbb{C}^2$. 

The original _McKay correspondence_ ([McKay 80](#McKay80)) states that in this case the corresponding [[McKay quivers]] are [[Dynkin quivers]]/[[Dynkin diagrams]] in the same [[ADE classification]] as the [[ADE singularity]] $\mathbb{C}^2 \sslash G$.

More precisely: If one uses _all_ [[irreducible representations]] including the 1-dimensiona [[trivial representation]] $\rho_0$ then one gets the "extended Dynkin diagram", where the extra node corresponds to $\rho_0$. This is the vertex indicated by a cross in the following diagrams:


\begin{center}
<img src="https://ncatlab.org/nlab/files/ExtendedADEQuivers.jpg" width="400">
\end{center}

> graphics grabbed from [GSV 83, p. 4](#GSV83)

In particular, for $G =\mathbb{Z}_N \subset SU(2)$ a [[cyclic group]] of [[order of a group|order]] $N$, there are $N$ complex [[irreps]] and the McKay quiver, i.e. the extended Dynkin diagram, has $N$-vertices, connected by edges to form a circle.



### As an equivalence of K-theories
 {#AsAnEquivalenceOfKtheories}

A strong version of the McKay correspondence is obtained when the [[cohomology theory]] is taken be ([[equivariant K-theory|equivariant]]) _[[K-theory]]_ ([Gonzalez-Sprinberg & Verdier 83](#GSV83)): 

Here the McKay correspondence becomes an [[isomorphism]] between the [[equivariant K-theory]] $K_{G_{ADE}}(\ast)$ of an [[ADE-singularity]] (equivalently the [[representation ring]] $R(G_{ADE})$) and the plain [[K-theory]] $K(\tilde X)$ of its [[blow-up]] [resolution](ADE+singularity#ResolutionBySpheresTouchingAlongADynkinDiagram) $\tilde X$. Much like in [[topological T-duality]], this isomorphism is given by [[integral transform]] ([[Fourier-Mukai transform]]) through the canonical [[correspondence]] that these spaces constitute:

\[
  \label{KMcKay}
  \array{
     &&
     && K( X \times_{X/G} \tilde X )
     \\
     && 
     & {}^{\mathllap{ p_1^\ast }}\nearrow && \searrow^{\mathrlap{Inv \circ (p_2)_\ast}}
     \\
     R(G) \simeq K_G(\ast) &\simeq& K_G(X) && \overset{\simeq}{\longrightarrow}  && K(\tilde X)
  }
\]

In terms of [[physics]] ([[string theory]]), the [[K-theory]] classes appearing here may be interpreted as [[groups]] of [[fractional D-brane|fractional]] [[D-brane charges]] (see [there](fractional+D-brane#DBranesAtOrbifoldSingularities)).
In terms of the [[worldvolume]] [[Chan-Paton gauge field|Chan-Paton]]-[[Yang-Mills theory]] on the D-branes the McKay correspondence is then seen as passage from the [[Higgs branch]] to the [[Coulomb branch]] (see [there](fractional+D-brane#InTermsOfTheWorldvolumeGaugeTheories)).

The proof of these statements generally proceeds by relating both sides of the equivalence to [[Dynkin diagrams]] of [[ADE-classification|ADE-type]].

The classical McKay correspondence, named after [[John McKay]], is a one-to-one correspondence between the [[McKay graphs]] of [[finite group|finite]] [[subgroups]] $G \subset \text{SL}_2(\mathbb{C})$ and the extended Dynkin diagrams of ADE type.



### Via $N=2 $ super Yang-Mills theory
 {#ViaSuperYangMillsTheory}

Various seemingly unrelated structures in mathematics fall into an [[ADE classification]]. Notably [[finite group|finite]] [[subgroups]] of [[special unitary group|SU(2)]] and [[compact Lie group|compact]] [[simple Lie groups]] do. The way this works usually is that one tries to classify these structures somehow, and ends up finding that the classification is governed by the combinatorics of [[Dynkin diagrams]].

While that does explain a bit, it seems the statement that both the [[icosahedral group]] and the Lie group [[E8]] are related to the same [[Dynkin diagram]] somehow is still more a question than an answer. Why is that so?

The first key insight is due to [Kronheimer 89](ADE+singularity#Kronheimer89a). He showed that the (resolutions of) the [[orbifold]] quotients $\mathbb{C}^2/\Gamma$ for finite subgroups $\Gamma$ of $SU(2)$ are precisely the generic form of the [[gauge group|gauge]] [[orbits]] of the [[direct product group]] of $U(n_i)$s acting in the evident way on the [[direct sum]] of $Hom(\mathbb{C}^{n_i}, \mathbb{C}^{n_j})$-s, where $i$ and $j$ range over the vertices of the [[Dynkin diagram]], and $(i,j)$ over its edges.

This becomes more illuminating when interpreted in terms of [[gauge theory]]: in a [[quiver gauge theory]] the [[gauge group]] is a [[direct product group]] of  $U(n_i)$ factors associated with vertices of a [[quiver]], and the [[particles]] which are [[charged particle|charged]] under this gauge group arrange, as a [[linear representation]], into a [[direct sum]] of $Hom(\mathbb{C}^{n_i}, \mathbb{C}^{n_j})$-s, for each edge of the quiver. 

Pick one such particle, and follow it around as the gauge group transforms it. The space swept out is its gauge [[orbit]], and [Kronheimer 89](#Kronheimer89) says that if the quiver is a Dynkin diagram, then this gauge orbit looks like $\mathbb{C}^2/\Gamma$.

On the other extreme, gauge theories are of interest whose gauge group is not a big direct product, but is a [[simple Lie group]], such as [[special unitary group|SU(N)]] or [[E8]]. The mechanism that relates the two classes of examples is [[spontaneous symmetry breaking]] ("[[Higgs field|Higgsing]]"): the ground state energy of the field theory may happen to be achieved by putting the fields at any one point in a higher dimensional space of field configurations, acted on by the gauge group, and fixing any one such point "spontaneously" singles out the corresponding [[stabilizer subgroup]]. 

Now here is the final ingredient: [[N=2 D=4 super Yang-Mills theory]] ("[[Seiberg-Witten theory]]"). These theories have a [[potential energy|potential]] such that its [[vacua]] break a simple gauge group, such as $SU(N)$, down to a [[Dynkin diagram]] [[quiver gauge theory]]. One place where this is reviewed, physics style, is in [Albertsson 03, section 2.3.4](N=2+D=4+super+Yang-Mills+theory#Albertsson03).

More precisely, these theories have two different kinds of vacua, those on the "[[Coulomb branch]]" and those on the "[[Higgs branch]]" depending on whether the scalars of the "[[vector multiplets]]" (the gauge field sector) or of the "[[hypermultiplet]]" (the matter field sector) vanish. The statement above is for the Higgs branch, but the Coulomb branch is supposed to behave "dually".

So that then finally is the relation, in the ADE classification, between the simple Lie groups and the finite subgroups of SU(2): start with an N=2 super Yang Mills theory with gauge group a simple Lie group. Let it spontaneously find its vacuum and consider the orbit space of the remaining spontaneously broken symmetry group. That is (a resolution of) the orbifold quotient of $\mathbb{C}^2$ by a discrete subgroup of $SU(2)$.



## Related concepts

* [[McKay quiver]]

* [[ADE classification]]

* [[quiver gauge theory]]

* [[wrapped brane]]


## References

The original article is

* {#McKay80} [[John McKay]], _Graphs, singularities, and finite groups_ Proc. Symp. Pure Math. Vol. 37. No. 183. 1980

As an isomorphism between the [[equivariant K-theory]] of [[ADE-singularity]] and the plain [[topological K-theory]] of its [resolution](ADE+singularity#ResolutionBySpheresTouchingAlongADynkinDiagram), the McKay correspondence is proven in:

* {#GSV83} [[Gérard Gonzalez-Sprinberg]], [[Jean-Louis Verdier]], _Construction géométrique de la correspondance de McKay_, Ann. Sci. ́École Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))

An analogous discussion for [[derived categories]] of coherent sheaves is in

* [[Tom Bridgeland]], [[Alastair King]], [[Miles Reid]], _The McKay correspondence as an equivalence of derived categories_ ([pdf](http://www.ams.org/journals/jams/2001-14-03/S0894-0347-01-00368-X/S0894-0347-01-00368-X.pdf))

See also:

* Duiliu-Emanuel Diaconescu, Mauro Porta, Francesco Sala, _McKay correspondence, cohomological Hall algebras and categorification_ ([arXiv:2004.13685](https://arxiv.org/abs/2004.13685))



Introductions and surveys include

* Graham Leuschke, _The McKay correspondence_ ([pdf](http://www.leuschke.org/uploads/McKay-total.pdf))

* Bockland, _Character tables and McKay quivers_ ([pdf](https://staff.fnwi.uva.nl/r.r.j.bocklandt/notes/kleinian.pdf))

* Drew Armstrong, _Lectures on the McKay correspondence_, 2015 ([pdf scan of notes](http://www.math.miami.edu/~armstrong/Talks/McKay_Talca.pdf))

* Max Lindh, _An Introduction to the McKay Correspondence
Master Thesis in Physics_ ([pdf](http://www.diva-portal.org/smash/get/diva2:1184051/FULLTEXT01.pdf))

* [[John Baez]], _The Geometric McKay Correspondence_, ([Part I](https://golem.ph.utexas.edu/category/2017/06/the_geometric_mckay_correspond.html), [Part II](https://golem.ph.utexas.edu/category/2017/07/the_geometric_mckay_correspond_1.html))

Literature collection:

* [[Miles Reid]], _[Links to papers on McKay correspondence](http://homepages.warwick.ac.uk/staff/Miles.Reid/McKay/)_



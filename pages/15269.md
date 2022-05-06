
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

Generally, the _McKay correspondence_ concerns identifications between [[linear representations]] of [[finite subgroups of SU(2)]], $G \subset SU(2)$ with [[cohomology]] of the [[blow-up]] [[resolution of singularities|resolution]] $\tilde X$ of the corresponding [[ADE-singularity]] [[orbifold]] $X \sslash G \coloneqq \mathbb{C}^2\sslash G$.

A strong version of the McKay correspondence is obtained when the [[cohomology theory]] is taken be ([[equivariant K-theory|equivariant]]) _[[K-theory]]_ ([Gonzalez-Sprinberg & Verdier 83](#GSV83)): 

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

In terms of [[physics]] ([[string theory]]), the [[K-theory]] classes appearing here may be interpreted as [[groups]] of [[fractional D-brane|fractional]] [[D-brane charges]] (see [there](fractional+D-brane#DBranesAtOrbifoldSingularities)).
In terms of the [[worldvolume]] [[Chan-Paton gauge field|Chan-Paton]]-[[Yang-Mills theory]] on the D-branes the McKay correspondence is then seen as passage from the [[Higgs branch]] to the [[Coulomb branch]] (see [there](fractional+D-brane#InTermsOfTheWorldvolumeGaugeTheories)).

The proof of these statements generally proceeds by relating both sides of the equivalence to [[Dynkin diagrams]] of [[ADE-classification|ADE-type]].

The classical McKay correspondence, named after [[John McKay]], is a one-to-one correspondence between the [[McKay graphs]] of [[finite group|finite]] [[subgroups]] $G \subset \text{SL}_2(\mathbb{C})$ and the extended Dynkin diagrams of ADE type.

### Construction

Take $G\subset \text{SL}_2(\mathbb{C})$ finite. Then, let $\rho_0, ..., \rho_n$ denote the irreducible representations of $G$, with $\rho_0$ being the trivial representation. Then, set $\langle \rho_i \otimes \mathbb{C}^2, \rho_j \rangle = m_{i j}$. Since $\mathbb{C}^2$ is self-dual, as it admits an invariant non-degenerate skew-symmetric bilinear form, $m_{i j} = m_{j i}$. Finally, consider the vertices $v_0, ..., v_n$ with $m_{i j}$ vertices between each $v_i$ and $v_j$. Furthermore, for $m_{i j} = 1$, we do not need to write the weight of the corresponding arrow. The resulting graph is the [[McKay graph]] of $G$.


(...)

### Interpretation in K-theory

In ([Gonzalez-Sprinberg & Verdier 83](#GSV83)) the McKay correspondence is interpreted as an isomorphism on [[K-theory]], based on the observation that the [[representation ring]] of $G$ is equal to the $G$-[[equivariant K-theory]] of $\mathbb{C}^2$. This is isomorphic to the ordinary K-theory of the minimal resolution of the Kleinian singularity, $\mathbb{C}^2\sslash G$.

See [above](#Idea)


### Via $N=2 $ super Yang-Mills theory
 {#ViaSuperYangMillsTheory}

Various seemingly unrelated structures in mathematics fall into an [[ADE classification]]. Notably [[finite group|finite]] [[subgroups]] of [[special unitary group|SU(2)]] and [[compact Lie group|compact]] [[simple Lie groups]] do. The way this works usually is that one tries to classify these structures somehow, and ends up finding that the classification is governed by the combinatorics of [[Dynkin diagrams]].

While that does explain a bit, it seems the statement that both the [[icosahedral group]] and the Lie group [[E8]] are related to the same [[Dynkin diagram]] somehow is still more a question than an answer. Why is that so?

The first key insight is due to [Kronheimer 89](ADE+singularity#Kronheimer89a). He showed that the (resolutions of) the [[orbifold]] quotients $\mathbb{C}^2/\Gamma$ for finite subgroups $\Gamma$ of $SU(2)$ are precisely the generic form of the [[gauge group|gauge]] [[orbits]] of the [[direct product group]] of $U(n_i)$s acting in the evident way on the [[direct sum]] of $Hom(\mathbb{C}^{n_i}, \mathbb{C}^{n_j})$-s, where $i$ and $j$ range over the vertices of the [[Dynkin diagram]], and $(i,j)$ over its edges.

This becomes more illuminating when interpreted in terms of [[gauge theory]]: in a [[quiver gauge theory]] the [[gauge group]] is a [[direct product group]] of  $U(n_i)$ factors associated with vertices of a [[quiver]], and the [[particles]] which are [[charged particle|charged]] under this gauge group arrange, as a [[linear representation]], into a [[direct sum]] of $Hom(\mathbb{C}^{n_i}, \mathbb{C}^{n_j})$-s, for each edge of the quiver. 

Pick one such particle, and follow it around as the gauge group transforms it. The space swept out is its gauge [[orbit]], and [Kronheimer 89](#Kronheimer89) says that if the quiver is a Dynkin diagram, then this gauge orbit looks like $\mathbb{C}^2/\Gamma$.

On the other extreme, gauge theories are of interest whose gauge group is not a big direct product, but is a [[simple Lie group]], such as [[special unitary group|SU(N)]] or [[E8]]. The mechanism that relates the two classes of examples is [[spontaneous symmetry breaking]] ("[[Higgs field|Higgsing]]"): the ground state energy of the field theory may happen to be achieved by putting the fields at any one point in a higher dimensional space of field configurations, acted on by the gauge group, and fixing any one such point "spontaneously" singles out the corresponding [[stabilizer subgroup]]. 

Now here is the final ingredient: it is [[N=2 D=4 super Yang-Mills theory]] ("[[Seiberg-Witten theory]]") which have a potential that is such that its [[vacua]] break a simple gauge group such as $SU(N)$ down to a Dynkin diagram [[quiver gauge theory]]. One place where this is reviewed, physics style, is in [Albertsson 03, section 2.3.4](N=2+D=4+super+Yang-Mills+theory#Albertsson03).

More precisely, these theories have two different kinds of vacua, those on the "[[Coulomb branch]]" and those on the "[[Higgs branch]]" depending on whether the scalars of the "[[vector multiplets]]" (the gauge field sector) or of the "[[hypermultiplet]]" (the matter field sector) vanish. The statement above is for the Higgs branch, but the Coulomb branch is supposed to behave "dually".

So that then finally is the relation, in the ADE classification, between the simple Lie groups and the finite subgroups of SU(2): start with an N=2 super Yang Mills theory with gauge group a simple Lie group. Let it spontaneously find its vacuum and consider the orbit space of the remaining spontaneously broken symmetry group. That is (a resolution of) the orbifold quotient of $\mathbb{C}^2$ by a discrete subgroup of $SU(2)$.



## Related concepts

* [[McKay quiver]]

* [[ADE classification]]

* [[quiver gauge theory]]

* [[wrapped brane]]


## References

Introductions and surveys include

* Graham Leuschke, _The McKay correspondence_ ([pdf](http://www.leuschke.org/uploads/McKay-total.pdf))

* Bockland, _Character tables and McKay quivers_ ([pdf](https://staff.fnwi.uva.nl/r.r.j.bocklandt/notes/kleinian.pdf))

* Drew Armstrong, _Lectures on the McKay correspondence_, 2015 ([pdf scan of notes](http://www.math.miami.edu/~armstrong/Talks/McKay_Talca.pdf))

* Max Lindh, _An Introduction to the McKay Correspondence
Master Thesis in Physics_ ([pdf](http://www.diva-portal.org/smash/get/diva2:1184051/FULLTEXT01.pdf))

* [[John Baez]], _The Geometric McKay Correspondence_, ([Part I](https://golem.ph.utexas.edu/category/2017/06/the_geometric_mckay_correspond.html), [Part II](https://golem.ph.utexas.edu/category/2017/07/the_geometric_mckay_correspond_1.html))

Literature collection

* [[Miles Reid]], _[Links to papers on McKay correspondence](http://homepages.warwick.ac.uk/staff/Miles.Reid/McKay/)_

As an isomorphism between the [[equivariant K-theory]] of [[ADE-singularity]] and the plain [[topological K-theory]] of its [resolution](ADE+singularity#ResolutionBySpheresTouchingAlongADynkinDiagram), the McKay correspondence is proven in:

* {#GSV83} [[Gérard Gonzalez-Sprinberg]], [[Jean-Louis Verdier]], _Construction géométrique de la correspondance de McKay_, Ann. Sci. ́École Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))

An analogous discussion for [[derived categories]] of coherent sheaves is in

* [[Tom Bridgeland]], [[Alastair King]], [[Miles Reid]], _The McKay correspondence as an equivalence of derived categories_ ([pdf](http://www.ams.org/journals/jams/2001-14-03/S0894-0347-01-00368-X/S0894-0347-01-00368-X.pdf))



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### D-branes at orbifold singularities
 {#DBranesAtOrbifoldSingularities}

For [[type II superstrings]] on a global [[orbifold]] [[spacetime]] $X\sslash G$, [[D-brane charge]] is measured by the [[equivariant K-theory]] $K_G(X)$. Under the canonical map $K(X/G) \longrightarrow K_G(X)$ from the plain [[topological K-theory]] of the [[quotient space]] irreducible elements of K-theory in general decompose into [[direct sums]] of smaller irreducible elements, hence into "smaller fractions stuck at the orbifold singularity" . 

At least some of these are associated with _fractional_ D-branes in the literature.


### D-branes on resolutions of orbifold singularities

Typically in the string theory literature, fractional D-branes are identified in a "[[duality in string theory|dual]]" formulation of the situation:

At least for $X  \simeq \mathbb{C}^2$ and $G$ a [[finite subgroup of SU(2)]] [[action|acting]] in the canonical way, hence for $X\sslash G$ an [[ADE-singularity]], the K-theoretic [[McKay correspondence]] ([Gonzalez-Sprinberg & Verdier 83](#GSV83)) identifies the [[equivariant K-theory]] of $X$ with the plain [[K-theory]] of a nice [[blow-up]] [[resolution of singularities|resolution]] $\tilde X$:

\[
  \label{KTheoreticMcKayIso}
  \array{
     &&
     && K( X \times_{X/G} \tilde S )
     \\
     && 
     & {}^{\mathllap{ p_1^\ast }}\nearrow && \searrow^{\mathrlap{Inv \circ (p_2)_\ast}}
     \\
     R(G) \simeq K_G(\ast) &\simeq& K_G(X) && \overset{\simeq}{\longrightarrow}  && K(\tilde X)
  }
\]


Under this [[equivalence]] ([[isomorphism]] of [[K-theory]] [[cohomology group|groups]]), fractional D-branes on the [[orbifold]] are identified with [[D-branes]] on $\tilde X$ which are [[wrapped brane|wrapped]] around some of the cycles in $\tilde X$ that appear through the [[blow-up]] of the [[ADE-singularity]] (in physics jargon these are the "vanishing cycles"). 

### In terms the worldvolume gauge theories
 {#InTermsOfTheWorldvolumeGaugeTheories}

In terms of the [[worldvolume]] [[gauge field theory]] the equivalence (eq:KTheoreticMcKayIso) between 

1. fractional D-branes stuck at [[orbifold]] [[singularities]] 

1. and [[wrapped branes]] on the [[blow-up]] [[resolution of singularities|resolution]] 

is supposed to be exhibited by passage from the [[Higgs branch]] to the [[Coulomb branch]]:

The first key insight is due to [Kronheimer 89](ALE+space#Kronheimer89). He showed that the (resolutions of) the orbifold quotients C^2/Gamma for $\Gamma$ a [[finite subgroup of SU(2)]] are precisely the generic form of the gauge orbits of the direct product of $U(n_i)$-s acting in the evident way on the direct sum of $Hom(C^{n_i}, C^{n_j})$-s, where $i$ and $j$ range over the [[vertices]] of the [[Dynkin diagram]], and $(i,j)$ over its [[edges]].

This becomes more illuminating when interpreted in terms of [[Yang-Mills theory|Yang-Mills]] [[gauge theory]]: in a "[[quiver gauge theory]]" the [[gauge group]] is a [[direct product group]] of [[circle group]] $U(n_i)$ factors associated with [[vertices]] of a [[quiver]], and the particles which are charged under this gauge group arrange, as a linear representation, into a [[direct sum]] of $Hom(C^{n_i}, C^{n_j})$-s, for each edge of the quiver. 

Pick one such particle, and follow it around as the gauge group transforms it. The space swept out is its gauge orbit, and Kronheimer says that if the quiver is a Dynkin diagram, then this gauge orbit looks like $\mathbb{C}^2/Gamma$.

On the other extreme, gauge theories are of interest whose gauge group is not a big direct product, but is a [[simple Lie group]], in the technical sense, such as the [[special unitary group]] $SU(N)$ or the [[exceptional Lie group]] $E_8$. The mechanism that relates the two classes of examples is [[spontaneous symmetry breaking]] ("[[Higgs mechanism|Higgsing]]"): the ground state energy of the field theory may happen to be achieved by putting the fields at any one point in a higher dimensional space of field configurations, acted on by the gauge group, and fixing any one such point "spontaneously" singles out the corresponding [[stabilizer subgroup]]. 

Now here is the final ingredient: it is [[N=2 super Yang-Mills theories]]  ("[[Seiberg-Witten theory]]") which have a potential that is such that its vacua break a simple gauge group such as $SU(N)$ down to a Dynkin diagram quiver gauge theory. One place where this is reviewed, physics style, is  [Albertsson 03, section 2.3.4](N=2+D=4+super+Yang-Mills+theory#Albertsson03).

More precisely, these theories have two different kinds of [[vacuum|vacua]], those on the "[[Coulomb branch]]" and those on the "[[Higgs branch]]" depending on whether the scalars of the "[[vector multiplets]]" (the gauge field sector) or of the "[[hypermultiplet]]" (the matter field sector) vanish. The statement above is for the Higgs branch, but the Coulomb branch is supposed to behave "dually".

So that then finally is the relation, in the [[ADE classification]], between the [[simple Lie groups]] and the [[finite subgroups of SU(2)]]: start with an [[N=2 super Yang-Mills theory]] with [[gauge group]] a [[simple Lie group]]. Let it spontaneously find its vacuum and consider the orbit space of the remaining spontaneously broken symmetry group. That is (a resolution of) the orbifold quotient of $\mathbb{C}^2$ by a [[finite subgroup of SU(2)]].



### Fractional M-branes

An analogous McKay correspondence for (fractional) [[M-branes]] 

<center>
<img src="http://ncatlab.org/nlab/files/ADESingularity.jpg" width="600" alt="ADE 2Cycle" />
</center>

> graphics grabbed from [HSS18](http://ncatlab.org/schreiber/show/Equivariant+homotopy+and+super+M-branes)


is considered informally in the [[string theory]] literature (for instance in discussion of [[M-theory on G2-manifolds]]) 
but has not been given a correspondingly precise cohomological formulation yet. 

## Related concepts

* [NS5 half-brane](NS5-brane#NSHalfBranes)


## References

Early discussion in physics language include

* [[Michael Douglas]], [[Brian Greene]], [[David Morrison]], _Orbifold Resolution by D-Branes_, Nucl.Phys.B506:84-106,1997 ([arXiv:hep-th/9704151](https://arxiv.org/abs/hep-th/9704151))

* Diaconescu, [[Michael Douglas]], [[Jaume Gomis]], _Fractional Branes and Wrapped Branes_, JHEP 9802:013,1998 ([arXiv:hep-th/9712230](http://arxiv.org/abs/hep-th/9712230))

The [[McKay correspondence]] as an [[integral transform]] ([[Fourier-Mukai transform]]) in ([[equivariant K-theory|equivariant]]) [[K-theory]], and hence in terms of fractional [[D-brane charge]] is due to

* {#GSV83} [[Gérard Gonzalez-Sprinberg]], [[Jean-Louis Verdier]], Construction g&eacute;om&eacute;trique de la correspondance de McKay, Ann. Sci. ́&Eacute;cole Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))

Detailed mathematical discussion of fractional D-branes in their incarnation as charges in $K(\tilde X)$ is  in

* S. Katz, [[Tony Pantev]], [[Eric Sharpe]], _D-branes, orbifolds, and Ext groups_, Nucl.Phys. B673 (2003) 263-300 ([arXiv:hep-th/0212218](https://arxiv.org/abs/hep-th/0212218))

See also 

* [[David Berenstein]], Richard Corrado, [[Jacques Distler]], _Aspects of ALE Matrix Models and Twisted Matrix Strings_, Phys. Rev. D 58, 026005 (1998) ([arXiv:hep-th/9712049](https://arxiv.org/abs/hep-th/9712049))

* [[Emil Martinec]], [[Gregory Moore]], bottom of p. 3 of _On Decay of K-theory_ ([arXiv:hep-th/0212059](http://arxiv.org/abs/hep-th/0212059))



[[!redirects fractional D-branes]]

[[!redirects fractional brane]]
[[!redirects fractional branes]]

[[!redirects half-brane]]
[[!redirects half-branes]]

[[!redirects half brane]]
[[!redirects half branes]]


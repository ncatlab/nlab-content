
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
 {#DBranesAtOrbifoldSingularities}
 

For [[type II superstrings]] on a global [[orbifold]] [[spacetime]] $X\sslash G$, [[D-brane charge]] is measured by the [[equivariant K-theory]] $K_G(X)$ ([Witten 98, section 5.1](#Witten98)) or at least some [[subgroup]] or [[quotient group]] thereof ([BDHKMMS 01, around (137)](#BDHKMMS01)). Under the canonical map $K(X/G) \longrightarrow K_G(X)$ from the plain [[topological K-theory]] of the [[quotient space]] [[simple object|irreducible elements]] of [[K-theory]] in general decompose into [[direct sums]] of smaller [[simple object|irreducible elements]], hence into "smaller fractions stuck at the orbifold singularity" . The corresponding [[D-branes]] are called _fractional_ D-branes in the literature.

In particular, at least for D-branes at an [[cyclic group|A-type]] singularity $\mathbb{C}^2\sslash (\mathbb{Z}/n)$, hence for $G = \mathbb{Z}/n$ a [[cyclic group]], the [[tension]] (hence [[mass]]) of a fractional D-brane is supposed to be the [[fraction]] $\tfrac{1}{{\vert G\vert}}  = \tfrac{1}{n}$ of that of the unit [[bulk]] brane away from the singularity ([Douglas-Greene-Morrison 97, p.10](#DouglasGreeneMorrison97)).

### At global linear orbifold singularities
 {#AtGlobalLinearOrbifoldSingularities}

If here $X$ is a [[contractible space]] (at it is in the majority of examples discussed in the literature!), then its [[equivariant K-theory]] is equivalently that of the point

$$
  K_G(X)
  \;\simeq\;
  K_G(\ast)
  \;\simeq\;
  R_{\mathbb{C}}(G)
$$

which is [[isomorphism|isomorphic]] to the [[representation ring]] of $G$. 

Under this identification, the (non-fractional) unit brane is identified with the [[regular representation]] $k[G/1]$ of $G$:

$$
  \array{
    &&
    K(X) &\longrightarrow & K_G(X)
    \\
    &&
    \simeq && \simeq
    \\
    \mathbb{Z}
    &\simeq&
    K(\ast) &\longrightarrow& K_G(\ast) &\simeq& R_{\mathbb{C}}(G)
    \\
    1 && & \mapsto & && k[G/1]
  }
$$

The non-fractional nature of the [[permutation representation]] is reflected in the fact that its [[character]] is still unity on the [[neutral element]] $e \in G$ and vanishes on other elements (i.e. in the non-trivial [[twisted sectors]]):

$$
  \chi_{k[G/1]}
  \;\colon\;
  g 
    \mapsto
  \left\{
  \array{
    1 &\vert& g = e
    \\
    0 &\vert& \text{otherwise}
  }
  \right.
$$

But, by a standard fact from [[representation theory]], the [[regular representation]] is far from [[irreducible representation|irreducible]], instead it is a [[direct sum]] of _all_ existing [[irreducible representations]] $V_i \in R_{\mathbb{C}}(G)$ (each appearing with multiplicity equal to its [[dimension]]):

$$
  k[G/1]
  \;\simeq\;
  \underset{i}{\bigoplus}
  d_i V_i
  \,.
$$

In this sense, the unit brane on $X$ decays into fractional branes at the orbifold  singularities $X\sslash G$.

For a general representation $V \in R(G)$ the general formula (see [this Prop.](character+of+a+linear+representation#NormalizedSumOfCharacters))

$$
  dim\left( V^G \right)
  \;=\;
  \frac{1}{{\vert G\vert}}
  \underset{g \in G}{\sum}
  \chi_V(g)
$$

shows that the total charge of the brane corresponding to $V$, summed over all [[twisted sectors]], is equal to the [[dimension]] of the [[fixed point space]] $V^G$.



### In terms of twisted sector boundary states

In the [[worldsheet]]-description of [[D-branes]] via [[boundary conformal field theory]], fractional D-branes are reflected by [[boundary states]] in "[[twisted sectors]]".
(e.g.  [Diaconescu-Gomis 99](#DiaconescuGomis99), [Recknagel-Schomerus 13, around p. 173](#RecknagelSchomerus13))



### D-branes on resolutions of orbifold singularities

In parts of the string theory literature, fractional D-branes are identified in a "[[duality in string theory|dual]]" formulation of the situation:

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

The first key insight is due to [Kronheimer 89](ALE+space#Kronheimer89). He showed that the (resolutions of) the orbifold quotients $\mathbb{C}^2/\Gamma$ for $\Gamma$ a [[finite subgroup of SU(2)]] are precisely the generic form of the gauge orbits of the direct product of $U(n_i)$-s acting in the evident way on the direct sum of $Hom(C^{n_i}, C^{n_j})$-s, where $i$ and $j$ range over the [[vertices]] of the [[Dynkin diagram]], and $(i,j)$ over its [[edges]].

This becomes more illuminating when interpreted in terms of [[Yang-Mills theory|Yang-Mills]] [[gauge theory]]: in a "[[quiver gauge theory]]" the [[gauge group]] is a [[direct product group]] of [[circle group]] $U(n_i)$ factors associated with [[vertices]] of a [[quiver]], and the particles which are charged under this gauge group arrange, as a linear representation, into a [[direct sum]] of $Hom(C^{n_i}, C^{n_j})$-s, for each edge of the quiver. 

Pick one such particle, and follow it around as the gauge group transforms it. The space swept out is its gauge orbit, and Kronheimer says that if the quiver is a Dynkin diagram, then this gauge orbit looks like $\mathbb{C}^2/\Gamma$.

On the other extreme, gauge theories are of interest whose gauge group is not a big direct product, but is a [[simple Lie group]], in the technical sense, such as the [[special unitary group]] $SU(N)$ or the [[exceptional Lie group]] $E_8$. The mechanism that relates the two classes of examples is [[spontaneous symmetry breaking]] ("[[Higgs mechanism|Higgsing]]"): the ground state energy of the field theory may happen to be achieved by putting the fields at any one point in a higher dimensional space of field configurations, acted on by the gauge group, and fixing any one such point "spontaneously" singles out the corresponding [[stabilizer subgroup]]. 

Now here is the final ingredient: it is [[N=2 super Yang-Mills theories]]  ("[[Seiberg-Witten theory]]") which have a potential that is such that its vacua break a simple gauge group such as $SU(N)$ down to a Dynkin diagram quiver gauge theory. One place where this is reviewed, physics style, is  [Albertsson 03, section 2.3.4](N=2+D=4+super+Yang-Mills+theory#Albertsson03).

More precisely, these theories have two different kinds of [[vacuum|vacua]], those on the "[[Coulomb branch]]" and those on the "[[Higgs branch]]" depending on whether the scalars of the "[[vector multiplets]]" (the gauge field sector) or of the "[[hypermultiplet]]" (the matter field sector) vanish. The statement above is for the Higgs branch, but the Coulomb branch is supposed to behave "dually". (see e.g. [Diaconescu-Gomis 99](#DiaconescuGomis99))

So that then finally is the relation, in the [[ADE classification]], between the [[simple Lie groups]] and the [[finite subgroups of SU(2)]]: start with an [[N=2 super Yang-Mills theory]] with [[gauge group]] a [[simple Lie group]]. Let it spontaneously find its vacuum and consider the orbit space of the remaining spontaneously broken symmetry group. That is (a resolution of) the orbifold quotient of $\mathbb{C}^2$ by a [[finite subgroup of SU(2)]].



### Fractional M-branes

An analogous McKay correspondence for (fractional) [[M-branes]] 

<center>
<img src="http://ncatlab.org/nlab/files/ADESingularity.jpg" width="600" alt="ADE 2Cycle" />
</center>

> graphics grabbed from [HSS18](http://ncatlab.org/schreiber/show/Equivariant+homotopy+and+super+M-branes)


is considered informally in the [[string theory]] literature (for instance in discussion of [[M-theory on G2-manifolds]]) 
but has not been given a correspondingly precise cohomological formulation yet. 

## Properties

### RR-Charge
 {#RRCharge}

Under the identification ([above](#AtGlobalLinearOrbifoldSingularities))

$$
  KU_G^0(\ast) \simeq R_{\mathbb{C}}(G)
$$

of the fractional D-brane charges at a $G$-[[orbifold]] [[singularity]] with of the [[equivariant K-theory]] of the point and hence with the [[representation ring]] of $G$, a [[character]] 

$$
  \chi_V \coloneqq tr_V(-) \;\colon\; ConjCl(G) \to \mathbb{C}
$$ 

of a [[representation]] $V \in R(G)$ correspondes to the [[RR-field]] [[charge]] 

\[
  \label{RRChargeOfFractionalDBraneInGTwistedSector}
  Q_V(g) \;=\; \frac{ \chi_V(g) }{ {\vert G \vert} }
\]

of the corresponding fractional D-brane in the $g$-[[twisted sector]].

([Douglas-Greene-Morrison 97, (3.8)](#DouglasGreeneMorrison97), [Diaconescu-Gomis 99 (2.4)](#DiaconescuGomis99), [Billó-Craps-Roose 01, (4.65) with (4.41)](#BilloCrapsRoose01), [EGJ 05, (4.5)](#EGJ05), [Recknagel-Schomerus 13 (4.102)](#RecknagelSchomerus13))

### Tadpole cancellation

See at _[[RR-field tadpole cancellation]]_ the section _[For fractional D-branes](RR-field+tadpole+cancellation#ForFractionalDBranes)_


## Related concepts

* [NS5 half-brane](NS5-brane#NSHalfBranes)

* [[permutation brane]]

* [[fractional M2-brane]]

* [[half M5-brane]]

## References
 {#References}


The concept originates with

* {#DouglasGreeneMorrison97} [[Michael Douglas]], [[Brian Greene]], [[David Morrison]], _Orbifold Resolution by D-Branes_, Nucl.Phys.B506:84-106,1997 ([arXiv:hep-th/9704151](https://arxiv.org/abs/hep-th/9704151))

* Diaconescu, [[Michael Douglas]], [[Jaume Gomis]], _Fractional Branes and Wrapped Branes_, JHEP 9802:013,1998 ([arXiv:hep-th/9712230](http://arxiv.org/abs/hep-th/9712230))

based on the analysis of [[perturbative string theory]] on (global) [[orbifold]] [[background field|backgrounds]] in 

* {#DixonHarveyVafaWitten85} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds_, Nuclear Physics B Volume 261, 1985, Pages 678-686 (<a href="https://doi.org/10.1016/0550-3213(85)90593-0">doi:10.1016/0550-3213(85)90593-0</a>)

* {#DixonHarveyVafaWitten86} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds (II)_, Nuclear Physics B Volume 274, Issue 2, 15 September 1986, Pages 285-314 (<a href="https://doi.org/10.1016/0550-3213(86)90287-7">doi:10.1016/0550-3213(86)90287-7</a>)

The proposal that D-brane charge on [[orbifolds]] is given by [[equivariant K-theory]] goes back to

* {#Witten98} [[Edward Witten]], section 5.1 of _D-Branes And K-Theory_, JHEP 9812:019,1998 ([arXiv:hep-th/9810188](http://arxiv.org/abs/hep-th/9810188))

but it was pointed out that only a subgroup or quotient group of equivariant K-theory can be physically relevant, in

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], around (137) of  _Triples, Fluxes, and Strings_, Adv.Theor.Math.Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))

Further discussion in terms of [[equivariant K-theory]]:

* {#GarciaCompean98} Hugo Garcia-Compean, _D-branes in Orbifold Singularities and Equivariant K-Theory_, Nucl.Phys. B557 (1999) 480-504 ([arXiv:hep-th/9812226](https://arxiv.org/abs/hep-th/9812226))

Survey with an eye towards [[string phenomenology]] is in 

* {#MalyshevVerlinde07} Dmitry Malyshev, [[Herman Verlinde]], _D-branes at Singularities and String Phenomenology_, Nucl.Phys.Proc.Suppl.171:139-163, 2007 ([arXiv:0711.2451](https://arxiv.org/abs/0711.2451))

The [[McKay correspondence]] as an [[integral transform]] ([[Fourier-Mukai transform]]) in ([[equivariant K-theory|equivariant]]) [[K-theory]], and hence in terms of fractional [[D-brane charge]] is due to

* {#GSV83} [[Gérard Gonzalez-Sprinberg]], [[Jean-Louis Verdier]], Construction g&eacute;om&eacute;trique de la correspondance de McKay, Ann. Sci. ́&Eacute;cole Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))

Detailed mathematical discussion of fractional D-branes in their incarnation as [[Ext]]-groups of [[coherent sheaves]] is in

* S. Katz, [[Tony Pantev]], [[Eric Sharpe]], _D-branes, orbifolds, and Ext groups_, Nucl.Phys. B673 (2003) 263-300 ([arXiv:hep-th/0212218](https://arxiv.org/abs/hep-th/0212218))

and with relation to [[Bridgeland stability conditions]] in 

* {#MalyshevVerlinde07} Dmitry Malyshev, [[Herman Verlinde]], _D-branes at Singularities and String Phenomenology_, Nucl.Phys.Proc.Suppl.171:139-163, 2007 ([arXiv:0711.2451](https://arxiv.org/abs/0711.2451))

Also on stability:

* [[Bogdan Stefanski]], _Dirichlet Branes on a Calabi-Yau Three-fold Orbifold_, Nucl.Phys.B589:292-314, 2000 ([arXiv:hep-th/0005153](https://arxiv.org/abs/hep-th/0005153))

See also 

* [[David Berenstein]], Richard Corrado, [[Jacques Distler]], _Aspects of ALE Matrix Models and Twisted Matrix Strings_, Phys. Rev. D 58, 026005 (1998) ([arXiv:hep-th/9712049](https://arxiv.org/abs/hep-th/9712049))

* [[Emil Martinec]], [[Gregory Moore]], bottom of p. 3 of _On Decay of K-theory_ ([arXiv:hep-th/0212059](http://arxiv.org/abs/hep-th/0212059))

Discussion in terms of [[twisted sector]] [[boundary states]] in [[worldsheet]] [[boundary conformal field theory]] includes

* {#DiaconescuGomis99} Diaconescu, [[Jaume Gomis]], _Fractional Branes and Boundary States in Orbifold Theories_, JHEP 0010 (2000) 001 ([arXiv:hep-th/9906242](https://arxiv.org/abs/hep-th/9906242))

* [[Matthias Gaberdiel]], [[Bogdan Stefanski]], _Dirichlet Branes on Orbifolds_, Nucl.Phys.B578:58-84, 2000 ([arXiv:hep-th/9910109](https://arxiv.org/abs/hep-th/9910109))

* M. Frau, A. Liccardo, R. Musto, _The Geometry of Fractional Branes_, Nucl.Phys. B602 (2001) 39-60 ([arXiv:hep-th/0012035](https://arxiv.org/abs/hep-th/0012035))

* {#BilloCrapsRoose01} M. Billó, B. Craps, F. Roose, _Orbifold boundary states from Cardy's condition_, JHEP 0101:038, 2001 ([arXiv:hep-th/0011060](https://arxiv.org/abs/hep-th/0011060))

* {#QuirozStefanski01} N. Quiroz, [[Bogdan Stefanski]], _Dirichlet Branes on Orientifolds_, Phys.Rev. D66 (2002) 026002 ([arXiv:hep-th/0110041](https://arxiv.org/abs/hep-th/0110041))
  
  (for [[orientifolds]] of orbifolds)

* {#MMR06} Jaydeep Majumder, Subir Mukhopadhyay, Koushik Ray, _Fractional Branes in Non-compact Type IIA Orientifolds_, JHEP0611:008, 2006 ([arXiv:hep-th/0602135](https://arxiv.org/abs/hep-th/0602135))

* {#KrizZayasQuiroz08} [[Igor Kriz]], Leopoldo A. Pando Zayas, Norma Quiroz, _Comments on D-branes on Orbifolds and K-theory_, Int.J.Mod.Phys.A23:933-974, 2008 ([arXiv:hep-th/0703122](https://arxiv.org/abs/hep-th/0703122))

* {#RecknagelSchomerus13} [[Andreas Recknagel]], [[Volker Schomerus]], _Boundary Conformal Field Theory and the Worldsheet Approach to D-branes_, Cambridge 2013 ([spire:1308990](http://inspirehep.net/record/1308990))


Relation to [[permutation branes]]:

* {#EGJ05} Bobby Ezhuthachan, Suresh Govindarajan, T. Jayaraman, _A quantum McKay correspondence for fractional 2p-branes on LG orbifolds_, JHEP 0508 (2005) 050 ([arXiv:hep-th/0504164](https://arxiv.org/abs/hep-th/0504164))

On [[polarized D-brane|polarization]] of fractional D-branes:

* Timothy J. Hollowood, S. Prem Kumar, _World-sheet Instantons via the Myers Effect and $\mathcal{N} = 1^\ast$ Quiver Superpotentials_, JHEP 0210:077, 2002 ([arXiv:hep-th/0206051](https://arxiv.org/abs/hep-th/0206051))






[[!redirects fractional D-branes]]

[[!redirects fractional brane]]
[[!redirects fractional branes]]

[[!redirects half-brane]]
[[!redirects half-branes]]

[[!redirects half brane]]
[[!redirects half branes]]


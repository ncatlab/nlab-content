
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[projective unitary group]] on an infinite-dimensional [[separable Hilbert space|separable]] [[complex vector space|complex]] [[Hilbert space]] $\mathcal{H}$ is traditionally denoted $PU(\mathcal{H})$, being the [[quotient space|quotient]] of the [[unitary group]] [[U(ℋ)]] by its [[circle group|circle]] [[subgroup]] $S^1 \simeq S(\mathbb{C}) \simeq$ [[U(1)]].

## Properties

### General

\begin{proposition}\label{UHCircleFiberBundle}
  The [[U(1)]]-[[quotient space]] [[coprojection]] of [[U(ℋ)]]  over [[PU(ℋ)]] -- both in their strong [[operator topology]] -- is a [[circle group|circle]]-[[principal bundle]]:
$$
  \array{
    S^1 &\hookrightarrow& \mathrm{U}(\mathcal{H})
    \\
    && \big\downarrow
    \\
    && PU(\mathcal{H})
    \mathrlap{ \; \simeq \; \mathrm{U}(\mathcal{H})/S^1 }
  }
$$
\end{proposition}
([Simms 1970, Thm. 1](#Simms70))
\begin{remark}
  Prop. \ref{UHCircleFiberBundle} means in particular that $\mathrm{U}(\mathcal{H}) \xrightarrow{\;} PU(\mathcal{H})$ is [[locally trivial bundle|locally trivial]], hence that the [[coset space]] [[coprojection]] $\mathrm{U}(\mathcal{H}) \xrightarrow{\;} \mathrm{U}(\mathcal{H})/S^1$ admits [[local sections]]. See also at *[[coset space coprojection admitting local sections]]*.
\end{remark}

\begin{prop}\label{WellPointedInOperatorTopology}
  In its [[operator topology]] ([[U(ℋ)#WithOperatorTopology|here]]), $PU(\mathcal{H})$ is a [[well-pointed topological group]].
\end{prop}
([Hebestreit & Sagave 2020, p. 23](#HebestreitSagave19), using [Dardalat & Pennig 2016, Prop. 2.26](twisted+K-theory#DardalatPennig16))

### Homomorphisms into $PU(\mathcal{H})$ 

Since $\Gamma \,\coloneqq\,$ [[PU(ℋ)]] is not a (finite-dimensional) [[Lie group]], it falls outside the applicability of the general theorem that [[nearby homomorphisms from compact Lie groups are conjugate]]. 
Nevertheless, the conclusion still holds, at least for [[domain]] $G$ a [[discrete group|discrete]], hence [[finite group]]:

  The [[PU(ℋ)]][[G-space|-space]] of homomorphisms $Hom\big(G,\, PU(\mathcal{H})\big)$ is a [[disjoint union]] ([as here](nearby+homomorphisms+from+compact+Lie+groups+are+conjugate#eq:DisjointUnionOfOrbits)) of [[orbits]] of the [[conjugation action]].

  This is established in [Uribe & Lück 2013, Sec. 15](#UribeLueck13), [p. 38](https://arxiv.org/pdf/1304.4862.pdf#page=38).


## Related concepts

* [[U(ℋ)]]

* [[universal equivariant PU(H)-bundle|universal equivariant $PU(\mathcal{H})$-bundle]]


## Literature

General discussion:

* {#Simms70} [[David John Simms]], *Topological aspects of the projective unitary group*, Math. Proc. Camb. Phil. Soc. **68** 1 (1970) 57-60  ([doi:10.1017/S0305004100001043](https://doi.org/10.1017/S0305004100001043))

* {#UribeLueck13} [[Bernardo Uribe]], [[Wolfgang Lück]], Section 15 of: _Equivariant principal bundles and their classifying spaces_, Algebr. Geom. Topol. 14 (2014) 1925-1995 ([arXiv:1304.4862](https://arxiv.org/abs/1304.4862), [doi:10.2140/agt.2014.14.1925](http://dx.doi.org/10.2140/agt.2014.14.1925))

* [[Jesus Espinoza]], [[Bernardo Uribe]], *Topological properties of spaces of projective unitary representations*, Rev. Acad. Colombiana Cienc. Exact. Fís. Natur. 40 (2016), no. 155, 337-352 ([arXiv:1511.06785](https://arxiv.org/abs/1511.06785), [scielo:S0370-39082016000200013](http://www.scielo.org.co/scielo.php?script=sci_arttext&pid=S0370-39082016000200013), [doi:10.18257/raccefyn.317](https://doi.org/10.18257/raccefyn.317))

Concerning well-pointedness:

* {#HebestreitSagave19} [[Fabian Hebestreit]], [[Steffen Sagave]], p. 23 of: *Homotopical and operator algebraic twisted K-theory*, Mathematische Annalen **378** (2020) 1021-1059 ([arXiv:1904.01872](https://arxiv.org/abs/1904.01872), [doi:10.1007/s00208-020-02066-6](https://doi.org/10.1007/s00208-020-02066-6))


[[!redirects PU(H)]]

[[!redirects projective unitary group on a Hilbert space]]

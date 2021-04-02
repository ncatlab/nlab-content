
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Generally, for $G$ some [[group]], a _$G$-equivariant bundle_ is a [[bundle]], specifically a [[fiber bundle]] ([[principal bundle]], [[vector bundle]], etc.) all whose component spaces (total space $E$, base space $X$, [[fiber]] $F$, but also possibly the [[structure group]] $\Gamma$) are equipped with $G$-[[actions]], such that all structure morphisms (in particular the projection $E \overset{p}{\to} X$, but also the $\Gamma$-[[action]] for [[principal bundles]] etc.)  are $G$-[[equivariant functions]].

In short, this should mean ([[schreiber:TED cohomology|GSS 21]], Def. \ref{EquivariantPrincipalBundles} below) that $G$-equivariant (fiber-, principal-,...) bundles are (fiber-, principal, ...) bundles _[[internalization|internal]]_ to a [[category]] of [[G-spaces]] (e.g. [[topological G-spaces]], [[G-manifolds]] but also [[G-sets]] etc.).

While the existing literature does not state the definition of equivariant bundles via [[internalization]], one sees (Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles} below) that the explicit definition in [tom Dieck 69](#tomDieck69), [tom Dieck 87, Sec. I.8](#tomDieck87) (for the case of [[principal bundles]]) is the equivalent external description, _including_, thereby, an [[action]] of the [[equivariance group]] $G$ on the [[structure group]] $\Gamma$ -- together with the respective compatibility conditions, which equivalently say (as highlighted in
[tom Dieck 69, Sec. 1.2](#tomDieck69), also [Murayama-Shimakawa 95, below 1.1](#MurayamaShimakawa95), see the discussion [here](category+of+G-sets#InternalGroupActions)) that the joint action is that of the [[semidirect product group]] $\Gamma \rtimes G$.

Beware that this [[action]] of the [[equivariance group]] $G$ on the [[structure group]] $\Gamma$ of an [[equivariant principal bundle]] is often and traditionally disregarded, i.e. implicitly taken to be the [[trivial action]] (e.g. [Lashof 82](#Lashof82), [Lashof-May-Segal 83](#LashofMaySegal83)), which equivalently means that the [[semidirect product group]] that acts is reduced to the [[direct product group]] $\Gamma \times G$, meaning that the [[action]] of the [[equivariance group]] _commutes_ with that of the [[structure group]]. This special case is the default meaning of _equivariant bundle_ in much of the literature!

(The definition of "generalized equivariant bundles" proposed in [Lashof-May 86](#LashofMay86) and advertized in [Lewis-May-Steinberger 86, Sec. IV.1](#LewisMaySteinberger86) allows any [[group extension]] of $G$ by $\Gamma$ to act. This reduces to [[semidirect products]] $\Gamma \rtimes G$ for [[split sequence|split extensions]] (see [there](group+extension#SplitExtensionsAndSemidirectProductGroups)) where $\Gamma$ is a [[normal subgroup]], and that is the case that [May 90](#May90), [Guillou-May-Merling 17](#GuillouMayMerling17) falls back to).

Much of the literature on equivariant bundles is interested

* in [[equivariant vector bundles]] regarded as representing [[cocycles]] for [[equivariant K-theory]] ([Segal 68, Sec 1](#Segal68), [Wasserman 69, Sec. 2](#Wasserman69),[HJJS 08, Sec. 13](#HJJS08));

and/or

* as [[twisted cohomology|twists]] for [[twisted equivariant cohomology theories]], and here most of the existing literature focuses on [[twisted equivariant K-theory]] and specifically on its equivariant degree-3 twist by equivariant [[projective bundles]] (e.g. [Barcenas-Espinoza-Joachim-Uribe 12](#BarcenasEspinozaJoachimUribe12),  [Uribe-Lück 14, Sec. 15](#UribeLueck14)).

## Definition

We discuss  equivariant groups in/as [[topological spaces]], for definiteness and due to their relevance as models in [[equivariant homotopy theory]].  All of the discussion generalizes, say to [[smooth manifolds]] or general [[toposes]].

### Preliminaries

\begin{defn}
(**convenient category of topological spaces**)
\linebreak
We write
$$
  TopologicalSpaces
  \;\in\;
  Categories
$$
for any [[convenient category of topological spaces]] whose [[mapping space]] serves as an [[internal hom]], such as

* [[D-topological spaces]]

* [[compactly generated topological spaces]].

This means in particular that for $X,Y,A \,\in\, TopologicalSpaces$, we have a [[natural bijection]]

\[
  \label{HomAdjunctInTopologicalSpaces}
  X \times Y
    \longrightarrow
  A
  \;\;\;\;\;\;\;
  \overset{adjuncts}{\leftrightarrow}
  \;\;\;\;\;\;\;
  X
    \longrightarrow
  Maps(Y,A)
\]

between [[maps]] (meaning: [[continuous functions]]) out of the [[product topological space]] with $Y$ and maps into the [[mapping space]].

\end{defn}

\begin{defn}\label{TopologicalGSpaces}
(**topological $G$-spaces**)
\linebreak
For $G$ be a [[topological group]] -- to be called the _[[equivariance group]]_ -- we write
$$
  G Actions(TopologicalSpaces)
  \;\in\;
  Categories
$$
for the [[category]] whose

* [[objects]] $(X,\rho)$ are [[topological spaces]] $X$ equipped with [[continuous function|continuous]] $G$-[[actions]]

  $$
    G \times X \overset{}{\longrightarrow} X
    \;\;\;\;\;\;
    \leftrightarrow
    \;\;\;\;\;\;
    G \overset{\rho}{\longrightarrow} Aut(X) \subset Maps(X,X)
    \,;
  $$

* [[morphisms]] are $G$-[[equivariant function|equivariant]] [[continuous functions]] between them ("maps"); i.e. for the category of "[[G-spaces]]", often denote "$G Spaces$" or even $G Sp$ or similar.

\end{defn}

\begin{remark}
(**further conditions on the equivariance group**)
\linebreak
For purposes of [[equivariant homotopy theory]] one typically assumes the [[topological group|topological]] [[equivariance group]] $G$ in Def. \ref{TopologicalGSpaces} to be that underlying a [[compact Lie group]], such as a [[finite group]] (as that guarantees that [[G-CW-complexes]] are well-behaved and that the [[equivariant Whitehead theorem]] holds). But for the plain [[point-set topology]] of equivariant bundles, this condition is not necessary.
\end{remark}


\begin{remark}\label{GSpacesAreCartesianMonoidal}
(**[[topological G-spaces]] are [[Cartesian monoidal category|cartesian monoidal]]**)
  The category of [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}) is a [[Cartesian monoidal category]]: The [[Cartesian product]] of two [[topological G-spaces]] $(X_i, \rho_i)$ is the underlying [[product topological space]] equipped with the [[diagonal action]] by $G$:
$$
  (X_1, \rho_1)
  \times
  (X_2, \rho_2)
  \;=\;
  \Big(
    X_1 \times X_2,
   \,
   \rho_{1,2}(g)(x_1,x_2)
   \,=\,
   \big(
     \rho_1(x_1), \rho_2(x_2)
   \big)
  \Big)
  \,.
$$
\end{remark}
In a [[Cartesian monoidal category]] there is a notion of [[internalization|internal]] [[group objects]]:

### Equivariant groups

\begin{defn}\label{EquivariantTopologicalGroup}
(**equivariant topological groups**)
\linebreak
Given an [[equivariance group]] $G$ (Def. \ref{TopologicalGSpaces}),
a _$G$-[[equivariant topological group]]_ $(\Gamma, \alpha)$ is a [[group object]] [[internalization|internal]] to [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}):
  $$
    \big(
      \Gamma,
      \,
      \alpha
    \big)
    \;\in\;
    Groups
    \big(
      G Actions
      (
        TopologicalSpaces
      )
    \big)
    \,.
  $$
\end{defn}
(See Prop. \ref{EquivariantGroupsAsSemidirectProductGroups} below for the choice of notation used here.)

\begin{remark}\label{UnderlyingTopologicalGroupOfAnEquivariantTopologicalGroup}
Since the [[forgetful functor]] from [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}) to underlying [[topological spaces]]
$$
  \array{
    G Actions
    (
      TopologicalSpaces
    )
   &
     \overset{
     }{\longrightarrow}
   &
   TopologicalSpaces
  }
$$
[[preserved limit|preserves]] [[Cartesian products]] (explicitly so by Remark \ref{GSpacesAreCartesianMonoidal}), it preserves [[group objects]] and hence sends $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) to underlying plain [[topological groups]]:
\[
  \label{ForgetfulFunctorFromEquivariantTopologicalGroupsToTopologicalGroups}
  \array{
    Groups
    \big(
    G Actions
    (
      TopologicalSpaces
    )
   \big)
   &
     \overset{
     }{\longrightarrow}
   &
   Groups
   (
     TopologicalSpaces
   )
   \\
   \big(
     \Gamma
     ,
     \alpha
   \big)
   &\mapsto&
   \Gamma
   \,.
  }
\]
\end{remark}



### Equivariant bundles

We say that a $G$-equivariant principal bundle is a [[principal bundle]] [[internalization|internal]] to [[topological G-spaces]]:

\begin{defn}\label{EquivariantPrincipalBundles}
(**[[equivariant principal bundle]]**)
  \linebreak
Given

  * an [[equivariance group]] $G \in Groups(TopologicalSpaces)$;

  * an [[equivariant topological group]] (Def. \ref{EquivariantTopologicalGroup})

    $
      (\Gamma, \alpha)
      \;\in\;
      Groups\big(  G Actions(TopologicalSpaces) \big)
    $

    to be called the $G$-equivariant _[[structure group]]_;

a _$G$-equivariant $(\Gamma,\alpha)$-principal bundle over $(X,\rho)$ is:

* an [[action object]] of $(\Gamma,\alpha)$, hence

  * a _total [[topological G-space]]_ $(P,\rho) \in G Actions(TopologicalSpaces)$;

  * an [[action]] of $\Gamma$ on $P$ (hence [[internalization|internal]] to [[G-spaces]]!);

such that, with the [[quotient]] denoted

$$
  P/\Gamma \;\simeq\; X
  \,,
$$

and called the _base space_ $(X,\rho) \in G Actions(TopologicalSpaces)$ the following two conditions are satisfied:

* **(principality)** the _shear map_

  $
    \array{
      P \times \Gamma
      &\longrightarrow&
      P \times_X P
      \\
      (p,\gamma)
      &\mapsto&
      (p, \rho(\gamma)(x))
    }
  $

  is an [[isomorphism]].

* {#EquivariantLocalTriviality} (**local triviality**) the quotient projection is locally trivial, in that there exists an [[open cover]] $U \to X$ of [[topological G-spaces]] and a $G$-equivariant trivialization of the [[pullback bundle|pullback]] of $P$ to $U$:

\begin{xymatrix}
  {U} \times \Gamma
  \ar@(ul,ur)|-{ \Gamma \rtimes_\alpha G }
  \ar[d]_{
    p_1
  }
  \ar[rr]
  \ar@{}[drr]|-{ \mbox{\tiny\rm (pb)} }
  &&
  {P}
  \ar@(ul,ur)|-{ \Gamma \rtimes_\alpha G }
  \ar[d]^-{p}
  \\
  \mathllap{\exists\;\;}
  {U}
  \ar@(dl,dr)|-{G}
  \ar@{->>}[rr]_-{ \mathrm{open} }
  &&
  {X}
  \ar@(dl,dr)|-{G}
\end{xymatrix}



\end{defn}


## Properties

### Notions of equivariant local triviality

In the internal definition
[above](#EquivariantLocalTriviality),
we demanded an equivariant fiber/principal bundle to be locally trivial in the evident sense *[[internalization|internal]]* to [[TopologicalGActions]]. But in the literature various variants of this notion are considered. We discuss how (some of) these are related to each other:

* [tom Dieck 69, Def. 2.3](#tomDieck69), [tom Dieck 87, p. 58](#tomDieck87)

\begin{definition}
**(Bierstone condition)**
  A principal

\end{definition}

[Bierstone 78, Sec. 4](#Bierstone78)

* [Lashof 82, p. 258](#Lashof82), [Lashof-May 86, p. 267](#LashofMay86)

* [Lashof-Rothenberg 78, p. 216](#LashofRothenberg78)

(...)

Lashof82 $\leftrightarrow$ Bierstone78 ([Lashof 82, Lemmas 1.1, 1.3](#Lashof82))



### As $(G,\alpha,\Gamma)$-principal bundles

\begin{prop}\label{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles}
(**principal bundles internal to $G$-spaces are equivalent to tom Dieck-bundles**)
\linebreak
  The
  $G$-equivariant $(\Gamma,\alpha)$-principal bundles in the [[internalization|internal]] sense of Def. \ref{EquivariantPrincipalBundles} form a [[full subcategory]] of the $(G,\alpha,\Gamma)$-principal bundles in the sense of [tom Dieck 69](#tomDieck69) on those which admit not just a local trivialization, but a $G$-equivariant local trivialization (as [above](#EquivariantLocalTriviality)).
\end{prop}
\begin{proof}
  This follows immediately by the fact ([this Prop.](equivariant+group#ActionsOfEquivariantGroupsAsSemidirectProductGroupActions)) that $G$-equivariant actions of [[equivariant groups]] $(G,\alpha)$ are equivalent to plain actions of the [[semidirect product group]] $\Gamma \rtimes_\alpha G$.
\end{proof}

\begin{remark}\label{SufficientConditionForEquivariantEnhancementOfLocalTrivialization}
  **(sufficient condition for plain local trivialization to have equivariant enhancement)**
  Sufficient conditions for existence of plain local trivialization to imply a $G$-equivariant local trivialization, and hence for the inclusion in Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles} to be an actual [[equivalence of categories]], are:

1. $G$ is a [[finite group]]; or

1. $X$ is a [[locally compact topological space|locally compact]] [[separable metric space]] of [[finite number|finite]] [[dimension of a separable metric space|dimension]] and with a [[finite number]] of $G$-[[orbit types]]; or

1. $\Gamma$ is a [[locally compact topological space|locally compact]] [[separable metric space]] such that for every $G$-[[orbit type]] $G/H \subset X$ the [[fixed locus]] $\Gamma^H$ is an [[absolute neighbourhood retract]] (such as a [[finite number|finite]]-[[dimension of a manifold|dimensional]] [[topological manifold]] or a [[finite number|finite]]-[[dimension of a cell complex|dimensional]] and [[locally finite CW-complex|locally finite]] [[CW-complex]], by the discussion [there](absolute+retract#Examples)).

Because ([Atiyah 66, p. 374](KR+cohomology+theory#Atiyah66)) then
for every plain local trivialization around any [[orbit]] the [[equivariant Tietze extension theorem]] implies the existence of an [[equivariant function]] to $\Gamma$ on an [[open neighbourhood]] of that orbit, which thus constitutes a $G$-equivariant local trivialization.

\end{remark}

## Examples

* [[equivariant tautological line bundle]]

* in [[arithmetic geometry]]: [[shtuka]]

## Related concepts

* [[twisted bundle]]

* [[equivariant differential topology]]

* [[equivariant cohomology]]

* [[equivariant connection]]

* [[equivariant K-theory]]



## References

### Equivariant fiber bundles

On general (topological) equivariant [[fiber bundles]]/[[principal bundles]]:

* {#tomDieck69} [[Tammo tom Dieck]], _Faserb&uuml;ndel mit Gruppenoperation_, Arch. Math 20, 136–143 (1969) ([doi:10.1007/BF01899003](https://doi.org/10.1007/BF01899003))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* {#Bierstone78} [[Edward Bierstone]], _The equivariant covering homotopy property for differentiable $G$-fibre bundles_, J. Differential Geom. 8(4): 615-622 (1973) ([doi:10.4310/jdg/1214431963](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-8/issue-4/The-equivariant-covering-homotopy-property-for-differentiable-G-fibre-bundles/10.4310/jdg/1214431963.full))

  > (for [[structure group]] commuting with the [[equivariance group]], but with [[equivariant differential topology|differentiable structure]])


* [[Goro Nishida]], Section 2 of: _The transfer homomorphism in equivariant generalized cohomology theories_, J. Math. Kyoto Univ. 18(3): 435-451 (1978) ([doi:10.1215/kjm/1250522505](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-18/issue-3/The-transfer-homomorphism-in-equivariant-generalized-cohomology-theories/10.1215/kjm/1250522505.full))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])


* {#LashofRothenberg78} [[Richard Lashof]], [[Melvin Rothenberg]], Section 1 of: _$G$-Smoothing theory_, p. 211-266 in: _Algebraic and Geometric Topology_, Proceedings of Symposia in Pure Mathematics, Vol. XXXII, Part 1, American Mathematical Society 1978 ([doi:10.1090/pspum/032.1](https://doi.org/10.1090/pspum/032.1), [[LashofRothenbergGSmoothingTheory.pdf:file]])

  > (for [[structure group]] commuting with the [[equivariance group]], but with [[equivariant differential topology|differentiable structure]])


* {#Lashof82} [[Richard Lashof]], _Equivariant bundles_, Illinois J. Math. 26(2): 257-271, 1982 ([doi:10.1215/ijm/1256046796](https://doi.org/10.1215/ijm/1256046796))

  > (for [[structure group]] commuting with the [[equivariance group]])

* {#LashofMay86} [[Richard Lashof]], [[Peter May]], _Generalized equivariant bundles_, Bull. Soc. Math. Belg. Sér. A 38, 265-271, 1986 ([pdf](http://math.uchicago.edu/~may/PAPERS/55.pdf), [[LashofMayGeneralizedEquivariantBundles.pdf:file]])

  > (for [[structure group]] [[group extension|extending]] the [[equivariance group]])


* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger, Section IV.1 of: _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf), [doi:10.1007/BFb0075778](https://link.springer.com/book/10.1007/BFb0075778))

  > (for [[structure group]] [[group extension|extending]] the [[equivariance group]])

* {#tomDieck87} [[Tammo tom Dieck]], Section I.8 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])


With [[abelian group|abelian]] [[structure group]]:

* {#LashofMaySegal83} [[Richard Lashof]], [[Peter May]], [[Graeme Segal]], _Equivariant bundles with abelian structural group_, Contemporary Mathematics,  Volume 19, 1983 ([doi:10.1090/conm/019](http://dx.doi.org/10.1090/conm/019), [pdf](http://www.math.uchicago.edu/~may/PAPERS/45.pdf), [[LashofMaySegalEquivariantBundles.pdf:file]])

  > (for [[structure group]] commuting with the [[equivariance group]])

* [[Andrzej Kozlowski]], _Equivariant Bundles and Cohomology_, Transactions of the American Mathematical Society, Vol. 296, No. 1 (Jul., 1986), pp. 181-190 ([jstor:2000568](https://www.jstor.org/stable/2000568))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

More on [[equivariant principal bundles]] and their [[classifying spaces]]/[[universal principal bundles]]:

* {#May90} [[Peter May]], _Some remarks on equivariant bundles and classifying spaces_, Théorie de l'homotopie, Astérisque, no. 191 (1990), 15 p. ([numdam:AST_1990__191__239_0](http://www.numdam.org/item/?id=AST_1990__191__239_0))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* {#MurayamaShimakawa95} [[Mitutaka Murayama]], [[Kazuhisa Shimakawa]], _Universal equivariant bundles_, Proc. Amer. Math. Soc. 123 (1995), 1289-1295 ([doi:10.1090/S0002-9939-1995-1231040-9](https://doi.org/10.1090/S0002-9939-1995-1231040-9))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* {#UribeLueck14} [[Bernardo Uribe]], [[Wolfgang Lück]], _Equivariant principal bundles and their classifying spaces_, Algebr. Geom. Topol. 14 (2014) 1925-1995 ([arXiv:1304.4862](https://arxiv.org/abs/1304.4862), [doi:10.2140/agt.2014.14.1925](http://dx.doi.org/10.2140/agt.2014.14.1925))

  > (back to [[structure group]] commuting with the [[equivariance group]])

* {#GuillouMayMerling17} [[Bertrand Guillou]], [[Peter May]], [[Mona Merling]] _Categorical models for equivariant classifying spaces_, Algebr. Geom. Topol. 17 (2017) 2565-2602 ([arXiv:1201.5178](https://arxiv.org/abs/1201.5178), [doi:10.2140/agt.2017.17.2565](https://doi.org/10.2140/agt.2017.17.2565))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])


Comparative discussion is in:

* {#Zou20} [[Foling Zou]], _Notes on equivariant bundles_ ([arXiv:2008.01268](https://arxiv.org/abs/2008.01268))




### Equivariant vector bundles

On equivariant [[vector bundles]]:

* [tom Dieck 87, Section I.9](#tomDieck87)

In the context of [[equivariant K-theory]]:

* {#Segal68} [[Graeme Segal]], Section 1 of: _Equivariant K-theory_, Inst. Hautes Etudes Sci. Publ. Math.  No. 34 (1968) p. 129-151 ([numdam:PMIHES_1968__34__129_0](http://www.numdam.org/item/PMIHES_1968__34__129_0))

* {#HJJS08} [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin  Schottenloher]], Section 13 of: _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Springer Lecture Notes in Physics __726__, 2008, ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726.pdf), [doi:10.1007/978-3-540-74956-1](https://link.springer.com/book/10.1007/978-3-540-74956-1))

In a context of [[equivariant differential topology]]:

* {#Wasserman69} [[Arthur Wasserman]], section 2 of: _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 (<a href="https://doi.org/10.1016/0040-9383(69)90005-6">doi:10.1016/0040-9383(69)90005-6</a>[pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))




### As twists for twisted equivariant K-theory

On equivariant pricipal bundles with [[structure group]] the [[projective unitary group]], hence providing twists for [[twisted equivariant K-theory]]:


* {#BarcenasEspinozaJoachimUribe12} Noe Barcenas, Jesus Espinoza, [[Michael Joachim]], [[Bernardo Uribe]], _Universal twist in Equivariant K-theory for proper and discrete actions_ ([doi:10.1112/plms/pdt061](https://doi.org/10.1112/plms/pdt061), [arXiv:1202.1880](https://arxiv.org/abs/1202.1880))

* [Uribe-Lueck 14, Sec 15](#UribeLueck14)


### For equivariant elliptic cohomology

In a context of [[equivariant elliptic cohomology]]:

* [[Matthew Ando]], [[John Greenlees]], Part I of: _Circle-equivariant classifying spaces and the rational equivariant sigma genus_, Math. Z. 269, 1021–1104 (2011) ([arXiv:0705.2687](https://arxiv.org/abs/0705.2687), [doi:10.1007/s00209-010-0773-7](https://doi.org/10.1007/s00209-010-0773-7))


### For gauge theory on orbifolds

The general notion of equivariant bundles from [tom Dieck 69](#tomDieck69) (with [[action]] of the [[semidirect product]] of the [[gauge group]] with the [[equivariance group]]) gets a brief mentioning in

* {#Horava96} [[Petr Hořava]], Section 5.3 of: _Chern-Simons Gauge Theory on Orbifolds: Open Strings from Three Dimensions_, J. Geom. Phys. 21:1-33, 1996 ([arXiv:hep-th/9404101](https://arxiv.org/abs/hep-th/9404101))

in a context of [[Chern-Simons theory]] on [[orbifolds]].


[[!redirects equivariant bundles]]

[[!redirects equivariant principal bundle]]
[[!redirects equivariant principal bundles]]

[[!redirects equivariant fiber bundle]]
[[!redirects equivariant fiber bundles]]

[[!redirects equivariant vector bundle]]
[[!redirects equivariant vector bundles]]



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

Generally, for $G$ some [[group]], a _$G$-equivariant bundle_ is a [[bundle]], specifically a [[fiber bundle]] ([[principal bundle]], [[vector bundle]], etc.) all whose component spaces (total space $E$, base space $X$, [[fiber]] $F$, but also possibly the [[structure group]] $\mathcal{G}$) are equipped with $G$-[[actions]], such that all structure morphisms (in particular the projection $E \overset{p}{\to} X$, but also the $\mathcal{G}$-[[action]] for [[principal bundles]] etc.)  are $G$-[[equivariant functions]].

In short, this should mean ([[schreiber:TED cohomology|GSS 21]]) that $G$-equivariant (fiber-, principal-,...) bundles are (fiber-, principal, ...) bundles _[[internalization|internal]]_ to a [[category]] of [[G-spaces]] (e.g. [[topological G-spaces]], [[G-manifolds]] but also [[G-sets]] etc.). 

While the existing literature does not state the definition of equivariant bundles via [[internalization]], one sees that the explicit definition in [tom Dieck 69](#tomDieck69) (for the case of [[principal bundles]]) is the equivalent external description, _including_, thereby, an [[action]] of the [[equivariance group]] $G$ on the [[structure group]] $\mathcal{G}$ -- together with the respective compatibility conditions, which equivalently say (as highlighted e.g. in [Murayama-Shimakawa 95, below 1.1](#MurayamaShimakawa95), see the discussion [here](category+of+G-sets#InternalGroupActions)) that the joint action is that of the [[semidirect product group]] $\mathcal{G} \rtimes G$.

Beware that this [[action]] of the [[equivariance group]] $G$ on the [[structure group]] $\mathcal{G}$ of an [[equivariant principal bundle]] is often and traditionally disregarded, i.e. implicitly taken to be the [[trivial action]] (e.g. [Lashof 82](#Lashof82), [Lashof-May-Segal 83](#LashofMaySegal83)), which equivalently means that the [[semidirect product group]] that acts is reduced to the [[direct product group]] $\mathcal{G} \times G$, meaning that the [[action]] of the [[equivariance group]] _commutes_ with that of the [[structure group]]. This special case is the default meaning of _equivariant bundle_ in much of the literature!
 
(The definition of "generalized equivariant bundles" proposed in [Lashof-May 86](#LashofMay86) allows any [[group extension]] of $G$ by $\mathcal{G}$ to act. This reduces to [[semidirect products]] $\mathcal{G} \rtimes G$ for [[split sequence|split extensions]] (see [there](group+extension#SplitExtensionsAndSemidirectProductGroups)) where $\mathcal{G}$ is a [[normal subgroup]], and that is the case that [May 90](#May90) eventually falls back to, apparently still independently of [tom Dieck 69](#tomDieck69); but see [Guillou-May-Merling 17](#GuillouMayMerling17)).

Much of the literature on equivariant bundles is interested 

* in [[equivariant vector bundles]] regarded as representing [[cocycles]] for [[equivariant K-theory]] ([Segal 68, Sec 1](#Segal68), [Wasserman 69, Sec. 2](#Wasserman69));

and/or

* as [[twisted cohomology|twists]] for [[twisted equivariant cohomology theories]], and here most of the existing literature focuses on [[twisted equivariant K-theory]] and specifically on its equivariant degree-3 twist by equivariant [[projective bundles]] (e.g. [Barcenas-Espinoza-Joachim-Uribe 12](#BarcenasEspinozaJoachimUribe12),  [Uribe-Lück 14, Sec. 15](#UribeLueck14)).

## Definition

> under construction

We discuss  equivariant bundles in/as [[topological spaces]], for definiteness and due to their relevance as models in [[equivariant homotopy theory]]. Much of the discussion generalizes, say to [[smooth manifolds]] or general [[toposes]].

\begin{defn}\label{TopologicalGSpaces}
(**topological $G$-spaces**)
\linebreak
For $G$ be a [[topological group]] we write 
$$
  G Actions(TopologicalSpaces)
  \;\in\;
  Categories
$$ 
for the [[category]] of [[topological spaces]] equipped with [[continuous function|continuous]] $G$-[[actions]] and with $G$-[[equivariant function|equivariant]] [[continuous functions]] between them ("maps"); i.e. for the category of "[[G-spaces]]", often denote "$G Spaces$" or even $G Sp$ or similar.

In the following we refer to this $G$ as the _[[equivariance group]]_.
\end{defn} 

\begin{remark}
(**further conditions on the equivariance group**) 
\linebreak
For purposes of [[equivariant homotopy theory]] one typically assumes (notably to guarantee that the [[equivariant Whitehead theorem]] applies) the [[topological group|topological]] [[equivariance group]] $G$ in Def. \ref{TopologicalGSpaces} to be that underlying a [[compact Lie group]], such as a [[finite group]], as that guarantees that [[G-CW-complexes]] are well-behaved. But for the plain [[point-set topology]] of equivariant bundles, this condition is not necessary.
\end{remark}

\begin{defn}\label{EquivariantTopologicalGroup}
(**equivariant topological groups**) 
\linebreak
Given an [[equivariance group]] $G$ (Def. \ref{TopologicalGSpaces}), 
a _$G$-[[equivariant topological group]]_ is a [[group object]] [[internalization|internal]] to [[topological G-spaces]]
  $$
    \mathcal{G}
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

\begin{prop}\label{EquivariantGroupsAsSemidirectProductGroups}
  (**Equivariant groups as semidirect product groups**)
\linebreak
The [[category]] of $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) is [[equivalence of categories|equivalent]] to that of [[semidirect products]] $(-) \rtimes G$ regarded as [[pointed objects]] in the [[slice category]] of [[Groups]] over $G$:

$$
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
         \;\;
         \;\;
      }{\hookrightarrow}
    &
    Groups^{G/}_{/G}
    \\
    \mathcal{G}
    &\mapsto&
    \mathcal{G} \rtimes G
    \,.
  }
$$
\end{prop}

\begin{prop}\label{ActionsOfEquivariantGroupsAsSemidirectProductGroupActions}
  (**Equivariant group actions as semidirect product group actions**)   
  \linebreak
  Under the identification of $G$-[[equivariant group|equivariant groups]] $\mathcal{G}$
  with [[semidirect product groups]] $\mathcal{G} \rtimes G$ 
  (Prop. \ref{EquivariantGroupsAsSemidirectProductGroups})
  we have an [[equivalence of categories|equivalence]] of their
  [[actions]] given by
  $$
    \array{
      \mathcal{G}
      Actions
      \big(
        G Actions
        (
          TopologicalSpaces
        )
      \big)
      &\overset{}{
        \longrightarrow
      }&
      (
        \mathcal{G} \rtimes G
      )
      Actions( TopologicalSpaces )
    }
  $$
\end{prop}

\begin{defn}
(**[[equivariant principal bundle]]**) 
  \linebreak
Given 

  * an [[equivariance group]] $G \in Groups(TopologicalSpaces)$;
 
  * $X \in G Actions(TopologicalSpaces)$ (Def. \ref{TopologicalGSpaces}),
  
  * $\mathcal{G} \in Groups\big(  G Actions(TopologicalSpaces) \big)$ (Def. \ref{EquivariantTopologicalGroup});

a _$G$-[[equivariant principal bundle]] over $X$ with [[structure group]] $\mathcal{G}$ is:

* a _total $G$-space_ $P \in G Actions(TopologicalSpaces)$;

* an [[action]] of $\mathcal{G}$ on $P$ (hence [[internalization|internal]] to [[G-spaces]]!);

such that :

* the action is [[free action]];

* its [[quotient]] is $X$:

  $
    P/\mathcal{G} \;\simeq\; X
    \,,
  $


* the quotient [[coprojection]] is [[locally trivial bundle|locally trivial]] (...)

\end{defn}



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

### General

On general (topological) equivariant [[fiber bundles]]/[[principal bundles]]:

* {#tomDieck69} [[Tammo tom Dieck]], _Faserb&uuml;ndel mit Gruppenoperation_, Arch. Math 20, 136–143 (1969) ([doi:10.1007/BF01899003](https://doi.org/10.1007/BF01899003))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* [[Edward Bierstone]], _The equivariant covering homotopy property for differentiable $G$-fibre bundles_, J. Differential Geom. 8(4): 615-622 (1973) ([doi:10.4310/jdg/1214431963](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-8/issue-4/The-equivariant-covering-homotopy-property-for-differentiable-G-fibre-bundles/10.4310/jdg/1214431963.full))

  > (for [[structure group]] commuting with the [[equivariance group]], but with [[equivariant differential topology|differentiable structure]])

* {#Lashof82} [[Richard Lashof]], _Equivariant bundles_, Illinois J. Math. 26(2): 257-271, 1982 ([doi:10.1215/ijm/1256046796.full](https://projecteuclid.org/journals/illinois-journal-of-mathematics/volume-26/issue-2/Equivariant-bundles/10.1215/ijm/1256046796.full))

  > (for [[structure group]] commuting with the [[equivariance group]])

* {#LashofMay86} [[Richard Lashof]], [[Peter May]], _Generalized equivariant bundles_, Bull. Soc. Math. Belg. Sér. A 38, 265-271, 1986 ([pdf](http://math.uchicago.edu/~may/PAPERS/55.pdf), [[LashofMayGeneralizedEquivariantBundles.pdf:file]])

  > (for [[structure group]] [[group extension|extending]] the [[equivariance group]])

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

Comparative discussion is in:

* {#Zou20} [[Foling Zou]], _Notes on equivariant bundles_ ([arXiv:2008.01268](https://arxiv.org/abs/2008.01268))


### Equivariant vector bundles

On equivariant [[vector bundles]]:

In the context of [[equivariant K-theory]]:

* {#Segal68} [[Graeme Segal]], Section 1 of: _Equivariant K-theory_, Inst. Hautes Etudes Sci. Publ. Math.  No. 34 (1968) p. 129-151 ([numdam:PMIHES_1968__34__129_0](http://www.numdam.org/item/PMIHES_1968__34__129_0))

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


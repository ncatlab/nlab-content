
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

In [[group theory]], and specifically in [[group cohomology]]-theory, the notion of *crossed homomorphisms* (Def. \ref{CrossedHomomorphism} below) is a generalization of that of [[group homomorphisms]] where a [[group action]] -- of the [[domain]]-group $G$ by [[automorphisms]] on the [[codomain]] group $\Gamma$ -- is incorporated.

Crossed homomorphisms are equivalently [[group homomorphism|homomorphic]] [[sections]] of the [[projection]] to $G$ out of the corresponding [[semidirect product group]] $\Gamma \rtimes G$ (Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup} below). 

This largely explains their relevance in all contexts of $G$-[[equivariant algebraic topology]] and [[equivariant differential topology]], such as in [[equivariant principal bundle]]-theory (Prop. \ref{EquivariantConnectedComponentsOfEquivariantClassifyingSpaces} below) where [[semidirect product groups]] appear as $G$-[[equivariant groups]].

In particular (Prop. \ref{GroupoidOfCrossedHomorphismsIsSlicedFunctorGroupoid} below, which is not made explicit in traditional literature):

* the [[local coefficient bundle]] for [[non-abelian cohomology|non-abelian]] [[group cohomology]] in degree-1 is the image of the projection out of the semidirect product group under forming [[delooping groupoids]],

* the [[strict (2,1)-category]]-theoretic [[sections]] of this bundle form precisely the [[groupoids]] of crossed homomorphisms with "crossed conjugations" (Def. \ref{AdjointActionOnCrossedHomomorphisms} below) between them;

* and the [[connected components]] of these groupoids is the [[non-abelian cohomology|non-abelian]] [[group cohomology]] $H^1(G,\Gamma)$ (Rem. \ref{AsGroup1Cocycles}, \ref{AsCoboundariesInGroupCohomology}).

This last fact is widely appreciated (see Rem. \ref{ReferencesForNonabelianCrossedHomomorphisms} below) in the special case that $\Gamma$ is an [[abelian group]], where it serves to define ordinary [[group cohomology]] with coefficients in degree 1.

Beware that, while the notion of crossed homomorphisms makes sense for [[group objects]] [[internalization|internal]] to any ambient [[category]] $\mathcal{C}$, it may not need to strictly coincide with that of [[cocycles]] in first [[group cohomology]] beyond $\mathcal{C} = $ [[Set]] (for reasons discussed at *[[Lie group cohomology]]*, or, for the case of [[profinite groups]], in [NSW 2008, p. 24](#NSW08)).


## Definition

In all of the following, let $G \,\in\, $ [[Grp]] be a [[group]] (or [[group object]] [[internalization|internal]] to an ambient [[category]] with [[finite products]]) and let $\Gamma \,\in\, G Act$ be an $G$-[[equivariant group]], hence a [[group]] equipped with a [[group action]] 

$$
  \alpha \;\colon\; G \xrightarrow{\;\;} Aut_{Grp}(\Gamma)
$$ 

of $G$ on $\Gamma$ by [[group homomorphism|group]] [[automorphisms]], hence equivalently a [[semidirect product group]], to be denoted:

$$
  1
  \to
  \Gamma
  \xhookrightarrow{\;i\;}
  \Gamma \rtimes_\alpha G
  \xrightarrow{ \;pr_2\; }
  G
  \to 
  1
  \,.
$$


### Component definition
 {#ComponentDefinition}

\begin{definition}\label{CrossedHomomorphism}
A *crossed homomorphism* from $G$ to $\Gamma$ is a [[function]] ([[morphism]] in the [[internalization|ambient]] category)

$$
  \phi \;\colon\; G \xrightarrow{\;} \Gamma
$$

satisfying the following "$G$-crossed" homomorphism property:

$$
  \underset{g_1, g_2 \in G}{\forall}
  \;\;\;
  \phi(g_1 \cdot g_2)  
  \;=\;
  \phi(g_1) \cdot \alpha(g_1)\big( \phi(g_2) \big)
  \,.
$$
\end{definition}
\begin{remark}
\label{ReferencesForNonabelianCrossedHomomorphisms}
Def. 
\ref{CrossedHomomorphism}
appears, already with the non-abelian generality in mind, back in [Whitehead 1949, (3.1)](#Whitehead49) (together with the notion of [[crossed modules]], both as tools for analyzing [[homotopy types]] with non-trivial [[fundamental group]]).
For [[abelian group|abelian]] $\Gamma$ the definition is picked up in [MacLane 1975, IV (2.1)](#MacLane75) and many following references on [[group cohomology]], e.g. [Brown 1982, p. 45](#Brown82).
For general [[non-abelian group|non-abelian]] $\Gamma$ the notion is later used in [Murayama & Shimakawa 1995](#MurayamaShimakawa95) for discussion of [[equivariant principal bundles]]. A textbook account is in [Milne 2017, 15.a](#Milne17), aimed at application to [[algebraic groups]].
\end{remark}

\begin{example}
  For $\alpha$ the [[trivial action]], 
  the notion of a crossed homomorphism (Def. \ref{CrossedHomomorphism})
  reduces to that of an ordinary [[group homomorphism]].
\end{example}

\begin{remark}\label{AsGroup1Cocycles}
**(as 1-[[cocycles]] in [[group cohomology]])**
\linebreak
  In the special case that $\Gamma$ in Def. \ref{CrossedHomomorphism} is an [[abelian group]], crossed homomorphisms are also known as *[[cocycles]] in [[group cohomology]]* in degree 1 (e.g. [Brown 1982, p. 45](#Brown82)). In general they may be understood as 1-cocyles in [[non-abelian cohomology|non-abelian]] group cohomology (e.g. [NSW 2008, p. 16](#NWS08)).
\end{remark}

\begin{example}\label{ConstantFunctionOnNeutralElement}
  The [[constant function]] 
  $const_{\mathrm{e}} \,\colon\, G \to \Gamma$
  on the [[neutral element]] $\mathrm{e} \in \Gamma$ is always a crossed homomorphism (Def. \ref{CrossedHomomorphism}), being the trivial cocycle under the interpretation of Rem. \ref{AsGroup1Cocycles}.
\end{example}

\begin{proposition}
  \label{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}
**(as splittings/[[homomorphism|homomorphic]] [[sections]] of the [[semidirect product group]]-projection)**
\linebreak
  Crossed homomorphisms $G \to \Gamma$ (Def. \ref{CrossedHomomorphism}) are equivalently [[group homomorphism|homomorphic]] [[sections]] of the [[projection]] out of the [[semidirect product group]] $\Gamma \rtimes_\alpha G \xrightarrow{pr_2} G$ (see also at [split group extensions](group+extension#SplitExtensionsAndSemidirectProductGroups)):

$$
  CrsHom(G,\,\Gamma)
  \;\simeq\;
  GrpHom_{{}_{/G}}
  \big(
    G 
    ,\,
    \Gamma \rtimes_\alpha G
  \big)
  \;\coloneqq\;
  GrpHom(G, \, \Gamma \rtimes_\alpha G)
  \underset{
    GrpHom(G,\,G)
  }{\times}
  \{id\}
  \,.
$$
\end{proposition}
(e.g. [Brown 1982, p. 88](#Brown82), [NSW 2008, Ex. 1 on p. 24](#NSW08), [Milne 2017, Exp. 15.1](#Milne17))
\begin{proof}
  By immediate unwinding of the definition of the [[semidirect product group]], such a section is an assignment
  $$
    \array{
      G &\xrightarrow{\;}& \Gamma \rtimes_\alpha G
      \\
      g 
      &\mapsto&
      \big(
        \phi(g), \, g
      \big)
    }
  $$
  such that
  $$
   \underset{
     g_1, g_2 \in G
   }{\forall}
   \;\;\;\;\;
    \big(
      \phi(g_1 \cdot g_2), \, g_1 \cdot g_2
    \big)    
    \;\overset{!}{=}\;
    \big(
      \phi(g_1), g_1
    \big)
    \cdot
    \big(
      \phi(g_2), g_2
    \big)
    \;=\;
    \Big(
      \phi(g_1) 
        \cdot
      \alpha(g_1)\big(\phi(g_2)\big)
      ,\,
      g_1 \cdot g_2
    \Big)    
    \,.
  $$  
\end{proof}

\begin{proposition}\label{GraphOfACrossedHomomorphism}
**([[graph of a function|graphs]] of [[crossed homomorphisms]])**
\linebreak
  The [[graph of a function]] of a [[crossed homomorphism]] (Def. \ref{CrossedHomomorphism})
  is a [[subgroup]] of the [[semidirect product group]]
  \[
    \label{MayStyleCrossedHomomorphism}
    \widehat G
    \;\subset\;
    \Gamma \rtimes G
    \,,
    \;\;\;\;
    \text{such that}
    \;\;\;\;
    \mathrm{pr}_2\big(\widehat G\big) \simeq G
    \;\;\;
    \text{and}
    \;\;\;
    \widehat{G} \cap i(\Gamma) 
      \;=\; 
    \big\{
      (\mathrm{e},\,\mathrm{e})
    \big\}    
    \,,
  \]
  and every subgroup of this form arises as the [[graph of a function|graph]] of a unique crossed homomorphism.
\end{proposition}
This is, essentially, considered in [tom Dieck 1969, Sec. 2.1](#tomDieck69).
\begin{proof}
  The first statement is immediate from the definition.

  For the converse, consider a subgroup $\widehat{G}$
  as in (eq:MayStyleCrossedHomomorphism). 
  Then 
  the subgroup property implies that
  $$
    (\gamma,g), (\gamma',g) \,\in\, \widehat{G}    
    \;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;
    (\gamma' ,\, g) \cdot (\gamma ,\, g)^{-1}
    \;=\;
    (\gamma' ,\, g)
    \cdot
    \big(
      \alpha(g^{-1})(\gamma^{-1})
      ,\,
      g^{-1}
    \big)
    \;=\;
    \big( 
      \gamma' \cdot \gamma^{-1} 
      ,\,
      \mathrm{e}
    \big)
    \;\;\;
    \in
    \;
    \widehat{G}
    \,.
  $$
  From this the second condition in (eq:MayStyleCrossedHomomorphism) implies that 
  $$
    (\gamma,\,g) ,\, (\gamma',\, g)
    \;\in\;
    \widehat{G}
    \;\;\;\;
    \Rightarrow
    \;\;\;\;
    \gamma = \gamma'
    \,.
  $$
  Together with the first condition in (eq:MayStyleCrossedHomomorphism) this implies that $\widehat{G}$ is the [[graph of a function]] $\phi \;\colon\; G \to \Gamma$. From this the claim follows by Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}.
\end{proof}

\begin{remark}
  Subgroups of the form (eq:MayStyleCrossedHomomorphism)
  are considered throughout articles by [[Peter May]] on [[equivariant principal bundles]] (e.g. in [Lashof & May 1986, Thm. 10](equivariant+bundle#LashofMay86), [May 1990, Thm. 7](equivariant+bundle#May90)).
That these are equivalently ([[graph of a function|graphs]] of) [[crossed homomorphisms]] may have been one the key observations that lead to [Murayama & Shimakawa 1995](#MurayamaShimakawa95), though the statement of Prop. \ref{GraphOfACrossedHomomorphism} is still not explicit there.
\end{remark}


\begin{definition}\label{AdjointActionOnCrossedHomomorphisms}
**(crossed conjugation)**
\linebreak
  Two crossed homomorphisms 
  $\phi_1, \phi_2$ (Def. \ref{CrossedHomomorphism}) are [[adjoint action|adjoint]] $\phi_1 \xrightarrow{\;\gamma\;} \phi_2$ if in 
  their incarnation as homomorphisms to $\Gamma \rtimes G$  (Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}) they are related by conjugation with an element  
  $\gamma \in \Gamma \xhookrightarrow{\;} \Gamma \rtimes G$, in that:
  $$
    \underset{
      g \in G
    }{\forall}
    \;\;\;\;
    \phi_2(g)
    \;=\;
    \gamma^{-1}
      \cdot
    \phi_1(g)
      \cdot
    \alpha(g)(\gamma)
    \,.
  $$
\end{definition}

\begin{remark}\label{AsCoboundariesInGroupCohomology}
**(as 1-[[coboundaries]] in [[group cohomology]])**
\linebreak
  When $\Gamma$ is an [[abelian group]], the conjugates according to Def. \ref{AdjointActionOnCrossedHomomorphisms} 
of the constant function $const_{0}$ (Exp. \ref{ConstantFunctionOnNeutralElement}) are of the form
\[
  \label{GroupCoboundaryInSpecializationOfConjugation}
  g \;\mapsto\; \alpha(g)(\gamma) - \gamma
\]
(writing now in additive notation as befits an [[abelian group]]).

These (eq:GroupCoboundaryInSpecializationOfConjugation) are also known as "principal crossed homomorphisms".

With crossed homomorphisms understood as 1-[[cocycles]] in [[group cohomology]] 
(Rem. \ref{AsGroup1Cocycles}), these elements (eq:GroupCoboundaryInSpecializationOfConjugation) are the *1-[[coboundaries]]*.

The definitions here apply verbatim also for [[non-abelian group|non-abelian]] $\Gamma$, where we get [[non-abelian cohomology|non-abelian]] [[group cohomology]] (e.g. [NSW 2008, p. 16](#NSW08)).
\end{remark}


### As sliced functors of delooping groupoids

All the formulas [above](#ComponentDefinition) may conceptually be understood as follows:

\begin{proposition}
  \label{GroupoidOfCrossedHomorphismsIsSlicedFunctorGroupoid}
**([[groupoid]] of [[crossed homomorphisms]] is [[slice category|sliced]] [[functor groupoid]] of [[delooping groupoids]])**
\linebreak
  The [[groupoid]] 
  $$
     CrsHom(G,\Gamma) \sslash_{\!\! ad} \Gamma  
     \;\;\;
     \in
     \;
     Grpd
  $$
  of crossed homomorphisms (Def. \ref{CrossedHomomorphism}) with conjugations between them (Def. \ref{AdjointActionOnCrossedHomomorphisms}) is [[isomorphism|isomorphic]] to the [[slice category|sliced]] [[functor groupoid]] of [[sections]] of the [[delooping groupoid]] $\mathbf{B}(\Gamma \rtimes G)$ of the [[semidirect product group]]:

\[
  \label{SlicedFunctorGroupoid}
  CrsHom(G,\Gamma) \sslash_{\!\! ad} \Gamma
  \;\;
    \simeq
  \;\;
  Fnctr_{{}_{/\mathbf{B}G}}
  \big(
    \mathbf{B}G
    ,\,
    \mathbf{B}(\Gamma \rtimes G)
  \big)
  \;=\;
  Fnctr
  \big(
    \mathbf{B}G
    ,\,
    \mathbf{B}(\Gamma \rtimes G)
  \big)
  \underset{
    Fnctr
    \big(
      \mathbf{B}G
      ,\,
      \mathbf{B}G
    \big)
  }{\times}
  \{id\}
  \,.
\]
\end{proposition}
\begin{proof}
\label{ProofOfCrossedHomomorpismsAreSlicedFunctors}
By definition, a morphism in the groupoid on the right is a 
[[commuting diagram]] of [[functors]] and [[natural transformations]]
as shown on the left of the following:

\begin{imagefromfile}
    "file_name": "CrossedHomomorphismsAsSlicedFunctors210831.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/TED+cohomology)"
\end{imagefromfile}

Unwinding the definitions, it is clear that functors fitting into this diagram (indicated by the dashed single arrows on the left) are bijective (under passage to their component functions shown on the right) to [[group homomorphisms]] $G \to \Gamma \rtimes G$ whose [[composition]] with $\Gamma \rtimes G \xrightarrow{pr_2} G$ is the [[identity morphisms]] -- hence are bijective to crossed homomorphisms, by Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}.

Moreover, [[natural transformations]] $F \Rightarrow F'$ fitting into this diagram (indicated by the dashed double arrow on the left) must be such that their [[whiskering]] with $\mathbf{B}pr_2$ is the [[identity natural transformation]], which means that their single component (as shown on the right) is of the form

$$
  \eta(\bullet) \;=\; \big( \gamma, \mathrm{e}\big)
  \;\;\;
  \in
  \;
  \Gamma \rtimes G
  \,,
$$

where $\mathrm{e} \in G$ denotes the [[neutral element]].

In conclusion, the [[naturality square]] in $\mathbf{B}(\Gamma \rtimes G)$
that all these components must make [[commuting square|commute]] is of the form

$$
  \array{
    \bullet
    &\;\;\;\;\mapsto\;\;\;\;&
    \bullet
    &\xrightarrow{\;\;\;\;\;\;(\gamma,\mathrm{e})\;\;\;\;\;\;}&
    \bullet
    \\
    {}^{\mathllap{ g }}
    \big\downarrow
    &&
    \big\downarrow
    {}^{\mathrlap{ \big( \phi_1(g),\, g\big) }}
    &&
    \big\downarrow
    {}^{\mathrlap{ \big( \phi_2(g),\, g\big) }}
    \\
    \bullet
    &\;\;\;\;\mapsto\;\;\;\;&
    \bullet
    &\xrightarrow{\;\;\;\;\;\;(\gamma,\mathrm{e})\;\;\;\;\;\;}&
    \bullet
  }
  {\phantom{AAAAAAAAAAA}}
  \in
  \;
  \mathbf{B}(\Gamma \rtimes G)
  \,.
$$

Since [[composition]] in the [[delooping groupoid]] is given by the group product, this is equivalently the condition that

$$
    \big(
      \phi_2(g)
      ,\,
      g
    \big)
      \;=\;
    \big(
      \gamma^{-1}
      ,\,
      \mathrm{e}
    \big)
      \cdot 
    \big(
      \phi_1(g)
      ,\,
      g
    \big)
      \cdot 
    \big(
      \gamma
      ,\, 
      \mathrm{e}
    \big)
    \;\;\;\;\;
    \in
    \;
    \Gamma \rtimes G
    \,,
$$

which is equivalently the defining relation from Def. \ref{AdjointActionOnCrossedHomomorphisms}.  
\end{proof}

\begin{remark}
**([[conjugacy classes]] of [[crossed homomorphisms]] are [[non-abelian cohomology|non-abelian]] first [[group cohomology]])**
\linebreak
  In view of the identification of crossed homomorphisms with 1-cocycles in [[non-abelian cohomology|non-abelian]] [[group cohomology]], we may identify their conjugacy classes (Def. \ref{AdjointActionOnCrossedHomomorphisms}), hence, by Prop. \ref{GroupoidOfCrossedHomorphismsIsSlicedFunctorGroupoid}, the [[connected components]] of the sliced functor groupoid (eq:SlicedFunctorGroupoid)
with the group cohomology sets (at least for [[discrete groups]]):
$$
  CrsHom(H,\Gamma)_{/\sim}
  \;\simeq\;
  \pi_0
  \Big(
    Fnctr_{{}_{/\mathbf{B}G}}
    \big(
      \mathbf{B}G
      ,\,
      \mathbf{B}(\Gamma \rtimes G)
    \big)
  \Big)
  \;\simeq\;
  H^1_{Grp}(G,\Gamma)
  \,.
$$
\end{remark}


## Examples

Let $G \,\in\, Grp(Top)$ and $\Gamma \,\in\, Grp\big( G Act(Top) \big)$ be [[topological groups]] which are [[compact Lie groups]] (to be on the safe side). Then:

\begin{proposition}
\label{EquivariantConnectedComponentsOfEquivariantClassifyingSpaces}
**(equivariant connected components of equivariant classifying spaces)**
\linebreak
A [[topological G-space|G-equivariant]] [[classifying space]] $B_G \Gamma$ for $G$-[[equivariant bundle|equivariant]] $\Gamma$-[[principal bundles]] exists, and the [[connected components]] of its $H$-[[fixed loci]], for [[compact subgroups]] $H \subset G$, are in [[bijection]] to the [[conjugacy classes]] (Def. \ref{AdjointActionOnCrossedHomomorphisms}) of crossed homomorphisms (Def. \ref{CrossedHomomorphism}) from $H$ to $\Gamma$ (with respect to the [[restricted action]] of $H$ on $\Gamma$):

\[
  \label{EquivariantConnectedComponentsOfEquivariantClassifyingSpaces}
  \pi_0
  \left(
    \left(
      B_G \Gamma
    \right)^{H}
  \right)
  \;\;
  \simeq
  \;\;
  CrsHom(H,\Gamma)_{/\sim}
  \,.
\]
\end{proposition}
\begin{proof}
After a little reformulation via
Prop. \ref{GraphOfACrossedHomomorphism}
and
Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}, this is the statement of [Lashof & May 1986, Thm. 10](equivariant+bundle#LashofMay86), [May 1990, Thm. 7](#May90). 
\end{proof}



## Related concepts

* [[group extension]]

* [[group cohomology]]

* [[semidirect product group]]

* [[Fox derivative]]



## Literature

### To abelian groups

Discussion for the special case that $\Gamma$ is an [[abelian group]]:

in the context of [[homological algebra]]:

* {#MacLane75} [[Saunders Mac Lane]], Section IV.2 of: _Homology_ (1975) reprinted as Classics in Mathematics. Springer-Verlag, Berlin, 1995. x+422 pp. ISBN 3-540-58662-8 ([doi:10.1007/978-3-642-62029-4](https://link.springer.com/book/10.1007/978-3-642-62029-4))

in the context of [[group cohomology]]:

* {#Brown82} [[Kenneth Brown]],  p. 45 of: _Cohomology of Groups_, Graduate Texts in Mathematics, **87**, Springer 1982 ([doi:10.1007/978-1-4684-9327-6](https://link.springer.com/book/10.1007/978-1-4684-9327-6))


### To general groups

The general [[non-abelian group|non-abelian]] notion: 

In discussion of [[homotopy theory]] (together with [[crossed modules]]):

* {#Whitehead49} [[J. H. C. Whitehead]], Section 3 of: _Combinatorial Homotopy II_, Bull. Amer. Math. Soc., 55, (1949), 453 – 496 ([euclid:1183513797](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society/volume-55/issue-5/Combinatorial-homotopy-II/bams/1183513797.full))

In discussion of [[equivariant principal bundles]]:

* {#tomDieck69} [[Tammo tom Dieck]], Sec. 2.1 in: _Faserbündel mit Gruppenoperation_, Arch. Math 20, 136–143 (1969) ([doi:10.1007/BF01899003](https://doi.org/10.1007/BF01899003))

  > (not using the terminology "crossed homomorphism", but already characterizing their graphs, as in Lem. \ref{GraphOfACrossedHomomorphism})

* {#MurayamaShimakawa95} [[Mitutaka Murayama]], [[Kazuhisa Shimakawa]], p. 2 of: _Universal equivariant bundles_, Proc. Amer. Math. Soc. 123 (1995), 1289-1295 ([doi:10.1090/S0002-9939-1995-1231040-9](https://doi.org/10.1090/S0002-9939-1995-1231040-9))

As 1-[[cocycles]] in [[non-abelian cohomology|non-abelian]] [[group cohomology]]:

* {#NSW08} [[Jürgen Neukirch]], Alexander Schmidt, Kay Wingberg, pages 16 & 24 in: *Cohomology of Number Fields*, Springer Grundlehren der mathematischen Wissenschaften **323**, Springer 2008 ([doi:10.1007/978-3-540-37889-1](https://link.springer.com/book/10.1007/978-3-540-37889-1), [webpage](https://www.mathi.uni-heidelberg.de/~schmidt/NSW2e/))

* {#Milne17} [[James Milne]], Sections 15.a-b (16.a-b in the pdf) of: *Algebraic Groups*, Cambridge University Press 2017  ([doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf))

* Groupprops, *[First cohomology set with coefficients in a non-abelian group](https://groupprops.subwiki.org/wiki/First_cohomology_set_with_coefficients_in_a_non-abelian_group)*

Discussion for [[finite groups]]:

* Tsunenobu Asai, Yugen Takegahara, *On the number of crossed homomorphisms*, Hokkaido Math. J. **28** 3 (1999) 535-543 ([doi:10.14492/hokmj/1351001235](https://projecteuclid.org/journals/hokkaido-mathematical-journal/volume-28/issue-3/On-the-number-of-crossed-homomorphisms/10.14492/hokmj/1351001235.full))

Discussion for [[Lie groups]]:

* [[Karl-Hermann Neeb]], Def. 2.3 in: *Lie group extensions associated to projective modules of continuous inverse algebras*, Archivum Mathematicum, **44** 5 (2008) 465-489 ([dml:127115](https://dml.cz/handle/10338.dmlcz/127115))

[[!redirects crossed homomorphisms]]

[[!redirects crossed group homomorphism]]
[[!redirects crossed group homomorphisms]]




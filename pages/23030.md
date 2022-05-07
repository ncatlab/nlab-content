
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


## Definition

\begin{definition}\label{CrossedHomomorphism}
  Let $G \,\in\, $ [[Grp]] be a [[group]] (or [[group object]] [[internalization|internal]] to an ambient [[category]] with [[finite products]]) and let $\Gamma \,\in\, G Act$ be an $G$-[[equivariant group]], hence a [[group]] equipped with a [[group action]] 

$$
  \alpha \;\colon\; G \xrightarrow{\;\;} Aut_{Grp}(\Gamma)
$$ 

of $G$ on $\Gamma$ by [[group homomorphism|group]] [[automorphisms]].

Then a *crossed homomorphism* from $G$ to $\Gamma$ is a [[function]] ([[morphism]] in the [[internalization|ambient]] category)

$$
  \phi \;\colon\; G \xrightarrow{\;} \Gamma
$$

satisfying the following "$G$-crossed" homomorphism property:

$$
  \underset{g_1, g_2 \in G}{\forall}
  \;\;\;
  \phi(g_1 \cdot g_2)  
  \;=\;
  \phi(g_1) \cdot \alpha(g_1)\big( \phi(g)_2 \big)
  \,.
$$
\end{definition}

For [[abelian group|abelian]] $\Gamma$ this terminology seems to be due to [MacLane 1975, IV (2.1)](#MacLane75); for general ([[non-abelian group|non-abelian]]) $\Gamma$ it is used, e.g., in [Karpilovsky 1987, p. 39](#Karpilovsky87), [Murayama & Shimakawa 1995](#MurayamaShimakawa95), [Milne 2017, 15.a](#Milne17).

\begin{remark}
  For $\alpha$ the [[trivial action]], 
  the notion of a crossed homomorphism (Def. \ref{CrossedHomomorphism})
  reduces to that of an ordinary [[group homomorphism]].
\end{remark}

\begin{remark}\label{AsGroup1Cocycles}
**(as 1-[[cocycles]] in [[group cohomology]])**
\linebreak
  In the special case that $\Gamma$ in Def. \ref{CrossedHomomorphism} is an [[abelian group]], crossed homomorphisms are also known as *[[cocycles]] in [[group cohomology]]* in degree 1. In general they may be understood as 1-cocyles in [[non-abelian cohomology|non-abelian]] group cohomology.
\end{remark}

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
(e.g. [Brown 1982, p. 88](#Brown82), [Milne 2017, Exp. 15.1](#Milne17))
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


\begin{definition}\label{AdjointActionOnCrossedHomomorphisms}
  Two crossed homomorphisms 
  $\phi_1, \phi_2$ (Def. \ref{CrossedHomomorphism}) are [[adjoint action|adjoint]] $\phi_1 \xrightarrow{\;\gamma\;} \phi_2$ if in 
  their incarnation as homomorphisms to $\Gamma \rtimes G$  (Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}) they are related by conjugation with an element  
  $\gamma \in \Gamma \xhookrightarrow{\;} \Gamma \rtimes G$, in that:
  $$
    \underset{
      g \in G
    }{\forall}
    \;\;\;
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
    \,,
  $$
  where $\mathrm{e} \in G$ denotes the [[neutral element]].
\end{definition}
This notion (Def. \ref{AdjointActionOnCrossedHomomorphisms}) is implicit in some texts (see Prop. \ref{EquivariantConnectedComponentsOfEquivariantClassifyingSpaces} below) but is maybe not made explicit in existing literature. It may conceptually be understood as follows:

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
By definition, a morphism in the groupoid on the right is a 
[[commuting diagram]] of [[functors]] and [[natural transformations]]
as shown in the following:

\begin{tikzcd}
      &&
      \mathbf{B}(\Gamma \rtimes G)
      \ar[
        d,
        "\mathbf{B}\mathrm{pr}_2"
      ]
      \\
      \mathbf{B}G
      \mathrlap{\,.}
      \ar[
        rr,-,
        shift right=1pt
      ]
      \ar[
        rr,-,
        shift left=1pt
      ]
      \ar[
        urr,
        dashed,
        bend left=30,
        "\ "{right, name=s}
      ]
      \ar[
        urr,
        dashed,
        bend right=10,
        "\ "{left, name=t}
      ]
      &&
      \mathbf{B}G
      %
      \ar[
        from=s,
        to=t,
        dashed,
        Rightarrow
      ]
\end{tikzcd}

Unwinding the definitions, it is clear that functors fitting into this diagram (indicated by the dashed single arrows) are bijective to group homomorphisms $G \to \Gamma \rtimes G$ whose [[composition]] with $\Gamma \rtimes G \xrightarrow{pr_2} G$ is the [[identity morphisms]], hence are crossed homomorphisms, by Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}.

Moreover, natural transformations $\eta \;\colon\; F \Rightarrow F'$ fitting into this diagram (indicated by the dashed double arrow) must be such that their [[whiskering]] with $\mathbf{B}pr_2$ is the identity transformation, which means that their single component is of the form

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

which is precisely the defining relation from Def. \ref{AdjointActionOnCrossedHomomorphisms}.  
\end{proof}

\begin{remark}
**([[conjugacy classes]] of [[crossed homomorphisms]] are [[non-abelian cohomology|non-abelian]] first [[group cohomology]])**
\linebreak
  In view of the identification of crossed homomorphisms with 1-cocycles in [[non-abelian cohomology|non-abelian]] [[group cohomology]], we may identify their conjugacy classes (Def. \ref{AdjointActionOnCrossedHomomorphisms}), hence, by Prop. \ref{GroupoidOfCrossedHomorphismsIsSlicedFunctorGroupoid}, the [[connected components]] of the sliced functor groupoid (eq:SlicedFunctorGroupoid)
with the group cohomology sets:
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

$$
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
  \;\;
  \simeq
  \;\;
  H^1_{Grp}(H,\Gamma)
  \,.
$$
\end{proposition}
\begin{proof}
After a little reformulation using Prop. \ref{CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup}, this is the statement of [Lashof & May 1986, Thm. 10](equivariant+bundle#LashofMay86). 
\end{proof}


## Related concepts

* [[group extension]]

* [[group cohomology]]

* [[semidirect product group]]

## References

### To abelian groups

Discussion for the special case that $\Gamma$ is an [[abelian group]]:

in the context of [[homological algebra]]:

* {#MacLane75} [[Saunders Mac Lane]], Section IV.2 of: _Homology_ (1975) reprinted as Classics in Mathematics. Springer-Verlag, Berlin, 1995. x+422 pp. ISBN 3-540-58662-8 ([doi:10.1007/978-3-642-62029-4](https://link.springer.com/book/10.1007/978-3-642-62029-4))

in the context of [[group cohomology]]:

* {#Brown82} [[Kenneth Brown]],  p. 45 of: _Cohomology of Groups_, Graduate Texts in Mathematics, **87**, Springer 1982 ([doi:10.1007/978-1-4684-9327-6](https://link.springer.com/book/10.1007/978-1-4684-9327-6))


### To general groups

The general [[non-abelian group|non-abelian]] notion: 

* {#Karpilovsky87} [[Gregory Karpilovsky]], p. 39 of: *The Algebraic Structure of Crossed Products*, Mathematics Studies **142**, North Holland 1987 ([ISBN:9780080872537](https://www.elsevier.com/books/the-algebraic-structure-of-crossed-products/karpilovsky/978-0-444-70239-5))

In discussion of [[topological G-space|equivariant]] [[classifying spaces]] for [[equivariant principal bundles]]:

* {#MurayamaShimakawa95} [[Mitutaka Murayama]], [[Kazuhisa Shimakawa]], p. 2 of: _Universal equivariant bundles_, Proc. Amer. Math. Soc. 123 (1995), 1289-1295 ([doi:10.1090/S0002-9939-1995-1231040-9](https://doi.org/10.1090/S0002-9939-1995-1231040-9))

In discussion of [[algebraic groups]]:

* {#Milne17} [[James Milne]], Section 15.a (16.a in the pdf) of: *Algebraic Groups*, Cambridge University Press 2017  ([doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf))


Discussion for [[finite groups]]:

* Tsunenobu Asai, Yugen Takegahara, *On the number of crossed homomorphisms*, Hokkaido Math. J. **28** 3 (1999) 535-543 ([doi:10.14492/hokmj/1351001235](https://projecteuclid.org/journals/hokkaido-mathematical-journal/volume-28/issue-3/On-the-number-of-crossed-homomorphisms/10.14492/hokmj/1351001235.full))

Discussion for [[Lie groups]]:

* [[Karl-Hermann Neeb]], Def. 2.3 in: *Lie group extensions associated to projective modules of continuous inverse algebras*, Archivum Mathematicum, **44** 5 (2008) 465-489 ([dml:127115](https://dml.cz/handle/10338.dmlcz/127115))

[[!redirects crossed homomorphisms]]

[[!redirects crossed group homomorphism]]
[[!redirects crossed group homomorphisms]]




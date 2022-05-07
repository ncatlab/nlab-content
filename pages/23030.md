
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
* table of contebts
{:toc}


## Definition

\begin{definition}\label{CrossedHomomorphism}
  Let $G \,\in\, $ [[Grp]] be a [[group]] (or [[group object]] [[internalization|internal]] to an ambient [[category]] with [[finite products]]) and let $\Gamma \,\in\, G Act$ be an $G$-[[equivariant group]], hence a [[group]] equipped with a [[group action]] $\alpha \;\colon\; G \to Aut_{Grp}(\Gamma)$ of $G$ on $\Gamma$ by [[group homomorphism|group]] [[automorphisms]].

Then a *crossed homomorphism* from $G$ to $\Gamma$ is a [[function]] ([[morphism]] in the [[internalization|ambient]] category)

$$
  \phi \;\colon\; G \xrightarrow{\;} \Gamma
$$

satisfying the following "$G$-crossed" homomorphism property:

$$
  \phi(g_1 \cdot g_2)  
  \;=\;
  \phi(g_1) \cdot \alpha(g_1)\big( \phi(g)_2 \big)
  \,.
$$
\end{definition}

\begin{remark}
  For $\alpha$ the [[trivial action]], 
  the notion of a crossed homomorphism (Def. \ref{CrossedHomomorphism})
  reduces to that of an ordinary [[group homomorphism]].
\end{remark}

\begin{remark}\label{AbelianCase}
  In the special case that $\Gamma$ in Def. \ref{CrossedHomomorphism} is an [[abelian group]], crossed homomorphisms are also known as

* [[cocycles]] in [[group cohomology]] in degree 1; 

* *[[derivations on a group]]*. 

\end{remark}

## Properties

### Relation to semidirect product groups

\begin{proposition}
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


## Related concepts

* [[group extension]]

* [[group cohomology]]

* [[semidirect product group]]

## References

### To abelian groups

Discussion for the special case that $\Gamma$ is an [[abelian group]]:

in the context of [[homological algebra]]:

* [[Saunders Mac Lane]], Section IV.2 of: _Homology_ (1975) reprinted as Classics in Mathematics. Springer-Verlag, Berlin, 1995. x+422 pp. ISBN 3-540-58662-8 ([doi:10.1007/978-3-642-62029-4](https://link.springer.com/book/10.1007/978-3-642-62029-4))

in the context of [[group cohomology]] ("[[derivation on a group]]"):

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





+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### Plain notion
 {#PlainNotion}

By default, by a _real vector bundle_ over a plain [[topological space]] one means a [[vector bundle]] of [[real vector spaces]] [[associated bundle|associated]] to an $O(n)$-[[principal bundle]] for $O(n)$ the [[orthogonal group]].

This is in contrast notably to [[complex vector bundles]] or [[quaternionic vector bundles]].


### In KR-theory
 {#InKRTheory}

In the context of [[KR-theory]] ("Real K-theory") and following [Atiyah 1966 p. 368](#Atiyah66) one considers a more general notion (which subsumes the plain notion above, see Exp. \ref{RealVectorBundlesAsRealVectorBundles} below):

\begin{definition}
\label{AtiyahRealVectorBundle}
**(Atiyah Real vector bundles)**
\linebreak
A *Real vector bundle* (capital "R" for disambiguation) over a [[Real space]] -- namely over 

* a [[cyclic group of order 2|$\mathbb{Z}_2$]]-[[G-space|equivariant space]] 

  $$
    \mathbb{Z}_2 \curvearrowright X
    \;\in\;
    \mathbb{Z}_2 Top 
    \;=\;
    Func\big(
      \mathbf{B}\mathbb{Z}_2
      ,\,
      Top
    \big)
  $$

  hence a [[topological space]] equipped with a [[continuous map|continuous]] [[involution]]

  $$
    \sigma
    \,\colon\,
    X \longrightarrow X
    ,\;\;\;\;\;
    \sigma \circ \sigma = id_X
  $$

is (according to [Atiyah 1966 p. 368](#Atiyah66)):

1. a [[complex vector bundle]] $p \colon E \to X$ over the [[underlying]] [[topological space]] $X$ 

1. whose total space $E$ is equipped with a [[continuous map|continuous]] [[involution]] $(\text{-})^\ast \,\colon\, E \to E$

such that:

1. the bundle projection $p$ is a $\mathbb{Z}_2$-[[equivariant map]], hence such that the following [[commuting diagram|diagram commutes]]

   $$
     \array{  
       E &\overset{(\text{-})^\ast}{\longrightarrow}& E
       \\
       \mathllap{{}^p}\big\downarrow 
         && 
       \big\downarrow\mathrlap{{}^p}
       \\   
       X &\underset{\sigma}{\longrightarrow}& X
     }
   $$

1. the involution on $E$ is [[fiber]]-wise [[anti-linear map|anti-linear]], ie. for $x \in X$ the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       \mathbb{C} \times E_x
         &\overset{(\text{-})\cdot(\text{-})}{\longrightarrow}& 
       E_x
       \\
       \mathllap{
         {}^{ 
           \overline{(\text{-})}
           \times
           (\text{-})^\ast 
         }
       }
       \big\downarrow 
         &&
       \big\downarrow\mathrlap{{}^{
         (\text{-})^\ast
       }}
       \\
       \mathbb{C} \times E_{\sigma(x)}
         &\underset{(\text{-})\cdot(\text{-})}{\longrightarrow}& 
       E_{\sigma(x)}      
     }
   $$

A [[homomorphism]] of such Real vector bundles is a homomorphism of the underlying complex vector bundles which respects all the involutions. 
\end{definition}

\begin{remark}
  The complex numbers $\mathbb{C}$ equipped with their [[involution]] by [[complex conjugation]] under their usual multiplication operation form a [[monoid object]] [[internalization|internal]] to the category of $\mathbb{R}$-vector spaces equipped with $\mathbb{R}$-linear involution, the "[Real numbers](Hermitian+form#RealComplexNumbers)"
\[
  \label{RealComplexNumbers}
  \mathbb{Z}_2 \curvearrowright \mathbb{C}
  \;\;\;
  \in
  \;\;
  Mon\big(
    Func(\mathbf{B}\mathbb{Z}_2, Mod_{\mathbb{R}})
  \big)
  \,.
\]
The Real vector bundles of Def. \ref{AtiyahRealVectorBundle} are equivalently the vector bundles [[internalization|internal]] to the [[topos]] [[G-set|$\mathbb{Z}_2 Set$]] with the "[[ground ring|ground monoid]]" taken to be the Real numbers (eq:RealComplexNumbers).
\end{remark}


\begin{example}\label{RealVectorBundlesAsRealVectorBundles}
**(real vector bundles as Real vector bundles)**
\linebreak
  In the special case that the involution on the base space $X$ is trivial, $\sigma = id_X$, a Real vector bundle in the sense of Def. \ref{AtiyahRealVectorBundle} is a complex vector bundle over $X$ equipped continuously with a complex [[anti-linear map|anti-linear]] involution on each fiber $(\text{-})^\ast \,\colon\, E_x \to E_x$.

The resulting $\pm 1$-[[eigenspace]]-decomposition realizes each fiber as the [[complexification]] 

$$
  E_x 
   \;\simeq\; 
  V_x \oplus \mathrm{i} V_x
  \;\simeq\;
  V_x \otimes_{\mathbb{R}} \mathbb{C}
$$  

of a [[real vector space|$\mathbb{R}$-vector space]] and this decomposition is preserved by homomorphisms of Real vector bundles over such $X$, which are thus given by complexifications of morphisms of real vector bundles.

Therefore the [[full subcategory]] of Real vector bundles over a [[Real space]] $X$ whose [[involution]] is trivial is [[equivalence of categories|equivalent]] to that of plain real vector bundles over $X$ as [above](#PlainNotion).
(cf. [Atiyah 1966, p. 369](#Atiyah66))

In fact, more is true: the [[full subcategory]] of Real vector bundles on all objects whose base carries the trivial $\mathbb{Z}/2$-action is equivalent to the category [[VectBund]] of real vector bundles over varying base spaces
\[
  \label{RealVectorBundlesOverVaryingBaseSpaces}
  \array{
    \underset{X \in Top}{\textstyle{\int}}
    \mathbb{R}Vect_X
    &\xrightarrow{\; \sim \;}&
    \underset{
      (X,id) \in \mathbb{Z}/2 Top
    }{\textstyle{\int}}
    RealVect_X
    \,.
  }
\]
\end{example}



\begin{remark}\label{ComplexVectorBundlesAsRealBundles}
  Similarly to (eq:RealVectorBundlesOverVaryingBaseSpaces), there is a [[subcategory]]-inclusion of [[complex vector bundles]] over varying base spaces into Real vector bundles over varying bases spaces with [[free action]]
\[
  \label{RealVectorBundlesOverVaryingBaseSpaces}
  \array{
    \underset{X \in Top}{\textstyle{\int}}
    \mathbb{C}Vect_X
    &\xrightarrow{\; \sim \;}&
    \underset{
      (\mathbb{Z}/2 \times X) \in \mathbb{Z}/2 Top
    }{\textstyle{\int}}
    RealVect_{\mathbb{Z}/2 \times X}
    \\
    E
    &&
    E & \overline{E}
    \\
    \big\downarrow
    &\mapsto&
    \big\downarrow
    &
    \big\downarrow
    \\
    X
    &&
    \{0\} \times X
    &
    \{1\} \times X
    \,
  }
\]
where $\overline{E}$ denotes the vector bundle with fiber-wise anti-linear structure. However, as is this is not a [[full functor]]: On the right, if a bundle morphism is nontrivial on the base labels $0 \leftrightarrow 1$, the over the remaining base space it corresponds to a fiberwise [[anti-linear map]].

To make the above into an [[equivalence of categories]] one can equip the Real vector bundles moreover with involutions which square to -1 -- ie. [[complex structures]] [[internalization|internal]] to Real vector bundles! -- and require the maps to respect these further involutions. Then the functor which takes a "Real vector bundle with complex structure" over a free $\mathbb{Z}/2$-space to the $+\mathrm{i}$-[[eigenvalue]] bundle (of the internal complex structure), constitutes an equivalence with complex vector bundles.

In this sense the term "Real vector bundle" is quite appropriate.
\end{remark}


## Related concepts

* [[KO]], [[MO]]

* [[KR]], [[MR cohomology theory|MR]]

* [[Pontryagin class]]

* [[complex vector bundle]], [[quaternionic vector bundle]]

* [[real oriented cohomology theory]]

## References

### Plain notion

Real vector bundles in the plain sense are the default notion of [[vector bundles]], and as such are discussed in essentially every reference on the topic, see the list [there](vector+bundle#Literature).

### In KR-theory

The notion of "Real vector bundle" over a [[Real space]] in the sense of [[KR-theory]] was introduced in:

* {#Atiyah66} [[Michael Atiyah]], p. 368 in: *K-theory and reality*, The Quarterly Journal of Mathematics. Oxford. Second Series **17** 1 (1966)  367-386 &lbrack;[doi:10.1093/qmath/17.1.367](https://doi.org/10.1093/qmath/17.1.367), [[AtiyahKReal.pdf:file]], ISSN:0033-5606&rbrack;

* [[Allan L. Edelson]], *Real Vector Bundles and Spaces with Free Involutions*, Transactions of the American Mathematical Society **157** (1971) 179-188 &lbrack;[doi:10.2307/1995841](https://doi.org/10.2307/1995841), [jstor:1995841](https://www.jstor.org/stable/1995841)&rbrack;

* [[Allan L. Edelson]], *Real Line Bundles on Spheres*, Proceedings of the American Mathematical Society **27** 3 (1971) 579-583 &lbrack;[doi:10.2307/2036501](https://doi.org/10.2307/2036501), [jstor:2036501](https://www.jstor.org/stable/2036501)&rbrack;

  > (on Real [[line bundles]] over [[spheres]] [[group actions on spheres|with involution action]])


[[!redirects real vector bundles]]

[[!redirects Real vector bundle]]
[[!redirects Real vector bundles]]


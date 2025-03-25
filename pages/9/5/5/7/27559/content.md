
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


\tableofcontents


## Idea

Given a [[subgroup]] inclusion $H \xhookrightarrow{\iota} G$ there is the evident [[functor]] $\iota^\ast \,\colon\, Rep(G) \xrightarrow{\;} Rep(H)$ sending any [[linear representation]] of $G$ to its [[restricted representation]] of $H$.
The [[adjoints]] to this construction are given by forming left/right *[[induced representations]]*. 

But one may also ask, for any  [[linear representation]] $\rho \in Rep(H)$ of the subgroup, to *extend* it to a representation of $G$, namely to find any $\widehat{\rho} \in Rep(G)$ such that $\rho \,=\, \iota^\ast\big(\widehat{\rho}\big)$. 

Specifically, for $R$ the [[ground field]] (or [[ground ring]]) and $GL_n(R)$ denoting its [[general linear groups]] ($n \in \mathbb{N}$), then the given representation is equivalently a [[group homomorphism]] $H \xrightarrow{\rho} GL_n(R)$ and an extended representation of $\rho$ is an [[extension]] of this [[morphism]] along the group inclusion:

\begin{tikzcd}
  H 
  \ar[r, "{ \rho }"]
  \ar[d, "{ \iota }"]
  &
  \mathrm{GL}_n(R)
  \\
  G
  \ar[
    ur, dashed,
    "{
      \widehat{\rho}
    }"{swap}
  ]
\end{tikzcd}

Specifically when $H \xrightarrow{\iota} G$ is a [[normal subgroup]] inclusion and $\rho$ is an [[irreducible representation]], there is a classification of extended irreps, --- hence of irreps of $G$ *relative* to the given irrep of $H$ ---  either on the nose or at least as [[projective representations]] ([Isaacs 1976](#Isaacs76))

## Properties

### Extensions along normal subgroup inclusions
 {#ExtensionAlongNormalSubgroupInclusions}

Consider

* $N \xhookrightarrow{\iota} G$ a [[normal subgroup]] inclusion,

* $\rho \in Rep(N)$ an $N$-[[linear representation|representation]].

It is immediate but important that:

\begin{proposition}
  For $\rho$ to admit any extension to $G$ it is necessary that the [[isomorphism class]] $[\rho]$ of $\rho$ is [[invariant]] under the [[conjugation action]] 
$$
  \begin{array}{ccc}
    Rep(H) &\overset{(-)^g}{\longrightarrow}& Rep(H)
    \\
    \rho &\mapsto& \rho\big(g(-)g^{-1}\big)
  \end{array}
$$
by all elements $g \in G$:
\[
  \label{InvariantRepresentation}
  \underset{ g \in G }{\forall}
  \;\;\;
  [\rho] = \big[\rho^g\big]
  \,.
\]
\end{proposition}
\begin{proof}
  Consider $\widehat{\rho}$ any extension and $g \in G$ any element. Then the fact that $\widehat{\rho}$ is a $G$-representation extending $\rho$ implies for $n \in N$ that
$$
  \begin{array}{ccl}
    \widehat{\rho}(g) 
      \circ \rho(n) \circ 
    \widehat{\rho}(g^{-1})
    &=&
    \widehat{\rho}(g) 
      \circ \widehat{\rho}(n) \circ 
    \widehat{\rho}(g^{-1})
    \\
    &=&
    \widehat{\rho}\big(g n g^{-1}\big)
    \\
    &=&
    \rho\big(g n g^{-1}\big)
    \\
    &=&
    \rho^g(n)
    \,.
  \end{array}
$$
But this says equivalently that $\widehat{\rho}(g)$ is an [[intertwiner]] which constitutes an [[isomorphism]] of representations
$$
  \rho \xrightarrow[\sim]{ \widehat{\rho}(g) } \rho^g
  \,,
$$
and hence that $[\rho] = \big[\rho^g\big]$.
\end{proof}

Now assume in addition that 

* the [[ground field]] is [[algebraically closed field]], like the [[complex numbers]] $\mathbb{C}$,

* $\rho$ is an [[irreducible representation]],

* $\rho$ is $G$-invariant (eq:InvariantRepresentation)

\begin{proposition}\label{ExtensionOfInvariantNormalIrrepByProjectiveReps}
There always exists a *projective* extension of $\rho$ in the sense of a [[projective representation]] $\widetilde{\rho} \in PRep(G)$ satisfying, for $n \in N$ and $g \in G$,

1. $\widehat{\rho}(n) \,=\, \rho(n)$,

1. $\widehat{\rho}(g n) = \widehat{\rho}(g) \circ \widehat{\rho}(n)$,

1. $\widehat{\rho}(n g) = \widehat{\rho}(n) \circ \widehat{\rho}(g)$,

and any [[pair]] $\widehat{\rho}, \widehat{\rho}'$ of such differ only by a function on $G$ with values in the [[group of units]] $k^{\times}$ and depending only on [[cosets]],

   \[
     \label{DifferenceOfProjectiveExtensions}
     \mu 
       \,\colon\, 
     G \xrightarrow{\;} G/N \xrightarrow{\;} k^\times
     \,,
   \]

   in that

   $$
      \widetilde{\rho}'(-)
      \;=\;
      \widetilde{\rho}(-)
      \cdot
      \mu(-)
      \,.
   $$

\end{proposition}
([Isaacs 1976 Thm. 11.2](#Isaacs76))

\begin{proposition}\label{ExtensionOfInvariantNormalIrrepByActualRep}
Given any projective extension $\widetilde{\rho}$ according to Prop. \ref{ExtensionOfInvariantNormalIrrepByProjectiveReps}, the corresponding [[cocycle|2-cocycle]] in the [[group cohomology]] of $G$,
$$
  \widetilde{\alpha} \,\colon\, 
  G \times G
  \longrightarrow
  k^{\times}
  \,,
  \;\;\;\;\;\;\;\;\;\;
  \text{s.t.}
  \;\;\;\;\;\;\;\;\;\;
  \underset{g_i \in G}{\forall}
  \;\;
  \widetilde{\rho}(g_1)
  \circ
  \widetilde{\rho}(g_1)
  \;=\;
  \widetilde{\rho}(g_1 g_2)
  \cdot
  \widetilde{\alpha}(g_1, g_2)
  \,,
$$
comes from a 2-cocycle $\alpha$ on the [[quotient group]]
$$
  \widetilde{\alpha}
  \;\colon\;
  G \times G
  \twoheadrightarrow
  (G/N) \times (G/N)
  \xrightarrow{ \alpha }
  k^{\times}
$$

whose [[group cohomology]] class 
$$
  [\alpha] \,\in\, H^2\big(G/N;\, k^\times\big)
$$
depends only on $[\rho]$ (is independent of the choice of $\widetilde{\rho}$).

Finally, $\rho$ admits an actual extension $\widehat{\rho}$ iff that class is trivial, $[\alpha] = 0$.
\end{proposition}
([Isaacs 1976 Thm. 11.7](#Isaacs76))

\begin{remark}
  It follows moreover that if an extension $\widehat{\rho}$ exists, then this is unique up to multiplication with (the pullback to $G$ of) a [[group character]] $\mu$ on $G/N$ (eq:DifferenceOfProjectiveExtensions).
\end{remark}



## Related concepts

* [[extension]]

* [[restricted representation]]

* [[induced representation]]


## References

Monographs:

* {#Isaacs76} [[I. Martin Isaacs]]: around Thm. 11.7 in: *Character theory of finite groups*, Academic Press, New York (1976) &lbrack;[ISBN:978-0-8218-4229-4](https://bookstore.ams.org/view?ProductCode=CHEL/359.H)&rbrack;

* {#Navarro18} [[Gabriel Navarro]], sections 5 & 6 of: *Character Theory and the McKay Conjecture*, Cambridge University Press (2018) &lbrack;[doi:10.1017/9781108552790](https://doi.org/10.1017/9781108552790)&rbrack;

Further discussion:

* Peter Schmid: *Extending irreducible representations of normal subgroups*, Journal of Algebra **94** 1 (1985) 30-51 \[<a href="https://doi.org/10.1016/0021-8693(85)90203-0">doi:10.1016/0021-8693(85)90203-0</a>\]

* G. Karpilovsky: *On extension of characters from normal subgroups*, Proceedings of the Edinburgh Mathematical Society **27** (1984) 7-9 &lbrack;[doi:10.1017/S0013091500022057](https://doi.org/10.1017/S0013091500022057), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/B051526AE20F219C468AFBF1D9546E43/S0013091500022057a.pdf/on_extension_of_characters_from_normal_subgroups.pdf)&rbrack;

* Qiang Huang: *Extension of irreducible characters from normal subgroups*, Linear and Multilinear Algebra **27** 2 (1990) &lbrack;[doi;10.1080/03081089008818001](https://doi.org/10.1080/03081089008818001)&rbrack;


* Robert B. Howlett : *Extending characters from normal subgroups*, in *Topics in Algebra*, Lecture Notes in Mathematics **697** (2006) 1–7 &lbrack;[doi:10.1007/BFb0103119](https://doi.org/10.1007/BFb0103119)&rbrack;


[[!redirects extended representations]]



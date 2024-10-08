
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **ribbon category** &lbrack;[Reshetikhin & Turaev (1990)](#ReshetikhinTuraev90)&rbrack; (also called a **tortile category** &lbrack;[Joyal & Street (1993)](#JoyalStreet93), [Shum 1994](#Shum94), [Selinger 2011 §4.7](#Selinger11)&rbrack; or **balanced rigid braided tensor category**) is a [[monoidal category]] $(\mathcal{C}, \otimes, \mathbb{1}, \alpha, l, r)$ equipped with [[braiding]] $\beta=\{\beta_{X,Y}\}$, twist $\theta=\{\theta_X\}$ and duality $(\vee, b, d)$ that satisfy some compatibility conditions. 


## Definition

Recall that:

\begin{definition}\label{BraidedMonoidalCategory}
A **[[braided monoidal category]]** is a [[monoidal category]] $\mathcal{C}$ equipped with a [[braiding]] $\beta$, which is a [[natural isomorphism]] $\beta_{X,Y}\colon X \otimes Y \to Y \otimes X$ obeying the [[hexagon identities]].
\end{definition}

\begin{definition}\label{RigidMonoidalCategory}
A **[[rigid monoidal category]]** is a [[braided monoidal category]] (Def. \ref{BraidedMonoidalCategory}) where for every [[object]] $X$, there exist objects $X^{\vee}$ and ${^{\vee}}X$ (called its [[dualisable object|right and left dual]]) and associated morphisms
$$b_X:\mathbb{1}\to X^{\vee}\otimes X, d_X: X\otimes X^{\vee}\to \mathbb{1}$$
$$b_X:\mathbb{1}\to X\otimes {^{\vee}}X, d_X: {^{\vee}}X\otimes X\to \mathbb{1}$$
obeying the [[zig-zag identities]]:

$$(d_X\otimes \text{id}_X)\circ (\text{id}_X\otimes b_{X})=\text{id}_{X},$$

$$(\text{id}_{X^{\vee}}\otimes d_{X})\circ ( b_{X}\otimes \text{id}_{X^{\vee}})=\text{id}_{X^{\vee}}.$$
\end{definition}

Now:

\begin{definition}
A **twist** on rigid braided monoidal category (Def. \ref{RigidMonoidalCategory}) is a [[natural isomorphism]] from the [[identity functor]] to itself, with components $\theta_X \colon X \to X$ for which
$$
  \theta_{X\otimes Y}
    \;=\;
  \beta_{Y,X}
    \circ
  \beta_{X,Y}
    \circ
  \theta_{X}\otimes \theta_{Y}
  \,,
$$
$$
  \theta_{\mathbb{1}} 
    \;=\; 
  \mathrm{id}
  \,,
$$
$$
  \theta_{X^{\vee}} 
    \;=\;
  \theta_{X}^{\vee}
  \,.
$$

A **ribbon category** (*tortile category*) is a rigid braided monoidal category equipped with such a twist.
\end{definition}
(e.g. [Shum 1994 Def. 1.3](#Shum94)).

A [[functor]] between ribbon categories is a **ribbon functor** (*tortile functor*) if it preserves all this structure up to [[isomorphism]].


## Properties

### Relation to tangles

\begin{proposition}\label{ShumTheorem}
**([[Shum's theorem]])**
\linebreak
  The [[category of framed oriented tangles]] is [[equivalence of categories|equivalently]] the [[free construction|free]] [[ribbon category]] generated by a single [[object]].
\end{proposition}
([Shum 1994](#Shum94), [Yetter 2001 Thm. 9.1](#Yetter01))


## Related concepts

* [[modular tensor category]]


## References

* {#ReshetikhinTuraev90} [[Nicolai Reshetikhin]], [[Vladimir Turaev]], *Ribbon graphs and their invariants derived from quantum groups*, Commun. Math. Phys. **127** 1 (1990) &lbrack;[doi:10.1007/BF02096491](https://doi.org/10.1007/BF02096491)&rbrack;

* {#JoyalStreet93} [[André Joyal]], [[Ross Street]], *Braided tensor categories*, Advances in Mathematics **102** (1993) 20–78 &lbrack;[doi:10.1006/aima.1993.1055](https://doi.org/10.1006/aima.1993.1055)&rbrack;

* {#Turaev94} [[Vladimir Turaev]], §I.1 in: *Quantum invariants of knots and 3-manifolds*, de Gruyter Studies in Mathematics **18**, de Gruyter & Co. (1994) &lbrack;[doi:10.1515/9783110435221](https://doi.org/10.1515/9783110435221), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/turaev5.pdf)&rbrack;

* {#Shum94} [[Mei Chee Shum]], *Tortile tensor categories*, Journal of Pure and Applied Algebra **93** 1 (1994) 57-110 &lbrack;<a href="https://doi.org/10.1016/0022-4049(92)00039-T">10.1016/0022-4049(92)00039-T</a>&rbrack;

* {#Yetter01} [[David N. Yetter]]: *Functorial Knot Theory -- Categories of Tangles, Coherence, Categorical Deformations, and Topological Invariants*, Series on Knots and Everything **26**, World Scientific (2001) &lbrack;[doi:10.1142/4542](https://doi.org/10.1142/4542)&rbrack;


* {#Selinger11} [[Peter Selinger]], §4.7 in: *A survey of graphical languages for monoidal categories*, Springer Lecture Notes in Physics **813** (2011) 289-355 &lbrack;[arXiv:0908.3347](https://arxiv.org/abs/0908.3347), [doi:10.1007/978-3-642-12821-9_4](https://doi.org/10.1007/978-3-642-12821-9_4)&rbrack;

Lecture notes:

* [[Daniel Bump]]: *Ribbon categories*, lecture 4 of *[Quantum Groups](http://sporadic.stanford.edu/quantum/)* (2022) &lbrack;slides: [pdf](http://sporadic.stanford.edu/quantum/lecture4.pdf), [[Bump-RibbonCategories.pdf:file]], notes: [pdf](http://sporadic.stanford.edu/quantum/Lecture-10-13-22.pdf)&rbrack;


[[!redirects ribbon category]]
[[!redirects ribbon categories]]
[[!redirects tortile category]]
[[!redirects tortile categories]]
[[!redirects tortile monoidal category]]
[[!redirects tortile monoidal categories]]

[[!redirects ribbon functor]]
[[!redirects ribbon functors]]

[[!redirects tortile functor]]
[[!redirects tortile functors]]


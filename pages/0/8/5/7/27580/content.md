
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

In [[representation theory]], the notion of *twisted intertwiners* is a generalization of that of *[[intertwiners]]*. 

References using the exact terminology "twisted intertwiner" include [Fuchs & Schweigert 2000a (7.2)](#FuchsSchweigert00), [2000b (2.2)](#FuchsSchweigert00b), [Felder, Fröhlich, Fuchs & Schweigert 2000 (4.7)](#FelderFröhlichFuchsSchweigert00), but the notion itself is older and may be known under other names.

## Definition

\begin{definition}
For $G$ a [[group]] and $\rho_1, \rho_2 \;\in\; Rep(G)$ a [[pair]] of [[linear representation]] on [[vector spaces]] $V_1$, $V_2$, respectively (all this generalizes straightforwardly to [[algebras]] and their [[modules]]), a *twisted intertwiner*

$$
  \rho_1 \Rightarrow \rho_2
$$

is 

1. an [[automorphism]] $\alpha \in Aut(G)$ of the group

1. a [[linear map]] $\eta \colon V_1 \longrightarrow V_2$

such that for all $g \in G$ we have

\[
  \label{ComponentDefinition}
  \eta \circ \rho_1(g)
    \;=\;
  \rho_2\big(\alpha(g)\big) \circ \eta
  \,.
\]

Given a pair of twisted intertwiners of the form
$\rho_1 \overset{(\alpha,\eta)}{\Rightarrow} \rho_2 \overset{(\alpha',\eta')}{\Rightarrow} \rho_3$ their [[composition]] is given by composing their components separately.
\end{definition}

This reduces to the ordinary notion of [[intertwiners]] in the case that the [[automorphism]] is the [[identity map]], $\alpha = id_G$.

## Properties

### Category-theoretically

Writing $\mathbf{B}G$ for the [[delooping groupoid]] of $G$ and $Vec$ for the [[category of vector spaces]] (over a given [[ground field]]), the ordinary [[category]] [[Rep]] of $G$-[[representations]] and ordinary [[intertwiners]] $\eta \colon \rho_1 \Rightarrow \rho_2$ between these is [[equivalence of categories|equivalently]] the [[functor category]]

$$
  Rep(G) \;\;\simeq\;\;
  Func\big(
    \mathbf{B}G
    ,\,
    Vec
  \big)
  \,.
$$

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    d, 
    bend right=40, 
    "{ \rho_1 }"{swap, pos=.53}, 
    "{\ }"{name=s}
  ]
  \ar[
    d, 
    bend left=40, 
    "{ \rho_2 }"{pos=.53}, 
    "{\ }"{name=t, swap}
  ]
  \ar[from=s, to=t, Rightarrow, "{ \eta }"]
  \\
  \mathrm{Vec}
\end{tikzcd}

In contrast, the category of $G$-representations with twisted intertwiners between them is the [[iso-comma category|iso-comma]] [[(2,1)-category]] between $\mathbf{B}G \,\colon\, \mathbf{B}Aut(\mathbf{B}G) \longrightarrow Grpd$ (on the left the [[delooping]] of the [[automorphism 2-group]] of $G$) and $Vec \,\colon\, \ast \to Grpd$, whose [[1-morphisms]] are [[diagrams]] in [[Grpd]] of this form:

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr,
    "{ \mathbf{B}\alpha }"
  ]
  \ar[
    dr,
    "{ \rho_1 }"{swap, pos=.4}, 
    "{\ }"{name=s}
  ]
  &[-40pt]&[-40]
  \mathbf{B}G
  \ar[
    dl,
    "{ \rho_2 }"{pos=.4}, 
    "{\ }"{name=t, swap}
  ]
  \ar[
    from=s, to=t, Rightarrow, "{ \eta }"
  ]
  \\
  &
  \mathrm{Vec}
\end{tikzcd}

and whose [[2-morphisms]] are the evident paper-cup pasting diagrams


\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr,
    bend left=20,
    "{ \mathbf{B}\alpha }"{description},
    "{\ }"{name=s2, swap}
  ]
  \ar[
    rr,
    bend right=20,
    "{ \mathbf{B}\alpha' }"{description},
    "{\ }"{name=t2}
  ]
  \ar[
    from=s2, to=t2,
    Rightarrow, 
    "{ \sim }"{sloped}
  ]
  \ar[
    dr,
    "{ \rho_1 }"{swap, pos=.4}, 
    "{\ }"{name=s}
  ]
  &[-40pt]&[-40]
  \mathbf{B}G
  \ar[
    dl,
    "{ \rho_2 }"{pos=.4}, 
    "{\ }"{name=t, swap}
  ]
  \ar[
    from=s, to=t, 
    Rightarrow, 
    bend right=10,
    shift right=5pt,
    "{ \eta }"{swap}
  ]
  \\
  &
  \mathrm{Vec}
\end{tikzcd}


## References

The component-definition (eq:ComponentDefinition) is considered  (in the broad context of [[2d CFT]]) in:

* {#FelderFröhlichFuchsSchweigert00} [[Giovanni Felder]], [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Christoph Schweigert]]: *The geometry of WZW branes*, J. Geom. Phys. **34** (2000) 162-190 \[<a href="https://doi.org/10.1016/S0393-0440(99)00061-3">doi:10.1016/S0393-0440(99)00061-3</a>, [arXiv:hep-th/9909030](https://arxiv.org/abs/hep-th/9909030)\]

* {#FuchsSchweigert00a} [[Jürgen Fuchs]], [[Christoph Schweigert]]: *Symmetry breaking boundaries II. More structures; examples*, Nucl. Phys. B **568** (2000) 543-593 &lbrack;[arXiv:hep-th/9908025](https://arxiv.org/abs/hep-th/9908025), <a href="https://doi.org/10.1016/S0550-3213(99)00669-0">doi:10.1016/S0550-3213(99)00669-0</a>&rbrack;

* {#FuchsSchweigert00b} [[Jürgen Fuchs]], [[Christoph Schweigert]]: *Lie algebra automorphisms in conformal field theory*, in *[Conference on Infinite Dimensional Lie Theory and Conformal Field Theory](https://inspirehep.net/conferences/972922)* (May 2000) &lbrack;[arXiv:math/0011160](https://arxiv.org/abs/math/0011160)&rbrack;

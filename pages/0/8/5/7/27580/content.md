
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

References using the terminology "twisted intertwiner" include [Fuchs & Schweigert 2000a (7.2)](#FuchsSchweigert00a), [2000b (2.2)](#FuchsSchweigert00b), [Felder, Fröhlich, Fuchs & Schweigert 2000 (4.7)](#FelderFröhlichFuchsSchweigert00), but the notion itself is probably older and may (or may not) be known under other names.


## Definition
 {#Definition}

\begin{definition}
For $G$ a [[group]] consider its [[linear representations]] $(\rho, V)$, on [[vector spaces]] $V$, with $g \in G \;\vdash\; V \xrightarrow{\rho(g)} V$.

For $(\rho_1,V_1), (\rho_2, V_2) \;\in\; Rep(G)$ a [[pair]] of [[linear representation]] respectively (all this generalizes straightforwardly to [[algebras]] and their [[modules]]), a *twisted intertwiner*

$$
  (\rho_1, V_1) \xrightarrow{(\eta, \alpha)} (\rho_2, V_2)
$$

is 

1. a [[linear map]] $\eta \colon V_1 \longrightarrow V_2$,

1. an [[automorphism]] $\alpha \in Aut(G)$ of the group

such that 

\[
  \label{ComponentDefinition}
  \underset{g \in G}{\forall}
  \;\;\;
  \vdash
  \;\;\;
  \eta \circ \rho_1(g)
    \;=\;
  \rho_2\big(\alpha(g)\big) \circ \eta
  \,.
\]

Moreover, given a pair of consecutive twisted intertwiners
$(\rho_1, V_1) \xrightarrow{(\alpha,\eta)} (\rho_2, V_2) \xrightarrow{(\alpha',\eta')} (\rho_3, V_3)$, their [[composition]] is given by the [[direct product]] form

\[
  \label{CompositionOfTwistedIntertwiners}
  (\alpha', \eta')
  \circ
  (\alpha, \eta)
  \;=\;
  \big(
    \alpha' \circ \alpha
    ,\,
    \eta'
    \circ \eta
  \big)
  \,.
\]

\end{definition}

This reduces to the ordinary notion of [[intertwiners]] in the case that the [[automorphism]] is the [[identity map]], $\alpha = id_G$.

## Properties

### Deformations
 {#Deformations}

There naturally are [[2-morphisms|higher order morphisms]] between twisted intertwiners (these seem not to have been considered in the literature and do not carry an established name --- we here refer to them as "deformations", just to have a word):

\begin{definition}
\label{DeformationOfTwistedIntertwiners}
Given a [[parallel pair]] of twisted intertwiners $(\alpha, \eta), (\alpha', \eta')\,\colon\, (\rho_1, V_1) \rightrightarrows (\rho_2, V_2)$, then a deformation *between* these 

$$
  a \;\colon\; (\alpha, \eta) \Rightarrow (\alpha', \eta')
$$

is $a \in G$ such that

\[
  \label{ShiftingAlpha}
  \alpha' \;=\; Ad_a \circ \alpha
  \,,
\]

(where "$Ad$" denotes the [[adjoint action]] of a group on itself by [[inner automorphisms]], $Ad_a(g) \coloneqq a g a^{-1}$)

and

\[
  \label{ShiftingEta}
  \eta' \;=\; \rho_2(a) \circ \eta 
  \,.
\]

\end{definition}

\begin{remark}
  Conversely, if $(\eta, \alpha) \colon (\rho_1, V_1) \xrightarrow{\;} (\rho_2, V_2)$ is a twisted intertwiner, and $a \in G$, then also
$$
  \big(   
    \rho_2(a)
    \circ 
    \eta
    ,\, 
    Ad_A \circ\alpha\big)
  \;\colon\; 
  (\rho_1, V_1) \xrightarrow{\;} (\rho_2, V_2)
$$
is a twisted intertwiner:
$$
  \begin{array}{rcl}
    \eta' \circ \rho_1(g)
    &\equiv&
    \big(\rho_2(a) \circ \eta\big) \circ \rho_1(g)
    \\
    &=&
    \rho_2(a) \circ \eta \circ \rho_1(g)    
    \\
    &=& 
    \rho_2(a) \circ \rho_2\big(\alpha(g)\big) \circ \eta
    \\
    &=& 
    \rho_2(a) 
    \circ \rho_2\big(\alpha(g)\big) 
    \circ \rho_2(a)^{-1} \circ \rho_2(a)
    \circ \eta
    \\
    &=&
    \rho_2\big(a \cdot \alpha(g) \cdot a^{-1} \big) 
     \circ 
    \eta'
    \\
    &\equiv&
    \rho_2\big( \alpha'(g) \big) 
     \circ 
    \eta'
    \,.
  \end{array}
$$

In other words, the group $G$ [[group action|acts]] on the [[hom-sets]] of twisted intertwiners by deformations.
\end{remark}

\begin{lemma}
  For linear representations $(\rho_1, V_1)$, $(\rho_2, V_2)$, deformation (Def. \ref{DeformationOfTwistedIntertwiners}) of twisted intertwiners $(\rho_1, V_1) \xrightarrow{\;} (\rho_2, V_2)$ is an [[equivalence relation]], and [[composition]] of twisted intertwiners (eq:CompositionOfTwistedIntertwiners) passes to its [[equivalence classes]].
\end{lemma}
\begin{proof}
  That we have an equvalence relation is clear. To see that it is respected by composition, consider
$$
  (\eta, \alpha), (\eta', \alpha') \,\colon\, (\rho_1, V_1) \rightrightarrows (\rho_2, V_2)
$$
with
$$
  a \,\colon\, (\eta, \alpha) \Rightarrow (\eta', \alpha')
$$

and

1. another $(\widetilde{\eta}, \widetilde{\alpha}) \,\colon\, (\rho_2, V_2) \xrightarrow{\;} (\rho_3, V_3)$, then

   $$
     \widetilde{\alpha}(a)
     \;\colon\;
       (\widetilde{\eta}, \widetilde{\alpha}) 
         \circ 
       (\eta, \alpha)
     \Rightarrow
       (\widetilde{\eta}, \widetilde{\alpha}) 
         \circ 
       (\eta', \alpha')
   $$

   because:

   $$
     \begin{array}{rcl}
       \widetilde{\eta} \circ \eta'
       &=&
       \widetilde{\eta} \circ \rho_2(a) \circ \eta
       \\
       &=&
       \rho_3\big( \widetilde{\alpha}(a) \big)
       \circ \widetilde{ \eta } \circ \eta
     \end{array}
   $$
   and
   $$
     \begin{array}{rcl}
       \widetilde{\alpha} \circ \alpha'
       &=&
       \widetilde{\alpha} \circ Ad_a \circ \alpha
       \\
       &=&
       Ad_{\widetilde{\alpha}(a)} 
        \circ \widetilde \alpha \circ \alpha
       \,,
     \end{array}
   $$

   

1. another $(\widetilde{\eta}, \widetilde{\alpha}) \,\colon\, (\rho_0, V_0) \xrightarrow{\;} (\rho_1, V_1)$, then we have

   $$
     a \;\colon\;
       (\eta, \alpha)
         \circ 
       (\widetilde{\eta}, \widetilde{\alpha}) 
     \Rightarrow
       (\eta', \alpha')
         \circ 
       (\widetilde{\eta}, \widetilde{\alpha}) 
   $$

   immediately:

   $$
     \begin{array}{rcl}
       \eta' \circ \widetilde{\eta}
       &=&
       \rho_2(a) \circ \eta \circ \widetilde{\eta}
     \end{array}
   $$
   and
   $$
     \begin{array}{rcl}
       \alpha' \circ \widetilde{\alpha}
       &=&
       Ad_a \circ \alpha \circ \widetilde{\alpha}
       \,.
     \end{array}
   $$
 
\end{proof}


\begin{remark}
This means that 

* there is a [[2-category]] of representations, twisted intertwiners and deformations

* with a [[homotopy category]] of representations and deformation classes of twisted intertwiners.

This becomes manifest by recasting the original component definition (eq:ComponentDefinition) of twisted intertwiners as characterizing certain [[slice 2-category|slice morphisms]] in [[Cat]], to be discussed [below](#CategoryTheoreticDescription).
\end{remark}



### Category theoretic description
  {#CategoryTheoreticDescription}

We discuss how the properties of twisted intertwiners [above](#Definition) becomes manifest when understanding them as a natural construction in [[category theory]], via [[slice 2-category|slices]] of the [[2-category]] [[Cat]] of [[categories]], [[functors]] and [[natural transformations]]:

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
    "{ \rho_1 }"{swap, pos=.5}, 
    "{\ }"{name=s}
  ]
  &[-40pt]&[-40]
  \mathbf{B}G
  \ar[
    dl,
    "{ \rho_2 }"{pos=.5}, 
    "{\ }"{name=t, swap}
  ]
  \ar[
    from=s, to=t, Rightarrow, "{ \eta }"
  ]
  \\
  &
  \mathrm{Vec}
\end{tikzcd}

hence [[natural transformations]]

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr, 
    bend left=30,
    "{ \rho_1 }"{description},
    "{\ }"{swap, name=s}
  ]
  \ar[
    rr, 
    bend right=30,
    "{ \rho_2\big( \alpha(-) \big) }"{description},    
    "{\ }"{name=t}
  ]
  \ar[
    from=s, to=t,
    Rightarrow,
    "{ \eta }"
  ]
  &&
  \mathrlap{ \mathrm{Vec} }
  \\
  \ast
  \ar[
    d, "{ g }"
  ]
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  V_1 
  \ar[r, "{ \eta }"]
  \ar[
    d,
    "{ \rho_1(g) }"
  ]
    & 
  V_2
  \ar[
    d,
    "{ \rho_2\big( \alpha(g) \big) }"
  ]
  \\
  \ast
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  V_1
  \ar[r, "{ \eta }"]
  &
  V_2
\end{tikzcd}

whose [[commuting square|commuting]] [[naturality square]] is equivalent to the component equation (eq:ComponentDefinition),

and whose composition by [[whiskering]]

\begin{tikzcd}
  \mathbf{B}G
  \ar[r, "{ \alpha }"]
  \ar[
    dr,
    "{ \rho_1 }"{description},
    "{\ }"{name=s}
  ]
  &
  \mathbf{B}G
  \ar[r, "{ \alpha' }"]
  \ar[
    d,
    "{ \rho_2 }"{description, name=middle}
  ]
  &
  \mathbf{B}G
  \ar[
    dl,
    "{ \rho_3 }"{description},
    "{\ }"{swap, name=t}
  ]
  \ar[from=s, to=middle, Rightarrow, "{ \eta }"]
  \ar[from=middle, to=t, Rightarrow, "{ \eta' }"]
  \\
  &
  \mathrm{Vect}
\end{tikzcd}

is the [[natural transformation]]

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr, 
    bend left=30,
    "{ \rho_1 }"{description},
    "{\ }"{swap, name=s}
  ]
  \ar[
    rr, 
    bend right=30,
    "{ \rho_3\big( \alpha'\circ \alpha(-) \big) }"{description},    
    "{\ }"{name=t}
  ]
  \ar[
    from=s, to=t,
    Rightarrow,
    "{ \eta }"
  ]
  &&
  \mathrlap{ \mathrm{Vec} }
  \\
  \ast
  \ar[
    d, "{ g }"
  ]
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  V_1 
  \ar[r, "{ \eta }"]
  \ar[
    d,
    "{ \rho_1(g) }"
  ]
    & 
  V_2
  \ar[
    d,
    "{ \rho_2\big( \alpha(g) \big) }"
  ]
  \ar[r, "{ \eta' }"]
  &
  V_3
  \ar[
    d,
    "{ \rho_3\big( \alpha'(\alpha(g)) \big) }"
  ]
  \\
  \ast
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  V_1
  \ar[r, "{ \eta }"]
  &
  V_2
  \ar[r, "{ \eta' }"]
  &
  V_r
\end{tikzcd}

which reflects the composition law (eq:CompositionOfTwistedIntertwiners),

while the [[2-morphisms]] are the evident paper-cup pasting diagrams

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr,
    bend left=20,
    "{ \mathbf{B}\alpha' }"{description},
    "{\ }"{name=t2, swap}
  ]
  \ar[
    rr,
    bend right=20,
    "{ \mathbf{B}\alpha }"{description},
    "{\ }"{name=s2}
  ]
  \ar[
    from=s2, to=t2,
    Rightarrow, 
    "{ a }"{swap}
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
    shift right=2pt,
    "{ \eta }"{swap}
  ]
  \\
  &
  \mathrm{Vec}
\end{tikzcd}

where

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr, 
    bend left=30,
    "{ \alpha }"{description},
    "{\ }"{swap, name=s}
  ]
  \ar[
    rr, 
    bend right=30,
    "{ \alpha' }"{description},    
    "{\ }"{name=t}
  ]
  \ar[
    from=s, to=t,
    Rightarrow,
    "{ a }"
  ]
  &&
  \mathbf{B}G
  \\
  \ast   
  \ar[d, "{ g }"]
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  \ast
  \ar[r, "{ a }"]
  \ar[d, "{ \alpha(g) }"]
  &
  \ast
  \ar[d, "{ \alpha'(g) }"]
  \\
  \ast
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  \ast
  \ar[r, "{ a }"]
  &
  \ast
\end{tikzcd}

gives the relation (eq:ShiftingAlpha),

from $(\alpha, \eta)$ to the [[whiskering|whiskered]] (now on the other side) composite transformation

\begin{tikzcd}
  \mathbf{B}G
  \ar[
    rr, 
    bend left=30,
    "{ \rho_1 }"{description},
    "{\ }"{swap, name=s}
  ]
  \ar[
    rr, 
    bend right=30,
    "{ \rho_2\big( \alpha'(-) \big) }"{description},    
    "{\ }"{name=t}
  ]
  \ar[
    from=s, to=t,
    Rightarrow,
    "{ \rho_2 \cdot a }"
  ]
  &&
  \mathrlap{ \mathrm{Vec} }
  \\
  \ast
  \ar[
    d, "{ g }"
  ]
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  V_1 
  \ar[r, "{ \eta }"]
  \ar[
    d,
    "{ \rho_1(g) }"
  ]
    & 
  V_2
  \ar[
    d,
    "{ \rho_2\big( \alpha(g) \big) }"
  ]
  \ar[
    r, 
    "{ \rho_2(a) }"
  ]
  &
  V_2
  \ar[
    d,
    "{ \rho_2\big(\alpha'(g)\big) }"
  ]
  \\
  \ast
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  V_1
  \ar[r, "{ \eta }"]
  &
  V_2
  \ar[
    r, 
    "{ \rho_2(a) }"
  ]
  &
  V_2
\end{tikzcd}

exhibiting the relation (eq:ShiftingEta).


## References

The component-definition (eq:ComponentDefinition) is considered  (broadly in a context of [[2d CFT]]) in:

* {#FuchsSchweigert00a} [[Jürgen Fuchs]], [[Christoph Schweigert]]: *Symmetry breaking boundaries II. More structures; examples*, Nucl. Phys. B **568** (2000) 543-593 &lbrack;[arXiv:hep-th/9908025](https://arxiv.org/abs/hep-th/9908025), <a href="https://doi.org/10.1016/S0550-3213(99)00669-0">doi:10.1016/S0550-3213(99)00669-0</a>&rbrack;

* {#FelderFröhlichFuchsSchweigert00} [[Giovanni Felder]], [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Christoph Schweigert]]: *The geometry of WZW branes*, J. Geom. Phys. **34** (2000) 162-190 \[<a href="https://doi.org/10.1016/S0393-0440(99)00061-3">doi:10.1016/S0393-0440(99)00061-3</a>, [arXiv:hep-th/9909030](https://arxiv.org/abs/hep-th/9909030)\]


* {#FuchsSchweigert00b} [[Jürgen Fuchs]], [[Christoph Schweigert]]: *Lie algebra automorphisms in conformal field theory*, in *[Conference on Infinite Dimensional Lie Theory and Conformal Field Theory](https://inspirehep.net/conferences/972922)* (May 2000) &lbrack;[arXiv:math/0011160](https://arxiv.org/abs/math/0011160)&rbrack;

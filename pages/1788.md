$$
  \array{
      \pi^V\left( S^V\right)^{\{0,\infty\}/}
      &
        \overset{\simeq}{\longrightarrow}
      &
      \underset{
        {
          {
              {H \in \mathrm{Isotr}_{S^V}(G)}
              \atop
              {H \neq G}
          }
        }
      }{\prod}
      \;\;
      {\vert W_G(H)\vert } \cdot \mathbb{Z}
      \\
      \big[
        S^V
          \overset{c}{\longrightarrow}
        S^V
      \big]
      &\mapsto&
      \Big(
        H 
          \mapsto
        \mathrm{deg}
        \big(
          c^H
        \big)
        -
        \mathrm{offs}(c,H)
      \Big)
  }
$$

***

\begin{centre}

\begin{tikzpicture}

\fill (0,0) circle[radius=2em];

\end{tikzpicture}

\end{centre}

An XY-Matrix diagram:

\begin{centre}

\begin{xymatrix}

A \ar[r] \ar[dr] & B^{2} \ar[d] \\ & C

\end{xymatrix}

\end{centre}

\begin{centre}

\begin{xymatrix[font = \large]}

A \rtwocell^f_g{\alpha} & B

\end{xymatrix}

\end{centre}

\begin{centre}

\begin{xymatrix[border = 2pc]}

A \ar@/^2.0pc/[r] \ar@/_2.0pc/[r] & B

\end{xymatrix}

\end{centre}

    <nowiki>
    \begin{tikzpicture}

    \draw (0,0) -- (2,0) -- (2,-2);

    \end{tikzpicture}
    </nowiki>

[[cellular model]]


***

##2-Functor##

###Idea###

A $2$-functor $F:\mathfrak{C}\to\mathfrak{D}$ is a mapping between $2$-categories that respects the composition of 1-cells/2-cells and identity 1-cells/2-cells in an appropriate sense.  At the 2-categorical level there are several possible versions of this notion one might want depending on the given setting, all of which collapse to the standard definition of a functor between categories when considered on $2$-categories with discrete hom-categories (viewed as $1$-categories). The least restrictive of these is a [[lax functor]], and the strictest is (appropriately) called a [[strict 2-functor]].

###Definition###

Let $\mathfrak{C}$ and $\mathfrak{D}$ be [[2-categories]]. A pseudofunctor $F:\mathfrak{C}\to\mathfrak{D}$ consists of

* A function $P:Ob_\mathfrak{C}\to Ob_\mathfrak{D}$, and for each pair of objects $A,B\in Ob_\mathfrak{C}$ a functor 

\begin{centre}

$P_{A,B}:\mathfrak{C}(A,B)\to\mathfrak{D}(P(A),P(B)).$ 

\end{centre} 

We will generally write the function and functors as $P$.

* For each pair of horizontally composable 1-cells $(f,g)\in Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$, a $2$-cell isomorphism $\gamma_{f,g}:P(g\circ f)\Rightarrow P(g)\circ P(f)$ called the _associator_ as below 

\begin{centre}

\begin{xymatrix@C20mm}

P(A) \rtwocell^{P(g\circ f)}_{P(g)\circ P(f)}{\;\;\;\;\gamma_{f,g}} & P(C)

\end{xymatrix}

\end{centre}

* For each object object $A\in Ob_\mathfrak{C}$, a $2$-cell isomorphism $\iota_A:P(1_A)\Rightarrow1_{P(A)}$ called the _unitor_ as below

\begin{centre}

\begin{xymatrix@C20mm}

P(A) \rtwocell^{P(1_A)}_{1_{P(A)}}{\;\;\;\;\iota_A} & P(A)

\end{xymatrix}

\end{centre}

These are subject to the following two axioms:

1. For any composable triplet of $1$-cells $(f,g,h)\in Ob_{\mathfrak{C}(C,D)}\times Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$ we have that 

\begin{centre}

$\gamma_{f\circ g,h}\circ(\gamma_{f,g}\star 1_{P(h)})=\gamma_{f,g\circ h}\circ(1_{P(f)}\star\gamma_{g,h}),$

\end{centre}

where $\circ$ denotes vertical composition and $\star$ denotes horizontal composition, as illustrated by the following commutative $2$-cell diagram in $\mathfrak{D}(P(A),P(D))$:

\begin{centre}

\begin{xymatrix@R20mm@C20mm}

P(f)\circ P(g)\circ P(h) \ar@2{->}[d]_{\gamma_{f,g}\star 1_{P(h)}} \ar@2{->}[r]^{1_{P(f)}\star\gamma_{g,h}} & P(f)\circ P(g\circ h)\ar@2{->}[d]^{\gamma_{f,g\circ h}} \\ P(f\circ g)\circ P(h)\ar@2{->}[r]_{\gamma_{f\circ g,h}} & P(f\circ g\circ h)

\end{xymatrix}

\end{centre}

2. For any composable $1$-cells $(f,g)\in Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$ we have that 

\begin{centre}

$\iota_B\star 1_{P(B)}=\gamma_{1_B,g}$,

\end{centre}

\begin{centre}

$1_{P(f)}\star\iota_B=\gamma_{f,1_B}$,

\end{centre}

as illustrated by the commutative $2$-cell diagrams below

\begin{centre}

\begin{xymatrix@R30mm@C35mm}

P(A)\rtwocell^{P(g)}_{P(g)}{\;\;\;\;\;\;1_{P(g)}} \drtwocell<5.5>_{P(g)\;\;\;\;\;}^{\;\;\;\;\;\;\;\;\;\;\;\;\;\;P(1_B)\circ P(g)}{\;\;\;\;\;\;\;\gamma_{1_B,g}} & P(B) \dtwocell^{\;\;\;\;\;\;P(1_B)}_{1_{P(B)\;\;\;\;\;\;}}{\iota_B} \\ & P(B)} 
\xymatrix@R30mm@C35mm{P(B) \rtwocell^{P(1_C)}_{1_{P(C)}}{\;\;\;\;\iota_B} \drtwocell<5.5>_{P(f)\;\;\;\;\;}^{\;\;\;\;\;\;\;\;\;\;\;\;\;\;P(1_C)\circ P(f)}{\;\;\;\;\;\;\;\gamma_{f,1_B}} & P(B) \dtwocell<4>^{\;\;\;\;P(f)}_{P(f)\;\;\;\;}{1_{P(f)}} \\ & P(C)

\end{xymatrix}

\end{centre}


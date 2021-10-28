
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The __Godement product__ of two [[natural transformations]] between appropriate [[functors]] is their [[horizontal composition]] as 2-cells in the [[2-category]] [[Cat]] of [[categories]], functors and natural transformations:

\begin{tikzcd}[column sep=small]
\textbf{A}
 \arrow[to=1-5, bend left=50]{r}[name=F1]{F_1}
 \arrow[to=1-5, bend right=50]{r}[name=G1,label=below:$\scriptstyle G_1$]{}
 \arrow[phantom,Rightarrow,to path={(F1) -- node[] {$\big\Downarrow\normalsize\alpha$} (G1)}]{}
 &&&& \textbf{B}
 \arrow[to=1-9, bend left=50]{r}[name=F2]{F_2}
 \arrow[to=1-9, bend right=50]{r}[name=G2,label=below:$\scriptstyle G_2$]{}
 \arrow[phantom,Rightarrow,to path={(F2) -- node[] {$\big\Downarrow\normalsize\beta$} (G2)}]{}
 &&&& \textbf{C}
 \arrow[to=1-10, mapsto]
 & \textbf{A}
 \arrow[to=1-14, bend left=50]{r}[name=F3]{F_2 \circ F_1}
 \arrow[to=1-14, bend right=50]{r}[name=G3,label=below:$\scriptstyle G_2 \circ G_1$]{}
 \arrow[phantom,Rightarrow,to path={(F3) -- node[] {$\big\Downarrow\normalsize\beta\circ\alpha$} (G3)}]{}
 &&&& \textbf{C}
\end{tikzcd}


## Definition

For [[categories]] $A,B,C$, if $\alpha\colon F_1\to G_1\colon A\to B$ and $\beta\colon F_2\to G_2\colon B\to C$ are [[natural transformation]]s of [[functor]]s, the components $(\beta \circ \alpha)_M$ of the Godement product $\beta \circ \alpha\colon F_2\circ F_1\to G_2\circ G_1\colon A\to C$ (or $\alpha \ast \beta\colon F_1 ; F_2 \to G_1 ; G_2\colon A\to C$) are defined by any of the two equivalent formulas:
$$
(\beta\circ\alpha)_M = \beta_{G_1(M)}\circ F_2(\alpha_M)
$$
$$
(\beta\circ\alpha)_M = G_2(\alpha_M)\circ \beta_{F_1(M)}
$$
that can be rewritten using the [morphismwise notation](natural+transformations#morphismwiseDefn) into:
$$
(\beta\circ\alpha)_M = \beta(\alpha_M)
$$
that is:
$$
  \array{
    F_2(F_1(M))
    &
    \stackrel{F_2(\alpha_M)}{\to}
    &
    F_2(G_1(M))
    \\
    \beta_{F_1(M)}\downarrow
    &
    \searrow^{(\beta\circ\alpha)_M}
    &
    \downarrow \beta_{G_1(M)}
    \\ G_2(F_1(M))
    &
    \stackrel{G_2(\alpha_M)}{\to} & G_2(G_1(M))
  }
  \,.
$$

The [[interchange law]] in (general) $2$-categories (which in the case of $Cat$ boils down to assertion that the two formulas above are equivalent) is also sometimes called _Godement interchange law_.

The definition above is for the Godement product of $2$ natural transformations, but we can generalise from $2$ to any [[natural number]].  The Godement product of $0$ natural transformations is the __[[identity natural transformation]] on an [[identity functor]]__.


## Properties

The Godement product is strictly associative (so that [[Cat]] is a [[strict 2-category]]).

## References

Name after [[Roger Godement]].

[[!redirects Godement product]]
[[!redirects Godement products]]

[[!redirects horizontal composite of natural transformations]]
[[!redirects horizontal composites of natural transformations]]
[[!redirects horizontal composition of natural transformations]]
[[!redirects horizontal compositions of natural transformations]]

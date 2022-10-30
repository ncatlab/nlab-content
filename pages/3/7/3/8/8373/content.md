
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

In [[algebraic topology]], a [[continuous function]] between [[topological spaces]] is called **$n$-connected** if it induces [[isomorphisms]] on all [[homotopy groups]] in degree $\lt n$ and [[epimorphisms]] in degree $n$. 

In older literature this is often called an **$n$-equivalence**, since an $\infty$-equivalence in this sense is a  _[[weak homotopy equivalence]]_.

In terms of the [[homotopy theory]] presented by the [[classical model structure on topological spaces]], an $n$-connected function represents an [[n-connected morphism]] in the [[(∞,1)-topos]] [[∞Gpd]].

## Definition


+-- {: .num_defn }
###### Definition

A map of [[topological space|topological spaces]] $f \colon X \to Y$ is called __$n$-connected__ (e.g. [tomDieck 08, p. 144](#tomDieck08)) or an __$n$-equivalence__ (older literature) if the following equivalent definitions hold:

1. The induced morphism on [[homotopy groups]] $\pi_\bullet(X,x)\to \pi_\bullet(Y,f(x))$ is, for all $x\in X$

   1. an [[isomorphism]] in degree $\lt n$;

   1. an [[epimorphism]] in degree $n$.

1. for all $i \le n$ and all commutative squares

  $$
    \begin{matrix}
      S^{i-1} & \overset{u}{\longrightarrow} & X 
      \\
      \big\downarrow & & \, \big\downarrow^\mathrlap{f} 
      \\
      D^i & \underset{v}{\longrightarrow} & Y
    \end{matrix}
  $$

  there exists a map $w \colon D^i \to X$ such that $w | S^{i-1} = u$ and $f w$ is homotopic to $v$ relative to $S^{i-1}$.

=--

Hence an $\infty$-connected map is a [[weak homotopy equivalence]].

## Properties

+-- {: .num_prop }
###### Proposition

For a map $f \colon X \to Y$ and an integer $n \ge -1$ the following conditions are equivalent.

1. $f$ is $n$-connected.

1. All [[homotopy fibers]] of $f$ are $(n-1)$-[[n-connected space|connected]].

=--

+-- {: .num_prop }
###### Proposition

Let $f \colon X \to Y$ and $g \colon Y \to Z$ be maps of spaces.

1. If $f$ and $g$ are $n$-connected, then so is $g f$.

1. If $f$ is $(n-1)$-connected and $g f$ is $n$-connected, then $g$ is $n$-connected.

1. If $g$ is $(n+1)$-connected and $g f$ is $n$-connected, then $f$ is $n$-connected.

=--

+-- {: .num_prop }
###### Proposition

Let
$$
\begin{matrix}
  B & \longleftarrow & A & \longrightarrow & C \\
  \mathllap{{}^g}\big\downarrow & & \big\downarrow^\mathrlap{f} & & \, \big\downarrow^\mathrlap{h} \\
  B' & \longleftarrow & A' & \longrightarrow & C'
\end{matrix}
$$
be a commutative diagram of maps of spaces. If $f$ is $(n-1)$-connected and $g$ and $h$ are $n$-connected, then the induced map between [[homotopy pushout|homotopy pushouts]] $B \sqcup_A^h C \to B' \sqcup_{A'}^h C'$ is $n$-connected.

=--

This is ([tom Dieck, Theorem 6.7.9](#tomDieck)).

+-- {: .num_prop }
###### Proposition

Let
$$
\begin{matrix}
  Y & \longrightarrow & X & \longleftarrow & Z \\
   \mathllap{{}^g} \big\downarrow & & \big\downarrow^\mathrlap{f} & & \, \big\downarrow^\mathrlap{h} \\
  Y' & \longrightarrow & X' & \longleftarrow & Z'
\end{matrix}
$$
be a commutative diagram of maps of spaces. If $f$ is $(n+1)$-connected and $g$ and $h$ are $n$-connected, then the induced map between [[homotopy pullback|homotopy pullbacks]] $Y \times_X^h Z \to Y' \times_{X'}^h Z'$ is $n$-connected.

=--

## Related concepts

* [[Postnikov tower]]

* [[n-image]]

## References

Textbook accounts:

* {#tomDieck08}[[Tammo tom Dieck]],  p. 144 and Thm 6.7.9 in: _Algebraic topology_, European Mathematical Society, Zürich (2008) ([doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/diecktop.pdf))
 

[[!redirects n-connected continuous functions]]

[[!redirects n-connected map]]
[[!redirects n-connected maps]]

[[!redirects n-simply connected map]]
[[!redirects n-simply connected maps]]

[[!redirects n-simply connected continuous function]]
[[!redirects n-simply connected continuous functions]]

[[!redirects n-equivalence]]
[[!redirects n-equivalences]]

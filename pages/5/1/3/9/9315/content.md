
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

For $G$ a [[group]] with [[action]] on two [[objects]] $X$ and $Y$, the *diagonal action* is canonically induced action on the [[product]] $X \times Y$. 

## Definition

Consider a [[group]] $G$ and a [[pair]] of [[sets]] $X_1, X_2 \,\in\, Set$, each equipped with a [[group action]]

$$
  \begin{array}{ccc}
    G \times X_i &\xrightarrow{\phantom{---}}& X_i
    \\
    (g,x_i) &\mapsto& g(x_i)
    \mathrlap{\,.}
  \end{array}
$$

In components, the *diagonal action* of $G$ on the [[Cartesian product]] $X_1 \times X_2$ is given by

$$
  \begin{array}{ccc}
    G \times (X_1 \times X_2) 
      &\xrightarrow{\phantom{-}g\phantom{-}}& 
    X_1 \times X_2
    \\
    \big(
     g, (x_1, x_2)
    \big)
    &\mapsto&
    \big(
      g(x_1)
      ,\,
      g(x_2)
    \big)
    \mathrlap{\,.}
  \end{array}
$$ 

More abstractly, regarding the $X_i \in G Set$ as [[G-sets]], the diagonal action is just their Cartesian product as such, formed in the [[category]] $G Set$.

## Related entries

* [[trivial action]]

* [[adjoint action]]

## Related concepts

* [[diagonal]]

* [[Atiyah Lie groupoid]]

[[!redirects diagonal actions]]

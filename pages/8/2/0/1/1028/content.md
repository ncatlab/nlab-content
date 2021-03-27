
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### In category theory

An **equalizer** is a [[limit]] 
$$\operatorname{eq}\underset{\quad e \quad}{\to}x\underoverset{\quad g \quad}{f}{\rightrightarrows}y$$
over a parallel pair i.e. of the [[diagram]] of the shape 
$$\left\lbrace
      x \underoverset{\quad g \quad}{f}{\rightrightarrows} y
  \right\rbrace.$$
(See also [[fork]] diagram).

This means that for $f : x \to y$ and $g : x \to y$ two [[parallel morphisms]] in a [[category]] $C$, their equalizer is, if it exists

* an object $eq(f,g) \in C$;

* a morphism $eq(f,g) \to x$

* such that 

  * pulled back to $eq(f,g)$ both morphisms become [[equality|equal]]: $ (eq(f,g) \to x \stackrel{f}{\to} y) = (eq(f,g) \to x \stackrel{g}{\to} y) $
  * and $eq(f,g)$ is the [[universal property|universal object]] with this property.

The dual concept is that of [[coequalizer]].

### In type theory

In [[type theory]] the [[equalizer]]
$$P \to A \stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}} B$$
is given by the [[dependent sum]] over the [[dependent type|dependent]] [[equality type]]
$$P \simeq \sum_{a : A} (f(a) = g(a)).$$

## Examples

* In $C =$ [[Set]] the equalizer of two functions of sets is the subset of elements of $c$ on which both functions coincide.
$$eq(f,g)=\left\{
     s \in c | 
     f(s) = g(s)
  \right\}.$$

* For $C$ a category with [[zero object]] the equalizer of a morphism $f : c \to d$ with the corresponding [[zero morphism]] is the [[kernel]] of $f$.

## Properties

+-- {: .num_prop}
###### Proposition

A category has equalizers if it has binary [[product]]s and [[pullback]]s.

=--

+-- {: .proof}
###### Proof

For $S \stackrel{\overset{g}{\longrightarrow}}{\underset{f}{\longrightarrow}} T$ the given diagram, form the [[pullback]] along the [[diagonal morphism]] of $T$:
$$\array{
     eq(f,g) 
       &\longrightarrow& 
     S 
     \\
     \big\downarrow 
       && 
     \big\downarrow {}^{\mathrlap{(f, g)}}
     \\
     T 
       &\underset{(id, id)}{\longrightarrow}&  
     T \times T
  }.$$

One checks that the horizontal morphism $eq(f,g) \to S$ equalizes $f$ and $g$ and that it does so universally.
=--

+-- {: .num_prop}
###### Proposition
If a category has equalizers and (finite) products, then it has (finite) [[limits]].
=--

For the finite case, we may say equivalently:

+-- {: .num_prop}
###### Proposition
If a category has equalizers, binary products and a terminal object, then it has finite [[limits]].
=--

\begin{prpn}
(Eckmann and Hilton [EH](#EH), Proposition 1.3.)
Let $e: E \rightarrow X$ be an arrow in a category $\mathcal{C}$ which is an equaliser of a pair of arrows of $\mathcal{C}$. Then $e$ is a [[monomorphism]].
\end{prpn}

\begin{proof}
If $g,h : A \rightarrow E$ are arrows of $\mathcal{C}$ such that $e \circ g = e \circ h$, then it follows immediately from the uniqueness part of the universal property of an equaliser that $g = h$.
\end{proof}

## Related concepts

* [[homotopy equalizer]]

## References

Equalizers were defined in the paper

* {#EH} [[Beno Eckmann]], [[Peter J. Hilton]], _Group-like structures in general categories II.  Equalizers, limits, lengths_.  Mathematische Annalen 151:2 (1963), 150–186.  [doi:10.1007/bf01344176](https://doi.org/10.1007/bf01344176).

for any finite collection of parallel morphisms.
The paper refers to them as _left equalizers_, whereas [[coequalizers]] are referred to as _right equalizers_.

[[!redirects equalizers]]
[[!redirects equaliser]]
[[!redirects equalisers]]
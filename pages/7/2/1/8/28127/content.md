

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


\tableofcontents



## Idea

In [[algebraic topology]], by *stable splitting* one refers to a situation where (the [[homotopy type]] of) a [[topological space]] or (the [[stable homotopy type]] of) a [[spectrum]] $X$ becomes [[weak homotopy equivalence|weakly homotopy equivalent]] to a [[wedge sum]] of (generally simpler) spaces/types after some number $n \in \mathbb{N} \sqcup \{\infty\}$ of ([[reduced suspension|reduced]]) [[suspensions]] $\Sigma(-)$:

$$
  \Sigma^n X
  \;\simeq\;
  \bigvee_i Y_i
  \mathrlap{\,.}
$$

## Examples

### Basic examples

\begin{example} **(stable splitting of product spaces)** 
\label{StableSplittingOfProductSpaces}
\linebreak
  For $X$ and $Y$ a [[pair]] of [[pointed topological space|pointed]] [[CW-complexes]], the reduced suspension of their [[product space]] is [[homotopy equivalence|homotopy equivalent]] to the [[wedge sum]] of their individual [[reduced suspensions]] with that of their [[smash product]] $X \wedge Y$:
$$
  \Sigma(X \times Y)
  \,\underset{hmtp}{\simeq}\,
  \Sigma X 
    \,\vee\, 
  \Sigma Y
    \,\vee\,
  \Sigma(X \wedge Y)
  \mathrlap{\,.}
$$
\end{example}
(cf. [Hatcher 2002 Prop. 4I.1](#Hatcher02))

### Of mapping spaces

Cf. *[[stable splitting of mapping spaces]]*


### Of Manifolds

On stable splitting for [[6-manifolds]] (such as [[Calabi-Yau 3-folds]]) see [Huang 2023](#Huang2023).

## References

Textbook account:

* {#Hatcher02} [[Allen Hatcher]], §4.I in: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

On stable splitting of [[6-manifolds]]:

* {#Huang2023} [[Ruizhi Huang]]: *Suspension homotopy of 6-manifolds*, Algebr. Geom. Topol. **23** (2023) 439-460 &lbrack;[arXiv:2104.04994](https://arxiv.org/abs/2104.04994), [doi:10.2140/agt.2023.23.439](https://doi.org/10.2140/agt.2023.23.439)&rbrack;


[[!redirects stable splittings]]

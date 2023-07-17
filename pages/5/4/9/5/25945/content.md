
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Definition

### Big O

Let $\mathbb{R}$ denote the [[set]] of [[real numbers]]. Then there is a function

$$O:(\mathbb{R} \to \mathbb{R}) \to \mathcal{P}(\mathbb{R} \to \mathbb{R})$$

from the set of [[endofunctions]] on the real numbers $\mathbb{R} \to \mathbb{R}$ to the set of [[subsets]] of [[endofunctions]] on the real numbers $\mathcal{P}(\mathbb{R} \to \mathbb{R})$, such that given a real-valued endofunction $g:\mathbb{R} \to \mathbb{R}$, an real-valued endofunction $f:\mathbb{R} \to \mathbb{R}$ is said to be in $O(g)$ if and only if there merely exists positive real numbers $c:\mathbb{R}^+$ and $n_0:\mathbb{R}^+$ such that for all positive real numbers $n:\mathbb{R}^+$, if $n \leq n_0$, then $\vert f(n) \vert \leq c \vert g(n) \vert$:

$$f \in O(g) \coloneqq \exists c:\mathbb{R}^+.\exists n_0:\mathbb{R}^+.\exists n:\mathbb{R}^+.(n \leq n_0) \implies (\vert f(n) \vert \leq c \vert g(n) \vert)$$

If one doesn't have [[power sets]] in the foundations, one would have to define $O(g)$ as a [[family]] of structural [[subsets]]: for each $g:\mathbb{R} \to \mathbb{R}$, a set $O(g)$ and an [[injection]] $i_O(g):O(g) \hookrightarrow (\mathbb{R} \to \mathbb{R})$. Then $f \in O(g)$ if $f$ is in the [[image]] of $i_O(g)$. 

### Big Omega

Let $\mathbb{R}$ denote the [[set]] of [[real numbers]]. Then there is a function

$$\Omega:(\mathbb{R} \to \mathbb{R}) \to \mathcal{P}(\mathbb{R} \to \mathbb{R})$$

from the set of [[endofunctions]] on the real numbers $\mathbb{R} \to \mathbb{R}$ to the set of [[subsets]] of [[endofunctions]] on the real numbers $\mathcal{P}(\mathbb{R} \to \mathbb{R})$, such that given a real-valued endofunction $g:\mathbb{R} \to \mathbb{R}$, an real-valued endofunction $f:\mathbb{R} \to \mathbb{R}$ is said to be in $\Omega(g)$ if and only if there merely exists positive real numbers $c:\mathbb{R}^+$ and $n_0:\mathbb{R}^+$ such that for all positive real numbers $n:\mathbb{R}^+$, if $n \geq n_0$, then $\vert f(n) \vert \geq c \vert g(n) \vert$:

$$f \in \Omega(g) \coloneqq \exists c:\mathbb{R}^+.\exists n_0:\mathbb{R}^+.\exists n:\mathbb{R}^+.(n \geq n_0) \implies (\vert f(n) \vert \geq c \vert g(n) \vert)$$

If one doesn't have [[power sets]] in the foundations, one would have to define $\Omega(g)$ as a [[family]] of structural [[subsets]]: for each $g:\mathbb{R} \to \mathbb{R}$, a set $\Omega(g)$ and an [[injection]] $i_\Omega(g):\Omega(g) \hookrightarrow (\mathbb{R} \to \mathbb{R})$. Then $f \in \Omega(g)$ if $f$ is in the [[image]] of $i_\Omega(g)$. 

### Big theta

Let $\mathbb{R}$ denote the [[set]] of [[real numbers]]. Then there is a function

$$\Theta:(\mathbb{R} \to \mathbb{R}) \to \mathcal{P}(\mathbb{R} \to \mathbb{R})$$

defined for all real-valued endofunctions $g:\mathbb{R} \to \mathbb{R}$ as the intersection of the subsets $O(g)$ and $\Omega(g)$

$$\Theta(g) \coloneqq O(g) \cap \Omega(g)$$

By the properties of [[power sets]], given a real-valued endofunction $f:\mathbb{R} \to \mathbb{R}$, $f$ is said to be in $\Theta(g)$ if it is in both $O(g)$ and $\Omega(g)$. 

$$f \in \Theta(g) \coloneqq (f \in O(g)) \wedge (f \in \Omega(g))$$

If one doesn't have [[power sets]] in the foundations, one would have to define $\Theta(g)$ as a [[family]] of structural [[subsets]]: for each $g:\mathbb{R} \to \mathbb{R}$, a set $\Theta(g)$ and an [[injection]] $i_\Theta(g):\Theta(g) \hookrightarrow (\mathbb{R} \to \mathbb{R})$. Then $f \in \Theta(g)$ if $f$ is in the [[image]] of $i_\Theta(g)$. 

## Examples

Let $p$ be a [[real polynomial function]] with [[degree]] $n$. Then $p \in \Theta(\lambda x:\mathbb{R}.x^n)$. 

## Related concepts

* [[algorithm]]
* [[analytic number theory]]

## References

* Wikipedia, [Asymptotic notation](https://en.wikipedia.org/wiki/Asymptotic_notation)

[[!redirects big O]]
[[!redirects big omega]]
[[!redirects big Omega]]
[[!redirects big theta]]
[[!redirects big Theta]]

[[!redirects big O notation]]
[[!redirects big omega notation]]
[[!redirects big Omega notation]]
[[!redirects big theta notation]]
[[!redirects big Theta notation]]

[[!redirects asymptotic notation]]
[[!redirects Bachmann-Landau notation]]
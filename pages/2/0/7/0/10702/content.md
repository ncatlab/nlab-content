
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Adams operations_ are endo-[[cohomology operations]] on [[topological K-theory]], induced from its [[Lambda-ring]] structure. They are an example of [[power operations]].

## Definition
 {#Definition}

The Adams operations have an explicit definition in terms of the [[Lambda-ring]] structure on [[topological K-theory]], this we state as def. \ref{DefinitionInTermsOfLambdaRing} below. While explicit, this definition may look contrived on first sight. But it turns out that it satisfied a list of properties, of which two natural ones already uniquely characterize the definition, this is proposition \ref{TheBasicProperties} below.

+-- {: .num_prop #LambdaRingStructureOnKTheory}
###### Definition
**(Lambda-ring structure on topological K-theory)**

Let $X$ be a [[compact topological space]] and write $K(X)$ for its [[topological K-theory]] [[ring]]. For $E$ a [[vector bundle]] over $X$, write $[E] \in K(X)$ for its class in K-theory.  Given $E$, write

$$
  \lambda_t[E]
  \;\coloneqq\;
  \underoverset{k = 0}{\infty}{\sum}
  [\wedge^k_X E] t^k
  \;\;\in\;\;
  K(X)[ [t] ] 
$$

for the [[formal power series]] with [[coefficients]] in the ring $K(X)$ being the K-theory casses of the skew-symmetrized [[tensor product of vector bundles]] of $E$ with itself. 

Since the constant term of this power series is always the unit $[\wedge^0 E] = 1$, hence

$$
  \lambda_t[E] \in 1 + (t) \cdot K(X)[ [t] ]
$$

there exists a multiplicative inverse formal power series $\lambda_t[E]^{-1}$.

Thn given the class of a [[virtual vector bundle]] $[E] - [F] \in K(X)$, define more genrally

$$
  \lambda_t[[E- F]]
  \;\;\coloneqq\;\,
  \lambda_t[E] \cdot \lambda_t[F]^{-1}
  \;\;\in\;\;
  K(X)[ [t] ]
  \,.
$$


=--

+-- {: .num_prop #DefinitionInTermsOfLambdaRing}
###### Definition
**(explicit definition of Adams operation)**

For $E$ a [[vector bundle]] over some [[topological space]] $X$, write 

$$
  \psi^0(E) \coloneqq rank(E)
$$ 

for the [[bundle]] which over each [[connected component]] of $X$ is the [[trivial bundle|trivial]] vector bundle of the same [[rank of a vector bundle|rank]] as $E$ over that component.

Define a [[formal power series]] with [[coefficients]] in the K-theory ring $K(X)$ by

$$
  \begin{aligned}
    \psi_t(E)
    & \coloneqq
   \underoverset{\infty}{k = 0}{\sum}
   \psi^k(E) t^k
   \\
    & \coloneqq
    \psi^0(E)
      -
     t \frac{d}{d t} log \lambda_{-t}(E)
    \;\;\in\;\;
    K(X)[ [t] ]
  \end{aligned}
  \,,
$$

where $\lambda_t$ is the [[Lambda-ring]] operation from def. \ref{LambdaRingStructureOnKTheory}.

Here the [[derivative]] of the [[logarithm]] of formal power series stands for the usual expression in terms of the [[geometric series]]:


$$
  \begin{aligned}
    \frac{d}{d t} log \lambda_{-t}(E)
    & =
    \frac{1}{\lambda_{-t}(E)}
    \frac{d}{d t}
     \lambda_{-t}(E)
     \\
     & =
     \underoverset{\infty}{k = 0}{\sum}
     \left(
        1  - \lambda_{-t}(E)
     \right)^k
    \cdot
     \frac{d}{d t} \lambda_{-t}(E)
  \end{aligned} 
  \,.
$$

The **$k$th Adams operation** is the [[cohomology operation]] on [[topological K-theory]]


$$
  \psi^k \;\colon\; K(-) \longrightarrow K(-)
$$


which is the coefficient of $t^k$ in $\psi_t$.


=--


+-- {: .num_prop #TheBasicProperties}
###### Proposition
**(basic properties and characterization of Adams operations)**

The Adams operations

$$
  \psi^k \;\colon\; K(X) \longrightarrow K(X)
$$

have the following properties, for all elements $x,y \in K(X)$ and $k, l \in \mathbb{N}$ and $p \; \text{prime}$:

1. $\psi^k(x + y) = \psi^k(x) + \psi^k(y)$

   ($\psi^k$ is a [[functor|functorial]] [[abelian group]] [[homomorphism]])

1. $x \,\text{a line} \;\;\Rightarrow\;\; \psi^k(x) = x^k$

   (applied to a class $x \coloneqq [L]$ represented by a [[line bundle]] $L$, $\psi^k$ is the $k$th [[tensor power]])

1. $\psi^k(x \cdot y) = \psi^k(x) \cdot \psi^k(y)$

   ($\psi^k$ is in fact a [[functor|functorial]] [[ring]] [[homomorphism]])

1. $\psi^k(\psi^l(x)) = \psi^{k l}(x)$

1. $\psi^p(x) = x^p \, \text{mod}\, p$

1. if $x \in \tilde K(S^{2n})$ ([[reduced cohomology]]) then 

   $x \in \tilde K(S^{2n}) \hookrightarrow K(S^{2n}) \;\;\Rightarrow\;\;\psi^k(x) = k^n \cdot x$.

Moreover, the first two of these already uniquely characterize the Adams operations.

=--

e.g. [Wirthmuller 12, section 11](#Wirthmuller12)

## Properties

### Adams conjecture

The [[Adams conjecture]] (a [[theorem]]) says that for all $k \in \mathbb{N}$ and $V \in K(X)$ there is $n \in \mathbb{N}$ such that the [[spherical fibration]] assigned to the [[K-theory]] class $k^n (\psi^k(V)-V)$ under the [[J-homomorphism]] is trivial, hence that


$$
  J
  \left(
     k^n \left(
       \psi^k(V) - V
     \right)
  \right)
  = 0
  \,.
$$


## Related concepts

* [[Lambda-ring]]

* [[Steenrod square]]

* [[Steenrod operation]]

* [[power operation]]

## References

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 11 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))

* {#Hatcher} [[Allen Hatcher]], section 2.3 of _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))


* Wikipedia, _[Adams operation](http://en.wikipedia.org/wiki/Adams_operation)_


* [[Jacob Lurie]], remark 2 in: _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 35 _The image of $J$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture35.pdf))
 


[[!redirects Adams operations]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[continuous function]] between two [[connected topological space|connected]] [[closed manifold|closed]] [[orientation|oriented]] [[topological manifolds]] of the same [[dimension]], its _degree_ is a measure for how often the function "wraps its domain around its codomain".

## Definition 

For $X$ is a [[connected topological space|connected]] [[closed manifold|closed]] [[orientation|oriented]] [[manifold]] of [[dimension]] $n$, its top [[singular homology|homology group]] $H_n(X) = H_n(X; \mathbb{Z})$ is isomorphic to $\mathbb{Z}$, where the generator $1 \in \mathbb{Z}$ is identified with the orientation class $[\omega_X]$ of $X$, the _[[fundamental class]]_ of $X$. 

+-- {: .num_defn}
###### Definition

Given a [[continuous map]] $f \colon X \to Y$ between two such [[manifolds]], the [[homomorphism]] $f_\ast = H_n(f) \colon H_n(X) \to H_n(Y)$ is therefore specified by the [[integer]] $n$ such that $f_\ast [\omega_X] = n [\omega_Y]$. This integer is called the **degree** of $f$. 

=--

## Computing the degree 

We suppose throughout that $X$ and $Y$ are connected closed oriented manifolds of the same dimension $n$. The degree of a continuous function $g \colon X \to Y$ is frequently computed according to the following considerations: 

* The space of continuous functions $g \colon X \to Y$ has a [[dense subspace]] consisting of [[smooth functions]] $f \colon X \to Y$, and in particular every continuous function $g$ is [[homotopy|homotopic]] to a smooth function $f$. It therefore suffices to compute the degree of $f$. 

* By [[Sard's theorem]], the set of [[singular values]] of a smooth function $f$ has [[measure]] zero (using for example the orientation on $Y$ to define a volume form and hence a measure). Accordingly, we may choose a [[regular value]] $y \in Y$. 

* The [[inverse image]] $f^{-1}(y)$ is a compact $0$-dimensional manifold, hence consists of finitely many (possibly zero) points $x_1, \ldots, x_r \in X$. Since these are regular points, $f$ restricts to a diffeomorphism 
$$f_i \colon U_i \to V$$ 
where $U_i$ is a small neighborhood of $x_i$ and $V$ is a small neighborhood of $y$. The diffeomorphism $f_i$ either preserves or reverses the orientation of $U_i$, i.e., the sign of the [[determinant]] as a mapping between [[differential n-forms]] 
$$\Omega^n(U_i) \to \Omega^n(V)$$ 
is either $+1$ or $-1$. 

* By a straightforward application of the [[excision axiom]] in [[homology]], it follows that the degree of $f$ is the sum of these signs: 
$$\deg(f) = \sum_{i=1}^r sign(\Omega^n(f_i))$$ 
and this quantity is independent of the choice of regular value $y$. 

## Properties

### Hopf degree theorem

+-- {: .num_prop}
###### Proposition
**(Hopf degree theorem)**

Let $n \in \mathbb{N}$ be a [[natural number]] and $X \in Mfd$ be a [[connected topological space|connected]] [[orientation|orientable]] [[closed manifold]] of [[dimension]] $n$. Then the $n$th [[cohomotopy]] classes $\left[X \overset{c}{\to} S^n\right] \in \pi^n(X)$ of $X$ are in [[bijection]] to the [[degree of a continuous function|degree]] $deg(c) \in \mathbb{Z}$ of the representing functions, hence the canonical function

$$
  \pi^n(X) 
    \underoverset{\simeq}{S^n \to K(\mathbb{Z},n)}{\longrightarrow}
   H^n(X,\mathbb{Z}) 
     \;\simeq\;   
   \mathbb{Z}
$$

from $n$th [[cohomotopy]] to $n$th [[integral cohomology]] is a [[bijection]].

=--

(e.g. [Kosinski 93, IX (5.8)](Hopf+degree+theorem#Kosinski93), [Kobin 16, 7.5](Hopf+degree+theorem#Kobin16))


### Poincaré–Hopf theorem

See at _[[Poincaré–Hopf theorem]]_.

### Generalization to the Adams d-invariant

The Hopf degree of a map is a special case of its _[[Adams d-invariant]]_; see [there](d-invariant#DInvariantSpecializesToDegreeOfAContinuousFunction) for more.

## Examples

* [[winding number]]

## Related concepts

* [[Poincaré–Hopf theorem]]


## References

Texbook accounts:

* {#DubrovinNovikovFomenko85} B. A. Dubrovin, [[S. P. Novikov]], A. T. Fomenko, section 13 of: _Modern Geometry — Methods and Applications: Part II: The Geometry and Topology of Manifolds_, Graduate Texts in Mathematics 104, Springer-Verlag New York, 1985

See also:

* Wikipedia, _[Degree of a continuous mapping](http://en.wikipedia.org/wiki/Degree_of_a_continuous_mapping)_


[[!redirects degree of a continuous map]]
[[!redirects degree of a continuous mapping]]


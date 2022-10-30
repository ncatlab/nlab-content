
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[microlocal analysis]], the _wave front set_ of a [[generalized function]] such as a [[distribution]] or a [[hyperfunction]] is a characterization of the singularity structure of the generalized function, hence of how it deviates from being an ordinary smooth function.

The wave front set is the sub-bundle of the [[cotangent bundle]] that consists of all those directions (non-zero co-vectors) such that the local [[Fourier transform]] of the distribution is not rapidly decaying in this direction (this definition turns out to make invariant sense, [H&#246;rmander 90, section 8.1](#Hoermander90)). 

A famous issue with [[distributions]] is that, when thought of as generalized functions, generally neither their composition nor their pointwise product is defined. However, closer inspection shows that the obstruction to these operations being defined for any given pair of distributions may be exactly characterized in terms of how the singular behaviours of the two distribuitions relate at each point. For instance the [[product of distributions]] is well defined precisely if the sum of their wave front sets does not intersect the zero-section ([H&#246;rmander 90, theorem 8.2.10](#Hoermander90)).



##Definition

### Motivation

The definition of wavefront sets is motivated by a version of a [[Paley-Wiener theorem]] that characterizes smooth compactly supported functions ($\mathbb{R}^n \to \mathbb{R}$) by a growth condition on their [[Fourier transform]] $\mathcal{F}$:

+-- {: .num_theorem}
###### Theorem
**(Paley-Wiener for $C^{\infty}_0$)**


The vector space $C_0^{\infty}(\mathbb{R}^n)$ of smooth compactly supported functions is (algebraically and topologically) [[isomorphism|isomorphic]], via the [[Fourier transform]], to the space of entire functions $F$ which satisfy the following estimate: there is a positive constant $B$ such that for every [[integer]] $m \gt 0$ there is a constant $C_m$ such that:
$$ 
      F(z) \le C_m (1 + |z|)^{-m} \exp{ (B \; |\operatorname{Im}(z)|)}
$$ 

=--

### Smoothness

We call a smooth compactly supported function that is identically $1$ in a neighbourhood of a point $x_0$ a **cutoff** function at $x_0$.
Let $U \subset \mathbb{R}^n$ be open, we identify the [[cotangent bundle]] of $U$ with $U \times \mathbb{R}^n$. A subset of $U \times \mathbb{R}^n$ is said to be **conic** if it is stable under the transformation
$$
    (x, \zeta) \mapsto (x, \rho \zeta) \quad \text{with} \; \rho \gt 0
$$

+-- {: .num_defn}
###### Definition

Let $f$ be a distribution and $(x_0, \zeta_0)$ with $\zeta_0 \neq 0$ be a point of the cotangent bundle of $U$. $f$ is **smooth** in $(x_0, \zeta_0)$ if there is a cutoff function $\chi$ in $x_0$ and an open cone $\Gamma_0$ in $\mathbb{R}^n$ containing $\zeta_0$ such that for every $m \gt 0$ there is a nonnegative constant $C_m$ such that for all $\zeta \in \Gamma_0$:
$$
\| \mathcal{F}(\chi f) (\zeta)   \| \le C_m (1 + \| \zeta \|)^{-m}
$$ 
where $\mathcal{F}(\chi f)$ is the [[Fourier transform]] (of the variable $\zeta$) of the function $\chi f$ (of the variable $x$).

=--


+-- {: .num_defn}
###### Definition

A distribution $f$ is smooth in a conic subset $\Gamma$ of the cotangent bundle of $U$ if $f$ is smooth in a neighbourhood of every point in $\Gamma$.

=--


### Wavefront set

Let $U \subseteq \mathbb{R}^n$ be an open subset, $T^* U$ its cotangent bundle and $f$ be a distribution on $U$. The complement of the union of all conic subsets of $T^* U$ where $f$ is smooth is the **wavefront set $WF(f)$**.


## Examples

### One-dimensional Examples

We take a brief look at distributions on $\mathcal{D} (\mathbb{R})$ with singular support consisting of the origin. In one dimension, at the origin, there are of course exactly two directions along which a distribution could be smooth, namely $\zeta \lt 0$ and $\zeta \gt 0$.

We define the [[Fourier transform]] to be
$$
\mathcal{F}(f)(\zeta) = \hat f (\zeta) = \int_{- \infty}^{\infty} f(x) \exp(-2 \pi i x \zeta) dx
$$

For the delta distribution $\delta$, we have $\mathcal{F}(\delta) = 1$, which does not satisfy the decay condition of smoothness.


## References

* {#Hoermander90} [[Lars Hörmander]], section 8.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


* Wikipedia: [wavefront set] (http://en.wikipedia.org/wiki/Wavefront_set)

[[!redirects wavefront sets]]

[[!redirects wave front set]]
[[!redirects wave front sets]]

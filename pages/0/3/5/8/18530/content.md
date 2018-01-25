
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _scaling degree_ or _degree of divergence_ ([Steinmann 71](#Steinmann71)) or more generally the _degree_ ([Weinstein 78](#Weinstein78)) of a [[distribution]] on [[Cartesian space]] $\mathbb{R}^n$  is a measure for how it behaves at the origin $0 \in \mathbb{R}^n$ under [[rescaling]] $x \mapsto \lambda x$ of the canonical [[coordinates]]. 

The concept controls the problem of [[extension of distributions]] from the [[complement]] $\mathbb{R}^n \setminus \{0\}$ of the origin to all of $\mathbb{R}^n$. Such extensions are important notably in the construction of [[perturbative quantum field theories]] via [[causal perturbation theory]], where the freedom in the choice of such extensions models the [[renormalization|("re"-)normalization]] freedom ("counter-terms") in the construction.


## Definition

+-- {: .num_defn #RescaledDistribution}
###### Definition
**(rescaled distribution)**

Let $n \in \mathbb{N}$. For $\lambda \in (0,\infty) \subset \mathbb{R}$ a [[positive number|positive]] [[real number]] write 

$$
  \array{ 
    \mathbb{R}^n 
      &\overset{s_\lambda}{\longrightarrow}& 
    \mathbb{R}^n
    \\
    x &\mapsto& \lambda x
  }
$$

for the [[diffeomorphism]] given by multiplication with $\lambda$, using the canonical [[real vector space]]-structure of $\mathbb{R}^n$.

Then for $u \in \mathcal{D}'(\mathbb{R}^n)$ a [[distribution]] on the [[Cartesian space]] $\mathbb{R}^n$ the _rescaled distribution_ is the [[pullback of a distribution|pullback]] of $u$ along $m_\lambda$

$$
  u_\lambda
  \coloneqq
   s_\lambda^\ast u
  \;\in\;
  \mathcal{D}'(\mathbb{R}^n)
  \,.
$$

Explicitly, this is given by

$$
  \array{
     \mathcal{D}(\mathbb{R}^n) 
       &\overset{ \langle  u_\lambda, - \rangle}{\longrightarrow}&
     \mathbb{R}
     \\
     b &\mapsto& \lambda^{-n} \langle u , b(\lambda^{-1}\cdot (-))\rangle
  }
  \,.
$$

Similarly for $X \subset \mathbb{R}^n$ an [[open subset]] which is invariant under $s_\lambda$, the rescaling of a distribution $u \in \mathcal{D}'(X)$ is is $u_\lambda \coloneqq s_\lambda^\ast u$.

=--

+-- {: .num_defn #ScalingDegree}
###### Definition
**([[scaling degree of a distribution]])**

Let $n \in \mathbb{N}$ and let $X \subset \mathbb{R}^n$ be an [[open subset]] of [[Cartesian space]] which is invariant under [[rescaling]] $s_\lambda$ (def. \ref{RescaledDistribution}) for all $\lambda \in (0,\infty)$, and let $u \in \mathcal{D}'(X)$ be a [[distribution]] on this subset. Then

1. The _[[scaling degree of a distribution|scaling degree]]_ of $u$ is the [[infimum]]

   $$
     sd(u)
     \;\coloneqq\;
     inf
     \left\{
       \omega \in \mathbb{R}
        \;\vert\;
       \underset{\lambda \to 0}{\lim}
        \lambda^\omega u_\lambda
        = 0
     \right\}
   $$

   of the set of [[real numbers]] $\omega$ such that the [[limit of a sequence|limit]] of the rescaled distribution $\lambda^\omega u_\lambda$ (def. \ref{RescaledDistribution}) vanishes. If there is no such $\omega$ one sets $sd(u) \coloneqq \infty$.

1. The _[[degree of divergence of a distribution|degree of divergence]]_ of $u$ is the difference of the scaling degree by the [[dimension]] of the underlying space:

  $$
    deg(u) \coloneqq sd(u) - n
     \,.
  $$

=--


## Examples

+-- {: .num_example #NonSingularDistributionsScalingDegree}
###### Example
**([[scaling degree of distributions|scaling degree]] of [[non-singular distributions]])**

If $u = u_f$ is a [[non-singular distribution]] given by [[bump function]] $f \in C^\infty(X) \subset \mathcal{D}'(X)$, then its [[scaling degree of a distribution|scaling degree]] (def. \ref{ScalingDegree}) is non-[[positive number|positive]]

$$
  sd(u_f) \leq 0
  \,.
$$

Specifically if the first non-vanishing [[partial derivative]] $\partial_\alpha f(0)$ of $f$ at 0 occurs at order ${\vert \alpha\vert} \in \mathbb{N}$, then the scaling degree of $u_f$ is $-{\vert \alpha\vert}$.

=--

+-- {: .proof}
###### Proof

By definition we have for $b \in C^\infty_{cp}(\mathbb{R}^n)$ any [[bump function]] that

$$
  \begin{aligned}
    \left\langle
      \lambda^{\omega}
      (u_f)_\lambda,
      n
    \right\rangle
    & =  
    \lambda^{\omega-n}
    \underset{\mathbb{R}^n}{\int} 
       f(x) g(\lambda^{-1} x)
    d^n x
    \\
    & =
    \lambda^{\omega}
    \underset{\mathbb{R}^n}{\int} 
       f(\lambda x) g(x)
    d^n x
  \end{aligned}
  \,,
$$

where in last line we applied [[change of integration variables]].

The limit of this expression is clearly zero for all  $\omega \gt 0$, which shows the first claim. 

If moreover the first non-vanishing [[partial derivative]] of $f$ occurs at order ${\vert \alpha \vert} = k$, then [[Hadamard's lemma]] says that $f$ is of the form

$$
  f(x) 
    \;=\; 
  \left( \underset{i}{\prod} \alpha_i ! \right)^{-1}
  (\partial_\alpha f(0))
  \underset{i}{\prod} (x^i)^{\alpha_i}
  +
  \underset{ {\beta \in \mathbb{N}^n} \atop { {\vert \beta\vert} = {\vert \alpha \vert} + 1 }  }{\sum}
  \underset{i}{\prod} (x^i)^{\beta_i}
  h_{\beta}(x)
$$

where the $h_{\beta}$ are [[smooth functions]]. Hence in this case

$$
  \begin{aligned}
    \left\langle
      \lambda^{\omega}
      (u_f)_\lambda,
      n
    \right\rangle
    & =
    \lambda^{\omega + {\vert \alpha\vert }}
    \underset{\mathbb{R}^n}{\int} 
      \left( \underset{i}{\prod} \alpha_i ! \right)^{-1}
     (\partial_\alpha f(0))
     \underset{i}{\prod} (x^i)^{\alpha_i}      
     b(x)
    d^n x
    \\
    & \phantom{=}
    +
    \lambda^{\omega + {\vert \alpha\vert} + 1}
    \underset{\mathbb{R}^n}{\int}
      \underset{i}{\prod} (x^i)^{\beta_i}
      h_{\beta}(x)
      b(x)
    d^n x
  \end{aligned}
  \,.
$$

This makes manifest that the expression goes to zero with $\lambda \to 0$ precisely for $\omega \gt - {\vert \alpha \vert}$, which means that

$$
  sd(u_f) = -{\vert \alpha \vert}
$$

in this case.






=--

+-- {: .num_example #DerivativesOfDeltaDistributionScalingDegree}
###### Example
**([[scaling degree of a distribution|scaling degree]] of [[derivative of a distribution|derivatives]] of [[delta-distributions]])**

Let $\alpha \in \mathbb{N}^n$ be a multi-index and $\partial_\alpha \delta \in \mathcal{D}'(X)$ the corresponding [[partial derivative|partial]] [[derivative of distributions|derivatives]] of the [[delta distribution]] $\delta_0 \in \mathcal{D}'(\mathbb{R}^n)$ [[support of a distribution|supported]] at $0$. Then the [[degree of divergence of a distribution|degree of divergence]] (def. \ref{ScalingDegree}) of $\partial_\alpha \delta_0$ is the total order the derivatives

$$
  deg\left(
    {\, \atop \,} \partial_\alpha\delta_0{\, \atop \,}
  \right)
  \;=\; 
  {\vert \alpha \vert}
$$

where ${\vert \alpha\vert} \coloneqq \underset{i}{\sum} \alpha_i$.

=--

+-- {: .proof}
###### Proof

By definition we have for $b \in C^\infty_{cp}(\mathbb{R}^n)$ any [[bump function]] that

$$
  \begin{aligned}
    \left\langle
      \lambda^\omega (\partial_\alpha \delta_0)_\lambda,
      b
    \right\rangle
    & =
    (-1)^{{\vert \alpha \vert}}
    \lambda^{\omega-n} 
    \left(
      \frac{
        \partial^{{\vert \alpha \vert}}
      }{
       \partial^{\alpha_1} x^1  \cdots \partial^{\alpha_n}x^n
      } 
      b(\lambda^{-1}x)
    \right)_{\vert x = 0}
    \\
    & = 
    (-1)^{{\vert \alpha \vert}}
    \lambda^{\omega - n - {\vert \alpha\vert}} 
    \frac{
      \partial^{{\vert \alpha \vert}}
    }{
     \partial^{\alpha_1} x^1  \cdots \partial^{\alpha_n}x^n
    } 
    b(0)   
  \end{aligned}
  \,,
$$

where in the last step we used the [[chain rule]] of [[differentiation]]. It is clear that this goes to zero with $\lambda$ as long as $\omega \gt n + {\vert \alpha\vert}$. Hence $sd(\partial_{\alpha} \delta_0) = n + {\vert \alpha \vert}$.

=--

+-- {: .num_example #FeynmanPropagatorOnMinkowskiScalingDegree}
###### Example
**([[scaling degree of a distribution|scaling degree]] of [[Feynman propagator]] on [[Minkowski spacetime]])**

Let 

$$
  \Delta_F(x)
  \;=\;
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
  }
  \, d k_0 \, d^p \vec k
$$

be the [[Feynman propagator]] for the massive [[free field|free]] [[real scalar field]] on $n = p+1$-dimensional [[Minkowski spacetime]] ([this prop.](Feynman+propagator#FeynmanPropagatorAsACauchyPrincipalvalue)). Its [[scaling degree of a distribution|scaling degree]] is

$$
  \begin{aligned}
    sd(\Delta_{F})
    & = n - 2 
    \\
    & = p -1
  \end{aligned}
  \,.
$$

=--

([Brunetti-Fredenhagen 00, example 3 on p. 22](#BrunettiFredenhagen00))

+-- {: .proof}
###### Proof

Regarding $\Delta_F$ as a [[generalized function]] via the given [[Fourier transform of distributions|Fourier-transform]] expression, we find by [[change of integration variables]] in the Fourier integral that in the scaling limit the Feynman propagator becomes that for vannishing [[mass]], which scales homogeneously:

$$
  \begin{aligned}
    \underset{\lambda \to 0}{\lim}
    \left(
    \lambda^\omega
    \;
    \Delta_F(\lambda x)
    \right)
    & =
    \underset{\lambda \to 0}{\lim}
    \left( 
    \lamba^{\omega} 
    \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
    \frac{+i}{(2\pi)^{p+1}}
    \int
    \int_{-\infty}^\infty
    \frac{
       e^{i k_\mu \lambda x^\mu}
    }{
      - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
    }
    \, d k_0 \, d^p \vec k
    \right)
    \\
    & =
    \underset{\lambda \to 0}{\lim}
    \left(
    \lambda^{\omega-n}
    \;
    \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
    \frac{+i}{(2\pi)^{p+1}}
    \int
    \int_{-\infty}^\infty
    \frac{
       e^{i k_\mu \lambda x^\mu}
    }{
      - (\lambda^{-2}) k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
    }
    \, d k_0 \, d^p \vec k
    \right)
    \\
    & =
    \underset{\lambda \to 0}{\lim}
    \left(
    \lambda^{\omega-n + 2 }
    \;
    \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
    \frac{+i}{(2\pi)^{p+1}}
    \int
    \int_{-\infty}^\infty
    \frac{
       e^{i k_\mu \lambda x^\mu}
    }{
      - k_\mu k^\mu + i \epsilon
    }
    \, d k_0 \, d^p \vec k
    \right)
    \,.
  \end{aligned}
$$

=--


## Properties

+-- {: .num_prop}
###### Proposition

Let $X \subset \mathbb{R}^n$ and $u \in \mathcal{D}'(X)$ be a [[distribution]] as in def. \ref{RescaledDistribution}, such that its [[scaling degree of a distribution|scaling degree]] is finite: $sd(u) \lt \infty$ (def. \ref{ScalingDegree}). Then

1. For $\alpha \in \mathbb{N}^n$, the [[partial derivative|partial]] [[derivative of distributions]] $\partial_\alpha$ increases scaling degree by at most ${\vert \alpha\vert }$:   

   $$
     deg(\partial_\alpha u) \leq deg(u) + {\vert \alpha\vert}
   $$

1. For $\alpha \in \mathbb{N}^n$, the [[product of distributions]] with the smooth coordinate functions $x^\alpha$ decreases scaling degree by at most ${\vert \alpha\vert }$:   


   $$
     deg(x^\alpha u) \leq deg(u) - {\vert \alpha\vert}
   $$

1. Under [[tensor product of distributions]] their scaling degrees add: 

   $$
     sd(u \otimes v) \leq sd(u) + sd(v)
   $$ 

   for $v \in \mathcal{D}'(Y)$ another distribution on $Y \subset \mathbb{R}^{n'}$;

1. $deg(f u) \leq deg(u) - k$ for $f \in C^\infty(X)$ and $f^{(\alpha)}(0) = 0$ for ${\vert \alpha\vert} \leq k-1$;


=--

([Brunetti-Fredenhagen 00, lemma 5.1](#BrunettiFredenhagen00))



+-- {: .proof}
###### Proof

The first three statements follow with manipulations as in example \ref{NonSingularDistributionsScalingDegree} and example \ref{DerivativesOfDeltaDistributionScalingDegree}. For the last one...

=--

## Related concepts

* [[support of a distribution]]

* [[order of a distribution]]

## References

The concept of scaling degree is due to 

* {#Steinmann71} O. Steinmann, _Perturbation Expansions in Axiomatic Field Theory_, volume 11 of Lecture Notes in Physics, Springer, Berlin Springer Verlag, 1971.

and the more general concept of _degree_ due to

* {#Weinstein78} [[Alan Weinstein]], _The order and symbol of a distribution_, Trans. Amer. Math. Soc. 241, 1&#8211;54 (1978).

Review and further developments includes

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], section 5.1 of _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))


* Dorothea Bahns, Micha&#322; Wrochna, _On-shell extension of distributions_ ([arXiv:1210.5448](https://arxiv.org/abs/1210.5448))




[[!redirects scaling degree of distributions]]

[[!redirects degree of divergence of a distribution]]
[[!redirects degree of divergence of distributions]]

[[!redirects degree of a distribution]]
[[!redirects degree of distributions]]

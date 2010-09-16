
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A Poisson Lie algebroid on a [[manifold]] $X$ is a [[Lie algebroid]]
on $X$ naturally defined from and defining the structure of a
[[Poisson manifold]] on $X$.

This is the degree-1 example of a tower of related concepts, described
at [[n-symplectic manifold]].


## Definition ##

Let $\pi \in \Gamma(T X) \wedge \Gamma(T X)$ be a Poisson structure on
$X$, regarded as a bivector.

### As vector-bundle with anchor

In terms of the vector-bundle-with anchor definition of [[Lie
algebroid]] the **Poisson Lie algebroid** $\mathfrak{P}(X,\pi)$ corresponding to $\pi$ is the [[cotangent bundle]]

$$
  \array{
      T^* X &&\stackrel{\pi(-)}{\to}&& T X
      \\
      & \searrow && \swarrow
      \\
      && X
  }
$$

equipped with the anchor map that sends a 1-form $\alpha$ to the vector obtained by contraction with the bivector $\pi$: $\alpha \mapsto \pi(\alpha,-)$.

The bracket $[-,-] : \Omega^1(X) \wedge \Omega^(X) \to \Omega^1(X)$ is given by

$$
 [\alpha,\beta] = \mathcal{L}_{\pi(\alpha)} \beta - \mathcal{L}_{\pi(\beta)} \alpha -d(\pi(\alpha,\beta))\,,
$$

where $\mathcal{L}$ denotes the [[Lie derivative]]. On a coordinate patch this reduces simply to $[d x^i , d x^j] = d_{dR} \pi^{i j}$.


### Chevalley-Eilenberg algebra

We describe the [[Chevalley-Eilenberg algebra]] of the Poisson Lie algebra given by $\pi$, which defines it dually.

Notice that $\pi$ is an element of degree 2 in the [[exterior algebra]]
 $\wedge^\bullet \Gamma(T X)$ of [[multivector field]]s on $X$. The Lie
 bracket on [[tangent bundle|tangent vector]]s in $\Gamma(T X)$
 extends to a bracket $[-,-]_{Sch}$ on multivector field, the
 **[[Schouten bracket]]**. The defining property of the Poisson structure
 $\pi$ is that

$$
  [\pi,\pi]_{Sch} = 0
  \,.
$$

This makes 

$$
  d_{CE(\mathfrak{P}(X,\pi))} := [\pi, -] : CE(\mathfrak{P}(X,\pi)) \to CE(\mathfrak{P}(X,\pi)))
$$ 

into a differential of degree +1 on multivector fields, that squares to 0. We write $CE(\mathfrak{P}(X,\pi))$ for the exterior algebra equipped with this
differential. 

More explicitly, let $\{x^i\} : X \to \mathbb{R}^{dim X}$ be a coordinate patch. Then the differential of $CE(\mathfrak{P}(X,\pi))$ is given by

$$
  d_{\mathfrak{P}(X,\pi)} : x^i \mapsto  2 \pi^{i j} \partial_j
$$  


$$
  d_{\mathfrak{P}(X,\pi)} : \partial_i \mapsto ...
  \,.
$$


## Properties

### Cohomology and Chern-Simons elements {#Cohomology}

We discuss aspects of the [[∞-Lie algebra cohomology|∞-Lie algebroid cohomology]] of $\mathfrak{P}(X,\pi)$.

We shall be lazy (and follow tradition) and write the following formulas in a local coordinate patch $\{x^i\}$ for $X$.

Then the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P}(X,\pi))$ is generated from the $x^i$ and the $\partial_i$, and the [[Weil algebra]] $W(\mathfrak{P}(X,\pi))$ is generated from $x^i$, $\partial_i$ and their shifted partners, which we shall write $\mathbf{d} x^i$ and $\mathbf{d}\partial_i$. The differential on the Weil algebra we may then write

$$
  d_{W(\mathfrak{P}(X,\pi))} = [\pi,-]_{Sch} + \mathbf{d}
  \,.
$$

Notice that $\pi \in CE(\mathfrak{P}(X,\pi))$ is a [[∞-Lie algebra cohomology|Lie algebroid cocycle]], since

$$
  d_{CE(\mathfrak{P}(X,\pi))} \pi = [\pi,\pi]_{Sch} = 0
  \,.
$$

**Proposition** The [[invariant polynomial]] in transgression with $\pi$ is 

$$
  \omega =  (\mathbf{d}\partial_i) \wedge (\mathbf{d}x^i)
   \in
  W(\mathfrak{P}(X,\pi))
  \,.
$$

**Proof** One checks that the following is a **Chern-Simons element** exhibiting the transgression

$$
  cs_\pi = \pi^{i j} \partial_i  \wedge \partial_j 
  + \partial_i \wedge \mathbf{d}x^i
  \;\;\;
  \in W(\mathfrak{P}(X,\pi))
$$

in that $d_{W(\mathfrak{P}(X,\pi))} cs_\pi = \omega$, and the restriction of $cs_\pi$ to $CE(\mathfrak{P}(X,\pi))$ is evidently the Poisson tensor $\pi$.

For the record (and for the signs) here is the explicit computation

$$
  \begin{aligned}
    d_{W(\mathfrak{P}(X,\pi))} (\pi^{i j} \partial_i \wedge \partial_j
   + \partial_i \wedge \mathbf{d} x^i)
    = &
   \mathbf{d}x^k (\partial_k \pi^{i j}) \partial_i \wedge \partial_j
   \\
   & + 2 \pi^{i j} (\mathbf{d}\partial_i) \wedge \partial_j
   \\
   & - (\partial_i \pi^{j k}) \partial_j \wedge \partial_k \wedge 
       \mathbf{d}x^i
   \\
   & +
   (\mathbf{d}\partial_i)\wedge (\mathbf{d} x^i)
   \\
   & + (-)(-) 2\pi^{i j} \partial_i \wedge \mathbf{d}\partial_j
   \\
   = & 
   (\mathbf{d}\partial_i)\wedge (\mathbf{d} x^i)
  \end{aligned}
  \,.
$$




**Remark** The invariant polynomial $\omega$ makes $\mathfrak{P}(X,\pi)$ a [[schreiber:symplectic ∞-Lie algebroid]].

**Remark** The [[Chern-Simons theory]] [[action functional]] induced from the above Chern-Simons element is that of the [[Poisson sigma-model]]:

it sends [[∞-Lie algebroid valued forms]]

$$
  \Omega^\bullet(\Sigma) \leftarrow W(\mathfrak{P}(X,\pi))
  (X,\eta)
$$

on a 2-dimensional manifold $\Sigma$ with values in a Poisson Lie algebroid on $X$ to the integral of the [[Chern-Simons form|Chern-Simons 2-form]]

$$
  \Omega^\bullet(\Sigma) \leftarrow 
  W(\mathfrak{P}(X,\pi))
  \stackrel{(\omega, cs_\omega)}{\leftarrow}
  W(b^2 \mathbb{R})
  : 
  CS_\omega(X,\eta)
$$

which, by the above, is in components

$$
  CS_\omega(X,\eta) = \eta_i \wedge d_{dR} X^i + \pi^{i j} \eta_i \wedge \eta_j
  \,.
$$




## Related concepts ##

* Under [[Lie integration]] a Poisson Lie algebroid is supposed to yield a [[symplectic groupoid]].

* There is a formulation of [[Legendre transformation]] in terms of Lie algebroid.

## References ##

One of the earliest reference seems to be

* [[Ted Courant]], _Tangent Lie algebroid_ ([pdf](http://www.iop.org/EJ/article/0305-4470/27/13/026/ja941326.pdf))

A review is for instance in appendix A of

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and
  even symplectic supermanifolds_
  ([arXiv](http://arxiv.org/abs/math/9910078))

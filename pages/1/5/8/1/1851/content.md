
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

Maxwell's equations for the [[electromagnetic field]] $F \in \Omega^2(X)$ on a $d$-dimensional [[spacetime]] $X$ in the presence of [[electric current]] $j_{el} \in \Omega^{d-1}(X)$ read

$$
  d F = 0
$$

$$
  d \star F = j_{el}
  \,.
$$

Formally this suggests an immediate generalization where a **magnetic current** $j_{mag} \in \Omega^{3}(X)$ is introduced and the first of the equations above is replaced by

$$
  d F = j_{mag}
  \,.
$$

One thing to notice about this is that

* net magnetic charge has not been observed in nature.

The other thing is a more conceptual problem: the [[electromagnetic field|Dirac quantization condition]] says that the $2$-form $F$ is not entirely arbitrary, but constrained to be the characteristic curvature $2$-form of a degree-$2$ cocycle in [[ordinary differential cohomology]], for instance the curvature $2$-form of a $U(1)$-[[principal bundle]] [[connection on a bundle|with connection]]. But this necessarily implies that $d F = 0$.

Indeed, to circumvent dealing with this problem Dirac, in his original argument, has considered removing from $X$ the support of any magnetic charge density. 

It was [[Dan Freed]] in ([Freed](#Freed)) who discussed that the global description of the [[electromagnetic field]] does make sense even in the presence of electric current if one generalizes the model of a degree-$2$ [[ordinary differential cohomology|differential cocycle]] to that of a [[twisted cohomology|twisted]] cocycle.

The magnetic current $3$-form $j_{mag}$ is then realized as the curvature characteristic $3$-form of a degree-$3$ cocycle in [[ordinary differential cohomology]] $\hat j_{mag}$, the [[electromagnetic field]] $F$ is the curvature characteristic $2$-form of a degree-$2$ [[twisted cohomology|twisted]] differential cocycle $\hat F$ and the equation

$$
  d F = j_{mag}
$$

expresses the twisting of $\hat F$ by $\hat j_{mag}$ at the level of curvature forms.

This means that Dirac almost found [[bundle gerbe]]s already in 1931, had he not discussed only the neighbourhood of magnetic monopoles.


## Magnetic charge anomaly 

Short of an experimental detection of magnetic monopoles the above considerations are of little practical relevance for ordinary [[electromagnetism]]. In their (straightforward) generalization to higher abelian [[gauge theory]] they do, however, serve to provide a more complete conceptual picture that provides the conceptual bases for effects such as the [[Green–Schwarz mechanism]].

Namely from the very fact that in the presence of magnetic charge the gauge field $\hat F$ is a twisted cocycle, it follows that the standard [[path integral|action functional]] for electrically charged quantum particles -- the one whose consideration led Dirac to his Dirac quantization condition -- in general has a [[quantum anomaly]].

To see this, consider the following.

In the simplest case we consider a single electrically charged particle with worldline $gamma : [0,1] \to X$ propagating inside a single patch $U_i  \to X$ of some [[cover]] over which the [[electromagnetic field]] is represented by a [[Deligne cohomology|Deligne cocycle]] with $1$-form $A_i \in \Omega^1(U_1)$. Then then action functional for the coupling of the particle to the background [[electromagnetic field]] is

$$
  (\hat F, \gamma) \mapsto
  \exp( -2 \pi i \int_\gamma A_i) \in U(1)
  \,.
$$

This may be rewritten by introducing the corresponding distributional $(d-1)$-form current $(j_{el})_i \in \Omega^{d-1}(U_i)$ as

$$
  (\hat F, \gamma) \mapsto
  \exp( -2 \pi i \int_{U_i} (j_{el})_i \wedge A_i) \in U(1)
  \,.
$$

This integrand may be recognized as the local connection $d$-form of the [[cup product]] of the Deligne $(d-1)$-cocycle $\hat {j_{el}}$ and the Deligne $2$-cocycle $\hat F$. This way

$$
  (\hat F, \gamma) \mapsto
  \exp( -2 \pi i \int_X \hat{j_{el}} \cdot \hat F) \in U(1)
  \,,
$$

where now the integral including the prefactor of $- 2 \pi i$ denotes push-forward in cohomology along $X \to {*}$, and we canonically identify degree-$0$ [[Deligne cohomology]] of the point with $U(1)$.

So far this is the formulation in [[differential cohomology]] of the ordinary action functional for the coupling of electric charges $\hat {j_{el}}$ to the [[electromagnetic field]] $\hat F$.

But in this formulation one can discuss what happens to this when a non-vanishing magnetic current $\hat {j_{mag}}$ is present. In that case $\hat F$ is no longer a plain $2$-cocycle, but a twisted $2$-cocycle. Accordingly, the above push-forward to the point produces not a $U(1)$-valued _function_ of $(\hat F, \hat {j_{el}})$, but a "twisted function", i.e. a section of a [[vector bundle|line bundle]].

Since $\hat F$ is twisted by $\hat {j_{mag}}$, this line bundle is the $2$-cocycle

$$
  \exp( -2 \pi i \int_X \hat{j_{el}} \cdot \hat {j_{mag}})  \,.
$$

(...discussion of how this is a $2$-cocycle on configuration space goes here...)

Comparing with the discussion at [[quantum anomaly]], it follows that the non-triviality of this $2$-cocycle is the _higher gauge theory anomaly_ of the ordinary action functional describing the coupling of electric charges to the [[electromagnetic field]] in the presense of magnetic charges.

This phenomenon has traditionally been known somewhat implicitly in the context of the [[Green–Schwarz mechanism]].

## References

The interpretation of magnetic charge in terms of degree-3 cocycles in [[ordinary differential cohomology]] is in the introduction-section of

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))


[[!redirects magnetic current]]
[[!redirects magnetic charges]]
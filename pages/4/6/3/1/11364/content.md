
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

# Contents 
* table of contents 
{: toc}

## Idea 

Let $k$ be a [[field]], and let $\mathbb{P}^1(k)$ be the [[projective line]] over $k$. A _M&#246;bius transformation_ (also called a _linear fractional transformation_, or a _fractional linear transformation_ which is my own preference -- Todd) is a function $f: \mathbb{P}^1(k) \to \mathbb{P}^1(k)$ defined by the rule 

$$f(x) = \frac{a x + b}{c x + d}$$ 

where $a, b, c, d \in k$ and $a d - bc \in k^\times$. M&#246;bius transformations form a group under composition, isomorphic to the [[projective linear group]]

$$PGL_2(k) \coloneqq GL_2(k)/\{\lambda I: \lambda \in k^\times\} \cong SL_2(k)/\pm I.$$ 

Alternatively, a fractional linear transformation can be considered as synonymous with an automorphism of the field of [[rational functions]] $k(x)$ as a field over $k$ of [[transcendence degree]] 1. 

In [[complex analysis]] (which is the usual context when one speaks of M&#246;bius transformations; otherwise one usually calls them by some combination of "linear" and "fractional"), M&#246;bius transformations are precisely the [[biholomorphisms]] of the [[Riemann sphere]], hence exactly its bijective [[conformal transformations]]. 

## Properties 

### Cross-ratios 

+-- {: .num_prop} 
###### Proposition 
The action $PGL_2(k) \times \mathbb{P}^1(k) \to \mathbb{P}^1(k)$ is 3-transitive, i.e., any triplet of distinct points $(a, b, c)$ may be mapped to 
any other triplet of distinct points $(a', b', c')$ by applying a group element. 
=--  

+-- {: .proof} 
###### Proof 
It suffices to consider $a' = 0, b' = 1, c' = \infty$ where one applies the transformation $x \mapsto \frac{(x-a)(b-c)}{(x-c)(b-a)}$. 
=-- 

This motivates the following definition: given a 4-tuple $(a, b, c, d)$ of distinct points in $\mathbb{P}^1(k)$, its _cross-ratio_ is 

$$\gamma(a, b, c, d) = \frac{(d-a)(b-c)}{(d-c)(b-a)}.$$ 

It is not hard to see that the group action preserves the cross-ratio, i.e., $\gamma(g \cdot a, g \cdot b, g \cdot c, g \cdot d) = \gamma(a, b, c, d)$. Moreover, the group action is transitive on each cross-ratio-equivalence class of 4-tuples. 

In the case $k = \mathbb{C}$ where $\mathbb{P}^1$ is interpreted as the Riemann sphere, it turns out that the cross-ratio of a 4-tuple is a [[real number]] if and only if the four points lie on a [[circle]] (or a line which is a circle passing through $\infty$). Hence M&#246;bius = conformal transformations take circles to circles. 

### Action on hyperbolic space 

As explained at [[Poincare group]], the group $PSL_2(\mathbb{C})$ can be identified with those transformations of Minkowski space $\mathbb{R}^4$ that preserve the Minkowski form $Q$, are orientation-preserving, and take the forward light cone $\{v = (\vec{x}, t): Q(v) \gt 0, t \gt 0\}$ to itself. It follows that $PSL_2(\mathbb{C})$ acts on the hyperboloid sheet 

$$H^3 = \{v = (\vec{x}, t): Q(v) = 1, t \gt 0\}$$ 

which is naturally identified with hyperbolic 3-space. There is a Poincar&#233; disk model for $H^3$, which can be visualized as the intersection of the forward light cone with the hyperplane $t = 1$, which is a 3-disk $D^3$, which can be placed in perspective with $H^3$ by considering lines through the origin in $\mathbb{R}^4$: each line that passes through a unique point in $H^3$ passes through a unique point of $D^3$. This gives an induced action of $PSL_2(\mathbb{C})$ on $D^3$. The restriction of this action to the boundary $S^2 = \partial D^3$ ("the heavenly sphere") coincides with the action on the Riemann sphere $S^2 = \mathbb{P}^1(\mathbb{C})$. 




[[!redirects Moebius transformations]]
[[!redirects moebius transformation]]
[[!redirects moebius transformations]]
[[!redirects Möbius transformation]] 
[[!redirects Möbius transformations]] 
[[!redirects möbius transformation]] 
[[!redirects möbius transformations]] 
[[!redirects linear fractional transformation]]
[[!redirects linear fractional transformations]]
[[!redirects fractional linear transformation]]
[[!redirects fractional linear transformations]]

[[!redirects Möbius group]]
[[!redirects Moebius group]]
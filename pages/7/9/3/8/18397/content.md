+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


\tableofcontents

## Idea

The **h-cobordism theorem** (due to [Smale 1962](#Smale1962)) and the **s-cobordism theorem** provide sufficient conditions for an [[h-cobordism]] to be [[isomorphism|isomorphic]] to a [[cylinder]].

There are famous [[counterexamples]] where the [[h-cobordism theorem]] fails (in the [[smooth manifold|smooth category]]) and [[h-cobordisms]] exist which are not [[isomorphism|isomorphic]] to a [[cylinder]]. These counterexamples arise specifically in the case of 5-dimensional cobordisms between 4-dimensional boundaries. The most prominent example involves the [[topological manifold]] known as the *[[E8 manifold|E₈ manifold]]*, constructed by [Freedman 1982](#Freedman1982). While this manifold exists [[topological manifold|topologically]], the work of [Donaldson 1983](#Donaldson1983) proves that it cannot admit any [[smooth structure]]. This discrepancy allows for the construction of a smooth h-cobordism between a standard smooth 4-manifold (such as the [[K3 surface]]) and a "fake" topological version containing the [[E8 manifold|E₈ manifold]]; this cobordism exists topologically but cannot carry a smooth product structure, thereby demonstrating the existence of [[exotic smooth structures]] on $\mathbb{R}^4$ and the failure of the smooth h-cobordism theorem in dimension 5.

In consequence, in dimensions $n$ where there exist [[h-cobordisms]] which are not [[isomorphism|isomorphic]] to [[cylinders]] (such as for $n=5$ or when non-trivial [[Whitehead torsion]] exists), the [[Segal space]] $PreCob(n)$ modeling the [[(infinity,1)-category|$(\infty,1)$-category]] $Cob(n)$ [[(infinity,n)-category of cobordisms|of cobordisms]]  fails to be a *[[complete Segal space]]*. This is because the [[infinity-groupoid|$\infty$-groupoid]] of [[invertible morphisms]] (in degree 1) contains components corresponding to these non-trivial [[h-cobordisms]], which are not in the image of the [[degeneracy map]] from the [[infinity-groupoid|$\infty$-groupoid]] of objects (in degree 0, which represents the [[classifying spaces]] of the [[diffeomorphism groups]] of closed $(n-1)$-manifolds). Consequently, the *[[complete Segal space|completion]]* of this Segal space has a space of objects strictly "larger" than the [[classifying space]] of the [[diffeomorphism groups]] ([Lurie 2009, Warning 2.2.8](#Lurie2009)).

## Statement

By an [[isomorphism]] of [[manifolds]] *relative* to a joint [[submanifold]] (usually a [[boundary]] component), we shall mean that the isomorphism restricts to the [[identity map]] on that submanifold.

### H-Cobordism theorem

Consider the [[category]] either of [[topological manifolds]], [[smooth manifolds]], or [[piecewise linear manifolds]].

\begin{proposition}
For $n \geq 6$, a [[compact topological space|compact]] [[simply connected topological space|simply connected]] $n$-dimensional [[h-cobordism]] $W$ between [[simply connected topological space|simply connected]] $(n-1)$-[[manifolds]] $W_{in}$ and $W_{out}$ is [[isomorphism|isomorphic]], relative to $W_{in}$, to the [[cylinder]] $W_{in} \times [0,1]$.
\end{proposition}

### S-Cobordism theorem

Consider the [[category]] either of [[topological manifolds]], [[smooth manifolds]], or [[piecewise linear manifolds]].

\begin{proposition}
For $n \geq 6$, a [[compact topological space|compact]] $n$-dimensional [[h-cobordism]] $W$ between $(n-1)$-[[manifolds]] $W_{in}$ and $W_{out}$ is [[isomorphism|isomorphic]], relative to $W_{in}$, to the [[cylinder]] $W_{in} \times [0,1]$ [[logical equivalence|if and only if]] its [[Whitehead torsion]] $\tau(W, W_{in})$ in the [[Whitehead group]] $Wh\big(\pi_1(W_{in})\big)$ vanishes.
\end{proposition}

## Related entries

* [[h-cobordism]]

* [[exotic smooth structure]]

* [[Poincaré conjecture]]

## References

The original h-cobordism theorem:

* {#Smale1962} [[Stephen Smale]], *On the structure of manifolds*, Amer. J. of Math. **84** (1962) 387-399 &lbrack;[doi:10.2307/2372978](https://doi.org/10.2307/2372978), [jstor:2372978](https://www.jstor.org/stable/2372978), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/structur.pdf)&rbrack;

Review:

* {#Milnor1965a} [[John Milnor]], _Lectures on the h-cobordism theorem_, Princeton Univ. Press (1965) &lbrack;[jstor:j.ctt183psc9](https://www.jstor.org/stable/j.ctt183psc9), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/surgery/hcobord.pdf)&rbrack;

See also:

* Wikipedia: _[H-cobordism](https://en.wikipedia.org/wiki/H-cobordism)_

Generalization to the s-cobordism theorem and counterexamples:

* {#Freedman1982} [[Michael H. Freedman]], *The topology of four-dimensional manifolds*, J. Differential Geom. **17** 3 (1982) 357-453 &lbrack;[doi:10.4310/jdg/1214437136](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-17/issue-3/The-topology-of-four-dimensional-manifolds/10.4310/jdg/1214437136.full)&rbrack;

* {#Donaldson1983} [[Simon Donaldson]], _An application of gauge theory to four-dimensional topology_, Journal of Differential Geometry. **18** 2 (1983) 279-315 &lbrack;[doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)&rbrack;

Relevance for the [[(infinity,n)-category of cobordisms|$(\infty,n)$-category of cobordisms]]:

* {#Lurie2009} [[Jacob Lurie]], Warning 2.2.8 in: _[[On the Classification of Topological Field Theories]]_, Current Developments in Mathematics **2008** (2009) 129-280 &lbrack;[doi:10.4310/CDM.2008.v2008.n1.a3](https://dx.doi.org/10.4310/CDM.2008.v2008.n1.a3), [arXiv:0905.0465](http://arxiv.org/abs/0905.0465)&rbrack;


Generalization to [[equivariant cobordism]]:

* [[Shôrô Araki]], Katsuo Kawakubo: *Equivariant $s$-cobordism theorems*, J. Math. Soc. Japan **40** 2 (1988) 349-367 &lbrack;[doi:10.2969/jmsj/04020349](https://doi.org/10.2969/jmsj/04020349), [pdf](https://projecteuclid.org/journals/journal-of-the-mathematical-society-of-japan/volume-40/issue-2/Equivariant-s-cobordism-theorems/10.2969/jmsj/04020349.pdf)&rbrack;

[[!redirects h cobordism theorem]]

[[!redirects s-cobordism theorem]]
[[!redirects s cobordism theorem]]


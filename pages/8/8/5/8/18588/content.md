
# Jordan curves
* table of contents
{: toc}

## Definition

A __continuous simple closed [[curve]]__, or __Jordan curve__, in a [[topological space]] (or [[convergence space]], [[locale]], etc) $X$ is the [[image]] of a [[continuous map|continuous]] [[injection]] to $X$ from the [[unit circle]] $S^1$.  (This map itself is a continuous [[parametrization]] of the curve.)  

The word 'continuous' is generally assumed, so that one speaks simply of a __simple closed curve__.  (If 'closed' is removed, then the domain is taken to be the [[unit interval]] $B^1$ instead of $S^1$.  If 'simple' is removed, then the map is no longer assumed injective.  If the image alone is not sufficient data, then the word 'parametrized' may be added to indicate the map itself while thinking of the map as its image.)

Similarly, a __Jordan [[surface]]__ in $X$ is the image of a continuous injection to $X$ from the [[unit sphere]] $S^2$.  This can be generalized to higher-dimensional [[spheres]] or other domains, so long as there is an appropriate term to use in place of 'curve' and 'surface'.  In particular, if $X$ has [[dimension]] $n$ (in some understood sense), then a __Jordan [[hypersurface]]__ in $X$ is the image of a continuous injection to $X$ from $S^{n-1}$.

### In cohesive homotopy type theory

In [[cohesive homotopy type theory]], let the [[continuum]] [[line object]] $\mathbb{A}$ be a [[commutative ring]] such that the [[shape]] of $\mathbb{A}$ is contractible $\mathrm{isContr}(\esh(\mathbb{A}))$. 

A Jordan curve is a type $J$ whose shape is equivalent to the [[circle type]]: $\esh(J) \simeq S^1$. Similarly, a Jordan surface is a type $J$ whose shape is equivalent to the sphere type $\esh(J) \simeq S^2$, and a $n$-dimensional Jordan hypersurface is a type $J$ whose shape is equivalent to the $(n-1)$-sphere type $S^{n-1}$. 

Commonly seen examples include in [[Euclidean geometry]] where $\mathbb{A}$ is the [[Dedekind real numbers]] $\mathbb{R}$, and [[algebraic geometry]] where $\mathbb{A}$ is the [[affine line]] $\mathbb{A}^1$.

## Related entries

* [[Cauchy integral formula]] (about Jordan curves in the [[complex plane]] $\mathbb{C}$)

* [[Jordan curve theorem]] (about Jordan curves in the [[Cartesian plane]] $\mathbb{R}^2$)

* [[Jordan--Brouwer separation theorem]] (about Jordan hypersurfaces in any [[Cartesian space]] $\mathbb{R}^n$)

## References

* Eric Weisstein, _[Jordan curve](http://mathworld.wolfram.com/JordanCurve.html)_


[[!redirects Jordan curve]]
[[!redirects Jordan curves]]
[[!redirects simple closed curve]]
[[!redirects simple closed curves]]
[[!redirects continuous simple closed curve]]
[[!redirects continuous simple closed curves]]

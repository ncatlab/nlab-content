

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let 

\[
  \label{TheMap}
  \big[
    X \overset{f}{\longrightarrow} Y
  \big]
\] 

be a [[morphism]] in the [[stable homotopy category]] (for instance the [[stabilization]] of a morphism in the [[classical homotopy category]]) and let $E$ be a [[Whitehead-generalized cohomology theory]] (usually assumed to be at least [[multiplicative cohomology theory|multiplicative]]).

Then the _$d$-invariant of $f$ with respect to $E$_ ([Adams 66, Sec. 3, p. 26](#Adams66), short for "degree invariant", see Example \ref{DInvariantSpecializesToDegreeOfAContinuousFunction} below)  is the class of the corresponding [[pullback in cohomology|pullback]] morphism $f^\ast_E$, regarded as an element of the 0th [[Ext-group]] (i.e. the plain [[hom-object]]) between the $E$-cohomologies of $X$ and $Y$:

\[
  \label{ThePullbackInECohomology}
  d(f)
  \;\coloneqq\;
  f^\ast_E
  \;\in\;
  \big(
    E^\bullet(Y);
    \,
    E^\bullet(X)
  \big)
  \;=\;
  Ext^0
  \big(
    E^\bullet(Y);
    \,
    E^\bullet(X)
  \big)
  \,.
\]

The fancy name is justified by the fact that this is beginning of a hierarchy of more interesting invariants of stable maps seen in $E$-cohomology, each of which defined when the previous one vanishes: The next is the _[[e-invariant]]_, then comes the _[[f-invariant]]_ (e.g. [BL 09, Section 2](#BL09)). These are the elements that appear in the first lines on the second page of the $E$-[[Adams spectral sequence]] for $[X,Y]_\bullet$.

## Examples

### Relation to the Hopf degree
  {#RelationToHopfDegree}

+-- {: .num_example #DInvariantSpecializesToDegreeOfAContinuousFunction} 
###### Example
**([[d-invariant]] specializes to [[degree of a continuous function]])**


In the special case that 

* $E = H\mathbb{Z}$ is [[integral cohomology|integral]] [[ordinary cohomology]];

* $X$ and $Y$ are [[connected topological space|connected]] [[closed manifold|closed]] [[orientation|oriented]] [[topological manifolds]] of the same [[dimension]] $n = dim(X) = dim(Y)$

then the $n$-component of the $d$-invariant (eq:ThePullbackInECohomology)  is the _[[degree of a continuous function|degree]] of $f$_

\[
  \label{DegreeOfAContinuousFunction}
  d^n(f) 
  =
  deg(f)
  \;\in\; 
  Hom_{Ab}
  \big(
    H^n(Y;\mathbb{Z}),
    \,
    H^n(YX;\mathbb{Z})
  \big)
  \;\simeq\;
  \mathbb{Z}
  \,.
\]

If moreover $Y = S^n$ is the [[n-sphere]], so that $f$ represents a class in the $n$th [[Cohomotopy]] of $X$, then $\widetilde H^\bullet(Y; \mathbb{Z})$ is concentrated on $\mathbb{Z}$ in degree $n$ and hence the $n$ component $d^n(f)$ is the full information in the d-invariant.

In this case, the [[Hopf degree theorem]] says that the degree of $f$, and hence the d-invariant of $f$ in integral cohomology, completely characterizes the homotopy class $[f]$.

=--





## Related concepts

* [[degree of a continuous function]], [[Hopf degree theorem]]

* [[e-invariant]]

* [[f-invariant]]

[[!include notions of pullback -- contents]]

## References

The notion was introduced, together with that of the [[e-invariant]], in:

* {#Adams66} [[John Adams]], Section 3 of: _On the groups $J(X)$ IV_, Topology 5: 21 (1966)   ([pdf](http://math.unice.fr/~cazanave/Gdt/ImJ/J-IV.pdf), <a href="https://doi.org/10.1016/0040-9383(66)90004-8">doi:10.1016/0040-9383(66)90004-8</a>)

Discussion in the broader context including also the [[f-invariant]]:

* {#BL09} Mark Behrens, Gerd Laures, _$\beta$-Family congruences and the $f$-invariant_, Geometry & Topology Monographs 16 (2009) 9–29 ([arXiv:0809.1125](https://arxiv.org/abs/0809.1125), [doi: 10.2140/gtm.2009.16.9](https://msp.org/gtm/2009/16/p002.xhtml))

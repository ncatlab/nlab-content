+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

The **Freudenthal suspension theorem** ([Freudenthal 37](#Freudenthal37)) is the following theorem about [[homotopy groups]] of [[n-spheres]]:


+-- {: .num_prop}
###### Proposition

The [[suspension]] [[homomorphism]] on [[homotopy groups of spheres]] 

$$
  \pi_{n+k}(S^n) \longrightarrow \pi_{n+k+1}(S^{n+1})
$$ 

is an [[isomorphism]] for $n\gt k+1$. 

More generally, for $X$ an [[n-connected]] [[CW-complex]], then the suspension homomorphism on [[homotopy groups]]

$$
  \pi_k(X) \longrightarrow \pi_{k+1}(\Sigma X)
$$

is an [[isomorphism]] for $k \leq 2n$.

=--

This follows from the [[Blakers-Massey theorem]] (e.g. [Kochmann 96, p. 70](#Kochmann96)). 

The following more general statement is also often referred to as the Freudenthal suspension theorem:

+-- {: .num_prop}
###### Proposition

For $X$ an [[n-connected]] [[CW-complex]] and $Y$ a [[CW-complex]] of [[dimension]] $\leq 2n$, then the maps of [[homotopy classes]] of [[continuous functions]]

$$
  [Y,X]\stackrel{}{\longrightarrow} [\Sigma Y, \Sigma X] \stackrel{}{\longrightarrow}[\Sigma^2 Y, \Sigma^2 X]
$$

are [[isomorphisms]]. In particular $[Y,X]$ canonically has the structure of an [[abelian group]].

=--

This follows from the fact that:

+-- {: .num_prop}
###### Proposition

If $X$ is an [[n-connected]] [[CW-complex]], then the [[unit of an adjunction|unit]] 

$$
  X \longrightarrow \Omega \Sigma X
$$

of the ([[suspension]]$\dashv$[[loop space]])-[[adjunction]] is an isomorphism on $\pi_{\leq 2n}$.

=--

This follows from applying the [[Serre long exact sequence]] (which itself follows from the [[Serre spectral sequence]]) to the [[path space]] fibration (e.g. [Kochmann 96, prop. 3.2.2](#Kochmann96)).

## Properties

### As motivation for stable homotopy theory

The Freudenthal suspension theorem motivated introducing the [[stable homotopy groups of spheres]] $\pi_k(S):=\pi_{n+k}(S^n)$, more generally the [[stable homotopy groups]] $\pi_k^S(Y) = \pi_{n+k}(\Sigma^n Y)$, both independent of $n$ where $n\gt k+1$, and still more generally the [[Spanier-Whitehead category]], then the [[stable homotopy category]] and eventually the [[stable (infinity,1)-category of spectra]].


## Related concepts

* [[suspension isomorphism]]

## References

Due to 

* {#Freudenthal37} [[Hans Freudenthal]],  _&#220;ber die Klassen der Sph&#228;renabbildungen_, Compositio Math., 5:299-314, 1937.

Textbook accounts include

* {#Switzer75} [[Robert Switzer]], theorem 6.26 in _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#Kochmann96} [[Stanley Kochmann]], section 3.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Alan Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, chapter 4 ([pdf](http://www.math.cornell.edu/~hatcher/AT/ATch4.pdf))

A nice expanded version of the latter is in

* Tengren Zhang, _Freudenthal suspension theorem_  ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/ZhangTengren.pdf))


A formalization in [[homotopy type theory]] in [[Agda]] is in 

* [[Peter Lumsdaine]], [[Dan Licata]], _[Freudenthal.agda](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Freudenthal.agda)_

Discussion in [[equivariant homotopy theory]] includes

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], p. 7,8 of _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))





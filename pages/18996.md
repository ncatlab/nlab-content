

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


+-- {: .num_defn #HCohomology}
###### Definition
**(H-cohomology)**

Given a [[smooth manifold]] or [[formal smooth manifold]] $X$, and given a [[differential 3-form]] $H \in \Omega^3(X)$, then forming the [[wedge product]] with $H$ is a nilpotent operation, and hence defines the [[differential]] of a [[cochain complex]] whose entries are the [[vector spaces]] $\Omega^{even/odd}(X)$ of all odd-graded or all even-graded [[differential forms]] on $X$:

$$
  \cdots
    \to
  \Omega^{even}(X)
    \overset{H\wedge(-)}{\longrightarrow}
  \Omega^{odd}(X)
    \overset{H\wedge(-)}{\longrightarrow}
  \Omega^{even}(X)
    \overset{H\wedge(-)}{\longrightarrow}
  \Omega^{odd}(X)
    \to
   \cdots
  \,.
$$

The [[cochain cohomology]] of this [[cochain complex]] 

$$
  H^{even/odd}_{H\wedge}(X)
  \coloneqq; 
  \frac{
    ker
    \left(
      \Omega^{even/odd}(X)
       \overset{H\wedge(-)}{\longrightarrow}
      \Omega^{odd/even}(X)
     \right)
   }{
    im
    \left(
      \Omega^{odd/even}(X)
       \overset{H\wedge(-)}{\longrightarrow}
      \Omega^{even/odd}(X)
     \right)
   }
$$

is also called the _H-cohomology_ of $X$. 

=--

([Cavalcanti 03, p. 19](#Cavalcanti03))

+-- {: .num_remark}
###### Remark

Often it is assumed that the 3-form $H$ in def. \ref{HCohomology} is [[closed differential form|closed]], because in this case H-cohomology serves as an approximation to the corresponding $H$-[[twisted de Rham cohomology]] (prop. \ref{TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint} below). But of course for def. \ref{HCohomology} to make sense in itself, $H$ need not be closed.

=--


## Properties

+-- {: .num_prop #TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint}
###### Proposition

If the [[de Rham complex]] $(\Omega^\bullet(X),d_{dr})$ is [[formal dg-algebra|formal]], then for $H \in \Omega_{cl}^3(X)$ a [[closed differential form|closed]] [[differential 3-form]], the H-cohomology of $X$ (def. \ref{HCohomology}) coincides with its $H$-[[twisted de Rham cohomology]]:

$$
  H^\bullet_{H \wedge (-)}(X)
  \simeq
  H^\bullet_{d + H \wedge (-)}(X)
  \,.
$$ 

=--

([Cavalcanti 03, theorem 1.6](#Cavalcanti03)).



## References

The terminology "$H$-cohomology" is used in

* {#Cavalcanti03} [[Gil Cavalcanti]], _New aspects of the $d d^c$-lemma_ ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

The case of H-cohomology for $H = \omega$ a graded symplectic form (as on a [[Poisson Lie algebroid]] regarded as a  [[symplectic Lie n-algebroid]]) is considered in

* {#Severa05} [[Pavol Ševera]], p. 1 of _On the origin of the BV operator on odd symplectic supermanifolds_, Lett Math Phys (2006) 78: 55. ([arXiv:0506331](https://arxiv.org/abs/math/0506331))

[[!redirects H-cohomology group]]
[[!redirects H-cohomology groups]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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
* table of contents
{:toc}

## Idea

A _differential characteristic class_ is a refinement of a [[characteristic class]] from ordinary [[cohomology]] to [[differential cohomology]].

For characteristic classes of [[classifying space]]s of [[Lie group]]s, the refinement to differential characteristic classes is the topic of [[Chern-Weil theory]]. In that context one traditionally speaks of [[secondary characteristic class]]es.

## Definition

There is an unrefined and a refined version of differential characteristic classes. The unrefined version takes values in [[de Rham cohomology]]. The refined version lifts this to [[ordinary differential cohomology]].

### Unrefined

The following definition is in terms of the axiomatics of [[cohesive (∞,1)-toposes]].

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]], $A \in \mathbf{H}$ any object and $K \in \mathbf{H}$ an abelian [[∞-group]] object. Write $\mathbf{B}^n K$ for the $n$-fold [[delooping]] of $K$.

An ordinary [[characteristic class]] on $A$ of with coefficients in $K$ of degree $n$ is a morphism

$$
  \mathbf{c} : A \to \mathbf{B}^n A
$$

or rather the class

$$
  [\mathbf{c}] \in  H^n(A,K) := \pi_0 \mathbf{H}(A,\mathbf{B}^n K)
$$

that it represents. By <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Structures">general properties of cohesive (∞,1)-toposes</a> there is a canonical morphism $curv : \mathbf{B}^n K \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}K$ to the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#deRhamCohomology">de Rham coefficient object</a> of $\mathbf{B}^n K$. This is the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#CurvatureCharacteristics">universal curvature characteristic class</a> on $\mathbf{B}^n K$.

+-- {: .un_defn}
###### Definition

The (unrefined) **differential characteristic class** or **curvature characteristic class** lifting the characteristic class $\mathbf{c} : A \to \mathbf{B}^n K$ is the composite

$$
  \mathbf{c}_{dR} : A \stackrel{\mathbf{c}}{\to}
     \mathbf{B}^n K \stackrel{curv}{\to} \mathbf{\flat}_{dR}\mathbf{B}^{n+1} K
$$

or rather its class 

$$
  [\mathbf{c}_{dR}] \in H^{n+1}_{dR}(A) :=
    \pi_0 \mathbf{H}(A, \mathbf{\flat}_{dR} \mathbf{B}^{n+1} K)
$$

that it represents. 

=--

Postcomposition with differential characteristic classes induces the (unrefined) <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#ChernWeilTheory">abstract Chern-Weil homomorphism</a>

$$
  \mathbf{c}_{dR} : 
    H(-,A) \to H_{dR}^{n+1}(-)
  \,.
$$

For $G \in \mathbf{H}$ an [[∞-group]] and $A = \mathbf{B}G$ its [[delooping]], this morphism 

$$
  \mathbf{c}_{dR} : 
    H^1(-,G) \to H_{dR}^{n+1}(-)
$$

sends $G$-[[principal ∞-bundle]]s $P \to X$ to the [[curvature characteristic class]] $\mathbf{c}_{dR}(P)$ that represents the characteristic class $\mathbf{c}(P)$ in intrinsic de Rham cohomology.



### Refined

(...)

## Examples

### Differential Pontryagin classes

(...)

* [[Chern-Simons circle 3-bundle]]

* [[Chern-Simons circle 7-bundle]]

(...)


## References

See the references at [[Chern-Weil theory]]  and [[Chern-Weil theory in Smooth∞Grpd]].

Lecture notes on [[secondary cohomology classes]] in [[differential cohomology]] for flat connections is presented in

* {#Bunke12} Ulrich Bunke, _Differential cohomology_, arXiv:[1208.3961](https://arxiv.org/abs/1208.3961)


[[!redirects differential characteristic classes]]


+-- {: .rightHandSide .toc}
##Context##
+-- {: .dropDown}
###Cohomology###
+-- {: .hide}
[[!include cohomology - contents]]
=--
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

By _hypercohomology_ is usually meant is a generalization of [[derived functor]] [[cohomology]]. Whereas derived functor cohomology works for single objects, hypercohomology works for complexes of objects.

In terms of the general [[nPOV]] on [[cohomology]] (as described there) this just means the following:

in a given [[(∞,1)-topos]] $\mathbf{H}$ (which if we are thinking of describing [[abelian sheaf cohomology]] over some [[site]] is the [[(∞,1)-category of (∞,1)-sheaves]] on that site) "ordinary" cohomology in degree $n$ with coefficients in a [[group object in an (∞,1)-category|group object]] A is just

$$
  H^n(X,A) := \pi_0 \mathbf{H}(X, K(A,n))
  \,,
$$

where $K(A,n) = \mathbf{B}^n A$ is the [[Eilenberg-MacLane object]] with $A$ in degree $n$. Typically this is the complex of sheaves $[\cdots \to 0 \to 0 \to A \to 0 \to 0 \to \cdots \to 0]$ turned into a [[simplicial presheaf|simplicial sheaf]] using the [[Dold-Kan correspondence]] 

$$
  \Xi :  Ch_\bullet \to KanCplx
$$

and then interpreted as an [[∞-stack]] using the [[model structure on simplicial presheaves]].

As the discussion at [[cohomology]] amplifies, this definition of cohomology in terms of the [[derived hom-space]] $\mathbf{H}(-,-)$ depends in no way on the coefficient object being an [[Eilenberg-MacLane object]]. It could be any object. Only some familiar _properties_ of cohomology (related to the notion of degree) do depend the coefficients being Eilenberg-MacLane objects. 

We could take a completely arbitrary coefficient object $K$ and consider 

$$
  H(X,K) := \pi_0 \mathbf{H}(X,K)
  \,.
$$

This is then called [[nonabelian cohomology]]. The notion of **hypercohomology** lies in between Eilenberg-MacLane-type cohomology and fully general nonabelian cohomology. For hypercohomology we allow the coefficient object to be a _general sheaf of [[chain complex]]es_ $A_\bullet = [\cdots \to A_2 \to A_1 \to A_0]$, or rather the [[simplicial presheaf]] $\Xi A_\bullet$ represented by that. Then hypercohomology is

$$
  H(X,A_\bullet) := \pi_0\mathbf{H}(X,\Xi A_\bullet)
  \,.
$$

For a bit more on this see also the discussion at [[abelian sheaf cohomology]].


## Examples

* [[Deligne cohomology]] is hypercohomology for complexes of sheaves of [[differential form]]s of the form

  $$
    [
    \cdots 
    \to
    0 
    \to
    C^\infty(-,U(1))
    \stackrel{d_{dR} log}{\to}
    \Omega^1(-)
    \stackrel{d_{dR}}{\to}
    \Omega^2(-)
    \stackrel{d_{dR}}{\to}
    \cdots 
    \Omega^{n-1}(-)
    \stackrel{d_{dR}}{\to}
    \Omega^n(-)
    ]
    \,.
  $$  


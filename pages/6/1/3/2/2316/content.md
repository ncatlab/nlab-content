#Idea#

A rational topological space is a [[topological space]] 
all whose (reduced) [[integral cohomology|integral homology]] groups are [[vector space]]s over the rational numbers $\mathbb{Q}$. 

Every simply connected [[topological space]] has a rationalization
and passing to that rationalization amounts to forgetting all
[[torsion]] information in the homology groups and the 
[[homotopy group]]s of that space. So rational spaces are a 
way to approximate homotopical and cohomological characteristics
of topological spaces. The idea is that comparatively little information
(though sometimes crucial information) is lost by passing to 
rationalizations, while there are powerful tools to handle and compute
with rational spaces. In particular, there is a precise sense in which
rational spaces are modeled by graded commutative
[[differential graded algebra|differential graded cochain algebra]]s.
This is the topic of [[rational homotopy theory]].

#Definition#

A [[topological space]] is called _rational_ if 

* it is
simply connected in that the 1st [[homotopy group]] vanishes, $\pi_1 X = 0$ 

* and the following 
equivalent conditions are satisfied

  1. the collection of [[homotopy group]]s form a $\mathbb{Q}$-[[vector space]],

  1. the [[reduced cohomology|reduced homology]] of $X$, $\tilde H_*(X,\mathbb{Z})$ is a $\mathbb{Q}$-[[vector space]],

  1. the [[reduced cohomology|reduced homology]] of the [[loop space]] $\Omega X$ of $X$, $\tilde H_*(\Omega X,\mathbb{Z})$ is a $\mathbb{Q}$-[[vector space]].


A morphism $\ell : X \to Y$ of simply connected [[topological space]] is
called a **rationalization** of $X$ if $Y$ is a rational topological space
and if $\ell$ induces an [[isomorphism]] in rational homology

$$
  H_*(\ell,\mathbb{Q}) : H_*(X,\mathbb{Q}) \stackrel{\simeq}{\to} H_*(Y,\mathbb{Q})
  \,.
$$

Equivlently, $\ell$ is a rationalization of $X$ if it induces an [[isomorphism]] 
on the rationalized [[homotopy group]]s, i.e. when the morphism

$$
  \pi_* \ell \otimes \mathbb{Q} : \pi_* X \otimes \mathbb{Q}
   \to \pi_* Y \otimes Q \simeq \pi_* Y
$$

is an [[isomorphism]].

A continuous map $\phi : X \to Y$ between simply connected space is a 
**rational homotopy equivalence** if the following equivalent conditions are satisfied:

1. it induces an isomorphism on rationalized homotopy groups in that 
   $\pi_*(\phi) \otimes \mathbb{Q}$ is an isomorphism;
   
1. it induces an isomorphism on rationalized homology groups in that 
   $H_*(\phi,\mathbb{Q})$ is an isomorohism;

1. it induces an isomorphism on rationalized [[cohomology group]]s in that 
   $H^*(\phi,\mathbb{Q})$ is an isomorphism;

1. it induces a weak [[homotopy equivalence]] on rationalizations $X_0, Y_0$ in that
   $\phi_0 : X_0 \to Y_0$ is a [[weak homotopy equivalence]].

# Examples #

## rational $n$-sphere ##

The **rational $n$-sphere** $(S^n)_0$ can be written as

$$
  (S^n)_0  :=
  \left(
     \vee_{k\geq 1} S^n_k
  \right) 
  \cup
  \left(
    \coprod_{k \geq 2} D^{n+1}_k
  \right)
  \,,
$$

where...

## rational $n$-disk ##

...

[[!redirects rational space]]
[[!redirects rational spaces]]
[[!redirects rational topological space]]
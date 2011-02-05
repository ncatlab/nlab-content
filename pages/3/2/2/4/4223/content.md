
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Poincar&#233; Lemma** asserts that if a [[smooth manifold]] $X$ is [[contractible]], then its [[de Rham cohomology]] vanishes in positive degree.

In other words: if $X$ is contractible then for every closed [[differential form]] $\omega \in \Omega^k_{cl}(X)$ with $k \geq 1$ there exists a differential form $\lambda \in \Omega^{k-1}(X)$ such that 

$$
  \omega = d_{dR} \lambda
  \,.
$$

Moreover, for $\omega$ a smooth smooth family of closed forms, there is a smooth family of $\lambda$s satisfying this condition.

The Poincar&#233; lemma is a special case of the more general statement that pullback of differential forms along [[homotopy|homotopic]] maps yields a [[chain homotopy]] of the corresponding [[de Rham complex]]es.

See also [[de Rham theorem]].

## Statement

+-- {: .un_theorem}
###### Theorem

Let $f_1, f_2 : X \to Y$ be two [[smooth function]]s between [[smooth manifold]] and $H : [0,1] \times X \to Y$ a (smooth) [[homotopy]] between them.

Then there is a [[chain homotopy]] between the induced morphisms 

$$
  f_1^*, f_2^* : \Omega^\bullet(Y) \to \Omega^\bullet(X)
$$

on the [[de Rham complex]]es of $X$ and $Y$.

In particular, the action on [[de Rham cohomology]] of $f_1^*$ and $f_2^*$ coincide,

$$
  H_{dR}^\bullet(f_1^*) \simeq H_{dR}^\bullet(f_2^*)
  \,.
$$


Moreover, an explicit formula for the chain homotopy is given by

$$
  \omega \mapsto (x \mapsto \int_{[0,1]} \iota_{\partial_t} (H_t^*\omega)(x) ) d t
  \,. 
$$

=--

Here $\iota_{\partial t}$ denotes contraction (see [[Cartan calculus]]). with the canonical [[vector field]] tangent to $[0,1]$ and the [[integration]] is that of functions with values in the [[vector space]] of differential forms.

+-- {: .proof}
###### Proof

Use [[Cartan's magic formula]] inside the integral.

=--

The **Poincar&#233; lemma** proper is the special case of this statement for the case that $f_1 = const_y$ is a function constant on a point $y \in Y$:

pullback along the constant map sends all forms of positive degree to 0. This being homotopic to the identity map means therefore that all positive de Rham cohomology groups of $X$ vanish.


## References

A nice account collecting all the necessary background is in

* Daniel Litt, _The Poincar&#233; lemma and de Rham cohomology_ ([Harvard College Mathematics Review](http://www.thehcmr.org/node/14): [pdf](http://www.thehcmr.org/issue1_2/poincare_lemma.pdf))

[[!redirects Poincaré lemma]]

>**under construction**  left in incoherent state for a minute...

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[rational homotopy theory]] one considers [[topological space]]s only up to maps that induce [[isomorphism]]s on _rationalized_ [[homotopy group]]s.

Every simply connected space is in this sense equivalent to a [[rational space]]: this is its **rationalization**.


## Definition

### Rationalization of a single space

A **rationalization** of a [[simply connected space|simply connected]] [[topological space]] $X$ is a continuous map $\phi : X \to Y$ where

* $Y$ is a [[simply connected space|simply connected]] [[rational space]];

* $\phi$ induces an [[isomorphism]] on rationalized [[homotopy group]]s:

  $$
    \pi_\bullet(\phi)\otimes \mathbb{Q} :
    \pi_\bullet(X) \otimes \mathbb{Q}
    \stackrel{\simeq}{\to} 
    \pi_\bullet(Y) \otimes \mathbb{Q}
  $$

  or equivalently if $\phi$ induces an isomorphism on rational [[homology]] groups

  $$
    H_\bullet(\phi,\mathbb{Q}) : H_\bullet(X,\mathbb{Q})
    \stackrel{\simeq}{\to}
    H_\bullet(Y,\mathbb{Q})
    \,.
  $$


### Rationalization as a localization of $Top$/$\infty Grpd$

In [[rational homotopy theory]] one consier 
the [[Quillen adjunction]]

$$
  (\Omega^\bullet
   \dashv K)
  :
  dgAlg_{\mathbb{Q}} 
   \stackrel{\overset{\Omega^\bullet}{\leftarrow}}{\underset{K}{\to}}
  sSet
$$

between the [[model structure on dg-algebras]] and the standard [[model structure on simplicial sets]], where $\Omega^\bullet$ is forming [[Sullivan differential forms]]:

$$
  \Omega^\bullet(X) = Hom_{sSet}(X, \Omega^\bullet_{pl}(\Delta^\bullet_{Diff}))
  \,.
$$

Intrinsically this _should_ model something like the [[localization of an (∞,1)-category]] of [[∞Grpd]] at those morphisms that are [[rational homotopy equivalence]]s.

$$
  \infty Grpd_{rat} \stackrel{\leftarrow}{\hookrightarrow} 
  \infty Grpd
  \,.
$$

(see the discussion at Properties below)

...

## Properties

+-- {: .un_theorem}
###### Theorem

The left [[derived functor]] of the Quillen left adjoint $\Omega^\bullet : sSet \to dgAlg_{\mathbb{Q}}$ preserves [[homotopy pullback]]s between objects of finite type.

In other words in the induces pair of [[adjoint (∞,1)-functor]]s

$$
  (\Omega^\bullet \dashv K)
   :
  (dgAlg_\mathbb{Q}^{op})^\circ
  \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  \infty Grpd
$$

the left adjoint preserves [[limit in a quasi-category|(∞,1)-categorical pullbacks]].

=--

+-- {: .proof}
###### Proof

The ingredients of the proof can be found [He06](http://www.math.uic.edu/~bshipley/hess_ratlhtpy.pdf). 

Let $A \to B \to C$ be a [[fibration sequence]] in [[∞Grpd]] with respect to a point $* \to C$. We may always assume that this is modeled by a [[Kan fibration]] $B \to C$ between [[Kan complex]]es $B$ and C and that $A$ is given by the ordinary [[pullback]]

$$
  \array{
    A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B &\to& C
  }
  \,.
$$

Assume that $C$ is a simplicial finite set.

Lemma: For every chosen [[Sullivan model]] $(\wedge^\bullet V^*, d_V)$ of $C$ we can find Sullivan models for $B$ and $C$ that fit into a diagram of the form

$$
  \array{
    (\wedge^\bullet V^*, d_V)
    &\hookrightarrow&
    (\wedge^\bullet V^* \otimes \wedge^\bullet W^* , D)
    &\to&
    (\wedge^\bullet W^* , \bar D)
    \\
    \stackrel{\simeq}{\to}
    &&
    \stackrel{\simeq}{\to}
    &&
    \stackrel{\simeq}{\to}
    \\
    \Omega^\bullet(C)
    &\stackrel{}{\to}&
    \Omega^\bullet(B)
    &\stackrel{}{\to}&
    \Omega^\bullet(B)
  }
  \,,
$$


where the top left morphism is a relative [[Sullivan algebra]], hence a cofibration, as indicated.

This is [He, theorem 2.2](http://www.math.uic.edu/~bshipley/hess_ratlhtpy.pdf).

So in particular this means that the left lart of the above diagram gives a fibrant replacement in $dgAlg^{op}$ of the diagram $\Omega^\bullet(B \to C \leftarrow {*})$. There fore the ordinary pullback of this fibrant diagram in $dgAlg^{op}$, hence the ordinary [[pushout]] of this diagram in 


> **Have to interrupt, left unfinished for the moment...**

=--


## References

Aorund definition 1.4 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv:math/0604626](http://arxiv.org/abs/math.AT/0604626))
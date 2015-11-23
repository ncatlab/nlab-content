
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
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

In [[rational homotopy theory]] one considers
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

Intrinsically this should model something like the (partially) left exact [[localization of an (∞,1)-category]] of [[∞Grpd]] at those morphisms that are [[rational homotopy equivalence]]s.

$$
  \infty Grpd_{ratio} \stackrel{\leftarrow}{\hookrightarrow} 
  \infty Grpd
  \,.
$$

Below we review classical results that says that the left [[adjoint (infinity,1)-functor]] here indeed preserves at least [[homotopy pullback]]s.

More generally, a setup by [[Bertrand Toen]] serves to provide a more comprehensive description of this situtation: see [[rational homotopy theory in an (infinity,1)-topos]].


## Properties {#Properties}

+-- {: .num_theorem}
###### Theorem

The left [[derived functor]] of the [[Quillen functor|Quillen left adjoint]] $\Omega^\bullet : sSet \to dgAlg_{\mathbb{Q}}$ preserves [[homotopy pullbacks]] of objects of [[finite type]] (each rational homotopy group is a [[finite dimensional vector space]] over the [[ground field]).

In other words in the induced pair of [[adjoint (∞,1)-functors]]

$$
  (\Omega^\bullet \dashv K)
   :
  (dgAlg_\mathbb{Q}^{op})^\circ
  \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  \infty Grpd
$$

the left adjoint preserves [[limit in a quasi-category|(∞,1)-categorical pullbacks]] of objects of finite type.

=--

+-- {: .proof}
###### Proof

This is effectively a restatement of a result that appears effectively below proposition 15.8 in HalperinThomas and is reproduced in some repackaged form as theorem 2.2 of [He06](http://www.math.uic.edu/~bshipley/hess_ratlhtpy.pdf). We recall the [[model category|model category-theoretic]] context that allows to rephrase this result in the above form.

Let $C = \{a \to c \leftarrow b\}$ be the pullback [[diagram]] category.

The [[homotopy limit]] functor is the right [[derived functor]] $\mathbb{R} lim_C$ for the [[Quillen adjunction]] (described in detail at [[homotopy Kan extension]])

$$
  [C,sSet]_{inj} \stackrel{\overset{const}{\leftarrow}}{\underset{lim_C}{\to}}
  sSet
  \,.
$$
 
At [[model structure on functors]] it is discussed that composition with the Quillen pair $\Omega^\bullet \dashv K$ induces a Quillen adjunction

$$
  ([C,\Omega^bullet] \dashv [C,K])
  :
  [C, dgAlg^{op}]
  \stackrel{\overset{[C,\Omega^\bullet]}{\leftarrow}}{\underset{[C,K]}{\to}}
  [C,sSet]
  \,.
$$

We need to show that for every fibrant and cofibrant pullback diagram $F \in [C,sSet]$ there exists a weak equivalence 

$$
  \Omega^\bullet \circ lim_C F
  \;\;
  \simeq
  \;\;
  lim_C   \widehat{\Omega^\bullet(F)}
  \,,
$$

here $\widehat{\Omega^\bullet(F)}$ is a fibrant replacement of $\Omega^\bullet(F)$ in $dgAlg^{op}$.

Every object $f \in [C,sSet]_{inj}$ is cofibrant. It is fibrant if all three objects $F(a)$, $F(b)$ and $F(c)$ are fibrant and one of the two morphisms is a fibration. Let us assume without restriction of generality that it is the morphism $F(a) \to F(c)$ that is a fibration. So we assume that $F(a), F(b)$ and $F(c)$ are three [[Kan complex]]es and that $F(a) \to F(b)$ is a [[Kan fibration]]. Then $lim_C$ sends $F$ to the ordinary [[pullback]]  $lim_C F = F(a) \times_{F(c)} F(b)$ in $sSet$, and so the left hand side of the above equivalence is

$$
  \Omega^\bullet(F(a) \times_{F(c)} F(b))
  \,.
$$


Recall that the [[Sullivan algebra]]s are the cofibrant objects in $dgAlg$, hence the fibrant objects of $dgAlg^{op}$. Therefore a fibrant replacement of $\Omega^\bullet(F)$ may be obtained by

* first choosing a [[Sullivan model]] $(\wedge^\bullet V, d_V) \stackrel{\simeq}{\to} \Omega^\bullet(c)$ 

* then choosing factorizations in $dgAlg$ of the composites of this with $\Omega^\bullet(F(c)) \to \Omega^\bullet(F(a)) $ and $\Omega^\bullet(F(c)) \to \Omega^\bullet(F(b))$ into cofibrations follows by weak equivalences.

The result is a diagram

$$
  \array{
    (\wedge^\bullet U^*, d_U)   
    &\leftarrow&
    (\wedge^\bullet V^*, d_V)
    &\hookrightarrow&
    (\wedge^\bullet W^* , d_W)
    \\
    \downarrow^{\simeq}
    &&
    \downarrow^{\simeq}
    &&
    \downarrow^{\simeq}
    \\
    \Omega^\bullet(F(a))
    &\stackrel{}{\leftarrow}&
    \Omega^\bullet(F(c))
    &\stackrel{}{\to}&
    \Omega^\bullet(F(b))
  }
$$

that in $dgAlg^{op}$ exhibits a fibrant replacement of $\Omega^\bullet(F)$. The limit over that in $dgAlg^{op}$ is the colimit

$$
  (\wedge^\bullet U^* , d_U)
  \otimes_{(\wedge^\bullet V^* , d_V)}
  (\wedge^\bullet W^* , d_W)
$$

in $dgAlg$. So the statement to be proven is that there exists a weak equivalence

$$
  (\wedge^\bullet U^* , d_U)
  \otimes_{(\wedge^\bullet V^* , d_V)}
  (\wedge^\bullet W^* , d_W)
  \simeq  
  \Omega^\bullet(F(a) \times_{F(c)} F(b))
  \,.
$$

This is precisely the statement of that quoted result [He, theorem 2.2](http://www.math.uic.edu/~bshipley/hess_ratlhtpy.pdf).

=--

> check the following

+-- {: .num_cor}
###### Corollary

Rationalization preserves homotopy pullbacks of objects of finite type.

=--

+-- {: .proof}
###### Proof

The theory of [[Sullivan model]]s asserts that rationalization of a space $X$ (a simplicial set $X$) is the derived unit of the derived adjunction $(\Omega^\bullet \dashv K)$, namely that the rationalization is modeled by $K$ applied to a Sullivan model $(\wedge^\bullet V^*, d)$ for $\Omega^\bullet(X)$.

$$
  X \to K \Omega^\bullet(X) \stackrel{\simeq}{\leftarrow} K \widehat {\Omega^\bullet(X)} := K (\wedge^\bullet V^* , d_V)
  \,.
$$

Being a Quillen right adjoint, the right derived functor of $K$ of course preserves homotopy limits. Hence the composite $K \circ \widehat{\Omega^\bullet(-)}$ preserves homotopy pullbacks between objects of finite type.


=--

## Related concepts

* [[p-localization]], [[p-completion]]

* [[fracture square]]

* [[rational homotopy theory]]

* [[rational equivariant stable homotopy theory]]

## References

Around definition 1.4 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv:math/0604626](http://arxiv.org/abs/math.AT/0604626))

[[!redirects rationalizations]]

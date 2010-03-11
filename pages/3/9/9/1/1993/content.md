
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $G$ and $H$ two strict [[2-group]]s, their [[delooping]]s are strict one-object [[2-groupoid]]s $\mathbf{B}G$ and $\mathbf{B}H$ and a general morphism $f : G \to H$ of 2-groups is by definition a morphism 

$$
 \mathbf{B}f : \mathbf{B}G \to \mathbf{B}H
$$

i.e. a [[2-functor]] -- in general a weak one.

A _butterfly diagram_ is a way to describe such weak 2-functors in terms of morphisms between the ordinary [[group]]s appearing in the [[crossed module]]s corresponding to $G$ and $H$.



## Definition

A __butterfly__ or __papillon__ is a [[crossed profunctor]] 

$$
  \mathbb{X} \to \mathbb{Y}
$$


between [[crossed module]]s $\mathbb{X}=(\partial_X : X_1\to X_0)$ and $\mathbb{Y}=(\partial_Y:Y_1\to Y_0)$ (actions surpressed from the notation), given by a diagram of [[group]]s

$$
  \array{
    X_1 &&&& Y_1
    \\
    & \searrow^{\mathrlap{x_1}} & & {}^{\mathllap{y_1}}\swarrow
    \\
    {}^{\mathllap{\partial_X}}\downarrow && P && 
    \downarrow^{\mathrlap{\partial_Y}}
    \\
    & \swarrow_{\mathrlap{x_0}} && {}_{\mathllap{y_0}}\searrow
    \\
    X_0 &&&& Y_0
  }
$$

satisfying the properties of a [[crossed profunctor]], and in addition such that the NE-SW sequence is exact i.e. a (nonabelian in general) [[group extension]] sequence. 

## Related concepts

Butterflies corresponds to weak functors between the corresponding $2$-[[2-group|groups]]. A butterfly is flippable, or reversible, if both diagonals are [[group extension]]s. There is also a straightforward generalization for $2$-group [[stack]]s. 

Under the correspondence between [[crossed module]]s and [[internal category|categories internal]] to [[Grp]], butterflies are precisely the saturated [[anafunctor|anafunctors]] internal to $Grp$, using the [[Grothendieck pretopology]] of surjective homomorphisms.


## References

Butterfly between strict 2-groups have been introduced in

* [[Behrang Noohi]], _On weak maps between 2-groups_, [arXiv](http://arxiv.org/abs/math/0506313)

* [[Behrang Noohi]], E. Aldrovandi, _Butterflies I: morphisms of 2-group stacks_, [arXiv](http://arxiv.org/abs/0808.3627), Advances in Mathematics, 221, (2009), 687&#8211;773.

* [[Behrang Noohi]], E. Aldrovandi, _Butterflies II: Torsors for 2-group stacks_,[arXiv](http://arxiv.org/abs/0910.1818)



[[!redirects pappilon]]
[[!redirects papillon]]
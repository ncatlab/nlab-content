#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If an [[(∞,1)-topos]] $\mathbf{H}$ is that of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on (the [[site]] of [[category of open subsets|open subsets]] of) a [[paracompact space|paracompact]] [[topological space]] -- $\mathbf{H} = Sh_{(\infty,1)}(X)$ --  then its **shape** is the _strong shape_ of $X$ in the sense of [[shape theory]]: a [[pro-object]] $Shape(X)$ in the category of [[CW-complex]]es.

It turns out that $Shape(X)$ may be extracted in a canonical fashion from just the [[(∞,1)-topos]] $Sh_{(\infty,1)}(X)$, and in a way that makes sense for any [[(∞,1)-topos]]. This then gives a definition of shape of general $(\infty,1)$-toposes.

## Definition

For every [[(∞,1)-topos]] $\mathbf{H}$ there is the [[terminal object|terminal]] [[geometric morphism]]

$$
  (LConst \dashv \Gamma) : \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}
  \infty Grpd
$$

where [[∞Grpd]] is the $(\infty,1)$-topos of [[∞-groupoids]],  $\Gamma$ is the [[global section]]s [[(∞,1)-functor]] and $LConst$ is the [[constant ∞-stack]] functor.

The **shape** of $\mathbf{H}$ is the composite functor

$$
  Shape(\mathbf{H}) := \Gamma \circ LConst
  \;\;:\;\;
  \infty Grpd \stackrel{LConst}{\to}
  \mathbf{H}
  \stackrel{\;\;\Gamma\;\;}{\to}
  \infty Grpd
$$

regarded as an object 

$$
  Shape(\mathbf{H})
  \in
  Pro(\infty Grpd)^{op}
  :=
  Func_{lex}(\infty Grpd, \infty Grpd)^{op}
$$

in the [[full subcategory]] of finite [[limit]] preserving [[(∞,1)-functors]].

## Shape of a topological space

For a discussion of how the $(\infty,1)$-topos theoretic shape of $Sh_{(\infty,1)}(X)$ relates to the ordinary shape-theoretic _strong shape_ of the topological space $X$ see [[shape theory]].

## References

The definition is due to

* [[Bertrand Toen]] and [[Gabriele Vezzosi]],  _Segal topoi and stacks over Segal categories_ , in Proceedings of the
Program _Stacks, Intersection theory and Non-abelian Hodge Theory_ , MSRI, Berkeley, January-May 2002 ([arXiv:math/0212330](http://arxiv1.library.cornell.edu/abs/math/0212330)).

The relatoin to [[shape theory]] of topological spaces is furhter discussed in section 7.1.6 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects shape of an (∞,1)-topos]]
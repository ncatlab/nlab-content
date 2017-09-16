

## in categories ##

Let $p : X \to Y$ be a [[functor]]. A [[morphism]] $f : x_1 \to x_2$ in the [[category]] $X$ is _cartesian_ with respect to $p$, or _$p$-cartesian. If it satisfies the following property:

$$
  \array{
    x'
    \\
    \downarrow^{\exists!} & \searrow^{\forall h}
    \\
    x &\stackrel{f}{\to}& y
  }
  \;\;\;
  \stackrel{p}{\mapsto}
  \array{
    p(x')
    \\
    \downarrow^{\forall g} & \searrow^{p(h)}
    \\
    p(x) &\stackrel{p(f)}{\to}& p(y)
  }
$$

If for every morphism in $Y$ there is a lift through $p$ that is a cartesian morphism, one says that $p$ is a [[Grothendieck fibration]].


## in $(\infty,1)$-categories

Let $p : X \to Y$ be a morhism of [[simplicial set]]s that may be the [[quasi-category]] incarnation of an [[infinity-functor]] of [[(infinity,1)-category|(∞,1)-categories]].



...


# References #

For the 1-categorical case see the references at [[Grothendieck fibration]].

The $(\infty,1)$-categorical version is in section 2.4 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]

# Idea #

Given a [[functor]] $p : X \to Y$ between categories one may ask for each [[morphism]] $f : y_1 \to y_2$ if given a lift of its target
$$
  \array{
    X &&& && \hat y_2
    \\
    \downarrow^p 
    \\
    Y &&& y_1 &\stackrel{f}{\to}& y_2
  }
$$

there is a _universal_ lift of $f$

$$
  \array{
    X &&& \hat y_1 &\stackrel{\hat f}{\to}& \hat y_2
    \\
    \downarrow^p 
    \\
    Y &&& y_1 &\stackrel{f}{\to}& y_2
  }
  \,.
$$

There may also be other lifts of $f$, but the universal one is essentially unique, as usual for anything having a universal property.  Specifically, $\hat f$ in $X$ is essentially uniquely determined by its source $\hat y_1$ and its image $f = p(\hat f)$ in $Y$, and is called a _cartesian morphism_ .

If there are enough cartesian morphisms in $Y$, they may be used to define [[functor]]s

$$
  f^* : X_{y_2} \to X_{y_1}
$$

between the [[fiber]]s of $p$ over $y_1$ and $y_2$. This way a functor $p : X \to Y$ with enough Cartesian morphisms -- called a [[Cartesian fibration]] or [[Grothendieck fibration]] -- determines and is determined by a fiber-assigning functor $Y \to Cat^{op}$.

This has its analog in [[higher category theory|higher categories]].


# Definition #

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
  \;\;\;
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

Let $p : X \to Y$ be a morphism of [[simplicial set]]s that may be the [[quasi-category]] incarnation of an [[infinity-functor]] of [[(infinity,1)-category|(∞,1)-categories]].

Assume that $p$ is an [[inner Kan fibration]] of simplicial sets.

Then an edge $f : x \to y$ in $X$ is _$p$-cartesian_ if the induced morphism

$$
  X_{/f} \to X_{/y} \times_{S_{/p(y)}} S_{/p(f)}
$$

is acyclic [[Kan fibration]].

This is def 2.4.1.1 in [[Higher Topos Theory|HTT]].

...



# References #

For the 1-categorical case see the references at [[Grothendieck fibration]].

The $(\infty,1)$-categorical version is in section 2.4 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]


[[!redirects Cartesian morphism]]
[[!redirects cartesian morphisms]]

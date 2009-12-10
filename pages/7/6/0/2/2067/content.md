#contents#
* automatic table of contents goes here
{:toc}


## Idea 

Given a [[functor]] $p\colon  X \to Y$ between categories one may ask for each [[morphism]] $f\colon  y_1 \to y_2$ if given a lift of its target
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

There may also be other lifts of $f$, but the universal one is essentially unique, as usual for anything having a universal property.  Specifically, $\hat f$ in $X$ is essentially uniquely determined by its source $\hat y_1$ and its image $f = p(\hat f)$ in $Y$, and is called a __cartesian morphism__.  A morphism which is cartesian relative to $p^{op}\colon X^{op}\to Y^{op}$ is called __opcartesian__ or __cocartesian__.

If there are enough cartesian morphisms in $Y$, they may be used to define [[functor]]s

$$
  f^* : X_{y_2} \to X_{y_1}
$$

between the [[fiber]]s of $p$ over $y_1$ and $y_2$. 

+--{: .query}
[[David Roberts]]: There would surely be an anafunctor version of this, that would require no choices whatsoever. It is unlikely that I would be able to find time to write this up, so my plea goes out to those in the know...

I imagine that there would then be an $(\infty,1)$-version using whatever passes as anafunctors in that setting (dratted memory, failing at the first gate)

[[Mike Shulman]]: Yes, there would surely be such a version.  (-:  The simplest way would be to take the specifications $|f^*|$ for the anafunctor $f^*$ to be the cartesian morphisms over $f$, with domain and codomain giving the functions $\sigma$ and $\tau$.  Unique factorization would give you the values of morphisms.
=--

This way a functor $p : X \to Y$ with enough Cartesian morphisms -- called a [[Cartesian fibration]] or [[Grothendieck fibration]] -- determines and is determined by a fiber-assigning functor $Y \to Cat^{op}$.

This has its analog in [[higher category theory|higher categories]].


## Definition

### in categories

Let $p : X \to Y$ be a [[functor]]. A [[morphism]] $f : x_1 \to x_2$ in the [[category]] $X$ is _cartesian_ with respect to $p$, or _$p$-cartesian. If it satisfies the following property:

$$
  \array{
    x'
    \\
    \downarrow^{\exists!} & \searrow^{\forall h}
    \\
    x_1 &\stackrel{f}{\to}& x_2
  }
  \;\;\;
  \;\;\;
  \stackrel{p}{\mapsto}
  \;\;\;
  \;\;\;
  \array{
    p(x')
    \\
    \downarrow^{\forall g} & \searrow^{p(h)}
    \\
    p(x_1) &\stackrel{p(f)}{\to}& p(x_2)
  }
$$

If for every morphism in $Y$ there is a lift through $p$ that is a cartesian morphism, one says that $p$ is a [[Grothendieck fibration]].

This may equivalently be expressed as follows:

let 

* $X/x_2$ by the [[overcategory]] of $X$ over the object $x_2$;

* $Y/p(x_2)$ the corresponding [[overcategory]] of $Y$ over $p(x_2)$;

* $X/f$ the category whose objects 

  $$
    Obj(X/f) = 
    \left\{
    \array{
       && a
       \\
       &\swarrow && \searrow
       \\
       x_1 &&\stackrel{f}{\to}&& x_2
    }
    \right\}
  $$
 
  are objects $a$ of $X$ eqipped with morphisms to $x_1$ and $x_2$ such that the obvious triangle commutes, and whose morphisms are morphisms between these tip objects such that all diagrams in sight commute.

* similarly $Y/p(f)$.

Then the condition that $f$ is cartesian with respect to $p$ is equivalently the condition that the functor

$$
  X_f \to X_{x_2} \times_{Y_{p(x_2)}} Y/p(f)
$$

into the [[pullback]] of the obvious projection $X_{x_2} \to S/p(x_2)$ along the projection $S/p(f) \to S/p(x_2)$ is a [[k-surjective functor|surjective equivalence]].

This definition in terms of pullbacks is the one that straightforwardly generalizes to [[higher category theory]].

### in $(\infty,1)$-categories

There is a notion of cartesian edge in a [[simplicial set]] $X$ relative to a morphism $p : X \to Y$ of simplicial sets. In the case that these simplicial sets are [[quasi-category|quasi-categories]] -- i.e. simplicial set incarnations of [[(∞,1)-category|(∞,1)-categories]] -- this yields a notion of cartesian morphisms in $(\infty,1)$-categories.

Let $p : X \to Y$ be a morphism of [[simplicial set]]s that may be the [[quasi-category]] incarnation of an [[infinity-functor]] of [[(infinity,1)-category|(∞,1)-categories]].
Let $f : x_1 \to x_2$ be an edge in $X$, i.e. a morphism $f : \Delta^1 \to X$.

Recall the notion of [[over quasi-category]] obtained from the notion of [[join of quasi-categories]]. Using this we obtain [[simplicial set]]s $X/f$, $X/{x_2}$, $S/p(f)$ and $S/p(x_2)$ in generalization of the categories considered in the above definition of cartesian morphisms in categories.


Assume that $p$ is an [[inner Kan fibration]] of simplicial sets.

Then $f $ in $X$ is _$p$-cartesian_ if the induced morphism

$$
  X_{/f} \to X_{/y} \times_{Y_{/p(y)}} Y_{/p(f)}
$$

is acyclic [[Kan fibration]].

This is def 2.4.1.1 in [[Higher Topos Theory|HTT]].

This is equivalent to the condition that for all [[horn]] inclusions

$$
  \array{
    \Delta^{\{n-1,n\}}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda[n]_n &\to& X
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& Y
  }
$$

(with $\Lambda[n]_n$ the $n$th [[horn]] of the $n$-[[simplex]]) such that the last edge of the horn is the given egde $f$, a lift $\sigma$

$$
  \array{
    \Delta^{\{n-1,n\}}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda[n]_n &\to& X
    \\
    \downarrow &{}^\sigma\nearrow& \downarrow
    \\
    \Delta[n] &\to& Y
  }
$$

exists. (See [[Higher Topos Theory|HTT remark 2.4.1.4]].)


## References 

For the 1-categorical case see the references at [[Grothendieck fibration]].

The $(\infty,1)$-categorical version is in section 2.4 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]


[[!redirects Cartesian morphism]]
[[!redirects cartesian morphisms]]
[[!redirects opcartesian morphism]]
[[!redirects opcartesian morphisms]]
[[!redirects cocartesian morphism]]
[[!redirects cocartesian morphisms]]


#Definition#

There is a very general notion of _injective object_s in a category $C$, and a sequence of refinements as $C$ is equipped with more [[stuff, structure, property|structure and property]], in particular for $C$ an [[abelian category]] [[additive and abelian categories|of sorts]].

## General definition ##

Let $C$ be a [[category]] and $J$ a collection of morphisms in $C$. An object $I$ in $C$ is **$J$-injective** if all diagrams

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} 
    \\
    Z
  }
$$

admit an extension

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} & \nearrow_{\exists}
    \\
    Z
  }
  \,.
$$

If $C$ has a [[terminal object]] $*$ this is to be thought of as a lift

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} & \nearrow_{\exists}
    &
    \downarrow
    \\
    Z
    &\to&
    *
  }
$$

as for [[weak factorization system|factorization systems]].

If $C$ is a [[small category]] then $I$ is $J$-injective precisely if the [[hom-functor]]

$$
  Hom_C(-,I) : C^{op} \to Set
$$

takes morphisms in $J$ to [[epimorphism]]s in [[Set]].


## In abelian categories ##

More specifically, the term "injective" is used for such object in the context that  $C$ is an [[abelian category]] for $J$ the class of morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is exact.
 
An [[object]] $I$ of $C$ is **injective** if it satisfies the following equivalent conditions:

* the [[hom-functor]] $Hom_C(-, I) : C^{op} \to Set$ is [[exact functor|exact]];

* for all [[morphism]]s $f : X \to Y$ such that $0 \to X \to Y$ is [[exact complex|exact]] and for all $k : X \to I$, there exists $h : Y \to I$ such that $ h\circ f = k$.

$$
  \array{
    0 &\to& X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^k & \swarrow_{\exists h
    \\
    &&
    I 
  }
  \,.
$$

## In categories of chain complexes ##

An object in the [[category of chain complexes]] modulo chain homotopy, $K(C)$, 
of an [[abelian category]] $C$ is **homotopically injective** if for every $X \in K(C)$ that is
[[quasi-isomorphism|quasi-isomorphic]] to $0$
we have
$$
  Hom_{K(C)}(X,I) = \{0\}
  \,.
$$

...
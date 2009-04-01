
#Definition#

Let $C$ be a [[small category]] and $J$ a collection of morphisms in $C$. An object $I$ in $C$ is **$J$-injective** if all diagrams

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} 
    \\
    Z
  }
$$

admit a lift

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

More spefifically, the term "injective" is used in the context that  $C$ is an [[abelian category]] for $J$ the class of morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is exact.
 
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

An object in the [[category of chain complexes]] $K(C)$ of $C$ is **homotopically injective** if 
$Hom_{K(C)}(X,I) \simeq 0$ is [[quasi-isomorphism|quasi-isomorphic]] to $0$ for all $X \in K(C)$ with $X \simeq 0$.

...
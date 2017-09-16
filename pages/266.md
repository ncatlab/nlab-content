#Idea#

The _Kan extension_ of a [[functor]]
$F : C \to D$ with respect to a functor
$$
 \array{
  C
  \\
  \downarrow^p
  \\
  C'
 }
$$

is, if it exists, a "best approximation" to extending the domain of $F$ through $p$ from $C$ to $C'$.


#Definition#

The following are three equivalent definitions

* Kan extension as the adjoint to pullback of functor categories;

* Kan extension in terms of a universal natural transformation;

* Kan extension in terms of weighted (co)limits.


## As adjoint to pullback of functor categories ##

The functor $p : C \to C'$ induces, by precomposition, a functor between [[functor category|functor categories]]
$$
  p^* : [C',D] \to [C,D]
  \,.
$$

The [[left adjoint]] to $p^*$ is **left Kan extension** of functors
$$
  Lan : [C,D] \to [C',D]
  \,,
$$
and the [[right adjoint]] is **right Kan extension** of functors
$$
  Ran : [C,D] \to [C',D]
  \,.
$$

## In terms of universal natural transformations ##

The left Kan extension $Lan F$ of $F : C \to D$ is the functor $Lan F : C' \to D$ such that there exists a [[natural transformation]] $\eta_F : F \Rightarrow p^* Lan F$

$$
  \array{
    C &&\stackrel{F}{\to}& D
    \\
    \downarrow^p & \Downarrow^{\eta_F} & \nearrow_{Lan F}
    \\
    C'
  }
$$

with the property that every other natural transformation
$F \Rightarrow p^* G$ factors uniquely through $\eta_F$ as

$$
  \array{
    C &&\stackrel{F}{\to}& D
    \\
    \downarrow^p & \Downarrow & \nearrow_{G}
    \\
    C'
  }
  \;\;\;
  =
  \array{
    C &&\stackrel{F}{\to}&& D
    \\
    \downarrow^p & \Downarrow^{\eta_F} 
    & \nearrow_{Lan F} &
    \Downarrow & \downarrow^{=}
    \\
    C' &&\stackrel{G}{\to}&& D
  }
  \,.
$$

Similarly for the right Kan extension, with the direction of the natural transformations reversed:

$$
  \array{
    C &&\stackrel{F}{\to}& D
    \\
    \downarrow^p & \Uparrow^{\epsilon_F}& \nearrow_{Ran F}
    \\
    E
  }
$$

## In terms of weighted (co)limits ##

(...)

# Definition in $(\infty,1)$-categories #

See [section 4.3, p. 215](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=215) of [[Higher Topos Theory]].


#Examples#

* For $C' = $ the [[point]], the right Kan extension of $F$ is the [[limit]] of $F$, $Ran F \simeq \lim F$ and the left Kan extension is the [[colimit]] $Lan F \simeq colim F$.




#References#

See for instance section 2.3 in 

* Kashiwara and Shapira, [[Categories and Sheaves]]

For the context of [[enriched category theory]] see 
chapter 4 of

* G.M. Kelly, _Basic Concepts of Enriched Category Theory_, 
 Cambridge University Press, Lecture Notes in Mathematics 64, 1982,  Republished in:
Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

The $(\infty,1)$-categorical discussion is in 

J. Lurie, [[Higher Topos Theory]]


#Contents#
* table of contents
{:toc}


## In the context of Brown representability

+-- {: .num_defn #BrownFunctorOnInfinityCategory}
###### Definition

Let $\mathcal{C}$ be a [[locally presentable (∞,1)-category]]. A [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ to [[Set]])

is called a **[[Brown functor]]** if 

1. it sends small [[coproducts]] to [[products]];

1. it sends [[(∞,1)-pushouts]] in $\mathcal{C}\to Ho(\mathcal{C})$ to [[weak pullbacks]] in [[Set]]. 

=--

+-- {: .num_remark}
###### Remark

A _[[weak pullback]]_ is a diagram that satisfies the existence clause of a [[pullback]], but not necessarily the uniqueness condition. Hence the second clause in def. \ref{BrownFunctorOnInfinityCategory} says that for a [[(∞,1)-pushout]] square 

$$
  \array{
    Z &\longrightarrow& X
    \\
    \downarrow &\swArrow& \downarrow
    \\
    Y &\longrightarrow& X \underset{Z}{\sqcup}Y 
  }
$$

in $\mathcal{C}$, then the induced universal morphism


$$
  F\left(X \underset{Z}{\sqcup}Y\right)
  \stackrel{epi}{\longrightarrow}
  F(X) \underset{F(Z)}{\times} F(Y)
$$

into the actual [[pullback]] is an [[epimorphism]].

=--

+-- {: .num_prop}
###### Proposition
**([[Brown representability theorem]])**

Let $\mathcal{C}$ be a [[locally presentable (∞,1)-category]]. 

If 

1. $\mathcal{C}$ is [[compactly generated (∞,1)-category|generated]] by a set

   $$
    \{S_i \in \mathcal{C}\}_{i \in I}
   $$

   of [[compact object in an (infinity,1)-category|compact objects]] (i.e. every object of $\mathcal{C}$ is an [[(∞,1)-colimit]] of the objects $S_i$.)

1. each $S_i$ admits the structure of a [[cogroup]] object in the [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(\mathcal{C})$, 

then a [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ to [[Set]])

is [[representable functor|representable]] precisely if it is a Brown functor, def. \ref{BrownFunctorOnInfinityCategory}.

=--



## In the context of categories of fibrant objects

A **right Brown functor** between [[categories of fibrant objects]] is a [[functor]] that preserves [[weak equivalences]] between [[fibrant objects]].

Dually for a _left Brown functor_ (for instance between [[Waldhausen categories]]).

[[!redirects Brown functors]]

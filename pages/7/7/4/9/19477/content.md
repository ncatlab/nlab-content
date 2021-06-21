

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A basic fact of [[category theory]] says that the [[limit]] or [[colimit]] of a [[diagram]] in a  [[category of presheaves]] is the [[presheaf]] whose value at any [[object]] is the [[limit]] or [[colimit]], respectively, in the [[category of sets]], of the values of the presheaves in the diagram, at that object.


## Statement

+-- {: .num_prop}
###### Proposition
**(limits of presheaves are computed objectwise)**

Let $\mathcal{C}$ be a [[category]] and write $[\mathcal{C}^{op}, Set]$ for its [[category of presheaves]]. Let moreover $\mathcal{D}$ be a [[small category]] and consider any [[functor]]

$$
  F \;\colon\; \mathcal{D} \longrightarrow [\mathcal{C}^{op}, Set]
  \,,
$$

hence a $\mathcal{D}$-shaped [[diagram]] in the [[category of presheaves]]. 

Then

1. The [[limit]] of $F$ exists, and is the [[presheaf]] which over any [[object]] $c \in \mathcal{C}$ is given by the [[limit]] in [[Set]] of the values of the presheaves at $c$:

   $$
     \left(
       \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{\lim}
       F(d)
     \right)(c)
     \;\simeq\;
     \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{\lim}
      F(d)(c)
   $$


1. The [[colimit]] of $F$ exists, and is the [[presheaf]] which over any [[object]] $c \in \mathcal{C}$ is given by the [[colimit]] in [[Set]] of the values of the presheaves at $c$:

   $$
     \left(
       \underset{\underset{d \in \mathcal{D}}{\longrightarrow}}{\lim}
       F(d)
     \right)(c)
     \;\simeq\;
     \underset{\underset{d \in \mathcal{D}}{\longrightarrow}}{\lim}
      F(d)(c)
   $$

=--


+-- {: .proof}
###### Proof

This is elementary, but we spell it out in detail.

We discuss the case of limits, the other case is [[formal duality|formally dual]].

Observe that there is a canonical [[equivalence of categories|equivalence]]

$$
  [\mathcal{D}, [\mathcal{C}^{op}, \Set]]
  \simeq
  [\mathcal{D} \times \mathcal{C}^{op}, Set]
$$

where $\mathcal{D} \times \mathcal{C}^{op}$ is the [[product category]].

This makes manifest that a [[functor]] $F \;\colon\; \mathcal{D} \to [\mathcal{C}^{op}, Set]$ is equivalently a [[diagram]] of the form

$$
  \array{ 
    &&
    \vdots && && \vdots
    \\
    && \big\downarrow && &&  \big\downarrow
    \\
    \cdots &\longrightarrow&
    F(d_1)(c_2) 
      && \overset{\phantom{AA}}{\longrightarrow} && 
    F(d_2)(c_2)
      &\longrightarrow&
      \cdots 
    \\
    &&
    \big\downarrow && &&  \big\downarrow
    \\
    \cdots
    &\longrightarrow&
    F(d_1)(c_1) 
      && \overset{\phantom{AA}}{\longrightarrow} && 
    F(d_2)(c_1)
      &\longrightarrow&
      \cdots
    \\
    &&
    \big\downarrow && && \big\downarrow
    \\
    && \vdots && &&  \vdots
  }
$$


Then observe that taking the limit of each "horizontal row" in such a diagram indead does yield a presheaf on $\mathcal{C}$, in that the construction extends from objects to morphisms, and uniquely so:
This is because for any [[morphism]] $c_1 \overset{g}{\to} c_2$ in $\mathcal{C}$, a [[cone]] over $F(-)(c_2)$ induces a cone over $F(-)(c_1)$, by vertical composition with $F(-)(g)$

$$
  \array{ 
    && 
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
    F(d)(c_2)
    \\
    & {}^{ }\swarrow && \searrow
    \\
    F(d_1)(c_2) 
      && \overset{\phantom{AA}}{\longrightarrow} && 
    F(d_2)(c_2)
    \\
    {}^{\mathllap{F(d_1)(g)}}\big\downarrow 
      && && 
    \big\downarrow^{\mathrlap{F(d_2)(g)}}
    \\
    F(d_1)(c_1) 
      && \overset{\phantom{AA}}{\longrightarrow} && 
    F(d_2)(c_1)
  }
$$

From this, the universal property of limits of sets implies that there is a _unique_ morphism between the pointwise limits which constitutes a presheaf over $\mathcal{C}$

$$
  \array{
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
    F(d)(c_2)
    \\
    \big\downarrow^{\mathrlap{ 
      \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
      F(d)(g)
    }}
    \\
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
    F(d)(c_1)   
  }
$$

and that is the tip of a cone over the diagram $F(-)$ in presheaves.

Hence it remains to see that this cone of presheaves is indeed universal. 

Now if $I$ is any other cone over $F$ in the category of presheaves, then by the universal property of the pointswise limits, there is for each $c \in \mathcal{C}$ a unique morphism of cones in sets

$$
  I(c) 
    \longrightarrow 
    \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
   F(d)(c)
   \,.
$$

Hence there is at most one morphisms of cones of presheaves, namely if these components make all their naturality squares commute. 


$$
  \array{
    I(c_2) 
      &\longrightarrow& 
      \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
     F(d)(c_2)
     \\
     \big\downarrow && \big\downarrow
     \\
    I(c_1) 
      &\longrightarrow& 
      \underset{\underset{d \in \mathcal{D}}{\longleftarrow}}{lim}
     F(d)(c_1) 
   }
   \,.
$$

But since everything else commutes, the two ways of going around this diagram constitute two morphisms from a cone over $F(-)(c_1)$ to the limit cone over $F(-)(c_1)$, and hence they must be equal, by the universal property of limits.



=--

## Related statements

* [[limits and colimits by example]]

* [[limits preserve limits]]

* [[hom-functor preserves limits]]

* [[adjoints preserve (co-)limits]]

[[!redirects colimits of presheaves are computed objectwise]]


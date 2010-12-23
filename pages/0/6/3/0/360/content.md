
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential-graded objects
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

## Definition

Let $G$ be an [[abelian group]]. Often one takes by default $G = \mathbb{Z}$ the additive group of [[integer]]s.

A **graded ring** is a [[ring]] $R$ equipped with a decomposition of the underlying [[abelian group]] as a [[direct sum]] $R = \oplus_{g \in G} R_g$ such that the product takes $R_{g} \times R_{g'} \to R_{g g'}$.

Analogously there is the notion of graded $k$-[[associative algebra]] over any commutative ring $k$.

Specifically for $k$ a [[field]] a **graded algebra** is a [[monoid]] internal to [[graded vector space]]s.

A [[differential graded algebra]] is a graded algebra $A$ equipped with a [[derivation]] $d : A\to A$ of degree +1 (or -1, dependig on conventions) and such that $d \circ d = 0$. This is the same as a [[monoid]] in the category of [[chain complex]]es.


## Properties


+-- {: .un_prop}
###### Proposition

For $R$ a commutative ring write $Spec R \in Ring^{op}$ for the corresponding object in the [[opposite category]]. Write $\mathbb{G}_m$ for the multiplicative group underlying the [[affine line]]. 

There is a [[natural isomorphism]] between

* $\mathbb{Z}$-gradings on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

+-- {: .proof}
###### Proof

First notice the structure of $\mathbb{G}$.

We have that $\mathbb{G} = Spec \mathbb{Z}[t, t^{-1}] \simeq 
\mathbb{Z}[ [ t ] ]$.

The product structure on $\mathbb{G}$

$$
  \mathbb{G} \times \mathbb{G} \to \mathbb{G}
$$

is dually the ring homomorphism

$$
  \mathbb{Z}[ [ t_1, t_2] ] \leftarrow \mathbb{Z}[ [t ] ]
  \,.
$$

given by

$$
  t \mapsto t_1 \cdot t_2
  \,.
$$

The unit 

$$
  * \to \mathbb{G}
$$

is dually the ring homomorphism

$$
  \mathbb{Z} \leftarrow \mathbb{Z}[ [ t ] ]
$$

given by

$$
  t \mapsto 1 
  \,.
$$


Now for the first direction, let $R$ be a $\mathbb{Z}$-graded commutative ring. Then $X = Spec R$ comes with a $\mathbb{G}$-action given as follows: the action morphism

$$
 \rho :  X \times \mathbb{G} \to X
$$

is dually the ring homomorphism

$$
  R \otimes \mathbb{Z}[ [t ] ] \leftarrow R
$$

defined on homogeneous elements $r$ of degree $n$ by

$$
  r \mapsto r \cdot t^n
  \,.
$$

The action property

$$
  \array{
     X \times \mathbb{G} \times \mathbb{G} &\stackrel{Id \times \cdot}{\to}& X \times \mathbb{G}
     \\
     {}^{\mathllap{\rho} \times Id}\downarrow && \downarrow^{\mathrlap{\rho}}
     \\
     X \times \mathbb{G} &\stackrel{\rho}{\to}& X
  }
$$

1is equivalently the equation

$$
  r (t_1)^n \cdot (t_2)^n = r (t_1 \cdot t_2)^n
$$

for all $n \in \mathbb{Z}$. Similarly the [[unitality]] of the action is the equation

$$
  (1)^n = 1
  \,.
$$

Conversely, given an action of $\mathbb{G}$ on $Spec R$ we have some morphism

$$
  R[ [ t ] ] \leftarrow R
$$

that sends

$$
  r \mapsto \sum_{n \in \mathbb{Z}} r_n t^n
  \,.
$$


By the action property we have that 

$$
  \sum_n r_n (t_1 t_2)^n = \sum_{n,k} (r_n)_k t_1^n t_2^k
  \,.
$$

Hence 

$$
  (r_n)_k = 
  \left\{
    \array{
       r_n & if \; n = k
       \\
       0 & otherwise
    }
  \right.
$$

and so the morphism gives a decomposition of $R$ into pieces labeled by $\mathbb{Z}$.

=--

[[!redirects graded algebras]]

[[!redirects graded ring]]
[[!redirects graded rings]]
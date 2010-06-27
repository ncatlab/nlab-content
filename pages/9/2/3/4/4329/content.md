
<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An **$(\infty,1)$-pullback**  is a [[limit in an (∞,1)-category]] $C$ over a [[diagram]] of the shape

$$
  \{a \to c \leftarrow b\} \to C
  \,.
$$

This is the analog in [[(∞,1)-category theory]] of the notion of [[pullback]] in [[category theory]]. 

## Incarnations

### In quasi-categories

Let $C$ be a [[quasi-category]]. Recall the notion of [[limit in a quasi-category]].

The non-degenerate cells of the [[simplicial set]] $\Delta[1] \times \Delta[1]$ obtained as the [[cartesian product]] of the simplicial 1-[[simplex]] with itself look like

$$
  \array{
    (0,0) &\to& (1,0)
    \\
    \downarrow &\searrow& \downarrow
    \\
    (0,1) &\to& (1,1)
  }
$$

A **sqare** in a [[quasi-category]] $C$ is an image of this in $C$, i.e. a morphism

$$
  s : \Delta[1] \times \Delta[1] \to C
  \,.
$$

The simplicial square $\Delta[1]^{\times 2}$ is [[isomorphism|isomorphic]], as a [[simplicial set]], to the [[join of simplicial sets]] of a 2-[[horn]] with the point:

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \{v\} \star \Lambda[2]_2
  = 
  \left(
  \array{
    v &\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    0 &\to& 2
  }
  \right)
$$

and

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \Lambda[2]_0 \star \{v\}
  = 
  \left(
  \array{
    0&\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    2 &\to& v
  }
  \right)
  \,.
$$

If a square $\Delta[1] \times \Delta[1] \simeq \Lambda[2]_0 \star \{v\} \to C$ exhibits $\{v\} \to C$ as a colimit over $F : \Lambda[2]_0 \to C$, we say the colimit

$$
  v := \lim_\to F := F(1) \coprod_{F(0)} F(2)
$$

is [[generalized the|the]] **pushout** of the diagram $F$.


We have the following $(\infty,1)$-categorical analog of the familiar [pasting law of pushouts](http://ncatlab.org/nlab/show/pullback#Pasting) in ordinary [[category theory]]:

+-- {: .un_prop}
###### Proposition

A pasting diagram of two squares is a morphism

$$
  \Delta[2] \times \Delta[1] \to C
  \,.
$$

Schematically this looks like

$$
  \array{
     x &\to& y &\to& z
     \\
     \downarrow && \downarrow && \downarrow
     \\
     x' &\to& y' &\to& z'
  }
  \,.
$$

If the left square is a pushout diagram in $C$, then the right square is precisely if the outer square is.

=--

+-- {: .proof}
###### Proof

A proof appears as [[Higher Topos Theory|HTT, lemma 4.4.2.1]]

=--



### In model categories

* [[homotopy pullback]]

### In derivators

(...)


## Examples

### Fiber sequence

If $\mathcal{C}$ has a [[terminal object]] and $* \to C \in \mathcal{C}$ is a [[pointed object]], then the **fiber** or **(\infty,1)-kernel** of a morphisms $f : B \to C$ is the $(\infty,1)$-pullback

$$
  ker(f) &\to& *
  \\
  \downarrow && \downarrow
  \\
  B &\stackrel{f}{\to}& C
  \,.
$$

For more on this see [[fiber sequence]].

[[!redirects (∞,1)-pullback]]

[[!redirects (infinity,1)-pullbacks]]
[[!redirects (∞,1)-pullbacks]]

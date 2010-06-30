#Contents#
* automatic table of contents goes here
{:toc}

## Definition

### Interval category

The **interval category** -- often denoted $\mathbf{2}$ or $I$ or $\Delta[1]$ -- is the [[category]] with two [[object]]s and precisely one nontrivial [[morphism]] connecting them:

$$
  I =
  \left\{
    0 \to 1
  \right\}
  \,.
$$

The interval category serves as a [[combinatorial]] model for the [[directed space|directed]] [[interval]]. It is the directed canonical [[interval object]] in [[Cat]].  It is also called the **[[walking structure|walking]] arrow**.  It might also be called the "arrow category" although that term is [[arrow category|also used]] for a category of functors out of $\mathbf{2}$.

The notation $\mathbf{2}$ comes from the fact that the interval category is also the [[ordinal number]] $2$ regarded as a [[poset]], regarded as a category.

It also appears as 

* the 1-[[simplex]];

* the first [[oriental]]; 

* the [[1-globe]].

Since every [[category]] is also an [[(n,r)-category]] for $n,r \geq 1$, we may regard $I$ also as some $(n,r)$-category. For instance regarded as a [[(∞,1)-category]] and modeled as a [[quasi-category]], the interval category is the [[simplicial set]] $\Delta[1]$.

### Interval groupoid

The interval _[[groupoid]]_ is a combinatorial model for the undirected [[interval]].

It is the [[free groupoid]] on the interval category, where the morphism $0 \to 1$ is an [[isomorphism]]. Accordingly the interval groupoid has a second nontrivial morphism, the [[inverse]] $1 \to 0$.

This is the _undirected_ [[interval object]] in [[Cat]] and in [[Grpd]].

## Applications

The interval category is one of those [[diagram]] category that are not terribly interesting in themselves, but that serve an important role in [[category theory]] as a whole. 

For instance a [[natural transformation]] $\eta : F \Rightarrow G$ between two [[functor]]s $F,G : C \to D$ is precisely the same as a strictly [[commuting diagram]]

$$
  \array{
    C \times \{0\}
    \\
    \downarrow & \searrow^{\mathrlap{F}}
    \\ 
    C \times I &\stackrel{\eta}{\to}& D
    \\
    \uparrow & \nearrow_{\mathrlap{G}}
    \\
    C \times \{1\}
  }
$$

in [[Cat]], where on the left we have the [[cartesian product]] of $C$ with $I$. 

Accordingly, for $I_{iso}$ the interval groupoid, a [[natural isomorphism]] $\eta : F \Rightarrow G$ is the same as a diagram

$$
  \array{
    C \times \{0\}
    \\
    \downarrow & \searrow^{\mathrlap{F}}
    \\ 
    C \times I_{iso} &\stackrel{\eta}{\to}& D
    \\
    \uparrow & \nearrow_{\mathrlap{G}}
    \\
    C \times \{1\}
  }
 \,.
$$

This is a [[left homotopy]] in $Cat$.

Dually, forming the [[functor category]] 

$$
  Arr(D) := [I,D]
$$

from the interval category produces the [[arrow category]] of $D$, and a natural transformation $\eta$ is also the same as a diagram

$$
  \array{
     && D \times \{0\}
     \\
     & {}^{\mathllap{F}}\nearrow & \uparrow
     \\
     C &\stackrel{\eta}{\to}& [I,D]
     \\
     & {}_{\mathllap{G}}\searrow & \downarrow
     \\
     && D \times \{1\}
  }
  \,.
$$

With $I$ replaced by $I_{iso}$ this is again a natural isomorphism, now represented as a [[right homotopy]] in [[Cat]].

The analogous statements are true in [[higher category theory]]. 



[[!redirects 2]]
[[!redirects I]]
[[!redirects interval groupoid]]
[[!redirects walking arrow]]
[[!redirects walking morphism]]


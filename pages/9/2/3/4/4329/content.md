
> under construction

<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An **$(\infty,1)$-pullback**  is a [[limit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of the shape

$$
  \{a \to c \leftarrow b\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cone]]

$$
  \array{
    A \times_C B &\to& B
    \\
    \downarrow &\swArrow& \downarrow
    \\
    A &\to& C
  }
$$

which is [[universal property|universal]] among all such cones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[pullback]] in [[category theory]]. 

## Incarnations

### In quasi-categories

Let $\mathcal{C}$ be a [[quasi-category]]. Recall the notion of [[limit in a quasi-category]].

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

If a square $\Delta[1] \times \Delta[1] \simeq \Lambda[2]_0 \star \{v\} \to C$ exhibits $\{v\} \to C$ as a [[limit in a quasi-category|quasi-categorical limit]] over $F : \Lambda[2]_0 \to C$, we say the limit

$$
  v := \lim_\leftarrow F := F(1) \prod_{F(0)} F(2)
$$

is [[generalized the|the]] **quasi-categorical pullback** of the diagram $F$.


We have the following quasi-categorical analog of the familiar [pasting law of pushouts](http://ncatlab.org/nlab/show/pullback#Pasting) in ordinary [[category theory]]:

A [[pasting]] diagram of two squares is a morphism

$$
  \sigma : \Delta[2] \times \Delta[1] \to \mathcal{c}
  \,.
$$

Schematically this looks like

$$
  \array{
     a &\to& b &\to& c
     \\
     \downarrow && \downarrow && \downarrow
     \\
     d &\to& e &\to& f
  }
$$

in $\mathcal{C}$.

+-- {: .un_prop}
###### Proposition
**(pasting law for quasi-categorical pullbacks)**

If the right square is a pullback diagram in $\mathcal{C}$, then the left square is precisely if the outer square is.

=--

This is [[Higher Topos Theory|HTT, lemma 4.4.2.1]]

+-- {: .proof}
###### Proof

Consider the diagram inclusions

$$
  \left(
    \array{
      && && c
      \\
      && && \downarrow
      \\
      d &\to& e &\to& f
    }
  \right)
  \;\;\to\;\;
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow && \downarrow
      \\
      d &\to& e &\to& f
    }
  \right)
  \;\;\leftarrow\;\;
  \left(
    \array{
      && b 
      \\
      && \downarrow
      \\
      d &\to& e
    }
  \right)
$$

and the induced diagram of [[over quasi-categories]]

$$
  \mathcal{C}_{/\sigma(c,d,f)}
  \stackrel{\phi}{\leftarrow} 
  \mathcal{C}_{/\sigma(b,c,d,e,f)}
  \stackrel{\psi}{\to}
  \mathcal{C}_{/\sigma(b,d,e)}
  \,.
$$

Notice that by definition of [[limit in a quasi-category]] the quasi-categorical pullback $\sigma(c) \times_{\sigma(f)} \sigma(d)$ is [[generalized the|the]] [[terminal object in a quasi-category|terminal object]] in $\mathcal{C}_{/\sigma(c,d,f)}$, while $\sigma(d) \times_{\sigma(d)} \sigma(e)$ is the terminal object in $\mathcal{C}_{/\sigma(b,d,e)}$. 

The strategy now is to show that both these morphisms $\phi$ and $\psi$ are acyclic fibrations in the [[model structure for quasi-categories]]. That will imply that these terminal objects coincide as objects of $\mathcal{C}$.

To see that, ...


=--



### In model categories

* [[homotopy pullback]]

### In derivators

(...)


## Examples

### Fiber sequence

If $\mathcal{C}$ has a [[terminal object]] and $* \to C \in \mathcal{C}$ is a [[pointed object]], then the **fiber** or **(\infty,1)-kernel** of a morphisms $f : B \to C$ is the $(\infty,1)$-pullback

$$
  \array{
    ker(f) &\to& *
    \\
    \downarrow && \downarrow
    \\
    B &\stackrel{f}{\to}& C
  }
  \,.
$$

For more on this see [[fiber sequence]].

[[!redirects (∞,1)-pullback]]
[[!redirects (infinity,1)-pullbacks]]
[[!redirects (∞,1)-pullbacks]]

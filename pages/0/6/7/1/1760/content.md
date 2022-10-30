#Idea#

The _delooping_ of an object $A$ is, if it exists, a uniquely [[pointed object]] $\mathbf{B} A$ such that $A$ is the [[loop space object]] of $\mathbf{B} A$:

$$
  A \simeq \Omega(\mathbf{B} A)
$$


#Definition#

Loop space objects are defined in any [[(infinity,1)-category]] $\mathbf{C}$ with [[homotopy pullback]]s: for $X$ any [[pointed object]] of $\mathbf{C}$ with point ${*} \to X$, its [[loop space object]] is [[generalized the|the]] [[homotopy pullback]] $\Omega X$ of this point along itself:

$$
  \array{
    \Omega X &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& X
  }
  \,.
$$

Conversely, if $A$ is given and a [[homotopy pullback]] diagram 

$$
  \array{
    A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& \mathbf{B}A
  }
$$

exists, with the point ${*} \to \mathbf{B} A$ being essentially unique, by the above $A$ has been realized as the [[loop space object]] of $\mathbf{B} A$

$$
  A = \Omega \mathbf{B} A
$$

and we say that $\mathbf{B} A$ is the **delooping** of $A$.

#Remarks#

If $\mathbf{B}$ is even a [[stable (infinity,1)-category]] then all deloopings exist and are then also denoted $\Sigma A$ and called the **suspension** of $A$.


#Examples#

## delooping of a group to a groupoid ##

Let $G$ be a [[group]] regarded as a [[discrete category|discrete groupoid]] in the [[(infinity,1)-topos]] [[Infinity-Grpd]] of [[infinity-groupoid]]s.

Then $\mathbf{B} G$ exists and is, up to equivalence, the [[groupoid]]

* with a single object $\bullet$

* with $Hom_{\mathbf{B} G}(\bullet, \bullet) = G$

* and with composition of morphisms in $\mathbf{B} G$ being given by the product operation in the group.

More informally but more suggestively we may write

$$
  \mathbf{B} G = \{ \bullet \stackrel{g}{\to} \bullet | g \in G\}
$$

or

$$
  \mathbf{B}G = \{ 
     \bullet \righttoleftarrow g \;|\; g \in G 
  \}
$$

to emphasize that there is really only a single arrow.

Notice how the [[homotopy pullback]] works in this simple case:

the universal 2-cell $\eta$

$$
  \array{
    G &\to& {*}
    \\
    \downarrow &\Downarrow^{\eta}& \downarrow
    \\
    {*} &\to& \mathbf{B}G
  }
$$

filling this [[2-limit]] diagram is the [[natural transformation]] from the constant [[functor]]

$$
  G \to {*} \to \mathbf{B}G
$$

to itself, whose map

$$
  \eta : Obj(G) \to Mor(\mathbf{B}G)
$$ 

is just the identity map, using that $Obj(G) = G$ and $Mor(\mathbf{B}G) = G$.
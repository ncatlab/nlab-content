<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Between any two [[objects]] $x,y$ in an [[(∞,1)-category]] $C$ there is an 
[[∞-groupoid]] of morphisms. It is well-defined up to equivalence. 
When the $(\infty,1)$-category is incarnated as a [[quasi-category]], there are
several explicit ways to extract representatives of this [[hom-object]].

## Definition

Let $C$ be a [[quasi-category]] (or any [[simplicial set]]), and $x,y \in C_0$
any two objects. Then write

$$
  Hom_C(x,y) := [\tau(C)(x,y)] \in Ho(sSet_{Quillen}) \simeq Ho(\infty Grpd)
  \,,
$$

where 

* $\tau$ is the [[left adjoint]] to the [[homotopy coherent nerve]];

* $\tau(C)$ is accordingly the [[simplicially enriched category]] incarnation of $C$,

* $\tau(C)(x,y)$ is the [[sSet]]-[[hom-object]] of that $sSet$-[[enriched category]];

* $[\tau(C)(x,y)]$ is the equivalence class of this object.

This defines $Hom_C(x,y)$ as an equivalence class of $\infty$-groupoids, but
at the same time defines a particular representative: if $C$ is a [[quasi-category]] then
$\tau(C)(x,y)$ is a [[Kan complex]] that represents this class.

This is useful for many purposes, but $\tau(C)$ is usually hard to compute explicitly.
The following three other definitions of representatives of $Hom_C(x,y)$ are often useful.

**Definition**

For $C$ and $x,y$ as above, write

$$
  Hom_C^{L R}(x,y) := \{x\} \times_C C^{\Delta[1]} \times_C \{y\}
$$

for the [[pullback]] 

$$
  \array{
    \{x\} \times_C C^{\Delta[1]} \times_C \{y\} &\to& C^{\Delta[1]}
    \\
    \downarrow && \downarrow^{\mathrlap{d_1 \times d_0}}
    \\
    \{x\} \times \{y\}
    &\to&
    C \times C
  }
$$

in [[sSet]] of the [[path object]] $C^{\Delta[1]}$ (the 
cartesian [[internal hom]] in [[sSet]] with the 1-[[simplex]] $\Delta[1]$) .


Write

$$
  Hom^R_C(x,y) \in sSet
$$

for the simplicial set whose $n$-[[simplex|simplices]] are defined to be those morphisms
$\sigma : \Delta[n+1] \to C$ such that the restriction to $\Delta\{0, \cdots, n\}$
is the constant map to $x$ and the restriction to $\Delta\{n+1\}$ is the map to $y$.

Analogously, write

$$
  Hom^L_C(x,y) \in sSet
$$

for the simplicial set whose $n$-simplices are morphisms $\Delta[n+1] \to X$ which restrict to
$x$ on $\{0\}$ and are constant on $y$ when restricted to $\{1, \cdots, n+1\}$.

**Remark** The 1-cells in $Hom_C^R(x,y)$, $Hom_C^L(x,y)$ and $Hom_C^{L R}(x,y)$ 
are 2-[[globes]] in $C$. The 2-cells are commuting squares of vertical composites 
of 2-globes forming a 3-globe.

Equivalently this may be understood in terms of fibers of [[over quasi-categories]].

Recall that for $p : K \to C$ a morphism, we have the [[over quasi-category]] $C_{/p}$ 
defined by

$$
  (C_{/p})_n := Hom(\Delta[n],C^{/p}) :=
  Hom_p(\Delta[n] \star K, C)
  \,,
$$

where on the right we have the set of morphisms in $sSet$ out of the 
[[join of simplicial sets]] that restrict on $K$ to $p$.

This comes with the canonical projection $C^{p/} \to C$, which sends
$(\Delta[n] \star K \to C)$ to the restriction 
$(\Delta[n] \to \Delta[n] \star K \to C)$.

There is also the other, equivalent, definition $C^{/p}$ of [[over quasi-category]], 
defined using the other, equivalent, definition $\diamondsuit$ 
of [[join of quasi-categories]] by

$$
  (C^{/p})_n := Hom_{K/sSet}( \Delta[n] \diamondsuit K, C)
  \,.
$$


**Obervation**

We have 

$$
  Hom^R_C(x,y) = C_{/{y}} \times_C \{x\}
  \,,
$$

where on the right we have the [[pullback]] in [[sSet]] in the diagram

$$
  \array{
    C_{/{y}} \times_C \{x\} &\to& C_{/y}
    \\
    \downarrow && \downarrow
    \\
    \{x\} &\to& C
  }
$$

and the equality sign denotes an [[isomorphism]] in [[sSet]].

And we have

$$
  Hom_C^{L R}(x,y) = C^{/y} \times_C \{x\}
$$


**Proof** For the first statement 
use the identification of $\Delta[n+1]$ with the [[join of simplicial sets]]
$\Delta[n] \star \Delta[0]$, as described there.

For the second statement use that $\Delta[n] \diamondsuit \Delta[0]$ 
is the colimit $\Delta[n+1]$ in

$$
  \array{
  && \Delta[n] \times \Delta[0] &\to & \Delta[0] 
  \\
  && \downarrow &\downarrow&
  \\
  \Delta[n] \times \Delta[0] &\to& C \times \Delta[0] \times \Delta[1] &\to& \Delta[n+1]
  \\
  \downarrow && \downarrow && \downarrow
  \\
  \Delta[n] &\to& C \times \Delta[1] &\to& \Delta[n+1]
  }
  \,,
$$

so that

$$
  C^{/y} = C^{\Delta[1]} \times_C \{y\}
$$

because

$$
  (C^{/y})_n = Hom_{\Delta[0]/sSet}( 
    \Delta[n]\times \Delta[1] \coprod_{\Delta[1] \times \Delta[0]} \Delta[0], C)
    =
    Hom(\Delta[n] \times \Delta[1], C) \times_{Hom(\Delta[1],C)} \{y\}
    = (C^{\Delta[1]} \times \{y\})_n
    \,.
$$
	
**Remark** One advantage of the representative $\tau(C)(c,y)$ of $Hom_C(x,y)$ is that,
by the fact that $\tau(C)$ is an [[sSet]]-[[enriched category]], there is a strict 
composition operation

$$
  \tau(C)(x,y) \times \tau(C)(y,z) \to \tau(C)(x,z)
  \,.
$$

This is not available for the $Hom_C^R(x,y)$ and $Hom_C^L(x,y)$	

## Properties

**Proposition** 

If the simplicial set $C$  is a [[quasi-category]], then $Hom_C^R(x,y)$ is a
[[Kan complex]].

**Proof**

This is [[Higher Topos Theory|HTT, prop 1.2.2.3]].

From the definition it is clear that $Hom_C^R(x,y)$ has fillers for all inner and
right outer horns $\Lambda[n]_{1 \leq i \leq n}$, because these yield inner horns in
$\Delta[n+1] = \Delta[n] \star \Delta[0]$. The claim follows then with the fact that
every [[right fibration]] over the point is a Kan complex, as described there.


**Proposition**

If $C$ is a [[quasi-category]] then the canonical inclusions

$$
  Hom_C^R(x,y) \to Hom_C^{L R}(x,y) \leftarrow Hom_C^L(x,y)
$$

are [[homotopy equivalences]] of [[Kan complexes]].

**Proof**

This is [[Higher Topos Theory|HTT, cor. 4.2.1.7]].

As described at [[join of quasi-categories]] the canonical morphism 
$C_{/y} \to C^{/y}$ is an equivalence of quasi-categories. So 
for the statement for $Hom_C^R(x,y)$ it suffices to
show that this induces an equivalence of fibers over $C$.
This follows from the fact that both $C_{/y} \to C$ and $C^{/y} \to C$
are [[Cartesian fibrations]]. 

See [[Cartesian fibrations]] for these statements. This is 
[[Higher Topos Theory|HTT, prop. 3.3.1.5. (2)]]. 

The statement for $Hom_C^L(x,y)$ follows dually.



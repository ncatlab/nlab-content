
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In general, [[limit]]s and [[colimit]]s do not commute. 

It is therefore of interest to list the special conditions under which certain limits do commute with certain colimits. 

This page lists some of these.

## Filtered colimits commute with finite limits 

For $C$ a small [[filtered category]], the functor $colim_C : [C,Set] \to Set$ commutes with finite limits.

More in detail, let

* $C$ be a small [[filtered category]]

* $D$ be a finite category;

* $F : C \times D^{op} \to Set$  a [[functor]];

then the canonical morphism

$$
  colim_C lim_D F \stackrel{\simeq}{\to}
   lim_D colim_C F
$$

is an [[isomorphism]].

In fact, $C$ is a [[filtered category]] if and only if this is true for all finite $D$ and all functors $F : C \times D^{op} \to Set$.

## Certain colimits are stable by base change {#ColimitsStableByBaseChange}

Let $C$ be a category with [[pullback]]s and [[colimit]]s of shape $D$. 

We say that colimits of shape $D$ are **stable by [[base change]]** or **stable under pullback** if for every functor $F : D \to C$ and for all [[pullback]] diagrams of the form

$$
  \array{
    (colim_D F) \times_Z Y &\to& colim_D F
    \\
    \downarrow && \downarrow
    \\
    Y &\to & Z
  }
$$

the canonical morphism

$$
  colim_{d \in D} (F(d) \times_Z Y)
  \stackrel{\simeq}{\to}
  (colim_D F) \times_Z Y
$$

is an [[isomorphism]].

All colimits are stable under base change in for instance

* $C =$ [[Set]];
* hence for $C =$ a [[presheaf]] category $[S^{op},Set]$ (since colimits in such $C$ are computed objectwise in $Set$), see [[limits and colimits by example]]);
* more generally, any [[topos]];

but not in for instance

* $C = $ [[Ab]].

**Remark**

In [[topos]] theory and [[(∞,1)-topos]] theory one says that _[[universal colimits|colimits are universal]]_ if they are preserved under pullback.
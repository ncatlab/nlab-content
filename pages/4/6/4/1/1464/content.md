
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
* table of contents
{:toc}

## Idea

In general, [[limit]]s and [[colimit]]s do not commute. 

It is therefore of interest to list the special conditions under which certain limits do commute with certain colimits. 

This page lists some of these.

## Filtered colimits commute with finite limits 
 {#FilteredColimitsCommuteWithFiniteLimits}

For $C$ a small [[filtered category]], the functor $colim_C : [C,Set] \to Set$ commutes with finite limits.

More in detail, let

* $C$ be a small [[filtered category]]

* $D$ be a finite category (or more generally an [[L-finite category]]);

* $F : C \times D^{op} \to Set$  a [[functor]];

then the canonical morphism

$$
  colim_C lim_D F \stackrel{\simeq}{\to}
   lim_D colim_C F
$$

is an [[isomorphism]].

In fact, $C$ is a [[filtered category]] if and only if this is true for all finite $D$ and all functors $F : C \times D^{op} \to Set$.

## Sifted colimits commute with finite products

Similarly to the example of filtered limits, for $C$ a small [[sifted category]], the functor $colim_C : [C,Set] \to Set$ commutes with finite products. In fact, this is usually taken to be the definition of a [[sifted category]], and then a theorem of Gabriel and Ulmer characterizes sifted categories as those for which the diagonal functor $C \to C \times C$ is a [[final functor]].

For more on this see at _[[distributivity of products and colimits]]_.

## Taking orbits under the action of a finite group commutes with cofiltered limits

More precisely, if $G$ is a finite group, $C$ is a small cofiltered category and $F : C \to G-Set$ is a functor, the canonical map

$$ (\lim F)/G \to \lim_{j \in F} (F(j)/G) $$

is an isomorphism. This fact is mentioned by Andr&#233; Joyal in _Foncteurs analytiques et esp&#232;ces de structures_; a proof can be found [here](http://math.ubc.ca/~oantolin/notes/fingrpcomm.html).

## Coproducts commute with connected limits

If $A$ is a set, $C$ is a [[connected category]], and $F : C\times A\to Set$ is a functor, the canonical map

$$ \coprod_{a\in A} \lim_{c\in C} F(c,a)\to \lim_{c\in C} \coprod_{a\in A}F(c,a) $$

is an isomorphism. This remains true if $Set$ is replaced by any [[Grothendieck topos]].

More generally, if $\mathbf{H}$ is an [[(∞,1)-topos]], $A$ is an [[n-groupoid]], and $C$ is a small [[(∞,1)-category]] whose [[classifying space]] is [[n-connected]], then $C$-limits commute with $A$-colimits in $\mathbf{H}$. This follows from the fact that the colimit functor $\mathbf{H}^A\to\mathbf{H}$ induces an equivalence of (∞,1)-topoi $\mathbf{H}^A\simeq \mathbf{H}_{/A}$. For example, if $C$ is a [[cofiltered (∞,1)-category]] or even a [[cosifted (∞,1)-category]], then the classifying space of $C$ is weakly contractible and hence $C$-limits commute with $A$-colimits in $\mathbf{H}$ for any [[∞-groupoid]] $A$.

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

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Given an [[action]] $\rho$ of a [[group]] $G$ on a [[set]] $S$, the action groupoid $S//G$ is a bit like the quotient set $S/G$ (the set of $G$-orbits).  But, instead of taking elements of $S$ in the same $G$-orbit as being [[equality|equal]] in $S/G$, in the action groupoid they are just [[isomorphism|isomorphic]].  We may think of the action groupoid as a [[homological resolution|resolution]] of the usual quotient.  When the action of $G$ on $S$ fails to be free, the action groupoid is generally better-behaved than the quotient set.

The action groupoid also goes by other names, including '[[weak quotient]]'.  It is a special case of a '[[pseudo colimit]]', as explained below. It is also called a "[[semidirect product]]" and then written $S \rtimes G$. The advantage of this is that it accords with the generalisation to the action of a group $G$ on a groupoid $S$, which is relevant to orbit space considerations, since if $G$ acts on a space $X$ it also acts on the fundamental groupoid of $X$; this is fully developed in  "Topology and Groupoids", Chapter 11. 

## Definition

### In category theory
Given an [[action]] 
$\rho : S \times G \to S$ of a group $G$ on the set $S$, the _action groupoid_ $S//G$ (or, more precisely, $S//_\rho G$) is the [[groupoid]] for which:

* an object is an element of $S$

* a morphism from $s \in S$ to $s' \in S$ is a group element $g \in G$ with $g s = s'$.  So, a general morphism is a pair $(g,s) : s \to g s$.

* The composite of $(g,s) : s \to g s = s'$ and $(g',s'): 
s' \to g's'$ is $(g' g, s) : s \to g' g s$.

Equivalently, we may define the _action groupoid_ $S//G$ to be the groupoid
$$
  \array{
     && S \times G
     \\
     & {}^{s := p_1}\swarrow
     &&
     \searrow^{t = \rho}
     \\
     S
     &&&&
     S
  }
$$
with composition 
$$(S \times G) \times_{t,s} (S \times G) \simeq S \times G \times G \to S \times G$$ 
given by the product in $G$.

We can denote the morphisms in $S//G$ by

$$S//G:=\{s\stackrel{g}{\to} \rho(s,g) | s\in S, g\in G\}.$$

### In (∞,1)-category theory

+-- {: .num_defn #ActionInfinityGroupoid}
###### Definition
Let $C$ be an ($\infty$,1)-category, let $G\in Grpd(C)$ be a groupoid object in $C$, let $X\in C$ be an object. Then the [[simplicial object]]

$$
  \array{
      \cdots
    &
      \underoverset{\to}{\to}{\to}
    &
      X\times_{G_0}G\times_p G
    &
      \rightrightarrows
    &
      X\times_{G_0}G
    &
      \to
    &
      X
  }
$$

such that the degree-wise projections give a simplicial map

$$
  \array{
        \cdots
      &
        \underoverset{\to}{\to}{\to}
      &
        X\times_{G_0}G\times_p G
      &
        \rightrightarrows
      &
        X\times_{G_0}G
      &
        \to
      &
        X
    \\
      &&
        \downarrow
      &&
        \downarrow
      &&
        \downarrow^a
    \\
        \cdots
      &
        \underoverset{\to}{\to}{\to}
      &
        G\times_p G
      &
        \rightrightarrows
      &
        G
      &
        \xrightarrow{p}
      &
        G_0
  }
$$

is called an _action of_ $G$ _on_ $X$. The colimit $colim\; X\times_{G_0}^{\times_\bullet}$ is called _action $\infty$-groupoid of_ $G$ _on_ $X$.


=--

## Interpretations


On top of the above explicit definitions, there are several useful ways to think of action groupoids. 

Recall that the action $\rho$ is equivalently thought of as a functor

$$
  \rho : \mathbf{B}G \to Sets
$$

from the [[group]] $G$ regarded as a one-object groupoid, denoted $\mathbf{B}G$.

This functor sends the single object of $\mathbf{B}G$ to the set $S$.


### As a pseudo colimit 

$S//G$ is the [[2-limit|2-colimit]] of $\rho$, i.e., the [[category of elements]] of $\rho$.

$$
  S//G \simeq colim_{\mathbf{B}G} \rho
  \,.
$$

The universal cocone consists of cells of the form

$$
  \array{
     S &&\stackrel{\rho(g)}{\to}&& S
     \\
     & \searrow &\stackrel{\simeq}{\Leftarrow}& \swarrow
     \\
     && S//G
  }
  \,,
$$

where the 2-morphism is uniquely specified and in components given by $s \mapsto (s \stackrel{g}{\to} \rho(s,g))$.



### As associated universal bundle 

Let $Set_*$ be the category of pointed sets and $Sets_* \to Sets$ be the canonical forgetful functor. 
We can think of this as the "universal $Set$-bundle".

Then $S//G$ is the pullback

$$
  \array{
    S//G
    &\to&
    Sets_*
    \\
    \downarrow
    &&
    \downarrow
    \\
    \mathbf{B}G
    &\stackrel{\rho}{\to}&
    Sets
  }
  \,.
$$


One place where we discussed this is the comment [It was David Roberts who apparently first noticed...](http://golem.ph.utexas.edu/category/2007/08/on_hess_and_lack_on_bundles_of_1.html#c019094).

Notice also that an action of $G$ on the set $S$ gives rise to a morphism $p: S \rtimes G \to G$ which has the property of unique path lifting, or in other words is a discrete opfibration. It is also called a covering morphism of groupoids, and models nicely covering maps of spaces. 

Higgins used this idea to lift presentations of a group $G$ to presentations of the  covering morphism of $G$ derived from the action of $G$ on cosets, and so to apply graph theory to obtain old and new subgroup theorems in group theory. 

### As a stack

In the case where the action is [[internalization|internal]] to sets with structure, such as internal to [[Diff]] one wants to realize the action groupoid as a [[Lie groupoid]]. That Lie groupoid in turn may be taken to present a [[differentiable stack]] which then usually goes by the same name $S//G$.


## Properties

### Relation to representation theory

The action groupoids $X//G$ of a group $G$ come equipped with a canonical map to $\mathbf{B}G \simeq \ast //G$. Regarded via this map as objects in the [[slice (infinity,1)-category|slice]] of groupoids over $\mathbf{B}G$, action groupoids are in fact [[equivalence|equivalent]] to the actions that they arise from.

For more on this see at _[[infinity-action]]_ and also at _[[geometry of physics -- representations and associated bundles]]_.

## Action $\infty$-groupoid {#ActionooGrpd}

All of this goes through almost verbatim for actions in the context of [[(∞,1)-category theory]].

Let $G$ be an [[∞-group]] in that $\mathbf{B}G$ is an [[∞-groupoid]] with a single object. An action of $G$ on an [[(∞,1)-category]] is an [[(∞,1)-functor]]

$$
  \rho : \mathbf{B}G \to (\infty,1)Cat
$$

to [[(∞,1)Cat]]. This takes the single object of $\mathbf{B}G$ to some $(\infty,1)$-category  $V$.

Again we want to **define** the _action groupoid_ $V//G$ as the [[limit in a quasi-category|(∞,1)-categorical colimit]] over the action:

$$
  V//G := \lim_\to \rho
  \,.
$$

By the result [described here](http://ncatlab.org/nlab/show/limit+in+a+quasi-category#WithValInooGrpd) this is, as before, equivalent to the pullback of the "universal $(\infty,1)Cat$-bundle" $Z \to (\infty,1)Cat$, namely to the [[coCartesian fibration]]

$$
  \array{
    V//G &\to& Z
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\rho}{\to}& (\infty,1)Cat
  }
$$

classified by $\rho$ under the [[(∞,1)-Grothendieck construction]]. As before, we can continue a [[fiber sequence]] to the left by adjoining the $(\infty,1)$-categorical pullback along the point inclusion $* \to \mathbf{B}G$

$$
  \array{
    V&\to& V//G &\to& Z
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& \mathbf{B}G &\stackrel{\rho}{\to}& (\infty,1)Cat
  }
  \,.
$$

The resulting total $(\infty,1)$-pullback rectangle is the fiber of $Z \to (\infty,1)Cat$ over the $(\infty,1)$-category $V$, which is $V$ itself, as indicated.

## Some comment

 * If the action of a Lie group $G$ on the manifold $X$ is free and proper, what you get is a manifold $X/G$.

 *  If the action of a Lie group $G$ on the manifold $X$ is not necesssarily free and proper, what you get is a Lie groupoid, denoted (among other symbols) by $X//G$.

## Related concepts

* [[global quotient orbifold]], [[quotient stack]], [[homotopy quotient]]


* the [[groupoid cardinality]] of action groupoids is given by the [[class formula]]

## References

* P.J. Higgins, 1971, "Categories and Groupoids", van
Nostrand, {New   York}. Reprints in Theory and Applications of Categories, 7 (2005) pp 1--195.

* R. Brown, "Topology and groupoids", Booksurge, 2006, available from amazon; details [here](http://groupoids.org.uk/topgpds.html).


* John Armstrong's article, [Groupoids (and more group actions)](http://unapologetic.wordpress.com/2007/06/09/groupoids-and-more-group-actions/)

* John Baez, [TWF 249](http://math.ucr.edu/home/baez/week249.html)

[[!redirects action groupoids]]
[[!redirects action group]]
[[!redirects action groups]]
[[!redirects groupoid quotient]]

> For the closure of a subset of a topological space, see at _[[closed subset]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _closure operator_ is a [[monad]] on a [[poset]], typically a [[poset of subobjects]] (of some [[object]]) in some [[category]].  In [[logic]], this is often referred to as a (monadic) _[[modal operator]]_.  The elements of the poset that are fixed by the closure operator are called _closed_ (or perhaps _[[modal type|modal]]_). 

Dually, a [[comonad]] on a poset is called a _co-closure operator_ and the elements fixed by it are called _co-closed_.

More generally, in [[type theory]]/[[category theory]], we may think of any [[idempotent monad]] on a [[category]] as being a closure operator, and of any idempotent [[comonad]] as a co-closure operator.

## Definition

+-- {: .num_defn #ClosureOperatorAsMonad}
###### Definition

For $\mathcal{C}$ a [[category]], a **closure operator** $\diamond$ on $\mathcal{C}$ is an [[idempotent monad]] on $\mathcal{C}$, hence an [[endofunctor]] $\diamond \colon \mathcal{C} \to \mathcal{C}$ equipped with [[unit of a monad|unit]] and product [[natural transformations]]

* $\eta_{\diamond} \;\colon\; id_{\mathcal{C}} \to \diamond$

* $\mu_{\diamond} \;\colon\; \diamond \circ \diamond \to \diamond$

such that the [[monad]]-axioms hold and such that the following equivalent conditions hold (idempotency)

* the product map is an [[isomorphism]];

* $\eta_{\diamond(-)}$ is an isomorphism.

=--

+-- {: .num_defn #ClosureAndClosedObjects}
###### Definition

For $\diamond \colon \mathcal{C} \to \mathcal{C}$ a closure operator, def. \ref{ClosureOperatorAsMonad}, and for $X \in \mathcal{C}$ an object, we say that 

* $\diamond X \in \mathcal{C}$ is the **$\diamond$-closure** of $X$;

* $\eta_{X} \colon X \to \diamond X$ is the **closing map** or **map to the closure**;

* $X$ is **$\diamond$-closed** precisely if $\eta_X$ is an [[isomorphism]].

We write

$$
  \mathcal{C}_\diamond \hookrightarrow \mathcal{C}
$$

for the [[full subcategory]] on the $\diamond$-closed objects.

=--

## Examples

* A closure operator on a [[power set]] is also called a _[[Moore closure]]_. See there for more.

* One well-known example of a Moore closure is [[topological closure]], which is precisely a Moore closure that preserves finite joins (unions). Similarly, one can view _[[topological interior]]_ as a co-closure operator on a power set that preserves finite meets, or dually as a closure operator on the *[[opposite poset|opposite]]* of a power set that preserves finite [[joins]] (given by [[intersections]] of subsets).

* A [[Lawvere-Tierney topology]] is a closure operator on the [[subobject classifier]] $\Omega$ of a [[topos]] $E$, viewed as an internal [[meet-semilattice]]. More precisely, it is a just such a closure operator that preserves internal finite meets. Externally, $\hom(-, \Omega) \colon E^{op} \to Set$ provides an example of a [[universal closure operator]]. 



## Induced closure on slices
 {#InducedClosureOnSlices}

We discuss here how a closure operator on a [[topos]] may induce closure operators on each of its [[slice categories]].

Throughout, our [[topos]] is denoted $\mathcal{C}$. 

Given a [[monad]] $\diamond \colon \mathcal{C} \to \mathcal{C}$ we write  $\eta_\diamond \colon id_{\mathcal{C}} \to \diamond$
for its [[unit of a monad|unit]], and write $\mu_\diamond \colon \diamond \circ \diamond \to \diamond$ for its multiplication. As we proceed, we add assumptions on $\diamond$, such as that it preserves certain [[limits]] and/or that it be [[idempotent monad|idempotent]]. 

For $X \in \mathcal{C}$ any [[object]], we write $\mathcal{C}_{/X}$ for the [[slice topos]] over it. The corresponding [[base change geometric morphism]] ([[dependent sum]] $\dashv$ [[context extension]] $\dashv$ [[dependent product]]) we write

$$
  \left(
    \underset{X}{\sum}
    \dashv 
    X^\ast
    \dashv
    \underset{X}{\prod}
  \right)
  \;\colon\;
  \mathcal{C}_{/X}
  \stackrel{\overset{\sum_X}{\to}}{\stackrel{\overset{X^\ast}{\leftarrow}}{\underset{\prod_X}{\to}}}
  \mathcal{C}
  \,.
$$

We denote an object $p \in \mathcal{C}_{/X}$ in the slice also by the corresponding [[morphism]] 

$$
  p \coloneqq 
  \left(
    \left(\sum_X p\right) \stackrel{p}{\to} X
  \right)
  \coloneqq
  \sum_X \left( p \to \ast_{X} \right)
$$

in $\mathcal{C}$, which is the image under [[dependent sum]] of the unique morphism from $p$ to the [[terminal object]] in $\mathcal{C}_{/X}$. Accordingly, a morphism $\phi \colon p_1 \to p_2$ in the slice we also denote by the corresponding triangular [[commuting diagram]]

$$
  \left(
   \array{
      \sum_X p_1 &&\stackrel{\sum_X \phi}{\to}&& \sum_X p_2
      \\
      & {}_{\mathllap{p}_1}\searrow && \swarrow_{\mathrlap{p_2}}
      \\
      && X
    }
  \right)
$$

in $\mathcal{C}$.


Here we study the following endofunctors on slices induced from a monad on the total topos.
  
+-- {: .num_defn #InducedOperatorOnSlice}
###### Definition

For $\diamond \colon \mathcal{C} \to \mathcal{C}$ an [[monad]] on a [[topos]] $\mathcal{C}$, and for $X \in \mathcal{C}$ any [[object]], the **induced operator**  

$$
  \diamond_{/X} \colon \mathcal{C}_{/X} \to \mathcal{C}_{/X}
$$

on the [[slice topos]] $\mathcal{C}_{/X}$ is the [[functor]] which sends an object $(E \stackrel{p}{\to} X) \in \mathcal{C}_{/X}$ to $(X \underset{\diamond X}{\times} \diamond E \stackrel{\eta_\diamond(X)^\ast \diamond p}{\to} X)$, hence to the left vertical morphism in the [[pullback]] [[diagram]]

$$
  \array{
    X \underset{\diamond X}{\times} \diamond E 
    &\to&
    \diamond E
    \\
    \downarrow^{\mathrlap{\eta_\diamond(X)^\ast \diamond p}} && \downarrow^{\mathrlap{\diamond p}}
    \\
    X &\stackrel{\eta_\diamond(X)}{\to}& \diamond X
  }
  \,,
$$

regarded as an object in $\mathcal{C}_{/X}$, and which sends morphisms to the corresponding universal maps between these pullbacks:

$$
  \diamond_{/X}
  \;\;
  \colon
  \;\;
  \left(
   \array{
     E_1 &&\stackrel{\phi}{\to}&& E_2
     \\
     & \searrow && \swarrow
     \\
     && X
   }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
    \array{
      X \underset{\diamond X}{\times} \diamond E_1
      && \stackrel{X \underset{\diamond X}{\times} \diamond \phi}{\to} 
      &&
      X \underset{\diamond X}{\times} \diamond E_2
      \\
      & \searrow && \swarrow
      \\
      && X
    }
  \right)
  \,.
$$

=--

We now want to identify conditions under which $\diamond_{/X}$ is itself a monad. First observe that the [[unit of a monad|unit]]-like map is canonically present.

+-- {: .num_prop #SliceOperatorHasUnit}
###### Proposition

In the situation of def. \ref{InducedOperatorOnSlice}, there is a [[natural transformation]]

$$
  \eta_{\diamond_{/X}} 
  \;\colon\;
  id_{\mathcal{C}_{/X}}
  \to 
  \diamond_{/X}
$$

from the identity on the slice to the induced operator on the slice, whose component over an object $(E \stackrel{p}{\to} X) \in \mathcal{C}_{/X}$ is the universal morphism into the defining [[pullback]] in def. \ref{InducedOperatorOnSlice} induced from the naturality of the $\diamond$-unit $\eta_{\diamond}$:

$$
  \array{
    \eta_{\diamond}(E) \colon
    & E &\stackrel{\sum_{X} \left(\eta_{\diamond_{/X}}\left(p\right)\right) }{\to}& X \underset{\diamond X}{\times} \diamond E 
    &\to&
    \diamond E
    \\
    & &{}_{\mathllap{p}}\searrow& \downarrow^{\mathrlap{\eta_\diamond(X)^\ast \diamond p}} && \downarrow^{\diamond \mathrlap{p}}
    \\
    & && X &\stackrel{\eta_\diamond(X)}{\to}& \diamond X
  }
  \,,
$$

=--

+-- {: .proof}
###### Proof

We have to show that for all morphisms 

$$
  \left(
    \array{
      E_1 &&\stackrel{f}{\to}&& E_2
      \\
      & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
      \\
      && X 
    }
  \right)
$$

in $\mathcal{C}_{/X}$ the induced diagram 

$$
  \array{
     E_1 &\stackrel{\sum_X (\eta_{\diamond_{/X}}(p_1) )}{\to}&
     X \underset{\diamond X}{\times} \diamond E_1
     \\
     \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{X \underset{\diamond X}{\times} \diamond f }}
     \\
     E_2 &\stackrel{\sum_X (\eta_{\diamond_{/X}}(p_2) )}{\to}&
     X \underset{\diamond X}{\times} \diamond E_2
  }
$$

in $\mathcal{C}$ commutes. Inspection of the defining pullback diagram shows that both composites in this diagram constitute [[cones]] over the pullback diagram that defines the bottom right object. Therefore by the [[universal property]] of the pullback they have to coincide.


=--

Next, to have also a product operation on the induced operator $\diamond_{/X}$ we need that $\diamond$ preserves some pullbacks:

+-- {: .num_prop #ProductOnSliceOperator}
###### Proposition

Assume that the monad $\diamond \colon \mathcal{C} \to \mathcal{C}$ preserves [[pullbacks]] over objects in its image. Then for each $X \in \mathcal{C}$ the induced endofunctor $\diamond_{/X}$ of def. \ref{InducedOperatorOnSlice} comes with a [[natural transformation]]

$$
  \mu_{\diamond_{/X}} \;\colon\; \diamond_{/X} \circ \diamond_{/X} \to \diamond_{/X}
$$

whose component on an object $(E \stackrel{p}{\to} X) \in \mathcal{C}_{/X}$ is the pullback of the component $\mu_{\diamond} E$ of the product of $\diamond$ itself over the component $\mu_\diamond X$ along the unit components $\eta_{\diamond} X$.

=--

+-- {: .proof}
###### Proof

First we produce the component map as claimed, then we show that it is indeed the component of a natural transformation.

So for $p \in \mathcal{C}_{/X}$ an object in the slice, consider the defining pullback diagram of $\diamond_{/X} p$ from def. \ref{InducedOperatorOnSlice}

$$
  \array{
    X \underset{\diamond X}{\times} \diamond E 
    &\to&
    \diamond E
    \\
    \downarrow^{\mathrlap{\eta_\diamond(X)^\ast \diamond p}} && \downarrow^{\mathrlap{\diamond p}}
    \\
    X &\stackrel{\eta_\diamond(X)}{\to}& \diamond X
  }
  \,.
$$

By the assumption that $\diamond$ preserves pullback diagrams of this form, application of $\diamond$ yields the pullback diagram

$$
  \array{
    \diamond( X \underset{\diamond X}{\times} \diamond E )
    &\to&
    \diamond \diamond E
    \\
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\diamond \diamond p}}
    \\
    \diamond X &\stackrel{\diamond(\eta_\diamond(X))}{\to}& \diamond \diamond X
  }
  \,.
$$

Pasting to this the pullback of its left vertical morphism along $\eta_\diamond(X)$ yields

$$
  \array{
    X \underset{\diamond X}{\times} \diamond(X \underset{\diamond X}{\times} \diamond E)
    &\to&
    \diamond( X \underset{\diamond X}{\times} \diamond E )
    &\to&
    \diamond \diamond E
    \\
    \downarrow
    &&
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\diamond \diamond p}}
    \\
    X
    &\stackrel{\eta_\diamond X}{\to}&
    \diamond X &\stackrel{\diamond(\eta_\diamond(X))}{\to}& \diamond \diamond X
  }
  \,,
$$

where the total rectangle is also a pullback, by the [[pasting law]]. 

We now build a morphism of [[diagrams]] from the underlying [[cospan]] of this diagram to another cospan, such that the induced map on pullbacks is the component of the natural transformation that we are looking for,

To this end, first paste to the above diagram the [[naturality square]] of the monad multiplication map $\mu_\diamond \colon \diamond \circ \diamond \to \diamond$ to obtain

$$
  \array{
    X \underset{\diamond X}{\times} \diamond(X \underset{\diamond X}{\times} \diamond E)
    &\to&
    \diamond( X \underset{\diamond X}{\times} \diamond E )
    &\to&
    \diamond \diamond E
    \\
    \downarrow
    &&
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\diamond \diamond p}}
    & \searrow^{\mathrlap{\mu_{\diamond}(E)}}
    \\
    X
    &\stackrel{\eta_\diamond X}{\to}&
    \diamond X &\stackrel{\diamond(\eta_\diamond(X))}{\to}& \diamond \diamond X
   && \diamond E
   \\
   && && & \searrow^{\mathrlap{\mu_\diamond X} } & \downarrow^{\mathrlap{\diamond p}}
   \\
   && && && \diamond X
  }
  \,,
$$

Then fill in the commuting diagram that exhibits the [[unitality]] axiom of $\diamond$ to obtain

$$
  \array{
    X \underset{\diamond X}{\times} \diamond(X \underset{\diamond X}{\times} \diamond E)
    &\to&
    \diamond( X \underset{\diamond X}{\times} \diamond E )
    &\to&
    \diamond \diamond E
    \\
    \downarrow
    &&
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\diamond \diamond p}}
    & \searrow^{\mathrlap{\mu_{\diamond}(E)}}
    \\
    X
    &\stackrel{\eta_\diamond X}{\to}&
    \diamond X &\stackrel{\diamond(\eta_\diamond(X))}{\to}& \diamond \diamond X
   && \diamond E
   \\
   && &\searrow^{\mathrlap{id_{\diamond X}}} & & \searrow^{\mathrlap{\mu_\diamond X} } & \downarrow^{\mathrlap{\diamond p}}
   \\
   && && \diamond X &\stackrel{id_{\diamond X}}{\to}& \diamond X
  }
  \,.
$$

Finally paste in an identity square, just as to manifestly exhibit a morphism of diagrams

$$
  \array{
    X \underset{\diamond X}{\times} \diamond(X \underset{\diamond X}{\times} \diamond E)
    &\to&
    \diamond( X \underset{\diamond X}{\times} \diamond E )
    &\to&
    \diamond \diamond E
    \\
    \downarrow
    &&
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\diamond \diamond p}}
    & \searrow^{\mathrlap{\mu_{\diamond}(E)}}
    \\
    X
    &\stackrel{\eta_\diamond X}{\to}&
    \diamond X &\stackrel{\diamond(\eta_\diamond(X))}{\to}& \diamond \diamond X
   && \diamond E
   \\
   &\searrow^{\mathrlap{id_X}}& &\searrow^{\mathrlap{id_{\diamond X}}} & & \searrow^{\mathrlap{\mu_\diamond X} } & \downarrow^{\mathrlap{\diamond p}}
   \\
   && X &\stackrel{\eta_\diamond X}{\to}& \diamond X &\stackrel{id_{\diamond X}}{\to}& \diamond X
  }
  \,.
$$

Now observe that the total front [[cospan]] of morphisms is such that the [[limit]] [[cone]] over it is the [[pullback]] that defines $X \underset{\diamond X}{\times} \diamond E$. By functoriality of [[pullbacks]] (by their universal property), this induces a component morphism

$$
  \mu_{\diamond_{/X}}
  \;\colon\;
  X \underset{\diamond X}{\times} \diamond (X \underset{\diamond}{\times} \diamond E)
  \to
  X \underset{\diamond X}{\times} \diamond E
$$

as claimed.

Since this is built just from universal constructions, the fact that this morphism is indeed [[natural transformation|natural]] follows as in prop. \ref{SliceOperatorHasUnit}.

=--

So far we have constructed from a monad that preserves pullbacks over objects in its image an operator on slices which is equipped with a unit-like and a multiplication-like transformation. We now claim that this yields indeed a monad on the slice.

+-- {: .num_prop #InducedOperatorOnSliceIsMonad}
###### Proposition

For $\diamond \colon \mathcal{C} \to \mathcal{C}$ a [[monad]] which preserves [[pullbacks]] over objects in its image, and for $X \in \mathcal{C}$ any object, the natural transformations

1. $\eta_{\diamond_{/X}} \colon id_{\mathcal{C}_{/X}} \to \diamond_{/X}$ of prop. \ref{SliceOperatorHasUnit}

1. $\mu_{\diamond_{/X}} \colon \diamond_{/X} \circ \diamond_{/X} \to \diamond_{/X}$ from prop. \ref{ProductOnSliceOperator}

constitute the unit and product of a [[monad]] structure $(\diamond_{/X}, \mu_{\diamond_{/X}}, \eta_{\diamond_{/X}})$ on the 
slice operator $\diamond_{/X}$ of def. \ref{InducedOperatorOnSlice}.

If moreover $\diamond$ is [[idempotent monad|idemponent]], then so is $\diamond_{/X}$.

=--

+-- {: .proof}
###### Proof

By forming cospan morphisms and inducing maps between the corresponding pullbacks, this follows from the monad structure $(\diamond, \mu_{\diamond}, \eta_{\diamond})$ by the same arguments as in the proof of prop. \ref{ProductOnSliceOperator}.

=--

+-- {: .num_remark}
###### Remark

If $\diamond$ is an [[idempotent monad]], hence a closure operator, then, by the discussion there, the monad unit exhibits an [[equivalence of categories]] between the objects in the image of $\diamond$ and the $\diamond$-closed objects. 

Therefore in this case the condition that $\diamond$ preserves pullbacks over objects in its image is equivalently that it preserves pullbacks over $\diamond$-closed objects. In this form we will mostly state this condition in the following.

=--

+-- {: .num_prop}
###### Proposition

Let $\diamond \colon \mathcal{C} \to \mathcal{C}$ be an [[idempotent monad]] that preserves pullbacks over $\diamond$-closed objects. Then the closed objects $p \in \mathcal{C}_{/X}$, def. \ref{ClosureAndClosedObjects}, of the induced idempotent monad $\diamond_{/X}$ on the slice over any $X \in \mathcal{C}$ are precisely those objects $(E \stackrel{p}{\to} X)$ for which the naturality square of the $\diamond$-unit is a pullback square in $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

By def. \ref{ClosureAndClosedObjects} we need to show that for $p \in \mathcal{C}_{/X}$ the corresponding component of the $\diamond_{/X}$-unit $\eta_{\diamond_{/X}}(p)$ is an [[isomorphism]] precisely if 

$$
  \array{
    E &\stackrel{\eta_{\diamond} E}{\to}& \diamond E
    \\
    \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{\diamond p}}
    \\
    X &\stackrel{\eta_{\diamond} X}{\to}& \diamond X
  }
$$

is a pullback diagram in $\mathcal{C}$. By prop. \ref{InducedOperatorOnSliceIsMonad} and  prop. \ref{SliceOperatorHasUnit},  the universal map from this diagram, regarded as a [[cone]] over the underlying [[cospan]], to the limiting cone is precisely $\eta_{\diamond_{/X}}(p)$. Hence the claim follows by the universal property of the pullback.

=--

As a special case of def. \ref{ClosureAndClosedObjects} we are therefore now interested in the following.

+-- {: .num_defn}
###### Definition

For $\diamond \colon \mathcal{C} \to \mathcal{C}$ an [[idempotent monad]] which preserves pullbacks over $\diamond$-closed objects, write

$$
  (\mathcal{C}_{/X})_{\diamond_{/X}}
  \hookrightarrow
  \mathcal{C}_{/X}
$$

of the [[full subcategory]] of the [[slice topos]] on the $\diamond_{/X}$-closed objects. 

=--





## Related concepts

* [[universal closure operator]]

* [[modal logic]]

* [[reflective factorization system]], [[stable factorization system]]

[[!redirects closure]]
[[!redirects closures]]

[[!redirects closure operator]]
[[!redirects closure operators]]
[[!redirects closure operation]]
[[!redirects closure operations]]

[[!redirects coclosure operator]]
[[!redirects coclosure operators]]
[[!redirects coclosure operation]]
[[!redirects coclosure operations]]
[[!redirects co-closure operator]]
[[!redirects co-closure operators]]
[[!redirects co-closure operation]]
[[!redirects co-closure operations]]

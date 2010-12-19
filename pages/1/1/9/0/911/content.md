
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For a functor $F : C \to Set$, we may think of $Set$ as the [[classifying space]] of "[[Set]]-bundles;" see [[generalized universal bundle]].  The category of elements of $F$ is, in this sense, the [[Set]]-bundle classified by $F$.  It comes equipped with a projection to $C$ which is a [[Grothendieck fibration|discrete fibration]], and provides an equivalence between presheaves and discrete fibrations.

Forming a category of elements can be thought of as "unpacking" a [[concrete category]]. For example, consider a concrete category $C$ consisting of two objects $X,Y$ and two non-trivial morphisms $f,g$

<img src="http://ncatlab.org/nlab/files/explode.jpg" width = "275"/>

The individual elements of $X,Y$ are "unpacked" and become objects of the new category. The "unpacked" morphisms are inherited in the obvious way from morphisms of $C$.

Note that an "unpacked" category of elements can be "repackaged".

<img src="http://ncatlab.org/nlab/files/implode.jpg" width = "275"/>

The generalization of the category of elements for functors landing in [[Cat]], rather than just $Set$, is called the [[Grothendieck construction]].


## Definition

Given a functor $P:C\to\mathbf{Set}$, the **category of elements** $el(P)$ or $El_P(C)$ (or obvious variations) may be understood in any of these equivalent ways:

* It is the [[category]] whose objects are pairs $(c,x)$ where $c$ is an object in $C$ and $x$ is an element in $P(c)$ and morphisms $(c,x)\to(c',x')$ are morphisms $u:c\to c'$ such that $P(u)(x) = x'$.

* It is the [[pullback]] along $P$ of the [[generalized universal bundle|universal Set-bundle]] $U : Set_* \to Set$

  $$
    \array{ 
       El_P(C) &\to& Set_* 
       \\ 
       \downarrow^{\mathrlap{\pi_P}} && 
       \downarrow^\mathrlap{U} 
       \\ 
       C &\to& Set
     }\,,
   $$
 
   where $U$ is the [[forgetful functor]] from [[pointed set|pointed sets]] to sets.

* It is the [[comma category]] $(*/P)$, where $*$ is the inclusion of the one-point set $*:*\to Set$ and $P:C\to Set$ is itself:

  $$
    \array{ 
       El_P(C) &\to& * 
       \\ 
       \downarrow^{\mathrlap{\pi_P}} &\Downarrow& \downarrow^{\mathrlap{pt}} 
       \\ 
       C &\to& Set
    }
   $$

* Its [[opposite category|opposite]] is the [[comma category]] $(Y/P)$, where $Y$ is the [[Yoneda embedding]] $C^{op}\to [C,Set]$ and $P$ is the functor $*\to [C,Set]$ which picks out $P$ itself:

  $$
    \array{ 
       El_P(C)^{op} &\overset{\pi_P^{op}}{\to}& C^{op} 
       \\ 
       \downarrow &\Downarrow& \downarrow^{\mathrlap{Y}} 
       \\ 
       * & \underset{P}{\to}& [C,Set]
    }
  $$

  $El_P(C)$ is also often written with [[end|coend]] notation as $\int^C P$, $\int^{c: C} P(c)$, or $\int^c P(c)$.  This suggests the fact the set of objects of the category of elements is the [[disjoint union]] (sum) of all of the sets $P(c)$.

When $C$ is a [[concrete category]] and the functor $F:C\to Set$ is simply the [[forgetful functor]], we can define a functor

$$Explode(-) := El_F(-).$$

This is intended to illustrate the concept that constructing a category of elements is like "unpacking" or "exploding" a category into its elements.

## Properties

* The category of elements is naturally equipped with a _projection functor_ $\pi_P:El_P(C) \to C$ given by $(c,x)\mapsto c$ and $u\mapsto u$.  This projection is a [[Grothendieck fibration|discrete opfibration]] and can be viewed also as a $C$-indexed [[family of sets]].


##Examples

### Action Groupoid

Given a [[vector space]] $V$, a group $G$, and a [[representation]] 

$$\rho:\mathbf{BG}\to Vect,$$

denote the image of $\rho$ by

$$V\nearrow G.$$

The [[action groupoid]] $V//G$ is then given by

$$V//G=Explode(V\nearrow G).$$



[[!redirects Exploding a Category]]
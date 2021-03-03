
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

For $C$ any [[category]], there is a [[functor]]

$$
  t : [I,C] \to C
  \,,
$$

from the [[arrow category]] $[I,C] = Arr(C)$ that sends each [[morphism]] $(c_1 \stackrel{f}{\to} c_2) \in [I,C]$ to its codomain $c_2$.

This functor is always an [[Grothendieck fibration|opfibration]]. It corresponds under the [[Grothendieck construction]] to the [[pseudofunctor]]

$$
  C/(-) : C \to Cat
$$

that sends each object $c \in C$ to the [[overcategory]] $C/c$.

If $C$ has all [[pullback]]s, then the functor is in addition a [[Grothendieck fibration|fibration]], hence a [[bifibration]]. 
Traditionally, though, its fibered aspect is emphasised (and it even motivates the notion of cartesianess for categories over categories).  A right adjoint $u_*$ of $u^*$ exists for every morphism $u$ in $C$ iff C is a [[locally cartesian closed category]].

This functor $cod : [I,C] \to C$ is called the **codomain fibration** of $C$.

Some say **basic fibration** or **[[indexed category|self-indexing]]** or the **fundamental fibration** --- anything with so many names must be important! 

If instead of the codomain the domain is used, one obtains the dual notion: [[domain opfibration]].

## Details

We spell out the details of the functor, of its cartesian and opcartesian morphisms and their properties.

### The arrow category

Recall from the discussion at [[arrow category]] that the objects in $Arr(C)$ are morphisms in $C$ and the morphisms $(f:x_1\to x_2)\to (g: y_1\to y_2)$ in $Arr(C)$ are the commutative squares in $C$ of the form 

$$\array{
    x_1 &\stackrel{v}\to& y_1
    \\
    \downarrow\mathrlap{f} 
    &&
   \downarrow\mathrlap{g}
   \\
   x_2 &\stackrel{u}\to& y_2
}$$

with the obvious composition. 

### The functor

The [[functor]] $ cod : Arr(C)\to C$ is given on objects by the codomain (= target) map, and on morphisms it gives the lower arrow of the commutative square. 

$$
  cod : 
  \;\;
  \left(
  \array{
    x_1 &\stackrel{v}\to& y_1
    \\
    \downarrow\mathrlap{f} 
    &&
   \downarrow\mathrlap{g}
   \\
   x_2 &\stackrel{u}\to& y_2
  }
  \right)
  \;\;
  \mapsto
  \;\;
  (x_2 \stackrel{u}\to y_2)
  \,.
$$

If we write $[I,C]$ for the [[arrow category]], where $I$ is the [[interval category]] $I = \{a \to b\}$, then this functor is the [[hom-functor]] applied to the inclusion $\iota_1 : {b} \to \{a \to b\}$

$$
  cod = Hom_\text{Cat}(\iota_1, 1_C) : [I,C] \to [{*}, C] = C
  \,.
$$


### The op-cartesian lifts

That the functor $cod : [I,C] \to C$ is an [[Grothendieck fibration|opfibration]] means that for each object $\hat c_1 \to c_1$ of $[I,C]$, each morphism $c_1 \stackrel{f}{\to} c_2$ in $C$ has a lift to a morphism

$$
  \array{
     \hat c_1 &\to& ??
     \\
     \downarrow && \downarrow
     \\
     c_1 &\to& c_2
  }
$$

in $[I,C]$ that is a [[cartesian morphism|opcartesian morphism]].

Such a lift is given by

$$
  \array{
     \hat c_1 &\stackrel{Id}{\to}& \hat c_1
     \\
     \downarrow && \downarrow
     \\
     c_1 &\to& c_2
  }
  \,.
$$

For given any commuting triangle 

$$
  \array{
     && c_2
     \\
     & \nearrow && \searrow
     \\
     c_1 &&\to&& c_3
  }
$$

in $C$, and any lift

$$
  \array{
    \hat c_1 &\to& d 
    \\
    \downarrow && \downarrow
    \\
    c_1 &\to& c_3
  }
$$

of $c_1 \to c_3$, there is the unique lift

$$
  \array{
    \hat c_1 &\to& d
    \\
    \downarrow && \downarrow
    \\
    c_2 &\to& c_3
  }
$$

such that

$$
  \left(
  \array{
    \hat c_1 &\stackrel{Id}{\to}& \hat c_1
    &\to& d
    \\
    \downarrow && \downarrow && \downarrow
    \\
    c_1 &\to& c_2 &\to& c_3
  }
  \right)
  \;\;\;
  = 
  \;\;\;
  \array{
    \hat c_1 
    &\to& d
    \\
    \downarrow && \downarrow
    \\
    c_1 &\to& c_3
  }  
  \,.
$$

### The cartesian lifts

If $C$ has [[pullback]]s, then $cod : [I,C] \to C$ is in addition a [[Grothendieck fibration|fibered category]] in the sense of Grothendieck:

for every object $\hat c_2 \to c_2$ in $[I,C]$, the cartesian lift of a morphism $c_1 \to c_2$ in $C$ is given by the morphism

$$
  \array{
    c_1 \times_{c_2} \hat c_2 &\to& \hat c_2
    \\
    \downarrow && \downarrow
    \\
    c_1 &\to& c_2
  }
  \,.
$$ 

Because for 

$$
  \array{
     && c_3
     \\
     & \swarrow && \searrow
     \\
     c_1 &&\to&& c_2
  }
$$

any commuting triangle in $C$, and for

$$
  \array{
    d &\to& \hat c_2
    \\
    \downarrow && \downarrow
    \\
    c_3 &\to& c_2
  }
$$

any lift of $c_3 \to c_2$ in $[I,C]$, which by the commutativity of the triangle we may write as

$$
  \array{
    d &\to& &\to& \hat c_2
    \\
    \downarrow && && \downarrow
    \\
    c_3 &\to& c_1 &\to& c_2
  }
$$

there is, precisely by the universal property of the [[pullback]], a unique morphism, $d\to c_1 \times_{c_2} \hat c_2$ in $C$ such that this factors as


$$
  \array{
    d &\to& c_1 \times_{c_2} \hat c_2 &\to& \hat c_2
    \\
    \downarrow && \downarrow && \downarrow
    \\
    c_3 &\to& c_1 &\to& c_2
  }
  \,.
$$

### Direct image operation

Recall that in an  [[Grothendieck fibration|opfibration]] $p : E\to B$ , the _direct image_ $f_!$ of an object $e \in E$ along a morphism $p(e) \to d$ is the codomain $f_!(e)$ of [[generalized the|the]] opcartesian lift $\hat f : e \to f_! e$ of $f$.

By the above discussion this means that in the codomain opfibration $cod : [I,C] \to C$ the direct image of an object $\hat c_1 \to c_1$ in $[I,C]$ along some morphism $f : c_1 \to c_2$ is the composite morphism $\hat c_1 \to c_1 \to c_2$ in $C$, regarded as an object in $[I,C]$: this yields the functor

$$
  f_! : C/{c_1} \to C/{c_2}
$$

of [[overcategory|overcategories]] obained by postcomposition with $f$.


### Inverse image operation

Recall that in an  [[Grothendieck fibration|fibration]] $p : E\to B$ , the _inverse image_ $f^*$ of an object $e \in E$ along a morphism $d \to p(e) $ is the domain $f^*(e)$ of [[generalized the|the]] cartesian lift $\hat f : f^* e \to e$ of $f$.

By the above discussion this means that in the codomain fibration $cod : [I,C] \to C$ the inverse image of an object $\hat c_2 \to c_2$ in $[I,C]$ along some morphism $f : c_1 \to c_2$ is the morphism out of the [[pullback]] $f^* c_2 = c_1 \times_{c_2} \hat c_2 \to c_1$ in $C$, regarded as an object in $[I,C]$: this yields the functor

$$
  C/{c_1} \leftarrow C/{c_2} : f^*
$$

of [[overcategory|overcategories]] obained by pullback.


### Adjointness of direct and inverse image

For every morphism $f : c_1 \to c_2$ in $C$, the direct and inverse image functors are a pair of [[adjoint functor]]s

$$
  f_! : C/{c_1} \to C/{c_2} : f^*
$$

with $f_!$ [[left adjoint]] and $f^*$ [[right adjoint]], $f_! \dashv f^*$.

By the above discussion, the adjunction isomorphism

$$
  Hom_{C_2}(f_! \hat c_1, \hat c_2)
  \simeq
  Hom_{C_1}(\hat c_1, f^*\hat c_2)  
$$

is given by the universal property of the [[pullback]] operation, which says that morphisms

$$
  (f_! \hat c_1 \to \hat c_2)
  =
  \left(
  \array{
    \hat c_1 &\to& \hat c_2
    \\
    \downarrow && \downarrow
    \\
    c_1 &\to& c_2
  }
  \right)
$$

factor uniquely through the [[pullback]]

$$
  \left(
  \array{
    \hat c_1 &\to& c_1 \times_{c_2} \hat c_2 &\to& \hat c_2
    \\
    &\searrow & \downarrow && \downarrow
    \\
    && c_1 &\to& c_2
  }
  \right)
$$

and hence uniquely correspond to morphisms

$$
  (\hat c_1 \to f^* \hat c_2)
  =
  \left(
  \array{
    \hat c_1 &\to& c_1 \times_{c_2} \hat c_2
    \\
    \downarrow && \downarrow
    \\
    c_1 &\to& c_2
  }
  \right)
  \,.
$$

If $C$ is a [[model category]], and $u:c\to d$ a morphism in $C$, we can consider the induced model structure on the overcategories $C/c$, and $C/d$. The adjoint pair

$$
   u_! : C/c \leftrightarrows  C/d : u^*
$$

is then a Quillen pair. 

## Monadic descent

Since the codomain fibration $cod : [I,C] \to C$ is a [[bifibration]] when $C$ has all [[pullback]]s, there is a notion of [[monadic descent]] in this case. Details on this are at [monadic descent for codomain fibrations](http://ncatlab.org/nlab/show/monadic+descent#ForCodomainFibs).

## The Subobject Fibration

By restricting our attention to a subset of arrows in the codomain fibration and using the notion of the [[skeleton of a fibration]], we can define a fibration on a category $\mathcal{C}$ with pullbacks called the *subobject fibration* whose fibers are categories of [[subobjects]] for objects of $\mathcal{C}$. 

Beginning with the codomain fibration $cod:\mathcal{C}^\to\to\mathcal{C}$ on a category $\mathcal{C}$ with pullbacks, we restrict our attention to the subcategory
$$
Mono(\mathcal{C})\subseteq\mathcal{C}^\to,
$$
the full subcategory of $\mathcal{C}^\to$ whose objects are monomorphisms in $\mathcal{C}$, called the **monomorphism category of $\mathcal{C}$**. The resulting functor 
$$
cod:Mono(\mathcal{C})\to\mathcal{C}
$$
is again a fibration since monomorphisms are stable under pullback; we will call this the **monomorphism fibration of $\mathcal{C}$**. The fibers $Mono(\mathcal{C})_X$ for $X\in\mathcal{C}$ are [[thin categories]] since parallel monos in a slice category are equal, but they aren't subobject categories since antisymmetry is only weakly satisfied -- objects with antiparallel arrows between them are necessarily isomorphic, but not necessarily equal. To remedy this, we take the [[fibered skeleton]] of the monomorphism fibration; briefly, we convert it into an [[indexed category]] using the [[Grothendieck construction]], take the [[skeleton]] of each index category, then turn it back into a fibration using the Grothendieck construction in the other direction. The resulting fibration is denoted 
$$
cod:Sub(\mathcal{C})\to\mathcal{C}
$$
and called the **subobject fibration of $\mathcal{C}$**, and the fibers $Sub(\mathcal{C})_X$ are skeletal thin categories, also known as [[poset categories]].

If we take $\mathcal{C}=Set$ then the fibers $Mono(Set)_X$ of the monomorphism fibration are proper classes consisting of all sets isomorphic to subsets of $X$, which isn't what we want. The fibers $Sub(Set)_X$ consist of one representative from each isomorphism class of sets isomorphic to subsets of $X$, and is thusly isomorphic to the powerset of $X$ viewed as a poset. That is, $Sub(Set)_X\cong\mathcal{P}(X)$ as posets, with equality holding if we choose the right representatives.

## In higher category theory

We discuss the codomain fibration in [[higher category theory]].

### In 2-category theory

A categorification in dimension 2  (see [[2-category theory]]) is a codomain 2-fibration, whose main example is $Cat^2$ over $Cat$.

+--{: .query}
[[Mike Shulman]]: I still don't believe that that is a 2-fibration.  How do you lift the 2-cells?

[[David Roberts]]: How does one lift the 2-cells in a 2-fibration anyway? The case of $Cat^\mathbf{2}\to Cat$ (using weak 2-functors in $Cat^\mathbf{2}$) should in my opinion be an guiding example for this. Although, perhaps it would be better to consider (at least at first) the underlying (2,1)-category or even the (2,1)-category $Gpd$.

[[Mike Shulman]]: I think the guiding example of a 2-fibration should actually be $Fib \to Cat$, as in [Hermida's paper](http://www.cs.math.ist.utl.pt/s84.www/cs/claudio/articles/2-fib.ps).  There, you can lift the 2-cells, because in each fibration you can lift the 1-cells.
=--

### In $(\infty,1)$-category theory
 {#InInfinityCategoryTheory}

Let $\mathcal{X}$ be an [[(∞,1)-category]].

+-- {: .num_prop }
###### Proposition

The codomain fibration 

$$
  Cod : \mathcal{X}^I \to \mathcal{X}
$$

is an [[coCartesian fibration]]. 

It is classified under the [[(∞,1)-Grothendieck construction]] by 

$$
  A \mapsto \mathcal{X}_{/A}
  \,,
$$

where on the right we have the [[over-(∞,1)-category]].

=--

This is a special case of ([Lurie, corollary 2.4.7.12](#Lurie)).

For $\mathcal{X}$ an [[(∞,1)-topos]], this is the canonical [[(infinity,2)-sheaf]].

## As a universe

(...)

$\mathbf{H}$ an [[(∞,1)-topos]] the codomain fibration is the [[dependent sum]]

$$
  \sum_{Type} : \mathbf{H}_{/Type} \to \mathbf{H}_{/*} \simeq \mathbf{H}
$$

where $Type \in \mathbf{H}$ is the [[object classifier]], of some size. This is the internal [[universe]]. Since the [[slice (∞,1)-topos]] $\mathbf{H}_{/X}$ is the [[context]] given by $X$, in a precise sense
$\mathbf{H}_{/Type}$ is the "context of the universe". And so this says that the codomain fibration is the "context of the universe" regarded over the base $\infty$-topos which is the "outermost universe".



(...)

## Related concepts

* [[tangent category]]

* [[tangent (infinity,1)-category]]

## References

Secton 2.4.7 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
 {#Lurie}

[[!redirects codomain fibrations]]
[[!redirects codomain opfibration]]
[[!redirects codomain opfibrations]]
[[!redirects self-indexing]]
[[!redirects self-indexing of a category]]
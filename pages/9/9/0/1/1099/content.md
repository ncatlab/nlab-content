
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An _$(\infty,1)$-functor_ is a [[homomorphism]] between [[(∞,1)-categories]]. It generalizes 

* the notion of [[functor]] between [[categories]];

* the notion of [[pseudofunctor]] from a [[category]] to a [[(2,1)-category]];

* the notion of [[2-functor]] between [[(2,1)-categories]];

* the notion of [[n-functor]] between [[(n,r)-category|(n,1)-categories]].

An $(\infty,1)$-functor is _functorial_ (respects [[composition]]) only up to [[coherent]] higher [[homotopies]]. It may be thought of as a **[[homotopy coherent functor]]** or **strongly homotopy functor**.

The collection of all $(\infty,1)$-functors between two $(\infty,1)$-categories form an [[(∞,1)-category of (∞,1)-functors]].

## Definition

The details of the definition depend on the model chosen for
[[(∞,1)-categories]].

1. [[quasi-category]]

1. [[simplicially enriched category]]

1. [[Segal category]]

1. [[complete Segal space]]


### In terms of quasi-categories

+-- {: .un_defn}
###### Definition

For $C$ and $D$ [[quasi-category|quasi-categories]], an **$(\infty,1)$-functor** $F : C \to D$ is simply a morphism of the underlying [[simplicial sets]].

A **natural transformation** $\eta : F \to G$ between two such $(\infty,1)$-functors is a simplicial [[homotopy]]

$$
  \array{
    C
    \\
    {}^{\mathllap{i_0}}\downarrow & \searrow^{\mathrlap{F}}
    \\
    C \times \Delta[1] &\stackrel{\eta}{\to}& D
    \\
    {}^{\mathllap{i_1}}\uparrow & \nearrow_{G}
    \\
    C
  }
  \,.
$$

A **[[modification]]** $\rho$ between natural transformations is an order 2 simplicial homotopy

$$
  \rho : C \times \Delta[2] \to D
  \,.
$$

Generally a **$k$-[[transfor]]** $\phi$ of $(\infty,1)$-functors is a simplicial homotopy of order $k$ between the corresponding quasi-categories

$$
  \phi : C \times \Delta[k] \to D
  \,.
$$

In total, the [[(∞,1)-category of (∞,1)-functors]] between given quasi-categories $C$ and $D$ is the simplicial function complex

$$
  (\infty,1)Cat(C,D) :=
  sSet(C,D)
  :=
  \int^{k \in \Delta} \Delta[k] \cdot Hom_{sSet}(C \times \Delta[k], D)
$$

as computed by the canonical [[sSet]]-[[enriched category|enrichment]] of $sSet$ itself.

=--

This serves to define the [[(∞,1)-category of (∞,1)-functors]].


## Examples

### $\infty$-Pseudo-functors / homotopy presheaves

Let $C$ be an ordinary [[category]]. The above definition in particular serves to generalize the notion of a [[pseudofunctor]] (functor up to homotopy)

$$
  F : C^{op} \to Grpd
$$

with values in the [[2-category]] [[Grpd]] as it appears in the theory of [[stack]]s/[[2-sheaves]]:

let $KanCplx \subset sSet$ be the [[full subcategory]] of [[sSet]] on the [[Kan complex]]es. This is naturally a [[simplicially enriched category]]. Write $N(\mathbf{KanCplx})$ for the [[homotopy coherent nerve]] of this simplicially enriched category. This is the [[quasi-category]]-incarnaton of [[∞Grpd]].

Write $N(C^{op})$ for the ordinary [[nerve]] of the ordinary category $C^{op}$ (passing to the [[opposite category]] is just a convention here, with no effect on the substance of the statement). Then an **$\infty$-pseudofunctor** or **[[(∞,1)-presheaf]]** or **homotopy presheaf** on $C$ is a morphism of simplicial sets

$$
  F : N(C^{op}) \to N(\mathbf{KanCplx})
  \,.
$$

One sees easily in low degrees that this does look like the a [[pseudofunctor]] there:

1. the 1-cells of $N(C)$ are just the [[morphism]]s in $C$, so that on 1-cells we have that $F$ is an assignment

   $$
     F : (x \stackrel{f}{\leftarrow} y) \mapsto (F(x) \stackrel{F(f)}{\to} F(y)
   $$

   of morphisms in $C$ to morphisms in $KanCplx$, as befits a functor;

1. the 2-cells of $N(C)$ are pairs of composable morphisms, so that on 2-cells we have that $F$ is an assignment

   $$
     F : 
     \left(
       \array{
          && y
          \\
          & {}^{\mathllap{g}}\swarrow 
          & & \nwarrow^{\mathrlap{f}}
          \\
          x &&\stackrel{g \circ f}{\leftarrow}&& z
       }
     \right)
     \;\;
     \mapsto
     \;\;
     \left(
       \array{
          && F(y)
          \\
          & {}^{\mathllap{F(g)}}\nearrow 
          & \Downarrow^{\mathrlap{F(f,g)}} & 
          \searrow^{\mathrlap{F(f)}}
          \\
          F(x) &&\stackrel{F(g \circ f)}{\rightarrow}&& F(z)
       }
     \right)     
   $$ 

   which means that $F$ does not necessarily respect the [[composition]] of morphisms, but instead does introduce [[homotopies]] $F(f,g)$ for very pairs of composable morphisms, which measure how $F(g)\circ F(f)$ differs from $F(g \circ f)$. These are precisely the homotopies that one sees also in an ordinary [[pseudofunctor]]. But for our $(\infty,1)$-functor there are now also higher and higher homotopies:

1. the 3-cells of $N(C)$ are triples of composable morphisms $(f,g,h)$ in $C$. They are sent by $F$ to a tetrahedron that consists of a homotopy-of-homotopies from the $F(f,g) \cdot F( h , g\circ f )$ to $F(g, h) \cdot F(f , h \circ g)$;

1. and so on.

For more see [[(∞,1)-presheaf]].

## Properties

It turns out that every $(\infty,1)$-functor $C \to \infty Grpd$ can be **rectified** to an _ordinary ([[sSet]]-[[enriched functor|enriched]]) functor_ with values in [[Kan complex]]es.


+-- {: .un_theorem}
###### Theorem

For $C = N(\mathbf{C})$ a quasi-category given as the [[homotopy coherent nerve]] of a Kan-complex enriched category $\mathbf{C}$ (which may for instance be just an ordinary 1-category), write 

$$
  [\mathbf{C}^{op}, \mathbf{sSet}]
$$

for the [[sSet]]-[[enriched category]] of _ordinary_ ($sSet$-[[enriched functor|enriched]]) functors (respecting composition strictly).

Then: every $(\infty,1)$-functor $N(\mathbf{C}^{op}) \to \infty Grpd$ is equivalent to a strictly composition respecting functor of this sort. Precisely: write $[\mathbf{C}^{op}, \mathbf{sSet}]^\circ$ for the full $\mathbf{sSet}$-enriched subcategory on those strict functors that are fibrant and cofibrant in a [[model structure on simplicial presheaves]] on $\mathbf{C}$. Then we have an [[equivalence of quasi-categories|equivalence]] of [[(∞,1)-categories]]

$$
  Hom_{(\infty,1)Cat}(N(\mathbf{C}^{op}), \infty Grpd)
  \simeq
  N([\mathbf{C}^{op}, \mathbf{sSet}]^\circ)
  \,.
$$

=--

More on this is at [[(∞,1)-category of (∞,1)-presheaves]].

## Related concepts

* [[function]]

* [[functor]]

* [[2-functor]] / [[pseudofunctor]] / [[(2,1)-functor]]

  * [[monoidal functor]]

* [[n-functor]]

* **(∞,1)-functor**

  * [[monoidal (∞,1)-functor]]

  * [[adjoint (∞,1)-functor]], [[(∞,1)-monad]]

* [[(∞,n)-functor]]


[[!include properties of functors -- contents]]



## References

section 1.2.7 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

discusses morphisms of [[quasi-category|quasi-categories]].

[[!redirects (infinity,1)-functors]]
[[!redirects (∞,1)-functor]]
[[!redirects (∞,1)-functors]]


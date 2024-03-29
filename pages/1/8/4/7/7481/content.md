
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Internal category theory
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notions of _[[presheaf]]_, _[[site]]_ and _[[sheaf]]_ can be formulated [[internalization|internal]] to any [[topos]]. The ordinary such notions are recovered by internalization into [[Set]].

More precisely, the direct internalization of these notions is into the [[universe enlargement|very large]] [[2-topos]] $\hat Sh_2(\mathcal{S},can)$ of the given ambient topos $\mathcal{S}$, since an internal presheaf is to be an $\mathcal{S}$-valued internal functor, but $\mathcal{S}$ does not quite sit inside itself. It does, however, sit inside $\hat Sh_2(\mathcal{S},can)$, incarnated as the [[2-sheaf]] $\bar \mathcal{S}$ corresponding to its [[codomain fibration]].

Therefore, regarding $\hat Sh_2(\mathcal{S}, can)$ as the [[2-category]] of [[internal categories]] in $\mathcal{S}$, an [[internal site]] in $\mathcal{S}$ is an object $\bar \mathbb{C}$ of $\hat Sh_2(\mathcal{S}, can)$ and an internal presheaf is a morphism $F : \bar \mathbb{C}^{op} \to \bar \mathcal{S}$.

## Definition

While it is straightforward to define an [[internal site]], hence the [[domain]] of an internal (pre)sheaf, the definition of the codomain is slightly more subtle, for that needs to be a copy of the ambient [[universe]] internalized into itself. One way to naturally say this is by passing to the _external_ [[2-sheaves]] [[2-topos]]. This version of the definition we state in 

* _[In terms of external 2-sheaves](#InTermsOf2Sheaves)_.

But the resulting notion can of course be expressed entirely in terms of data in the ambient topos. This we spell out in 

* _[Explicit definition](#ExplicitDefinition)_.

### In terms of external 2-sheaves
 {#InTermsOf2Sheaves}

Let  $\mathcal{S}$ be a [[topos]] and let $\mathbb{C}$ be an [[internal category]] in $\mathcal{S}$:

$$
  \mathbb{C} = 
  \left(
    C_1 \stackrel{\overset{s}{\to}}{\underset{t}{\to}}
    C_0
  \right)
  \in \mathcal{S}
  \,.
$$

+-- {: .num_defn }
###### Definition

Write $\bar \mathbb{C}$ for the [[2-sheaf]] on $\mathcal{S}$

$$
  \bar \mathbb{C} : \mathcal{S}^{op} \to Cat
$$

that is [[representable functor|represented]] by $\mathbb{C}$. More explicitly, this is the [[pseudofunctor]] which to an [[object]] $X \in \mathcal{S}$ assigns

$$
  \bar \mathbb{C} : X 
    \mapsto 
  \left(
    \mathcal{S}(X,C_1)
    \stackrel{\overset{\mathcal{S}(X,s)}{\to}}{\underset{\mathcal{S}(X,t)}{\to}}
    \mathcal{S}(X,C_0)
  \right)
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

Write 

$$
  \bar \mathcal{S} : \mathcal{S}^{op} \to Cat
$$

for the [[2-sheaf]] that [[Grothendieck construction|classifies]] the [[codomain fibration]] of $\mathcal{S}$, the [[pseudofunctor]] which sends an object to the corresponding [[slice topos]] and morphisms to [[base change]]

$$
  \bar \mathcal{S} : X \mapsto \mathcal{S}_{/X}
$$

(also called the "[[indexed category|self-indexing]] of $\mathcal{S}$").

=--

+-- {: .num_remark }
###### Remark

This is the incarnation of $\mathcal{S}$ itself, regard internal to its [[2-sheaf]] [[2-topos]] $\hat Sh_{2}(\mathcal{T}, can)$.

=--

+-- {: .num_defn }
###### Definition

An **internal presheaf** on $\mathbb{C}$ (internal to $\mathcal{T}$) is a morphism

$$
  F : \bar \mathbb{C}^{op} \to \bar \mathcal{S}
$$

of [[2-sheaves]] on $\mathcal{S}$. (Also called an "[[indexed functor]]" between [[indexed categories]]".)

Suppose moreover that $\mathbb{C}$ is equipped with the structure of an [[internal site]]. Then $F$ above is an **internal sheaf** on $\mathbb{C}$ if it satisfies the evident [[descent]] condition.

A [[morphism]] of internal presheaves is simply a [[2-morphism]] in $\hat Sh_2(\mathcal{S}, can)$ (also called an "[[indexed functor|indexed natural transformation]]"). This yields a [[category]]

$$
  PSh(\mathbb{C})
$$

of internal presheaves. Accordingly we have the 
[[full subcategory]]

$$
  Sh(\mathbb{C}, \mathcal{S})
  \hookrightarrow PSh(\mathbb{C}, \mathcal{S})
$$

of internal sheaves.

=--

### Explicit definition
 {#ExplicitDefinition}

We unwind what the above amounts to more explicitly.

Let $(\mathbb{C},J)$ be an [[internal site]] in $\mathcal{S}$, i.e. an [[internal category]] $\mathbb{C}$ equipped with an internal [[coverage]] $J$. Let $\mathcal{S}^{\mathbb{C}^{op}}$ be the topos of [[internal diagram|internal diagrams]] on $\mathbb{C}^{op}$.

+-- {: .num_defn }
###### Definition

1. An **internal presheaf** on $\mathbb{C}$ is an internal diagram $F \in \mathcal{S}^{\mathbb{C}^{op}}$.

1. An **internal sheaf** on $\mathbb{C}$ (with respect to $J$) is an internal presheaf on $\mathbb{C}$ satisfying one of the following equivalent conditions:
    1. $F$ satisfies the [usual sheaf condition](/nlab/show/sheaf#GeneralComponentwiseDefinition) interpreted in the [[internal language]] of $\mathcal{S}$.
    1. $F$ is a $j$-sheaf for the [[Lawvere-Tierney topology]] on $\mathcal{S}^{\mathbb{C}^{op}}$ induced by $J$.
(The equivalence is because the usual proof for $\mathcal{S} = $[[Set]] is constructive and can thus be internalized in an arbitrary topos.)

=--

## Properties

Let $\mathcal{S}$ and $\mathbb{C}$ be as above.

+-- {: .num_prop }
###### Proposition

The category of internal presheaves $PSh(\mathbb{C}, \mathcal{S})$ is a [[topos]].

=--

This appears as ([Johnstone, cor. B.2.3.17](#Johnstone)).

+-- {: .num_prop }
###### Proposition

Let $f : \mathbb{C} \to \mathbb{D}$ be an [[internal functor]]. Write $\bar f : \bar \mathbb{C} \to \bar \mathbb{D}$ for the corresponding morphism in $\hat Sh_2(\mathcal{S}, can)$. Precomposition with this morphism induces a [[functor]] of internal presheaf catgeories

$$
  f^* \colon PSh(\mathbb{D}, \mathcal{S}) 
    \to 
   PSh(\mathbb{C}, \mathcal{S})
  \,.
$$

This is the [[inverse image]] of a [[geometric morphism]] of [[toposes]]

$$
  f \colon PSh(\mathbb{C}, \mathcal{S})
   \to 
  PSh(\mathbb{D}, \mathcal{S})
  \,.
$$

=--

This appears as ([Johnstone, cor. B.2.3.22](#Johnstone)).


The global section functors of internal sheaf toposes in $\mathcal{S}$ are [[bounded geometric morphisms]] over $\mathcal{S}$.


## Related concepts

* [[internal diagram]]

## References

On internal presheaves in [[elementary toposes]]:

* [[Marta Bunge]], *Internal Presheaf Toposes*, [[Cahiers,Cahiers de topologie et géométrie différentielle catégoriques]] **18** 3 (1977) 291-330 &lbrack;[numdam:CTGDC_1977__18_3_291_0](http://www.numdam.org/item/?id=CTGDC_1977__18_3_291_0)&rbrack;

On internal presheaves in a [[Grothendieck toposes]]:

* [[Saunders MacLane]], [[Ieke Moerdijk]], Section V.7 of _[[Sheaves in Geometry and Logic]]_ (1992)

and in section B2.3 of

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 

In these references internal presheaves are introduced in components as in the [explicit definition](#ExplicitDefinition) above. The equivalence to the [abstract formulation](#InTermsOf2Sheaves) above, in terms of morphisms between 2-sheaves, follows for instance with ([Johnstone, lemma B.2.3.13](#Johnstone)).

category: sheaf theory
[[!redirects internal sheaves]]
[[!redirects internal presheaf]]
[[!redirects internal presheaves]]
[[!redirects category of internal sheaves]]
[[!redirects category of internal presheaves]]
[[!redirects categories of internal sheaves]]
[[!redirects categories of internal presheaves]]
[[!redirects internal presheaf topos]]
[[!redirects internal sheaf topos]]

[[!redirects internal presheaf toposes]]
[[!redirects internal sheaf toposes]]
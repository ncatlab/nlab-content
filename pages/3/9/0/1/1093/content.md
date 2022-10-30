
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

This entry is about the properties and the characterization of the category $Sh(S)$ of ([[set]]-valued) [[sheaf|sheaves]] on a ([[small category|small]]) [[site]] $S$, which is a [[Grothendieck topos]].  Among other things it gives a definition and a characterization of the notion of [[sheaf]] itself, but for more details on [[sheaf|sheaves]] themselves see there. 

## Definition

Let $(C,J)$ be a [[site]]: a (small) [[category]] equipped with a [[coverage]].

+-- {: .num_defn}
###### Definition

The **category of sheaves** on $(C,J)$ is the [[full subcategory]] of the [[category of presheaves]] 

$$
  i : Sh_J(C) \hookrightarrow
  PSh(C)
$$

on those presheaves which are [[sheaves]] with respect to $J$.

=--

+-- {: .num_prop}
###### Proposition

Every category of sheaves is a [[reflective subcategory]]

$$
  (L \dashv i) : Sh_J(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  Psh(C)
  \,,
$$

hence a [[subtopos]] of the [[presheaf topos]].  Moreover, every such subtopos arises in this way: there is a [[bijection]] between [[Grothendieck topologies]] on $C$ and equivalence classes of [[geometric embeddings]] into $PSh(C)$.

=--

This appears for instance as ([Johnstone, corollary 2.1.11](#Johnstone)).  See also [[Lawvere-Tierney topology]].

+-- {: .proof}
###### Proof

Details on the first statement are at [[sheafification]]. A full proof for the second statement is at [[(∞,1)-category of (∞,1)-sheaves]] (there proven in [[(∞,1)-category theory]], but the proof is verbatim the same in [[category theory]]).


=--



## Equivalent characterizations


### As localizations

+-- {: .num_prop}
###### Proposition

The category of sheaves is equivalent to the [[homotopy category]] of the [[category with weak equivalences]] $PSh(C)$ with the weak equivalences given by $W = $[[local isomorphisms]]

$$
  Sh(S) \simeq Ho_{PSh(S)} = PSh(C)[local isomorphisms]^{-1}
  \,.
$$

The converse is also true: for every [[left exact functor]] $L : PSh(S) \to PSh(S)$ (preserving finite limits) which is [[adjoint functor|left adjoint]] to the inclusion of its image, there is a Grothendieck topology on $S$ such that the image of $L$ is the category of sheaves on $S$ with respect to that topology.

=--

We spell out proofs of some of the above claims.

Let $C$ be a [[small category]] and 

$$
  i : \mathcal{E} \hookrightarrow [C^{op}, Set]
$$ 

a [[reflective subcategory]], hence a [[full subcategory]] with a [[left adjoint]] $L : [C^{op}, Set] \to \mathcal{E}$, such that moreover $L$ preserves [[finite limit]]s.

Write $W := L^{-1}(isos) \subset Mor([C^{op}, Set])$ for the [[class]] of [[morphism]]s in $[C^{op}, Set]$ that are sent to [[isomorphism]]s by $L$.

+-- {: .num_prop #CharacterizationOfLocalObjects}
###### Proposition

A [[presheaf]] $A \in [C^{op}, Set]$ is in $\mathcal{E}$ (meaning: in the [[essential image]] of $i$) precisely if for all $f : X \to Y$ in $W$ the induced function

$$
  Hom(f,A) : Hom(Y,A) \to Hom(X,A)
$$

is a [[bijection]].

=--

+-- {: .proof}
###### Proof


If $A \simeq i \hat A$, then by the $(L \dashv i)$-[[adjunction]] [[isomorphism]] we have

$$
  Hom(f, i \hat A) \simeq \mathcal{E}(L(f), A)
  \,.
$$

But by assumption $L(f)$ is an [[isomorphism]], so the claim is immediate.

Conversely, if for all $f$ the function $Hom(f,A)$ is a bijection, define $\hat A := L(A)$ and let $ \epsilon_A : A \to i L(A)$ be the 
$(L \dashv i)$-[[unit of an adjunction|unit]]. 

By the assumption that $i$ is a [[full and faithful functor]] and basic properties of [[adjoint functor]]s we habe that the counit

$$
  L i \to Id
$$

is a [[natural isomorphism]]. By the [[zig-zag law]] the composite

$$
  L A \stackrel{L \epsilon_A}{\to} L i L A \stackrel{\simeq}{\to} L A
$$

is the [[identity]] and therefore $L \epsilon$ is an [[isomorphism]] and so $\epsilon_A$ is in $W$, under our assumption on $A$.

Using this it follows that 

$$
  Hom(\epsilon_A, A) : Hom(i L A, A) \stackrel{\simeq}{\to} Hom(A,A)
$$

is an [[isomorphism]]. Write $k_A : i L A \to A$ for the preimage of $id_A$ under this isomorphism, which is therefore a [[left inverse]] of $\epsilon_A$. This immediately implies that also $k_A$ is in $W$, and so we can enter the same argument with $k_A$ to find that it has a left inverse itself. But this means that $k_A$ is in fact an [[isomorphism]] and hence so is $\epsilon A$, which thus exhibits $A$ as being in the essential image of $i$.

=--

+-- {: .num_prop #WeakEquivalencesDetectedOnRepresentableCodomains}
###### Proposition

A [[morphism]] $f : X \to Y$ is in $W$ precisely if for every morphism $z : j(c) \to Y$ with [[representable functor|representable]] [[domain]], the [[pullback]] $z^* f$ in 

$$
  \array{
     X \times_Y j(c) &\to& X
     \\  
     {}^{\mathllap{z^* f}}\downarrow && \downarrow^{\mathrlap{f}}
     \\
     j(c) &\stackrel{z}{\to}& Y
  }
$$

is in $W$.

=--

+-- {: .proof}
###### Proof

Assume first that $f$ is in $W$. Since by assumption $L$ preserves finite limits, it follows that 

$$
  \array{
     L(X \times_Y j(c)) &\to& L X
     \\  
     {}^{\mathllap{L(z^* f)}}\downarrow && \downarrow^{\mathrlap{L f}}
     \\
     L(j(c)) &\stackrel{L z}{\to}& L Y
  }
$$

is still a [[pullback]] diagram in $\mathcal{E}$ and hence that $L(z^* f)$ is the pullback of the [[isomorphism]] $L f$ and thus itself an isomorphism. Therefore $z^* f$ is in $W$.

Conversely, suppose that all these pullbacks are in $W$. Then use the "[[co-Yoneda lemma]]" to write the presheaf $Y$ as a [[colimit]] over all representables mapping into it

$$
  {\lim_\to}_{j(c_i) \stackrel{z_i}{\to} Y} j(c)  \stackrel{\simeq}{\to} Y
  \,.
$$

Forming the [[pullback]] along $f$, using that in a [[topos]] (such as our [[presheaf topos]]) colimits are preserved by pullbacks, we get

$$
  \array{
    {\lim_\to}_i f^* j(c_i) &\stackrel{\simeq}{\to}& X
    \\   
    {}^{\mathllap{{\lim_\to}_i z_i^* f}}\downarrow && \downarrow^{\mathrlap{f}}
    \\   
    {\lim_\to}_i j(c_i)
    &\stackrel{\simeq}{\to}&
    Y
  }
  \,.
$$

Since $L$ preserves all colimits and finite limits, we also get

$$
  \array{
    {\lim_\to}_i L(f^* j(c_i)) &\stackrel{\simeq}{\to}& L(X)
    \\   
    {}^{\mathllap{{\lim_\to}_i L(z_i^* f)}}\downarrow && \downarrow^{\mathrlap{L(f)}}
    \\   
    {\lim_\to}_i L(j(c_i))
    &\stackrel{\simeq}{\to}&
    L(Y)
  }
  \,.
$$

Since by assumption now all $L(z_i^* f )$ are isomorphisms, also ${\lim_\to}_i L(z_i^* f) $ is an isomorphism and hence three sides of the above square are isomorphisms. Therefore also $L(f)$ is and hence $f$ is in $W$.

=--

+-- {: .num_prop #LocalizationInducesGrothendieckTopology}
###### Proposition

The collection of [[sieve]]s in $W$, hence the collection of [[monomorphism]]s in $W$ whose [[codomain]] is a [[representable functor|representable]], constitute a [[Grothendieck topology]] on $C$.

=--

+-- {: .proof}
###### Proof

We check the list of axioms, given at [[Grothendieck topology]]:

1. _Pullbacks of covering sieves are covering_ : 

   First of all, the pullback of a sieve along a morphism of representables is still a sieve, because [[monomorphism]]s are (as discussed there) stable under pullback.

   Next, since $L$ preserves [[finite limit]]s, $L$ applied to the pullback sieve is the pullback of an isomorphism, hence is an isomorphism, hence the pullback sieve is in $W$.

1. _The maximal sieve is covering._ Clear: $L$ applied to an [[isomorphism]] is an [[isomorphism]].

1. _Two sieves cover precisely if their intersection covers._ This is again due to the [[pullback]]-stability of elements of $W$, due to the preservation of finite limits by $L$.

1. _If all pullbacks of a sieve along morphisms of a covering sieve are covering, then the original sieve was covering_ .

   This is the same argument as in the second part of the proof of
   prop. \ref{WeakEquivalencesDetectedOnRepresentableCodomains}.

=--

+-- {: .num_prop}
###### Proposition

$\mathcal{E}$ is a [[Grothendieck topos]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{LocalizationInducesGrothendieckTopology} and
prop. \ref{CharacterizationOfLocalObjects} we are reduced to showing that an object $A$ is in $\mathcal{E}$ already if for all _[[monomorphisms]]_ $f$ in $W$ the function $Hom(f,A)$ is a bijection.

(...)

=--



### As toposes
 {#AsToposes}

Categories of sheaves are examples of [[categories]] that are [[topos]]es: they are the [[Grothendieck topos]]es characterized among all toposes as those satisfying [[Grothendieck topos|Giraud's axioms]].

+-- {: .num_prop}
###### Proposition

[[Grothendieck topos|Sheaf toposes]] are equivalently the [[geometric embedding|subtoposes]] of [[presheaf toposes]].

=--

This appears for instance as 
([Johnstone, corollary 2.1.11](#Johnstone)).


### As accessible reflective subcategories
 {#AsAccessibleReflectiveSubcategories}

+-- {: .num_prop}
###### Proposition

[[sheaf topos|Sheaf toposes]] are equivalently the [accessible reflective subcategories](reflective+subcategory#AccessibleReflectiveSubcategories) of [[categories of presheaves]].

=--

See at _[[reflective sub-(∞,1)-category]]_.


## Properties

### Dependence on the site

+-- {: .num_prop}
###### Definition

For $(L \dashv i) : \mathcal{E} \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}$ a category of sheaves and $(C,J)$ a [[site]] such that we have an equivalence of categories $\mathcal{E} \simeq Sh_J(C)$ we say that $C$ is a **site of definition** for the [[topos]] $\mathcal{E}$.

=--

+-- {: .num_remark}
###### Remark

There are always different [[site]]s $(C,J)$ whose categories of sheaves are [[equivalence of categories|equivalent]]. First of all for fixed $C$ and given a [[coverage]] $J$, the category of sheaves depends only on the [[Grothendieck topology]] generated by $J$. But there may be site structures also on inequivalent categories $C$ that have equivalent categories of sheaves.

=--

+-- {: .num_defn #InducedCoverage}
###### Definition

For $(C,J)$ a [[site]] with [[coverage]] $J$ and $D \to C$ any [[subcategory]], the **induced coverage** $J_D$ on $D$ has as [[covering]] [[sieve]]s the intersections of the covering sieves of $C$ with the morphisms in $D$.

=--

+-- {: .num_defn #DenseSubSite}
###### Definition

Let $(C,J)$ be a [[site]] (possibly [[large site|large]]). A [[subcategory]] $D \to C$ (not necessarily full) is called a **[[dense sub-site]]** with the [induced coverage](#InducedCoverage) $J_D$ if

1. every object $U \in C$ has a [[covering]] $\{U_i \to U\}$ in $J$ with all $U_i$ in $D$;

1. for every morphism $f : U \to d$ in $C$ with $d \in D$ there is a [[covering]] family $\{f_i : U_i \to U\}$ such that the composites $f \circ f_i$ are in $D$.

=--

+-- {: .num_remark}
###### Remark

If $D$ is a [[full subcategory]] then the second condition is automatic.

=--

+-- {: .num_theorem}
###### Theorem
**(comparison lemma)**

Let $(C,J)$ be a (possibly [[large site|large]]) [[site]] with $C$ a [[locally small category]] and let $f : D \to C$ be a [[small category|small]] [dense sub-site](#DenseSubSite). Then pair of [[adjoint functor]]s

$$
  (f^* \dashv f_*) 
    : 
  PSh(D)
    \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}  
   PSh(C)
$$

with $f^*$ given by precomposition with $f$ and $f_*$ given by right [[Kan extension]] induces an [[equivalence of categories]] between the categories of sheaves

$$
  (f_* \dashv f^*) : 
  Sh_{J_D}(D)
  \underoverset
    {\underset{f_*}{\to}}{\overset{f^*}
    {\leftarrow}}
    {\simeq}
  Sh_J{C}
  \,.
$$


=--

This appears as ([Johnstone, theorm C2.2.3](#Johnstone)).

+-- {: .num_example}
###### Examples


* Let $X$ be a [[locale]] with [[frame]] $Op(X)$ regarded as a site with the canonical coverage (\{U_i \to U\} covers if the [[join]] of the $U_i$ us $U$). Let $bOp(X)$ be a [[basis for the topology]] of $X$: a complete join-[[semilattice]] such that every object of $Op(X)$ is the [[join]] of objects of $bOp(X)$. Then $bOp(X)$ is a dense sub-site.

  * For $X$ a [[locally contractible space]], $Op(X)$ its [[category of open subsets]] and $cOp(X)$ the full subcategory of [[contractible]] open subsets, we have that $cOp(X)$ is a dense sub-site.

* For $C = TopManifold$  the category of all [[paracompact topological space|paracompact]] [[topological manifold]]s equipped with the [[open cover]] coverage, the category [[CartSp]]${}_{top}$ is a dense sub-site: every paracompact manifold has a [[good open cover]] by [[open balls]] [[homeomorphic]] to a [[Cartesian space]].

* Similaryl for $C = $ [[Diff]] the category of [[smooth manifold]]s equipped with the [[good open cover]] [[coverage]], the full subcategory [[CartSp]]${}_{smooth}$ is a dense sub-site.

=--


### Epi- mono- and isomorphisms
 {#EpiMonoIsomorphisms}


Let $Sh(C)$ be a category of sheaves.

+-- {: .num_prop}
###### Proposition

A morphism $f : X \to Y$ is a [[monomorphism]] if it is a monomorphism of [[presheaves]], that is if for each $U \in C$ the [[function]] $f(U) : X(U) \to Y(U)$ is [[injective]].

=--


+-- {: .num_prop}
###### Proposition

A morphism $f : X \to Y$ in $Sh(C)$ is an [[epimorphism]] precisely if it is **locally surjective** in the sense that:

for all $U \in C$ there is a [[covering]] $\{p_i : U_i \to U\}_{i \in I}$ such that for all $i \in I$ and every element $y \in Y(U)$ the element $f(p_i)(y)$ is in the image of $f(U_i) : X(U_i) \to Y(U_i)$.


=--


### Exactness properties

Every sheaf topos satisfies the following [[exactness properties]]. it is an 

* [[extensive category]];

* [[adhesive category]];

* [[exhaustive category]].

## Related concepts

* **category of sheaves**

* [[(∞,1)-category of (∞,1)-sheaves]].


[[!include locally presentable categories - table]]


## References

Secton A.4 and C.2 in

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_ .
 {#Johnstone}


The characterization of sheaf toposes and Grothendieck topologies in terms of left exact [[reflective subcategory|reflective subcategories]] of a presheaf category is also in

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

where it is implied by the combination of Corollary VII 4.7 and theorem V.4.1.


The characterization of $Sh(S)$ as the [[homotopy category]] of $PSh(S)$ with respect to local isomorphisms is emphasized at the beginning of the text

* [[Bertrand Toen]], _Stacks and non-abelian cohomology_ ([web](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html)) .

Details are in 

* Kashiwara-Schapira, _[[Categories and Sheaves]]_ .

It's a bit odd that the full final statement does not seem to be stated there explicitly, but all the ingredients are discussed:

* exercise 16.7 shows that [[sheafification]] inverts precisely the [[local isomorphism]]s, so that in particular every [[local isomorphism]] between [[sheaf|sheaves]] is an [[isomorphism]];

* lemma 16.3.2 states that the unit of the [[adjoint functor|adjunction]] $Id_{PSh(S)} \rightarrow i \circ \bar{(-)} : PSh(S) \to PSh(S)$ is componentwise a [[local isomorphism]];

* using this corollary 7.2.2 says that $Sh(S) \simeq Ho_{PSh(S)}$ with the [[homotopy category]] $Ho_{PSh(S)}$ formed using [[local isomorphism]]s as weak equivalences.



[[!redirects sheaf category]]
[[!redirects categories of sheaves]]
[[!redirects topos of sheaves]]
[[!redirects topoi of sheaves]]
[[!redirects toposes of sheaves]]

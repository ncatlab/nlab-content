
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

A _site_ is a [[small category]] equipped with a [[coverage]] or [[Grothendieck topology]]. The [[category of sheaves]] is a [[sheaf topos]] and the site is a _site of definition_ for this topos.

## Definition 

+-- {: .un_defn}
###### Definition

A _site_ is a category $C$ equipped with a [[Grothendieck topology]] $J$.

=--

+-- {: .un_defn}
###### Definition

Sometimes it is useful to define a site to be a category equipped merely with a [[coverage]]. This does generate a Grothendieck topology, but many constructions are more elegantly carried out just with the coverage.

Notice also that there are many equivalent ways to define a [[Grothendieck topology]], for instance in terms of a system of [[local isomorphisms]], or in terms of a system of [[dense monomorphisms]] in the [[presheaf]] category $PSh(S)$.

=--

+-- {: .un_defn}
###### Definition


A **morphism of sites** $f : (C,J) \to (D,K)$ is 

* a [[functor]] $f : C \to D$;

* such that 

  * $f$ preserves covers in that for every $U \in C$ and every [[covering]] $\{p_i : U_i \to U\}$ on $U$, the images $f(p_i)$ cover $f(U)$.

  * $f$ is a [[flat functor]];

=--


Equivalently this means that the [[Yoneda extension]] $\hat f^t : [S_Y^\op, Set] \to [S_X^{op}, Set]$ (of $Y_X \circ f^t : S_Y \to [S_X^{op}, Set]$) sends [[local isomorphisms]] to local isomorphisms.


For $f : X \to Y$ a morphisms of sites, coming from a functor $f^t : S_Y \to S_X$, we have the induced [[inverse image]] functor 

$$
  f^{*} : Sh(Y) \to Sh(X)
  \,.
$$

as well as the[[direct image]] functor 

$$
  f_* : Sh(X) \to Sh(Y)
$$


+-- {: .un_prop}
###### Proposition

For $f : X \to Y$ a morphism of sites, the direct and inverse image functors give a [[geometric morphism]] between the corresponding [[category of sheaves|sheaf]] [[topos]]es in that they restrict to an [[adjunction]] 

$$
  (f_* \dashv f^*) : Sh(X) \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} Sh(Y)
$$

where $f^*$ preserves finite limits.

=--

## Examples

### Sites

* The archetypical class of examples is the [[category of open subsets]] $S = Op(X)$ of a [[topological space]] $X$. Notice that a morphism $f : X \to Y$ of topological spaces induces naturally a [[functor]] $f^t : Op(Y) \to Op(X)$ going the other way around, sending an open subset $U \in Y$ to the open subset $f^{-1}(U)$ in $X$.

(...)

### Morphisms of sites

#### Sub-sites 

For $X$ a presite and $U \in S_X$ an object in the corresponding category, the [[comma category]] $(Y_{S_X} / U)$ is naturally regarded as the presite defined by $U$, which by convenient abuse of notation one would just write $U$ itself, so that $S_U = S_X \downarrow U$. 

For instance for $X$ a topological space and $U \in Op(X)$ an open subset, $U$ regarded as a topological space in its own right has corresponding to it the site $U$ with $S_U = Op(U) = Op(X) \downarrow U$.

The [[stuff, structure, property|forgetful]] [[functor]]
$$
  j^t_{U \to X} : (S_U = (Y_{S_X} / U)) \to S_X
$$
therefore constitutes a canonical morphism of pre-sites
$$
  j_{U \to X} : X \to U  
  \,.
$$
This induces a [[Grothendieck topology]] on the site $U$ whose [[local epimorphisms]] $(Y \to U) \in [S_U^{op}, Set]$ are precisely those morphisms for which
$$
  \hat j^t_{U \to X}(Y \to U)
  \in 
  [S_X^{op}, Set]
$$
is a [[local epimorphism]].

There are natural operations for [[restriction and extension of sheaves]] from a sub-site $U$ to $X$ and back.


#### Morphisms of frames

For $A$ and $B$ [[frame]]s equipped with their [[canonical coverage]]s, a morphism of sites $A \to B$ is the same as a frame homomorphism: a function preserving finite meets and arbitrary joins.

#### Morphisms of regular categories

For $C$ and $D$ [[regular category|regular categories]] equipped with their [[regular coverage]]s, a morphism of sites is the same as a [[regular functor]], i.e. a functor preserving finite limits and covers.


#### Injections into tangent categories {#TangentCategories}

We discuss morphisms of sites from a site to its [[tangent category]].

> check

Let $C$ be a category with finite limits and let $T_C \to C$ be its [[tangent category]], the fiberwise abelianization of the [[codomain fibration]]: for $A \in C$ we have $(T_C)_A = Ab(C/A)$, the category of abelian [[group object]]s internal to the [[overcategory]] of $C$ over $A$.

The standard example is $(T_C \to C) = $ [[Mod]] $\to$ [[CRing]].

There is then the 0-section $i : C \to T_C$ which sends $A$ to the terminal object $Id : A\to A$ in the overcategory, equipped, necessarily, with the trivial group structure. This exhibits $C$ as a [[retract]] of $T_C$

$$
  (C \stackrel{i}{\to} T_C \stackrel{p}{\to} C) = Id_C
  \,.
$$

Assume now that $C^{op}$ has [[pullback]]s and is equipped with a [[coverage]], hence with the structure of a site.

Equip $(T_C)^{op}$ with the [[coverage]] where $\{f_i : U_i \to U\}$ is a cover in $(T_C)^{op}$ precisely if its image $\{p(f_i) : p(U_i) \to p(U)\}$ is a cover in $C^{op}$.

Then the 0-section $C^{op} \to (T_C)^{op}$ preserves covers. 

We claim it also preserves limits: i.e. that $i : C \to T_C$ preserves [[colimit]]s:

let $F : K \to C$ be a diagram and $\lim_\to F$ its colimit in $C$. Then let $Q$ be any cocone under $i \circ F $ in $T_C$. By applying $p$ to that cocone we find that there is a unique morphism of cocones $\lim_\to F \to p(Q)$ in $C$. But any morphism of the form $A \to p(B)$ for $A \in C$ and $B \in T_C$ has a unique lift to a morphism $i(A) \to B$ in $T_C$ (because the trivial ablian group is initial, so that the morphism in $T_C$ is fixed by its underlying morphism in $C$).

So for any coverage on $C^{op}$ and the above induced coverage on $(T_C)^{op}$, the 0-section $i : C^{op} \to (T_C)^{op}$ is a morphism of sites.

Accordingly, we obtain a [[geometric morphism]] of [[category of sheaves|sheaf toposes]]

$$
  Sh((T_C)^{op}) \stackrel{\leftarrow}{\underset{}{\to}}
  Sh(C^{op})
  \,.
$$


#### Concrete sites

A site that is also a [[concrete category]] in a compatible way is called a [[concrete site]].

## Related concepts

* **site**

* [[2-site]], [[(2,1)-site]]

* [[(∞,1)-site]]

  * [[model site]], [[simplicial site]]


## References 

Morphisms between sites are discussed for instance

in section 17.2 of 

* Kashiwara-Schapira, _[[Categories and Sheaves]]_

(in terms of [[local isomorphisms]])

as well as in section VII. 10 of

* [[Saunders MacLane]] [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

(in terms of covering [[sieves]]), where also the relation to [[geometric morphisms]] is discussed.

In 

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephan]]_

sites are discussed in section C2.1 and morphism of sites in C2.3.

[[!redirects sites]]
[[!redirects morphism of sites]]
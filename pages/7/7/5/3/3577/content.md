
<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The structure of an $(\infty,1)$-site on an [[(∞,1)-category]] $C$ is precisely the data encoding an [[(∞,1)-category of (∞,1)-sheaves]] 

$$
  Sh(C) \hookrightarrow PSh(C)
$$

inside the [[(∞,1)-category of (∞,1)-presheaves]] on $C$.

The notion is the analog in [[(∞,1)-category]] theory of the notion of a [[site]] in 1-[[category theory]].


## Definition

The definition of $(\infty,1)$-sites parallels that of 1-categorical [[site]]s closely. In fact the structure of an $(\infty,1)$-site on an $(\infty,1)$-category is equivalent to that of a 1-categorical site on its [[homotopy category of an (infinity,1)-category|homotopy category]] (see below).

+-- {: .un_defn}
###### Definition
**($(\infty,1)$Grothendieck topology)**

A **[[sieve]] in** an [[(∞,1)-category]] $C$ is a full [[sub-(∞,1)-category]] $D \subset C$ which is closed under precomposition with morphisms in $C$.

A **sieve on** an [[object]] $c \in C$ is a sieve in the [[over quasi-category|overcategory]] $C_{/c}$.

Equivalently, a sieve on $c$ is an equivalence class of [[monomorphism in an (infinity,1)-category|monomorphisms]]  $U \to j(c)$ in the [[(∞,1)-category of (∞,1)-presheaves]] $PSh(C)$, with $j : C \to PSh(C)$ the [[(∞,1)-Yoneda embedding]]. (See below for the proof of this equivalence).

For $S$ a sieve on $c$ and  $f : d \to c$ a [[morphism]] into $c$, we take the **pullback sieve** $f^* S$ on $d$ to be that spanned by all those morphisms into $d$ that become equivalent to a morphism in $S$ after postcomposition with $f$.

A **[[Grothendieck topology]]** on the $(\infty,1)$-category $C$ is the specification of a collection of sieves on each object of $C$ -- called the **covering sieves** , subject to the following conditions:

1. _the trivial sieve covers_ -- For each object $c \in C$ the overcategory $C_{/c}$ regarded as a maximal subcategory of itself is a covering sieve on $c$. Equivalently: the monomorphism $Id : j(c) \to j(c)$ covers.

1. _the pullback of a sieve covers_ -- If $S$ is a covering sieve on $c$ and $f : d \to c$ a morphism, then the pullback sieve $f^* S$ is a covering sieve on $d$. Equivalently, the [[pullback]]

   $$
     \array{  
        f^* U &\to& U 
        \\
        \downarrow && \downarrow
        \\
        d &\stackrel{f}{\to}& c
     }
   $$

   in $PSh(C)$ is covering.

1. _a sieve covers if its pullbacks cover_ -- For $S$ a covering sieve on $c$ and $T$ any sieve on $c$, if the pullback sieve $f^* T$ for every $f \in S$ is covering, then $T$ itself is covering.

An $(\infty,1)$-category equipped with a Grothendieck topology is an **$(\infty,1)$-site**.

=--





## Properties

### Of sieves

+-- {: .un_lemma}
###### Lemma

A sieve $S'$ on $c$ that contains a covering sieve $S \subset S'$ is itself covering.

=--

+-- {: .proof}
###### Proof


For every $f : d \to c$ an object of $S \subset C_{/c}$, the pullback sieve 
$f^* S'$ equals the pullback sieve $f^* S$. So it covers $d$ by the second axiom on sieves. So by the third axiom $S'$ itself is covering.

=--


+-- {: .un_proposition}
###### Proposition

There is a natural bijection between covering sieves on $c$ in $C$ and equivalence class of [[monomorphism in an (infinity,1)-category|monomorphisms]] $U \to j(C)$ in $PSh(C)$.

=--

This is [[Higher Topos Theory|HTT, prop. 6.2.2.5]].

+-- {: .proof}
###### Proof

First observe that equivalence classes of $(-1)$-[[truncated]] object of $PSh(C_{/c})$ are in bijection with sieves on $c$:

An $(\infty,1)$-presheaf $F$ is $(-1)$-truncated if its value on any object is either the empty [[∞-groupoid]] $\emptyset$ or a [[contractible]] $\infty$-groupoid. The full subcategory of $C_{/c}$ on those objects on which $F$ takes a contractible value is evidently a sieve (because there is no morphism from a contractible to the empty $\infty$-groupoid). Conversely, given a sieve $S$ on $c$ we obtain a (-1)-truncated presheaf fixed by the demand that it takes the value $* = \Delta[0] \in \infty Grpd$ on those objects that are in $S$, and $\emptyset$ otherwise.

Now, as described at <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-category+of+(infinity%2C1)-presheaves#WithOvercategories">Interaction of presheaves and overcategories</a> we have an equivalence

$$
  PSh(C_{/c})
  \simeq
  PSh(C)_{/j(c)}
  \,.
$$

Under this equivalence our bijection above maps to the statement that there is a bijection between sieves on $c$ and equivalence class of $(-1)$-[[truncated]] objects in $PSh(C)_{/j (c)}$. But such a (-1)-truncated object is precisely a [[monomorphism in an (infinity,1)-category|monomorphism]] $U \to j(c)$.

=--



### Of coverages

+-- {: .un_lemma}
###### Observation

The set of Grothendieck topologies on an $(\infty,1)$-category $C$ is in natural bijection with the set of Grothendieck topologies on its [[homotopy category of an (infinity,1)-category|homotopy category]].

=--

This is [[Higher Topos Theory|HTT, remark 6.2.2.3]].

+-- {: .proof}
###### Proof

Because picking full sub-1-categories as well as full sub-$(\infty,1)$-categories amounts to picking sub-sets/sub-classes of the set of equivalence classes of objects.

=--

+-- {: .un_corollary}
###### Corollary

If the $(\infty,1)$-category $C$ happens to be an ordinary [[category]] (for instance in its incarnation as a [[quasi-category]] it is the [[nerve]] of an ordinary [[category]]), then the structure of an $(\infty,1)$-site on it is the same as the 1-categorical structure of a [[site]] on it.

=--


### Of sites


+-- {: .un_prop}
###### Proposition

Structures of $(\infty,1)$-sites on an [[(∞,1)-category]] $C$ correspond bijectively to [[topological localization]]s of the [[(∞,1)-category of (∞,1)-presheaves]] to a [[(∞,1)-category of (∞,1)-sheaves]]. See there for more details.

=--


## Incarnations and models

If [[(∞,1)-categories]] are incarnated as [[simplicially enriched categories]], then an $(\infty,1)$-site appears as an 

* [[sSet-site]]

If $(\infty,1)$-categories are [[presentable (∞,1)-category|presented]] by [[model categories]], then the notion of $(\infty,1)$-site appears as that of

* [[model site]].

## Examples

* The **trivial Grothendieck-topology** on an $(\infty,1)$-category is that where the only covering sieve on each object $c$ is $C_{/c}$ itself. Equivalently, where the only covering monomorphisms $U \to j(c)$ in $PSh(C)$ are the equivalences.

  The [[(∞,1)-category of (∞,1)-sheaves]] on this site is just the [[(∞,1)-category of (∞,1)-presheaves]] itself. The localization is an equivalence.



## References

Section 6.2.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

[[!redirects (∞,1)-site]]

[[!redirects (infinity,1)-sites]]
[[!redirects (∞,1)-sites]]
[[!redirects (∞,1)-Grothendieck topology]]
[[!redirects (∞,1)-Grothendieck topologies]]
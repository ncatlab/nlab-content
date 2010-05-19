
<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The analog in [[(∞,1)-category]] theory of the notion of a [[site]] in ordinary [[category theory]].

## Definition

A quick but  somewhat deceptive definition is:

an $(\infty,1)$-site is a [[(∞,1)-category]] equipped with the structure of an ordinary [[site]] on its [[homotopy category of an (∞,1)-category]].

An equivalent but more natural definition is the following

+-- {: .un_defn}
###### Definition
**($(\infty,1)$Grothendieck topology)**

A **[[sieve]] in** an [[(∞,1)-category]] $C$ is a full [[sub-(∞,1)-category]] $D \subset C$ which is closed under precomposition with morphisms in $C$.

A **sieve on** an [[object]] $c \in C$ is a sieve in the [[over quasi-category|overvategory]] $C_{/c}$.

For $S$ a sieve on $c$ and  $f : d \to c$ a [[morphism]] into $c$, we take the **pullback sieve** $f^* S$ on $d$ to be that spanned by all those morphisms into $d$ that become equivalent to a morphism in $S$ after postcomposition with $f$.

A **[[Grothendieck topology]]** on the $(\infty,1)$-category $C$ is the specification of a collection of sieves on each object of $C$ -- called the **covering sieves** , subject to the following conditions:

1. _the trivial sieve covers_ -- For each object $c \in C$ the overcategory $C_{/c}$ regarded as a maximal subcategory of itself is a covering sieve on $c$.

1. _the pullback of a sieve covers_ -- If $S$ is a covering sieve on $c$ and $f : d \to c$ a morphism, then the pullback sieve $f^* S$ is a covering sieve on $d$.

1. _a sieve covers if its pullbacks cover_ -- For $S$ a covering sieve on $c$ and $T$ any sieve on $c$, if the pullback sieve $f^* T$ for every $f \in S$ is covering, then $T$ itself is covering.

An $(\infty,1)$-category equipped with a Grothendieck topology is an **$(\infty,1)$-site**.

=--


## Properties

+-- {: .un_prop}
###### Proposition

Structures of $(\infty,1)$-sites on an [[(∞,1)-category]] $C$ correspond bijectively to [[topological localization]]s of the [[(∞,1)-category of (∞,1)-presheaves]] to a [[(∞,1)-category of (∞,1)-sheaves]]. See there for more details.

=--


## Incarnations and models

If [[(∞,1)-categories]] are incarnated as [[simplicially enriched categories]], then an $(infty,1)$-site appears as an 

* [[sSet-site]]

If $(\infty,1)$-categories are [[presentable (∞,1)-category|presented]] by [[model categories]], then the notion of $(\infty,1)$-site apears as that of

* [[model site]].

## References

def 6.2.2.1 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

[[!redirects (∞,1)-site]]

# Irreducible ideals
* table of contents
{: toc}

## Idea

_Irreducible ideals_ generalize [[prime ideals]] by replacing [[ideal product|multiplication]] of [[ideals]] with [[intersection]].  (Strictly speaking, this gives us the notion of _strongly_ irreducible ideals; the irreducible ideals are found by replacing a containment with an equality.  However, in many common situations, these are equivalent.)

In [[lattices]] (or [[prosets]] more broadly), where multiplication of ideals *is* intersection, the (strongly) irreduicible ideals are the same as the prime ideals; this is true in some other cases, such as the [[ring of integers]].  (For this reason, the term 'strongly irreducible' is not needed in [[order theory]].)

There is also an infinitary version, the _completely_ irreducible ideals_, which also have a strong version.  (The completely strongly irreduicible ideals are usually called 'completely prime' in order theory, although they are different from the [[completely prime ideals]] of noncommutative ring theory).

Irreducible ideals are related to [[irreducible elements]] but don\'t line up perfectly.


## Definitions

Let $R$ be a [[ring]], or more generally a [[rig]], possibly even [[nonassociative ring|nonassociative]], or even just a [[monoid]], possibly just a [[magma]]; or on the other hand a [[lattice]], or even just a [[proset]].  In other words, anything with a concept of _[[ideals]]_.  In the noncommutative case, we could be talking about left ideals, right ideals, or two-sided ideals; pick a meaning and stick with it.  We need the concept of [[intersection]] of ideals (which all of these have), and that\'s pretty much it; that is, we use the structure of the [[meet-semilattice]] $Idl(R)$ of ideals of $R$.

+-- {: .num_defn #basic}
###### Definition

An ideal $I$ of $R$ is __irreducible__ if $I$ is [[proper ideal|proper]] and, whenever $I$ equals the intersection of two ideals of $R$, $I$ equals at least one of those two ideals:

$$ \forall\, J \in Idl(R),\; \forall\, K \in Idl(R),\; I = J \cap K \;\Rightarrow\; I = J \;\vee\; I = K .$$

Also, $I$ is __completely irreducible__ if, whenever $I$ contains the intersection of any collection of ideals of $R$, $I$ contains at least one of the ideals in that collection:

$$ \forall\, \mathcal{J} \subseteq Idl(R),\; I = \bigcap \mathcal{J} \;\Rightarrow\; \exists\, J \in Idl(R),\; J \in \mathcal{J} \;\wedge\; I = J .$$

Alternatively, $I$ is __strongly irreducible__ if $I$ is [[proper ideal|proper]] and, whenever $I$ contains the intersection of two ideals of $R$, $I$ contains at least one of those two ideals:

$$ \forall\, J \in Idl(R),\; \forall\, K \in Idl(R),\; I \supseteq J \cap K \;\Rightarrow\; I \supseteq J \;\vee\; I \supseteq K .$$

Finally, $I$ is __strongly completely irreducible__ if, whenever $I$ contains the intersection of any collection of ideals of $R$, $I$ contains at least one of the ideals in that collection:

$$ \forall\, \mathcal{J} \subseteq Idl(R),\; I \supseteq \bigcap \mathcal{J} \;\Rightarrow\; \exists\, J \in Idl(R),\; J \in \mathcal{J} \;\wedge\; I \supseteq J .$$
=--

Every strongly irreducible ideal is irreducible, every completely irreducible ideal is irreducible, and every strongly completely irreducible ideal is both strongly irreducible and completely irreducible.  (The converses of these hold in various situations that we should describe below.)

The definition of 'completely irreducible' doesn\'t need to explicitly require $I$ to be proper; that is covered by considering the [[empty collection]] $\mathcal{J}$ of ideals.  The definition of 'irreducible' can take care of that automatically too if it is made [[unbiased definition|unbiased]]:

+-- {: .num_defn #unbiased}
###### Definition

An ideal $I$ of $R$ is __irreducible__ if, whenever $I$ equals the intersection of a [[finite list]] of ideals of $R$, $I$ equals at least one of the ideals in the list:

$$ \forall\, n \in \mathbb{N},\; \forall\, J \in Idl(R)^n,\; I = \bigcap_{k\in[n]} J_k \;\Rightarrow\; \exists\, k \in [n],\; I = J_k .$$

Also, $I$ of $R$ is __strongly irreducible__ if, whenever $I$ contains the intersection of a [[finite list]] of ideals of $R$, $I$ contains at least one of the ideals in the list:

$$ \forall\, n \in \mathbb{N},\; \forall\, J \in Idl(R)^n,\; I \supseteq \bigcap_{k\in[n]} J_k \;\Rightarrow\; \exists\, k \in [n],\; I \supseteq J_k .$$
=--

As is typical, the case for $n \gt 2$ follows from the case for $n = 2$ by [[mathematical induction|induction]], the case for $n = 2$ is the significant requirement in the unbiased definition, the case for $n = 1$ is trivial, and the case for $n = 0$ is the extra requirement (in this case, being proper) that rules out ideals that are [[too simple to be simple|too irreducible to be irreducible]].

As with [[prime ideals]], it may be helpful to focus on the [[complements]] of the ideals involved, which are known (especially in [[constructive mathematics]]) as [[anti-ideals]].  Of course, we could just repeat the definitions involving the [[join-semilattice]] $AIdl(R)$ of antiideals of $R$ (which classically is equivalent to $Idl(R)^op$); I won\'t write that out here, but it does make the term 'irreducible' have more of the flavour of its usual meaning; a proper anti-ideal is irreducible if it cannot be _reduced_ as the union of two smaller anti-ideals.


## Properties

If $Idl(R)$ is a [[distributive lattice]], then irreducible ideals are the same as strongly irreducible ideals.  If $R$ is a distributive lattice, then not only are these the same, but the [[prime ideals]] are also the same as them.

An ideal generated by an [[irreducible element]] is irreducible, but not always conversely (not even if we ignore $0$).


## References

*  Kiyoshi Iséki. 1956. Ideal Theory of Semiring. _Proceedings of the Japan Academy_ A 32:8, 554--559. [Project Euclid](https://projecteuclid.org/euclid.pja/1195525272).


[[!redirects irreducible ideal]]
[[!redirects irreducible ideals]]

[[!redirects completely irreducible ideal]]
[[!redirects completely irreducible ideals]]

[[!redirects strongly irreducible ideal]]
[[!redirects strongly irreducible ideals]]

[[!redirects completely strongly irreducible ideal]]
[[!redirects completely strongly irreducible ideals]]

[[!redirects strongly completely irreducible ideal]]
[[!redirects strongly completely irreducible ideals]]

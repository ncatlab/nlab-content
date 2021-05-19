

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _maximal ideal_ (in say a [[commutative ring]] $R$) is an [[ideal]] $M$ which is maximal among [[proper ideals]]. (This is a second-order definition, as it quantifies over subsets of $R$.) 

Equivalently, an ideal $M \subseteq R$ is maximal if the [[quotient]] ring $R/M$ is a [[field]]. This suggests a [[first-order logic|first-order]] definition: an ideal $M$ is maximal if $(\forall_x)\; \neg (x \in M) \Rightarrow \exists_y x y = 1$. 

## Properties

### General

+-- {: .num_prop #EveryProperIdealisContainedInAMaximalOne}
###### Proposition
**(every proper ideal is contained in a maximal one)**

Assuming the [[axiom of choice]] then:

Let $R$ be a [[commutative ring]] and let $I \subset R$ be a proper ideal. Then $R$ contains a maximal ideal $\mathfrak{m}$ containing $I$, i.e. $I \subset \mathfrak{m}$.

=--

(See also at _[[prime ideal theorem]]_.)

+-- {: .proof}
###### Proof

Write $PropIdl(R)_{\subset}$ for the set of proper ideals of $R$, [[partially ordered set|partially ordered]] by inclusion. We claim that every chain in $PropIdl(R)_{\subset}$ has an upper bound ([def.](#Zorn's+lemma#ChainAndUpperBound)). This then implies the statement by [[Zorn's lemma]] (equivalent to the [[axiom of choice]]).

To show the claim, assume that $\mathcal{C} \subset PropIdl(R)_{\subset}$ is a chain. We have to produce an $I \in PropIdl(R)$ such that for all $c \in C$ then $c \subset I$.

We claim that such $I$ is provided by the union:

$$
  I \coloneqq  \underset{J \in \mathcal{C}}{\cup} J
  \,.
$$

It is clear that if this is indeed a proper ideal, then it is an upper bound of the chain. 

To see first of all that this $I$ is an ideal, consider $x_1, x_2 \in I$. There are thus $J_1, J_2 \in \mathcal{C}$ with $x_1 \in J_1$ and $x_2 \in J_2$. Since a chain is [[totally ordered set|total order]] by definition, either $J_1 \subset J_2$ or $J_2 \subset J_1$. We may assume the former without restriction, otherwise rename $1 \leftrightarrow 2$. Therefore now $x_1, x_2 \in J_2$ and so we may add them there and find that $x_1 + x_2 \in J_2 \subset I$. Similarly if $r \in R$ then $r x_i \in J_2 \subset I$. 

Finally to see that this idea $I$ is indeed proper. But since all the $J_i$ are proper, neither of them contains $1 \in R$, and hence $I$ does not contain $1 \in R$.

=--

+-- {: .num_prop #MaximalIdealsArePrimeIdeals}
###### Proposition

In [[classical mathematics]] then:

Every maximal ideal is a [[prime ideal]].

=--

### Relation to points in the spectrum

Assuming [[axiom of choice|AC]] and [[excluded middle|EM]], then

Maximal ideals in the [[spectrum of a commutative ring]] $Spec(R)$ correspond precisely to the [[closed points]] in the [[Zariski topology]] on $Spec(R)$ ([this prop.](Zariski+topology#MaximalIdealsAreClosedPoints)).  

Closed points are at the heart of the definition of _[[schemes]]_. A scheme $X$ is a sheaf with respect to the [[Zariski topology]] that admits a covering by open embeddings of affine schemes, where "covering" means that every *closed* point $p: Spec(F) \to X$ ($F$ a *field*) factors through one of the embeddings. 

## Related concepts

* [[minimal ideal]]

* [[residue field]]

## References

* Mathematics StackExchange, _[Meaning of closed points of a scheme](http://math.stackexchange.com/questions/942/meaning-of-closed-points-of-a-scheme)_

[[!redirects maximal ideals]]
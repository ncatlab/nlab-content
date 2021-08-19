
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Grothendieck group construction_ is an explicit presentation of the [[group completion]] of a [[commutative monoid]] to an [[abelian group]]. For a [[cancellative monoid]] it reduces to the age-old construction that turns the additive monoid of [[natural numbers]] into the aditive group of [[integers]], or the multiplicative monoid of non-zero [[integers]] into the multiplicative group of non-zero [[rational numbers]]. But the construction also applies to non-[[cancellative monoids]]. The archetypical application of the construction is to monoids of [[topological vector bundles]] over some [[topological space]] $X$ under [[direct sum of vector bundles]], in which case it yields the _[[topological K-theory]] group_ $K(X)$ of $X$. 

Motivated by the example of [[topological K-theory]] there is a vaguelly related construction of [[algebraic K-theory]] groups from [[Quillen exact categories]]. Applied to the category of [[topological vector bundles]] this coincides with the Grothendieck group of the monoid of vector bundles, and hence is also called _Grotheniek group construction_. For more on this [[category theory|category theoretic]] operation see at _[[Grothendieck group]]_.

## Definition

+-- {: .num_defn #GrothendieckGroupViaQuotientOfCartesianProduct}
###### Definition
**([[Grothendieck group of a commutative monoid]])**

Let $(A,+)$ be a [[commutative monoid]] (i.e. a commutative [[semi-group]]).

On the [[Cartesian product]] of underlying sets $A \times A$ (the set of ordered [[pairs]] of elements in $A$), consider the [[equivalence relation]]

$$
  \big(
    (a_+, a_-) \sim_1 (b_+, b_-)
  \big) 
    \;\Leftrightarrow\; 
  \left(
    \underset{k \in A}{\exists}
    \left( 
      a_+ + b_- + k = b_+ + a_- + k
    \right)
  \right)
$$

or equivalently the equivalence relation

$$
  \big(
    (a_+, a_-) \sim_2 (b_+, b_-)
  \big) 
    \;\Leftrightarrow\; 
  \left(
    \underset{k_1, k_2 \in A}{\exists}
    \left(
      (a_+ + k_1, a_- + k_1)
      =
      (b_+ + k_2, b_- + k_2)
    \right)
  \right)
  \,.
$$

Write

$$
  G(A) \coloneqq (A \times A)/\sim
$$

for the set of [[equivalence classes]] under this equivalence relation. This inherits a binary operation

$$
  + \;\colon\; G(A) \times G(A) \longrightarrow G(A)
$$

by applying the addition in $A$ on representatives:


$$
  [a_+,a_-] + [b_+,b_-] \coloneqq [ a_+ + b_+ , a_- + b_- ]
  \,.
$$

This defines the structure of an [[abelian group]]

$$
  (G(A),+)
$$

and this is the _Grothendieck group_ of $A$. 

This comes with a canonical [[homomorphism]] of [[monoids]] ([[semigroups]] with [[unitality|unit]]):

$$
  \array{
    A &\overset{\phantom{A} \eta_A \phantom{A} }{\longrightarrow}& G(A)
    \\
    a &\overset{\phantom{AAA}}{\mapsto}& [a,0]
  }
  \,.
$$

=--

+-- {: .num_prop #UniversalProperty}
###### Proposition
**([[universal property]] of Grothendieck group)**

The Grothendieck group in def. \ref{GrothendieckGroupViaQuotientOfCartesianProduct} is well defined, and the homomorphism $A \to G(A)$ satisfies the [[universal property]] of the [[group completion]] of $A$: 


Given an [[abelian group]] $B$ and a [[homomorphism]] of commutative [[semi-groups]] ([[commutative monoids]]) $f \colon A \longrightarrow B$ then there is a unique homomorphism of [[abelian groups]] $\tilde A \;\colon\; G(A) \longrightarrow B$ such that $f = \tilde f\circ \eta_A$:

$$
  \array{
    A
    \\
    {}^{\mathllap{\eta_A}}\downarrow & \searrow^{\mathrlap{f}}
    \\
    G(A) &\overset{\exists ! \tilde f}{\longrightarrow}& B    
  }
$$


=--

+-- {: .proof}
###### Proof

First to see that the two equivalence relations in def. \ref{GrothendieckGroupViaQuotientOfCartesianProduct} are indeed the same:

If $a_+ + b_- + k = b_+ + a_- + k$ then take $k_1 \coloneqq b_- + k$ and $k_2 \coloneqq a_- + k$ to find that

$$
  \begin{aligned}
    (a_+ + k_1 , a_- + k_1)
    & = 
    ( a_+ + b_- + k, a_- + b_- + k)
    \\
    & =
    (b_+ + a_- + k, a_- + b_- + k)
    \\
    & =
    (b_+ + k_2, b_- + k_2)
  \end{aligned}
  \,.
$$ 

Conversely, if $(a_+ + k_1 , a_- + k_1) = (b_+ + k_2, b_- + k_2)$ then take $k \coloneqq k_1 + k_2$ to find that

$$
  \begin{aligned}
    a_+ + b_- + k 
      & = 
    a_+ + k_1 + b_- + k_2
    \\
      & =
    b_+ + k_2 + a_- + k_1
    \\
      & = 
    b_+ + a_- + k
  \end{aligned}
  \,.
$$

Now to see that $(G(A),+)$ is indeed an abelian group: 

1. the second equivalence relation also makes it immediate that the [[neutral element]] is the class 

   $$
     [0,0] =  [a,a]
   $$
   
   for all $a \in A$.

1. with this the second equivalence relation makes it immediate that the [[inverse element]] to any $[a_+, a_-]$ is 

   $$
     -[a_+, a_-] = [a_-, a_+]
     \,, 
   $$


That this group is abelian is immediate from the fact that $A$ is assumed to be abelian.

Regarding the universal property: let $B$ be any abelian group and let

$$
  \tilde f \colon G(A) \longrightarrow B
$$

be a homomorphism of abelian groups. Observe from the above that then

$$
  \begin{aligned}
    \tilde f([a_+,a_-])
    & = 
    \tilde f( [a_+,0]  - [a_-, 0] )
    \\
    & = 
    \tilde f([a_+,0]) - \tilde f([a_-,0])
    \\
    & = 
    \tilde f(\eta_A(a_+)) - \tilde f(\eta_A(a_-))
    \\
    & = 
    f(a_+) - f(a_-)
  \end{aligned}
$$

by the linearity of $f$ and the definition of $\eta_A \colon A \to G(A)$. 

Conversely, given $f \colon A \to B$ then this equation uniquely defines $\tilde f$ with $f = \tilde f \circ \eta_A$.

=--

+-- {: .num_remark #GrothendieckGroupForCancellativeMonoids}
###### Remark
**(Grothendieck group for [[cancellative monoids]])**

If $(A,+)$ is a [[cancellative monoid]], in that 

$$
  \underset{a,b,z \in A}{\forall}
  \left(
    \left(
      a + z = b + z
   \right)
     \Rightarrow
   \left(
     a = b
   \right)
  \right)
$$  

then, as is immediate from the first of the two equivalence relations in def. \ref{GrothendieckGroupViaQuotientOfCartesianProduct}, the definition of the Grothendieck group $G(A)$ simplifies to 

$$
  G(A) = (A \times A)/ \sim
$$

with

$$
  \big(
    (a_+,a_-)
      \sim
    (b_+,b_-)
  \big)
     \;\Leftrightarrow\;
  \big(
    a_+ + b_- = b_+ + a_-
  \big)
  \,.
$$


=--



## Examples

+-- {: .num_example #GrothendieckGroupOfNaturalNumbersUnderAdditionIsTheIntegers}
###### Example
**(Grothendieck group of the [[natural numbers]] is the [[integers]])

Let $(\mathbb{N}, +)$ be the [[commutative monoid]] of [[natural numbers]] under [[addition]]. By def. \ref{GrothendieckGroupViaQuotientOfCartesianProduct} its Grothendieck group consists of pairs $(n_+, n_-) \in \mathbb{N} \times \mathbb{N}$ subject to some equivalence relation, and since $(\mathbb{N}, +)$ is [[cancellative monoid|cancellative]], remark  \ref{GrothendieckGroupForCancellativeMonoids} says that this equivalence relation is simply

$$
  \big(
    (a_+,a_-)
      \sim
    (b_+,b_-)
  \big)
     \;\Leftrightarrow\;
  \big(
    a_+ + b_- = b_+ + a_-
  \big)
  \,.
$$

Let

$$
  \array{
    (G(\mathbb{N}),+) &\longrightarrow& (\mathbb{Z},+)
    \\
    (n_+, n_-) &\mapsto&  n_+ - n_-
  }
$$

be the evident [[homomorphism]] of abelian groups to the additive group of [[integers]].

This is manifestly [[surjective function|surjective]]. For it to be injective we need that 

$$
  (a_+, a_-) \sim (b_+,b_-)
$$

precisely if 

$$
  a_+ - a_- = b_+ - b_- \;\; \in \mathbb{Z}
  \,.
$$

The last condition holds precisely if

$$
  a_+ + b_- = b_+ + a_- \;\; \in \mathbb{Z}
$$

which is precisely the above equivalence relation. Therefore the above homomorphism is a [[bijection]] and hence the Grothendieck group of the natural numbers is the [[integers]]:

$$
  (G(\mathbb{N}), +) \simeq \mathbb{Z}
  \,.
$$

=--

+-- {: .num_example }
###### Example

Consider the commutative monoid $(\mathbb{Z}^\times, \cdot)$ of non-zero [[integers]] under [[multiplication]]. 

Consider the homomorphism

$$
  \array{
     (G(\mathbb{Z}), \cdots)
       &\longrightarrow&
     (\mathbb{Q}^\times, \cdot)
     \\
     ( n_+ ,n_- )
        &\mapsto&
     n_+/n_-
  }
$$

to the non-zero [[rational numbers]] under multiplication.

It is immediate that this is surjective. For it to be injective we need that 

$$
  (a_+, a_-)
    \sim
  (b_+, b_-)
$$

precisely if 

$$
  a_+/ a_- = b_+ / b_- \;\; \in \mathbb{Q}
$$

which is the case precisely if

$$
  a_+ \cdot b_- = b_+ \cdot a_-
  \,.
$$

Since $(\mathbb{Z}^\times, \cdot)$ is a [[cancellative monoid]], this is indeed the equivalence relation on $G(\mathbb{Z}^\times)$, according to remark \ref{GrothendieckGroupForCancellativeMonoids}.



=--


+-- {: .num_example}
###### Example
**([[topological K-theory]])**

Let $X$ be a [[topological space]] and let $(Vect(X)_{/\sim}, \oplus)$ be the monoid of [[isomorphism classes]] of [[topological vector bundles]] on $X$ with addition induced from the [[direct sum of vector bundles]]. (This is in general not a [[cancellative monoid]]). Then the Grothendieck group

$$
  K(X) \coloneqq (G(Vect(X)_{/\sim}), +)
$$

is called the _[[topological K-theory]]_ group of $X$.

=--

## References

See also 

* Wikipedia, _[Grothendieck group](https://en.wikipedia.org/wiki/Grothendieck_group)_

[[!redirects Grothendieck groups of commutative monoids]]

[[!redirects Grothendieck group construction on commutative monoids]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Boardman-Vogt tensor product_ is a natural [[tensor product]] on [[symmetric operads]]. It makes the category [[Operad]] of colored [[symmetric operads]] over [[Set]] into a [[closed monoidal category]].

## Definition

All [[operads]] in the following are colored [[symmetric operads]] enriched over [[Set]], equivalently [[symmetric multicategories]].

Let $\mathcal{P}$ be an operad over a set of colors $C$, and $\mathcal{Q}$ be an operad over a set of colors $D$.

Their **Boardman-Vogt tensor product** $\mathcal{P} \otimes_{BV} \mathcal{Q}$ is the operad whose set of colors is $C \times D$, and whose operations are given by generators and relations as follows:

There is one generating operation for every pair $(p,d)$ with $p \in \mathcal{P}(c_1, \cdots, c_n; c)$ and with $d \in D$, denoted

$$
  p \otimes d 
  \in 
  \mathcal{P} \otimes_{BV} \mathcal{Q}(
    (c_1,d), \cdots, (c_n,d); (c,d)
  )
$$

and for each pair $(c,q)$ with $c \in C$ and $q \in \mathcal{Q}(d_1, \cdots, d_n; d)$, denoted

$$
  c \otimes q
  \in
  \mathcal{P}\otimes_{BV} \mathcal{Q}(
   (c, d_1), \cdots, (c, d_n);
   (c,d)
  )
$$

for all $n \in \mathbb{N}$. These are subject to the following relations

1. The tensor product $c \otimes (-)$ with $c \in C$ respects the composition in $\mathcal{Q}$, and the tensor product $(-) \otimes d$ with $d \in D$ respects the composition in $\mathcal{P}$ and both respect the action of the [[symmetric group]] on the operations.
   
   Equivalently this means that for all $c \in C$ tensoring with $c$ extends to a morphism of operads

   $$
     \mathcal{Q} \to \{c\} \otimes_{BV}\mathcal{Q}
   $$

   and for all $d \in D$ a morphism of operads

   $$
     \mathcal{P} \to \mathcal{P} \otimes_{BV} \{d\}
     \,.
   $$

1. The operations  in $\mathcal{P}$ and $\mathcal{Q}$ [[distributive law|distribute]] over each other in $\mathcal{P} \otimes_{BV} \mathcal{Q}$ in the evident sense (...).

## Properties

### Closed monoidal structure
 {#ClosedMonoidalStructure}

+-- {: .num_prop}
###### Proposition

Equipped with the Boardman-Vogt tensor product, [[Operad]] is a [[closed monoidal category|closed]] [[symmetric monoidal category]].

=--

See for instance the proof provided in ([Weiss, theorem 2.22](#Weiss)).

This implies directly several useful statements about the BV-tensor product

+-- {: .num_cor}
###### Corollary

* The BV tensor products preserves [[colimits]] of operads in each variable separately.

=--

We write in the following

$$
  [-,-] : Operad^{op} \times Operad \to Operad
$$

for the corresponding [[internal hom]] (leaving a subscrip "${}_{BV}$" implicit.)

+-- {: .num_prop #InternalHomOperadAsAlgebraOperad}
###### Proposition

For $P, Q \in $ [[Operad]], the internal hom operad $[P, Q]$ has

* as colors the [[algebra over an operad|P-algebras]] in $Q$;

* as unary operations the $P$-algebra homomorphisms in $Q$. 

=--

See ([Weiss, lemma 2.23](#Weiss)).

We may therefore speak of $[P,Q]$ as being the **operad of $P$-algebras in $Q$.

+-- {: .num_example}
###### Example

Write $Set$ for the operad induced by the [[cartesian monoidal category|cartesian]] [[symmetric monoidal category]] structure on [[Set]]. Then for $P$ any operad, the vertices and unary operations of the internal hom operad $[P,Set]$ form the ordinary [[algebra over an operad|category of algebras over]] $P$ in $Set$.

=--



+-- {: .num_corollary}
###### Corollary

For $P_1, P_2, E \in Operad$, the category of $P_1$-algebras in $P_2$-algebras in $E$ is equivalent to the category of $P_2$-algebras in $P_1$-algebras in $E$. 

=--

In view of prop. \ref{InternalHomOperadAsAlgebraOperad} this is the statement of the [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]] structure $(Operad, \otimes_{BC})$:

$$
  [P_1, [P_2, E]] \simeq [P_1 \otimes_{BV} P_2, E]
  \simeq 
  [P_2 \otimes_{BV} P_1, E]
  \simeq
  [P_2, [P_1, E]]
  \,.
$$

## Examples

(...)

## Related concepts

* The Boardman-Vogt tensor product extends from operads to a tensor product on [[dendroidal sets]]. See there for more details.

* [[tensor product of monads]]

## References

The original reference is

* [[Michael Boardman]], [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_, Lecture Notes in Mathematics, Vol. 347, Springer-Verlag, (1973).

A review is in

* {#Weiss} [[Ittay Weiss]], _From Operads to Dendroidal Sets_, in _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS (2011) ([arXiv:1012.4315](http://arxiv.org/abs/1012.4315))
  

see around def. 2.21 there.


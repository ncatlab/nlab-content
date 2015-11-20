
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents #
* table of contents 
{: toc}

## Idea

The _join_ of two categories $C$ and $C'$ is obtained from the [[disjoint union]] of $C$ with $C'$ by throwing in a unique morphism from every object of $C$ to every object of $C'$.

## Definition

The **join** of [[category|categories]] $C$ and $C'$ is the category with

* objects $Obj(C \star C') := Obj(C) \amalg Obj(C')$;

* morphisms given by
$$
  Mor_{C \star C'}(a,b) :=
  \left\lbrace
    \array{
      Mor_C(a,b) & \text{ if  }\;\; a,b \in C
      \\
      Mor_{C'}(a,b) & \text{ if }\;\; a,b \in C'\\
      \emptyset & \text{ if  }\;\;  a \in C', b \in C;
      \\
      \mathrm{pt} & \text{ if  } \;\; a \in C, b \in C';
    }
  \right.
$$

### In terms of profunctors

The join of categories $C,C'$ can also be described to be the [[cograph of a profunctor|cograph]] of the unique profunctor $W\colon C &#8696; \; C'$ sending all objects $(c,c')$ to the terminal set (the definition speaks for itself).

### In terms of adjoint functors

Consider the inclusion of the [[boundary of a simplex|boundary]] of the standard 1-simplex, $i\colon \{0,1\}\to [1]$ as a functor between the [[discrete category]] with two elements and the [[interval category|walking arrow]] $I=\{0 \leq 1\}$. It induces a functor
$$
i^*\colon \Cat / I 
\to  
\Cat \times \Cat
$$
which admits a right adjoint. This right adjoint is precisely the [[bifunctor]] $\star\colon \Cat \times \Cat \to \Cat / I$, once we noticed that the category $C\star C'$ comes naturally equipped with an arrow $C\star C'\to I=1\star 1$ induced by (bi)functoriality of $\star$, starting from the canonical arrows $C\to 1, C'\to 1$ to the [[terminal category]]. 

+-- {: .proof}
###### Proof
It is quite clear that $i^*$ is defined by sending $C\to I$ to the pair of categories $i^\leftarrow(0)=C_0, C_1=i^\leftarrow(1)$. The bijection 
$$
\Cat^{\mathbf{2}}\Big(i^*\big( C\to I\big), (A,B)\Big)\cong 
\Cat / I \Big( C, A\star B \Big)
$$
is now rather obvious, since any functor 
$i^*
\Big(
\array{ C\\ \downarrow \\ I }
\Big)
\to (A,B)$ 
determines a functor $C\to A\star B$ and viceversa.
=--

## Properties

* If the small categories $C,C'$ are two posets, their join consists of their [[ordinal sum]];
* The monoidal structure induced on $\Cat$ by $\star$ is not symmetric (if it was, then the right cone of $C$ would be equivalent to the left cone, which is blatantly false);
* The monoidal structure induced on $\Cat$ by $\star$ is not closed, since the functor $A\star -$ does not preserve colimits.
* The functor $-\star C'\colon \Cat \to C'\!/\!\Cat\colon A\mapsto (A\to A\star C')$ is a left adjoint, and similarly is the functor $C\star-$; see [Joyal, Ch. 3.1.1-2](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf#page=96) for a detailed description.

## Examples

* The **cone** below a category $C$ is the join $C \star \mathrm{pt}$. The cone above $C$ is the join $\mathrm{pt} \star C$. 

## Related concepts

* [[join of topological spaces]]

* [[join of quasi-categories]];

* [[join of simplicial sets]].

## References

See [p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of 

* [[Jacob Lurie]], _Higher topos theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))

See also [Ch. 3](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf#page=95) of

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf))
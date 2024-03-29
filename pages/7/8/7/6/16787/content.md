# Contents # 
* table of contents 
{:toc}

## Idea 

A topological field is a [[field]] equipped with a topology such that all of the field operations are [[continuous functions]]. 

## Definition 

A _topological field_ is a [[topological ring]] whose underlying [[ring]] in $Set$ is a [[field]] $K$ and such that the multiplicative inversion operation $i: K \setminus \{0\} \to K \setminus \{0\}$ is [[continuous function|continuous]] with respect to the [[subspace]] topology inherited from $K$. 

+-- {: .num_remark} 
###### Remark 
Note it is not automatic that inversion is continuous for a field equipped with a ring topology (when it is, we say the ring topology is a *field topology*). The following gives an example of a ring topology that is not a field topology: on the [[rational numbers]] $\mathbb{Q}$, take the set of [[ideals]] $n\mathbb{Z}$, $0 \neq n \in \mathbb{Z}$, to be a filter base for a [[filter]] of [[neighborhoods]] of $0$. That this gives a ring topology follows from three easily verified facts: (1) for any ideal $I$ there is an ideal $J$ such that $J + J \subseteq I$ and $-J \subseteq I$ (e.g., $J = I$), (2) if $I$ is any ideal and $q \in \mathbb{Q}$ is any element, there is an ideal $J$ such that $q J \subseteq I$, and (3) if $I$ is any ideal, there is an ideal $J$ such that $J J \subseteq I$ (again take $J = I$). It's easy to see that this ring topology is [[Hausdorff space|Hausdorff]]. 

But inversion on the nonzero elements is not continuous. Indeed, for a neighborhood of $1$ not containing $0$, e.g., $1 + 2\mathbb{Z}$, no neighborhood $1 + m\mathbb{Z}$ of $1$ will fit inside the set of reciprocals $\{\frac1{1 + 2n}: n \in \mathbb{Z}\}$. 
=-- 

+-- {: .num_remark} 
###### Remark 
If $K$ is a topological field, then either $K$ is a [[codiscrete space]] or is a [[Tychonoff space]]. The reason is that the closure of $\{0\}$ in a topological ring $K$ must be an [[ideal]] $I$, and since $K$ is a field, $I$ is either all of $K$ (whence $K$ is codiscrete), or $I = \{0\}$ in which case $K$ is a $T_1$-[[separation axiom|space]]. In the latter case, since a topological ring is a [[uniform space]], the $T_1$-condition implies $K$ is a Tychonoff space. 
=-- 


## Internalization 

As discussed at [[field]], the notion of field is not algebraic in the sense of [[algebraic theory]], and there are various inequivalent ways of attempting to [[internal logic|internalize]] the notion inside structured categories. This issue is compounded in $Top$ by the fact that $Top$ has few of the exactness properties one needs to enact the more "traditional" fragments of first-order logic (such as being a [[pretopos]] or [[Heyting category]] or [[exact category]] or [[regular category]]). So it is a matter of interest to give a categorical definition of field that internalizes correctly in $Top$, as well as in other categories of interest. 

(Note that $Top$ does enjoy *some* elementary exactness properties: it is a [[lextensive category]] with finite colimits. It also satisfies a strong non-elementary condition: it is $\infty$-extensive and the underlying-set functor $Top \to Set$ is a [[topological functor]]. Curiously, $Top^{op}$ is a [[regular category]].) 

### "Classical" internalization  

One straightforward approach, at least if we are thinking along lines of [[excluded middle|classical logic]], is to define a field $K$ in terms of the following limit-colimit [[sketch]]: 

1. Introduce structure to make $K$ a commutative [[ring object]]: two binary operations $a: K \times K \to K$ (addition) and $m: K \times K \to K$ (multiplication), two constants $0: 1 \to K$ and $e: 1 \to K$ (additive and multiplicative identities), additive inversion $-: K \to K$, all subject to the usual equations for [[commutative rings]]; 

1. Letting $i: U \to K \times K$ denote the [[equalizer]] of $m: K \times K \to K$ and $e \circ !: K \times K \to 1 \to K$, add the axiom that $j = \pi_1 \circ i: U \to K \times K \to K$ (provably monic in finite limit logic) is a [[regular monomorphism]]: the [[equalizer]] of its [[cokernel pair]]; 

1. Add the axiom that $(0, j): 1 + U \to K$ is a [[monomorphism|monic]] [[epimorphism|epic]]. 

Some commentary might be in order. Clearly $U$ plays the role of the [[group of units]] of $K$, realized as a [[subobject]] by $j: U \to K$. Axiom 3. says that $0$ and $U$ exhaust all of $K$, but without going so far to say that $(0, j): 1 + U \to K$ is an [[isomorphism]], an inappropriately strong condition in the case of $Top$ (as it would force the point $0: 1 \to K$ to be open, making $K$ a [[discrete space]]). 

Axiom 2. is more subtle: a mono $k: A \to B$ in $Top$ is regular iff $A$ has the subspace topology inherited from $B$ via $k$. So Axiom 2. interpreted in $Top$ says that the subspace topology on $U$ coming from its inclusion into $K$ coincides with the topology it has by definition, viz. the subspace topology coming from its embedding $i$ in $K \times K$. Notice that inversion on $U$ is continuous if we use the definitional topology, since inversion is effected by permuting the two factors of $K \times K$. Thus Axiom 2. is a sneaky way of forcing inversion on $U$ with the subspace topology from $K$ to be continuous (and in fact it is equivalent to continuity of inversion). 

## Examples

* The [[real numbers]] with their [[metric topology]] as a [[Euclidean space]];

* The [[complex numbers]], similarly,

etc.

[[!redirects topological field]]
[[!redirects topological fields]]

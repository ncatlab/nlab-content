
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition {#Def}

+-- {: .num_defn}
###### Definition

An **algebraic lattice** is a [[lattice]] which is

* a [[complete lattice]];

* such that every element is a [[join]] of [[compact elements]].

=--


An __algebraic lattice__ is a [[complete lattice]] (equivalently, a [[suplattice]], or in different words a [[poset]] with the [[extra property|property]] of having arbitrary [[colimits]] but with the [[structure]] of [[directed colimits]]/[[directed joins]]) in which every element is the [[supremum]] of the [[compact element]]s below it (an element $e$ is compact if, for every subset $S$ of the lattice, $e$ is less than or equal to the supremum of $S$ just in case $e$ is less than or equal to the supremum of some finite subset of $S$). 

Here is an alternative formulation: 
+-- {: .num_defn} 
###### Definition 
An algebraic lattice is a [[poset]] which is [[locally finitely presentable category|locally finitely presentable]] as a category. 
=-- 

This formulation suggests a useful way of viewing algebraic lattices in terms 
of [[Gabriel-Ulmer duality]] (but with regard to enrichment in [[truth values]], instead of in $Set$). 

As this last formulation suggests, algebraic lattices typically arise as [[subobject lattices]] for objects in locally finitely presentable categories. As an example, for any (finitary) [[Lawvere theory]] $T$, the subobject lattice of an object in $T$-$Alg$ is an algebraic lattice (this class of examples explains the origin of the term "algebraic lattice", which is due to Garrett Birkhoff). In fact, all algebraic lattices arise this way (see Theorem \ref{GS} below). 

It is trivial that every finite lattice is algebraic. 

## Properties

### The category of algebraic lattices

The [[morphisms]] most commonly considered between algebraic lattices are the [[finitary functors]] between them, which is to say, the [[Scott topology|Scott-continuous]] functions between them; i.e., those functions which preserve directed joins (hence the parenthetical remarks [above](#Def)). 

The resulting category __AlgLat__ is [[cartesian closed]] and is dually equivalent to the category whose objects are [[meet semilattices]] (construed as categories with [[finite limits]] [[enriched category|enriched]] over [[truth values]]) and whose morphisms are meet-preserving [[profunctors]] between them (using the convention that a $V$-enriched profunctor from $C$ to $D$ is a functor $D^{op} \times C \rightarrow V$; of course, with an opposite convention, one could similarly state a covariant equivalence). 

There is a _full_ [[full embedding|embedding]] 

$$i \colon AlgLat \to Top_0$$ 

to the category of $T_0$-[[separation axioms|spaces]], taking an algebraic lattice $L$ to the space whose points are elements of $L$, and whose [[open sets]] $U$ are defined by the property that their [[characteristic maps]] 

$$\chi_U: L \to \mathbf{2}$$ 

($\chi_U(a) = 1$ if $a \in U$, else $\chi_U(a) = 0$) are poset maps that preserve [[directed colimits]]. The [[specialization order]] of $i(L)$ is $L$ again. 

Every $T_0$-space $X$ occurs as a [[subspace]] of some space $i(L)$ associated with an algebraic lattice. Explicitly, let $L(X)$ be the [[power set]] of the underlying set of the [[topology]], $P{|\mathcal{O}(X)|}$, and define 

$$X \to (i\circ L)(X)$$ 

to take $x$ to $N(x) \coloneqq \{U \in \mathcal{O}(X): x \in U\}$. This gives a topological embedding of $X$ in $i(L(X))$. 

+-- {: .un_remark}
###### Remark 
On similar grounds, if $U \colon AlgLat \to Set$ is the forgetful functor, then the [2-image](http://ncatlab.org/nlab/show/stuff%2C+structure%2C+property#a_factorisation_system_14) of the projection functor $\pi \colon Set\downarrow U \to Set$ is the category of topological spaces $Top$. In more nuts-and-bolts terms, an object $(S, L, f \colon S \to U(L))$ gives a space with underlying set $S$ and open sets those of the form $f^{-1}(O)$, where $O$ ranges over the Scott topology on $L$. Notice that if $(f \colon S \to S', g \colon L \to L')$ is a morphism in $Set \downarrow U$, then $f$ is continuous with respect to these topologies. Therefore the projection $\pi \colon Set \downarrow U \to Set$ factors through the faithful forgetful functor $Top \to Set$. Thus, working in the factorization system (eso+full, faithful) on $Cat$, we have a faithful functor $2$-$im(\pi) \to Top$ filling in as the diagonal 

$$\array{
Set \downarrow U & \to & Top \\
\downarrow & \nearrow & \downarrow \\
2\text{-}im(\pi) & \to & Set.
}$$ 

But notice also that $Set \downarrow U \to Top$ is [eso and full](http://ncatlab.org/nlab/show/ternary+factorization+system#examples_9). It is eso because any topology $\mathcal{O}(S)$ on $S$ can be reconstituted from the triple $(S, P{|\mathcal{O}(S)|}, x \mapsto N(x) \colon S \to P{|\mathcal{O}(S)|})$. We claim it is full as well. For, every continuous map $X \to X'$ between topological spaces induces a continuous map between their $T_0$ reflections $X_0 \to X_{0}'$, and since algebraic lattices like $P{|\mathcal{O}(X)|}$ (being continuous lattices) are [[injective objects]] in the category of $T_0$ spaces, we are able to complete to a diagram 

$$\array{
X & \to & X_0 & \to & P{|\mathcal{O}(X)|} \\
\downarrow & & \downarrow & & \downarrow \\
X' & \to & X_{0}' & \to & P{|\mathcal{O}(X')|}
}$$ 

where the rightmost vertical arrow is Scott-continuous (and the horizontal composites are of the form $x \mapsto N(x)$). Finally, since $Set \downarrow U \to Top$ is eso and full, it follows that $2$-$im(\pi) \to Top$ is eso, full, and faithful, and therefore an equivalence of categories. 

This connection is explored in more depth with the category of [[equilogical spaces]], which can be seen either as a category of (set-theoretic) [[equivalence relation|partial equivalence relations]] over $AlgLat$, or equivalently of (set-theoretic) total [[equivalence relations]] on $T_0$ topological spaces.
=-- 

### Relation to locally finitely presentable categories 
 {#RelationToLocallyFinitelyPresentableCategories}

One of our definitions of algebraic lattice is: a poset $L$ which is locally finitely presentable when viewed as a category. The completeness of $L$ means that right adjoints $L \to Set$ are representable, given by $L(p, -) \colon L \to Set$, and we are particularly interested in those representable functors that preserve [[filtered colimits]]. These correspond precisely to finitely presentable objects $p$, which in lattice theory are usually called compact elements. These compact elements are closed under finite joins. 

By [[Gabriel-Ulmer duality]], $L$ is determined from the join-semilattice of compact elements $K$ by $L \cong Lex(K^{op}, Set)$. Since the elements of $K^{op}$ are subterminal, we can also write $L \cong Lex(K^{op}, 2)$ where $2 = Sub(1)$. 



+-- {: .num_theorem}
###### Theorem 
**(Porst)**

If $C$ is a [[locally finitely presentable category]] and $X$ is an object of $C$, then 

* The lattice of subobjects $Sub(X)$, 

* the lattice of quotient objects (equivalence classes of epis sourced at $X$) $Quot(X)$, 

* the lattice of congruences (internal equivalence relations) on $X$ 

are all algebraic lattices. 
=-- 

This is due to [Porst](#Porst). Of course if $C$ is the category of algebras of an Lawvere theory, then the lattice of quotient objects of an algebra is isomorphic to its congruence lattice, as such $C$ is an [[exact category]]. 

### Congruence lattices 

The following result is due to Gr&#228;tzer and Schmidt: 

+-- {: .num_theorem #GS} 
###### Theorem 
Every algebraic lattice is isomorphic to the congruence lattice of some [[model]] $X$ of some finitary algebraic theory. 
=-- 

In particular, since every finite lattice is algebraic, every finite lattice arises this way. Remarkably, it is not known at this time whether every finite lattice arises as the congruence lattice of a *finite* algebra $X$. It has been conjectured that this is in fact **false**: see this [MO discussion](http://mathoverflow.net/a/196074/2926). 

Another problem which had long remained open is the congruence lattice problem: is every *distributive* algebraic lattice the congruence lattice (or lattice of quotient objects) of some lattice $L$? The answer is negative, as shown by Wehrung in 2007: see this [Wikipedia article](http://en.m.wikipedia.org/wiki/Congruence_lattice_problem). 

### Completely distributive lattices

+-- {: .num_prop}
###### Proposition


The category of [[Alexandroff locales]] is equivalent to that of [[completely distributive lattice|completely distributive]] algebraic lattices. 
=--

This appears as ([Caramello, remark 4.3](#Caramello)).

The [[completely distributive lattice|completely distributive]] algebraic lattices form a [[reflective subcategory]] of that of all distributive lattices. The reflector is called _[[canonical extension]]_.

## Related concepts

See also [[compact element]], [[compact element in a locale]].

[[!include locally presentable categories - table]]


## References

* [[Andrej Bauer]], [[Lars Birkedal]], [[Dana Scott]], _Equilogical Spaces_, Theoretical Computer Science, 315(1):35-59, 2004. ([web](http://math.andrej.com/2002/07/05/equilogical-spaces/)) 

* Olivia Caramello, _A topos-theoretic approach to Stone-type dualities_ ([arXiv:1103.3493](http://arxiv.org/abs/1103.3493))
 {#Caramello}

The relation to [[locally finitely presentable categories]] is discussed in

* [[Hans Porst]], _Algebraic lattices and locally finitely presentable categories_, Algebra Univers. **65**, 285–298 (2011). <https://doi.org/10.1007/s00012-011-0129-0> ([pdf](http://www.math.uni-bremen.de/~porst/dvis/PORST_AlgebraicLattices_revfinAU.pdf))
 {#Porst} 

That every algebraic lattice is a congruence lattice is proved in 

* G. Gr&#228;tzer and E. T. Schmidt, _Characterizations of congruence lattices of abstract algebras_, Acta Sci. Math. (Szeged) 24 (1963), 34&#8211;59.


[[!redirects algebraic lattice]]
[[!redirects algebraic lattices]]
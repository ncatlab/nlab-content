
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Cogroup objects#
* table of contents
{:toc}


## Idea ##

**Cogroup objects** are [[group object]] in an [[opposite category]], and often one takes the [[opposite category]] of group object in an opposite category to be the category of cogroup objects.  

The defining property of a cogroup object is that morphisms *out* of it form a [[group]].  Specifically, if $C$ is a category, then $G$ is a cogroup object in $C$ if $\operatorname{Hom}(G,X)$ is a group for any object $X$ in $C$ (and the group structure must be natural in $X$).

There are many examples of cogroup objects.  Perhaps the most well-known are the [[n-sphere]] in the [[homotopy category]] of [[pointed topological spaces]], $\operatorname{hTop}_*$.  Then the fact that $S^n$ is a cogroup object in $\operatorname{hTop}$ is precisely the statement that the [[homotopy group]] $\pi_n(X)$ for $n \geq 1$ is indeed a [[group]], naturally in $X$, for all topological spaces $X$.


## Definition ##

The basic definition is as follows.

+-- {: .num_defn}
###### Definition

Let $C$ be a category.  To give an object $G$ of $C$ a **cogroup structure** in $C$ is to give the functor $\operatorname{Hom}(G,-)$ a [[lift]] from $\operatorname{Set}$ to $\operatorname{Grp}$.

A **cogroup object** in $C$ is an object $G$ together with a choice of cogroup structure.

A **morphism of cogroup objects** $G_1 \to G_2$ is a morphism in $C$ between the underlying objects of the $G_i$ such that the [[natural transformation]] $\operatorname{Hom}(G_2,-) \to \operatorname{Hom}(G_1,-)$ lifts to a natural transformation of functors into $\operatorname{Grp}$.
=--

Thus cogroup objects and their morphisms can be thought of as the category of [[representable functors]] from $C$ to $\operatorname{Grp}$.

Providing $C$ has enough coproducts of $G$ (the $0,1,2,3$th copowers to be precise), the concept of a cogroup structure on $G$ can be internalised.

+-- {: .num_theorem}
###### Theorem
To give an object $G$ of $C$ a cogroup structure is equivalent to choosing morphisms $\mu \colon G \to G \amalg G$, $\eta \colon G \to 0_C$, and $\iota \colon G \to G$ satisfying the diagrams for associativity, unit, and inverse but _the other way around_.
=--

Here, the phrase "the other way around" means: take the normal diagrams for a [[group object]] that express the properties of associativity, unit, and inverses, invert all the arrows, and replace products by coproducts.


## Relationship To Group Objects ##

A cogroup object in a category, say $C$, is nothing more than a [[group object]] in the [[opposite category]]: $C^{op}$.  However, morphisms in the cogroup category go the other way around.  That is to say, with the obvious notation:

$$
C\operatorname{coGrp} = (C^{op}\operatorname{Grp})^{op}
$$


## Relationship to Other Objects ##

Of course, there is nothing special about groups here.  The same style of definition works for any [[variety of algebras]] in the sense of universal algebra, where $C coAlg_T \coloneqq (C^{op}Alg_T)^{op}$. 

Some terminological care should be taken in the case of [[comonoid]], which makes sense in any [[monoidal category]], not just cocartesian monoidal categories which is the general default environment for discussing co-$T$-algebras. Thus, check with the author to see which monoidal product is meant; in the case of comonoid it's likely that it's *not* the cocartesian notion that is intended. Whereas in the case of cogroups, confusion is not so likely: one needs the cocartesian structure (codiagonals, etc.) essentially because the axioms of a group involve duplication of variables, whereas this is not the case for axioms of a monoid. (Cf. the distinction between [[operad]] and [[Lawvere theory]], where the latter can be viewed as a kind of "cartesian operad".) 


## Examples ##

1. All [[n-spheres]] for all $n$ are cogroup objects in the [[homotopy category]] of [[based topological spaces]], $\operatorname{hTop}_*$.  

   This is the origin of the [[group]] structure on [[homotopy groups]]. it is also crucial in the structure of the [[Brown representability theorem]].

   The higher spheres are actually _abelian_ cogroup objects, as demonstrated by the fact that $\pi_n(X)$ is abelian for $n \ge 2$.


1. More generally, any [[suspension]] is a cogroup object with the "pinch" map as the comultiplication.  See at _[[suspensions are H-cogroup objects]]_. (Since the $0$-sphere is not a suspension in $\operatorname{hTop}_*$, but only in $\operatorname{hTop}$, it need not be a cogroup and in fact is not.)  This is dual to, and equivalent to, the statement that (based) [[loop spaces]] are group objects in $\operatorname{hTop}_*$ since there is an [[adjunction]], internal to $\operatorname{hTop}_*$:

   $$
   \operatorname{Hom}(\Sigma X,Y) \cong \operatorname{Hom}(X,\Omega Y)
   $$


1. There are examples of spaces that are cogroups in $\operatorname{hTop}_*$ that are **not** suspensions, see Bernstein & Harper _Cogroups which are not suspensions_.  Note that cogroups in $\operatorname{hTop}_*$ are the same as [[co-H-spaces]] which are additionally (co-)associative and have (co-)inverses.

1. Cogroup objects in the [[Grp|category of groups]] are [[free groups]], and to give a free group the structure of a cogroup object is the same a choosing a generating set.  This is an old result of [[Daniel Kan]].

1. On the other hand, every abelian group is again an abelian cogroup since $\operatorname{Ab}$ is self-enriched.  Indeed, in an [[abelian category]] every object is simultaneously an abelian group object and an abelian cogroup object.  In $\operatorname{Ab}$, the abelian cogroup object structure is unique, with comultiplication given by the [[diagonal morphism]].

1. In [[Set]], the only cogroup object (abelian or otherwise) is the [[empty set]].  This is because the counit map must be a morphism from $X$ to the terminal object _of the opposite category_.  In the case of $\operatorname{Set}$, this is the empty set.

1. This extends further: any category with a [[faithful functor]] to $\operatorname{Set}$ which preserves an [[initial object]] will have no non-trivial cogroup objects.  In particular, the category [[Top]] of *unbased* topological spaces has only the [[empty space]] as a cogroup object.

1. The case of cogroups, and some other co-things, in certain other varieties of algebras has been extensively studied by [Bergman & Hausknecht 1996](#BergmanHausknecht96).

   In particular, a co-group in the category of (unital) commutative rings is a commutative [[Hopf ring]] and a cogroup in the category of (unital) commutative $k$-algebras is a commutative [[Hopf algebra|Hopf]] $k$-algebra; a fact highlighted in homotopy theory by [[Haynes Miller]] (in view of his generalization to [[commutative Hopf algebroid]]s as cogroupoids in commutative algebra) in the context of discussion of [[dual Steenrod algebras]], see ([Ravenel 86, appendix A](#Ravenel86)) for review.

## References

Discussion of commutative [[Hopf algebras]] as cogroups:

* {#Ravenel86} [[Doug Ravenel]], appendix A1 of _[[Complex cobordism and stable homotopy groups of spheres]]_, Academic Press 1986

Cogroups [[internalization|internal to]] the category of (graded or not) [[associative algebras]] are very rare (unlike Hopf algebras) -- in fact the underlying algebras are free; this has been clear since

* Israel Berstein, On cogroups in the category of graded algebras. Trans. Amer. Math. Soc. 115 (1965), 257&#8211;269 [jstor](http://www.jstor.org/stable/1994268)

Monograph:

* {#BergmanHausknecht96} [[George M. Bergman]], Adam O. Hausknecht, _Cogroups and co-rings in categories of associative rings_, A.M.S. Math. Surveys and Monographs __45__ (1996) &lbrack;ISBN 0-8218-0495-2, [ams:surv-45](https://bookstore.ams.org/surv-45), [MR 97k:16001](http://www.ams.org/mathscinet-getitem?mr=97k:16001), [errata and updates](http://math.berkeley.edu/~gbergman/papers/updates/coalg.html)&rbrack;

 > (also for [[corings]])

This fact is later observed in greater generality

* [[Benoit Fresse]], _Cogroups in algebras over an operad are free algebras_, Commen. Math. Helv. __73__:4, 1998, 637-676
&lbrack;[doi](http://dx.doi.org/10.1007/s000140050072)



[[!redirects cogroups]]

[[!redirects co-H-object]]

[[!redirects cogroup object]]
[[!redirects cogroup objects]]

[[!redirects co-group object]]
[[!redirects co-group]]
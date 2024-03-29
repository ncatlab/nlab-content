
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--



# $E$-theory
* table of contents
{: toc}


## Idea

_$E$-Theory_ is the name of a [[category]] whose [[objects]] are [[C*-algebras]] and whose [[hom-sets]] are homotopy classes of slightly generalized $C*$-homomorphisms, called _[[asymptotic C*-homomorphisms]]_. These hom-sets have the structure of an [[abelian group]] and are also called the _E-groups_ of their arguments. Since under [[Gelfand duality]] [[C*-algebras]] may be thought of as exhibiting [[noncommutative topology]], one also speaks of _[[noncommutative stable homotopy theory]]_.

This construction may be understood as the universal improvement of [[KK-theory]] under [[excision]] ([Higson 90](#Higson90)). Accordingly, the $E$-groups behave like groups of a [[K-theory]]-like [[generalized cohomology theory]].

In terms of [[noncommutative topology]] (regarding, in view of [[Gelfand duality]], noncommutative [[C*-algebras]] as [[algebras of functions]] on "noncommutative topological spaces") one may understand this as dealing with "locally badly behaved space" such as certain [[quotients]] of [[foliations]] ([Connes-Higson 90](ConnesHigson90))
in a way that resembles a noncommutative version of [[shape theory]] ([D&#257;d&#257;rlat 94](#Dadarlat94)).

## Definition

First some notation and terminology.

For $A \in $ [[C*Alg]], we write

$$
  \Sigma A \coloneqq C_0((0,1),A)
$$

for the $C^\ast$-algebra of continuous $A$-valued functions on the open inverval [[vanishing at infinity]]. This is also called the _suspension_ of $A$.

For $A,B \in $ [[C*Alg]], write $[A,B]$ for the set of [[homotopy]]-[[equivalence classes]] of [[asymptotic C*-homomorphisms]]  $A \to B$. As discussed there

1. there is a natural [[composition operation]] $[A,B] \times [B,C] \to [A,C]$;

1. $[A,\Sigma B]$ is naturally an [[abelian group]].

Finally, write $\mathcal{K} \in $ [[C*Alg]] for the $C^\ast$-algebra of [[compact operators]] on an infinite-dimensional [[separable Hilbert space]]. For $A \in C^\ast Alg$ the [[tensor product of C*-algebras]] $A \otimes \mathcal{K}$ is also called the _stabilization_ of $A$.


+-- {: .num_defn }
###### Definition

For $A,B \in $ [[C*Alg]], the **E-group** of $A$ with [[coefficients]] in $B$ is

$$
  E(A,B) \coloneqq [(\Sigma A )\otimes \mathcal{K}, (\Sigma B) \otimes \mathcal{K}]
  \in Ab
  \,.
$$

Under the induced [[composition]] operation this yields an [[additive category]] $E$ whose [[objects]] are [[C*-algebras]], and whose [[hom-objects]] are $E(-,-)$.

=--

## Properties

### Universal characterization

E-theory is the [[universal construction|universal]] 
localization [[C*Alg]] $\to E$ which is homotopy-invariant, stable and preserves [[exact sequences]] in the middle.

(...)

### Relation to KK-theory
 {#RelationToKKTheory}

Because KK-theory is the universal _split exact_ (stable and homotopy-invariant) localization of [[C*Alg]], and E-theory the universal half-exact localization, and since every [[split exact sequence]] is in particular exact, there is a universal [[functor]] 

$$
  KK \to E
$$ 

from the [[KK-theory]] [[homotopy category]] to that of $E$-theory. 

Restricted to [[nuclear C*-algebras]] this is a [[full and faithful functor]]. ([Higson 90](#Higson90)) (...)

If in the definition of E-theory by [[asymptotic C*-homomorphisms]] one restricts to those which take values in contractive [[completely positive maps]], then the results is isomorphic to KK-theory again. (K. Thomsen, [Introduction, p. 34](#Introduction)). The above universal functor $KK \to E$ is then just the corresponding [[forgetful functor]].

It follows that the Kasparov product in [[KK-theory]] is equivalently given by the composition of the corresponding completely positive [[asymptotic C*-homomorphisms]].


## Related concepts

* [[KK-bootstrap category]]

[[!include noncommutative motives - table]]


## References

### General

The idea of E-theory was introduced in 

* [[Alain Connes]], [[Nigel Higson]], _D&#233;formations, morphismes asymptotiques et $K$-th&#233;orie bivariante_, C. R. Acad. Sci. Paris S&#233;r. I Math. __311__ (1990), no. 2, 101&#8211;106, [MR91m:46114](http://www.ams.org/mathscinet-getitem?mr=1065438), [pdf](ftp://ftp.bnf.fr/578/N5781521_PDF_107_112DM.pdf)
 {#ConnesHigson90}

* [[Nigel Higson]], _Categories of fractions and excision in KK-theory_ J. Pure Appl. Algebra, 65(2):119&#8211;138, (1990) ([pdf](http://www.math.psu.edu/higson/math/Papers_files/Higson%20-%201990%20-%20Categories%20of%20fractions%20and%20excision%20in%20KK-theory.pdf))
 {#Higson90}

Reviews and surveys include

* _Introduction to KK-theory and E-theory_, Lecture  notes (Lisbon 2009) ([pdf slides](http://oaa.ist.utl.pt/files/cursos/courseD_Lecture4_KK_and_E1.pdf))
 {#Introduction}

A standard textbook account is in section 25 of 

* [[Bruce Blackadar]], _[[K-Theory for Operator Algebras]]_

The [[stable homotopy theory|stable]] [[homotopy theory]] aspects are further discussed in

* Martin Grensing, _Noncommutative stable homotopy theory_ ([arXiv:1302.4751](http://arxiv.org/abs/1302.4751))


* Rasmus Bentmann, _Homotopy-theoretic E-theory and n-order_ ([arXiv:1302.6924](http://arxiv.org/abs/1302.6924))

See also


* web page of a project [Noncommutative topology - homotopy functors and E-theory ](http://www.math.ku.dk/~jg/papers/etheory.html)


* [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities and applications to topological $\mathbb{T}$-duality_  [pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf)
 {#Mahanta}

* [pdf](http://faculty.tcu.edu/epark/papers/ETheory_JFA.pdf)

### Relation to shape theory

Relation to [[shape theory]] is discussed in 

* [[Marius Dādārlat]], _Shape theory and asymptotic morphisms for $C^\ast$-algebras_, Duke Math. J. __73__ (3):687-711, 1994, [MR95c:46117](http://www.ams.org/mathscinet-getitem?mr=1262931), [pdf](http://www.math.purdue.edu/~mdd/Publications/shape.pdf)
 {#Dadarlat94}

* Vladimir Manuilov, Klaus Thomsen, _Shape theory and extensions of $C^\ast$-algebras_, ([arxiv/1007.1663](http://arxiv.org/abs/1007.1663))



[[!redirects E-theory]]

[[!redirects asymptotic morphism]]
[[!redirects asymptotic morphisms]]

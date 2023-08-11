
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Frobenius algebra
* table of contents
{: toc}

## Idea

A **Frobenius algebra** is a [[vector space]] that is both an [[algebra]] and a [[coalgebra]] in a compatible way.  This sort of compatibility is different (and more "topological") from that involved in a [[bialgebra]]/[[Hopf algebra]].  More generally, Frobenius algebras can be defined in any [[monoidal category]], and even in any [[polycategory]], in which case they are sometimes called **Frobenius monoids**.

Frobenius algebras have connections to [[TQFT]]s; for some more historical motivation see [this MO question](http://mathoverflow.net/questions/32193/why-did-people-originally-like-frobenius-algebras).


## Definition

There are a number of equivalent definitions of the concept of Frobenius algebra.

The original definition is an associative algebra with a suitable [[linear form]] on it.

* [As an associative algebra with linear form](#AsAssociativeAlgebraWithLinearForm).

In the context of [[2d TQFT]] what crucially matters is that this is equivalent to an associative algebra structure with a compatible coalgebra structure

* [As an associative algebra with compatible coalgebra structure](#AlgebraCoalgebra).

There are

* [Further equivalent definitions](#FurtherDefinition)

### As associative algebra with coalgebra structure
 {#AlgebraCoalgebra}

+-- {: .num_defn}
###### Definition
A Frobenius algebra in a [[monoidal category]] is a quintuple $(A, \delta, \epsilon, \mu, \eta)$ such that

1. $(A, \mu, \eta)$ is a [[monoid]] with multiplication $\mu:A\otimes A\to A$ and unit $\eta:I\to A$,
1. $(A, \delta, \epsilon)$ is a [[comonoid]] with comultiplication $\delta:A\to A\otimes A$ and counit $\epsilon:A\to I$, and
1. the **Frobenius laws** hold: $(1 \otimes \mu) \circ (\delta \otimes 1) = \delta \circ \mu = (\mu \otimes 1) \circ (1 \otimes \delta)$.
=--

In terms of [[string diagrams]], this definition says:

[[frobenius_algebra.jpg:pic]]

The first line here shows the associative law and left/right unit laws for a [[monoid]].  The second line shows the coassociative law and left/right counit laws for a [[comonoid]].  The third line shows the Frobenius laws.

In fact, although this seems rarely to be remarked, the two Frobenius laws can be replaced by the single axiom $(1 \otimes \mu) \circ (\delta \otimes 1) = (\mu \otimes 1) \circ (1 \otimes \delta)$.  Here is a proof in string diagram notation that this axiom implies $(1 \otimes \mu) \circ (\delta \otimes 1) = \delta \circ \mu$ (taken from [Pastro-Street 2008](#PastroStreet2008)):

[[frobenius_axioms_one_to_two.png:pic]]

Here the first and fifth steps use the counitality property of the comonoid structure, the second and fourth steps use the assumed axiom (once in each direction), and the third step uses coassociativity.


### As associative algebra with linear form
 {#AsAssociativeAlgebraWithLinearForm}

Frobenius algebras were originally formulated in the category [[Vect]] of [[vector spaces]] with the following equivalent definition:

+-- {: .num_defn}
###### Definition

A **Frobenius algebra** is a unital, [[associative algebra]] $(A, \mu, \eta)$ equipped with a linear form $\epsilon : A \rightarrow k$ such that $\epsilon\circ\mu$ is a non-degenerate pairing. I.e. the induced map

\[  u \mapsto (v\mapsto\epsilon\circ\mu(v \otimes u)) \]

is an [[isomorphism]] of $V$ with its [[dual vector space|dual space]] $V^*$. In such a case, $\epsilon$ is called a **Frobenius form**.

=--

From this definition it is easy to see that every Frobenius algebra in [[Vect]] is necessarily finite-dimensional.

### Further definitions
 {#FurtherDefinitions}

There are about a dozen equivalent definitions of a Frobenius algebra. [Ross Street (2004)](#Street2004) lists most of them.

## Types of Frobenius algebras

### Commutative Frobenius algebras ###

We can define 'commutative' Frobenius algebras in any [[symmetric monoidal category]].  Namely, a Frobenius algebra is **commutative** if its associated monoid is commutative --- or equivalently, if its associated comonoid is cocommutative.  

### Symmetric Frobenius algebras ###

We can define 'commutative' or 'symmetric' Frobenius algebras in any [[symmetric monoidal category]].  A Frobenius algebra $A$ is **symmetric** if 
$$\epsilon \mu \circ S_{A,A} = \epsilon \mu \, $$
where $S_{A,A} : A \otimes A \to A \otimes A$ is the symmetry, and $\epsilon\mu$ is the nondegenerate pairing induced as above from the multiplication and the counit.  Any commutative Frobenius algebra is symmetric, but not conversely: for example the algebra of $n \times n$ matrices with entries in a field, with its usual trace as $\epsilon$, is symmetric but not commutative when $n \gt 1$.  

A theorem of [Eilenberg & Nakayama (1955)](#Eilenberg1955) says that in the category [[Vect]] of [[vector spaces]] over a [[field]] $k$, an algebra $A$ can be equipped with the structure of a symmetric Frobenius algebra if (but not only if) it is **[[separable algebra|separable]]**, meaning that for any field $K$ [[field extension|extending]] $k$, $A \otimes_k K$ is a [[semisimple algebra|semisimple]] algebra over $K$.   

### Special Frobenius algebras ###

If $\mu \circ \delta = 1$, a Frobenius algebra is said to be **special**.   In the category of vector spaces, any element $a$ of an associative unital algebra gives a left multiplication map 
$$ \array{ 
L_a : &A &\to& A \\
      &b &\mapsto& a b 
}
$$
which in turn gives a bilinear pairing $g: A \times A \to k$ defined by
$$ g(a,b) = tr(L_a L_b) $$
One can show that the algebra $A$ can be equipped with the structure of a special Frobenius algebra if and only if $g$
is nondegenerate, i.e., if there is an isomorphism $A \to A^*$ given by
$$ a \mapsto g(a, -)  $$
In this case, there is just one way to make $A$ into a special Frobenius algebra, namely by taking the counit to be 
$$ \epsilon(a) = tr(L_a) $$
(In any Frobenius algebra, the unit, multiplication and counit determine the comultiplication.)  

In fact, all the results of the previous paragraph generalize to Frobenius algebras in any symmetric monoidal category, since the proofs can be done using string diagrams.  

An associative unital algebra for which the bilinear pairing $g$ is nondegenerate is called **strongly separable**.  So, any strongly separable algebra becomes a special Frobenius algebra in a unique way.  For more details, see [[separable algebra]] and [Aguiar (2000)](#Aguiar2000).

To get a feeling for some of the concepts we are discussing, an example is helpful.  The group algebra $k[G]$ of a finite group $G$ is always separable but strongly separable if and only if the order of $G$ is invertible in the field $k$.  By the results mentioned, this means that $k[G]$ can always be made into a symmetric Frobenius algebra, but only into a special Frobenius algebra when $|G|$ is invertible in $k$.

To see this, we can check that the group algebra $k[G]$ becomes a symmetric Frobenius algebra if we define the counit $\epsilon: k[G] \to k$ to pick out the coefficient of $1 \in G$:
$$   \epsilon : \sum_{g \in G} a_g \, g \mapsto a_1 \,. $$
But when $|G|$ is invertible in $k$, we can check that $k[G]$ becomes a _special_ symmetric Frobenius algebra if we normalize the counit as follows:
$$  \epsilon : \sum_{g \in G} a_g \, g \mapsto \frac{a_1}{|G|} \, .$$

We should warn the reader that [Rosebrugh et al (2005)](#Rosebrugh2005) call a special Frobenius algebra 'separable'. This usage conflicts with the standard definition of a [[separable algebra]] in the category of vector spaces over a field, so we suggest avoiding it.

### &#8224;-Frobenius algebras ###

If a Frobenius algebra lives in a monoidal [[†-category]], $(\delta)^\dagger = \mu$ and $(\epsilon)^\dagger = \eta$, then it is said to be a **&#8224;-Frobenius algebra**. These crop up in the theory of 2d [[TQFTs]], and also in the foundations of [[quantum mechanics in terms of dagger-compact categories|quantum theory]]. 

## Examples


(...)

## Properties 

### General


+-- {: .num_prop}
###### Proposition 
A Frobenius algebra $A$ in a [[monoidal category]] is an [[dual object|object dual]] to itself. 
=-- 

+-- {: .proof}
###### Proof 
Let $I$ be the [[monoidal unit]]. To say $A$ is dual to itself means there are maps $e: I \to A \otimes A$ and $p: A \otimes A \to I$ such that the [[triangle identities]] hold. The maps are defined by 
$$e = (I \stackrel{\eta}{\to} A \stackrel{\delta}{\to} A \otimes A), \qquad p = (A \otimes A \stackrel{\mu}{\to} A \stackrel{\epsilon}{\to} I)$$ 
and one of the [[triangle identities]] uses one of the Frobenius laws and unit and counit axioms to derive the following [[commutative diagram]]: 

$$\array{
A & \stackrel{1 \otimes \eta}{\to} & A \otimes A & \stackrel{1 \otimes \delta}{\to} & A \otimes A \otimes A \\
 & {}_1\searrow & \downarrow \mathrlap{\mu} & & \downarrow \mathrlap{\mu \otimes 1} \\
 & & A & \overset{\delta}{\to} & A \otimes A \\
 & &  & {}_{1}\searrow & \downarrow \mathrlap{\epsilon \otimes 1} \\
 & & & & A
} 
$$ 

The other [[triangle identity]] uses the other Frobenius law and unit and counit axioms.
 
=-- 

As a result, we see that in the monoidal category [[Mod|$Mod_k$]] of [[modules]] over a [[commutative ring]] $k$, Frobenius algebras $A$ considered as modules over $k$ are [[finitely generated module|finitely generated]] and [[projective module|projective]]. This is because $A \otimes_k -$, being [[adjoint functor|adjoint]] to itself, is a [[left adjoint]] and [[left adjoints preserve colimits|therefore preserves all colimits]]. That $A \otimes_k -$ preserves arbitrary small coproducts means $A$ is finitely generated over $k$, and that $A \otimes_k-$ preserves coequalizers means $A$ is projective over $k$. 

* Every Frobenius algebra $A$ is a [[quasi-Frobenius algebra]]: projective and injective left (right) modules over $A$ coincide. 

* Every Frobenius algebra $A$ is a [[pseudo-Frobenius algebra]]: $A$ is an injective cogenerator in the category of left (right) $A$-modules. 

Frobenius algebras are closely connected with [[ambidextrous adjunctions]]. For example, a **[[Frobenius monad]]** on a category $C$ is by definition a Frobenius monoid in the monoidal category of [[endofunctors]] on $C$ (with monoidal product given by endofunctor composition), and if we have a pair of [[adjunctions]] $F \dashv U$ and $U \dashv F$, then $M = U F$ carries a monad structure and a [[comonad]] structure and the Frobenius laws are satisfied, a fact most easily seen by using [[string diagrams]].  


### PROPs for Frobenius algebras

Certain kinds of Frobenius algebras have nice [[PROPs]] or [[PRO|PROs]].  The PRO for Frobenius algebras is the monoidal category of planar thick tangles, as noted by [Lauda (2006)](#Lauda2006) and illustrated here:

[[frobenius_algebra.jpg:pic]]


Lauda and Pfeiffer [Lauda (2008)](#Lauda2008) showed that the PROP for _symmetric_ Frobenius algebras is the category of 'topological open strings', since it obeys this extra axiom:

[[symmetric_frobenius_algebra_law.jpg:pic]]

The PROP for _commutative_ Frobenius algebras is [[2Cob]], as noted by many people and formally proved in ([Abrams (1996)](#Abrams1996)).  This means that any commutative Frobenius algebra gives a 2d [[TQFT]].  See [Kock (2006)](#Kock2006) for a history of this subject and [Kock (2004)](#Kock2004) for a detailed introduction.  In 2Cob, the circle is a Frobenius algebra.  The monoid laws look like this:

[[monoid_laws.jpg:pic]]

The comonoid laws look like this:

[[comonoid_laws.jpg:pic]]

The Frobenius laws look like this:

[[frobenius_laws.jpg:pic]]

and the commutative law looks like this:

[[commutative_law.jpg:pic]]

The PROP for _special_ commutative Frobenius algebras is Cospan(FinSet), as proved by Rosebrugh, Sabadini and Walters.  This is worth comparing to the PROP for commutative [[bialgebra|bialgebras]], which is Span(FinSet).  For details, see [Rosebrugh et al (2005)](#Rosebrugh2005), and also [Lack (2004)](#Lack2004).  

A special commutative Frobenius algebra gives a 2d TQFT that is insensitive to the genus of a 2-manifold, since in terms of pictures, the 'specialness' axioms $m \circ \delta = 1$ says that

[[special_law.jpg:pic]]

### Classification of 2d TQFT

[[!include 2d TQFT -- table]]

### Frobenius algebras in polycategories

In fact, Frobenius algebras can be defined in any [[polycategory]], and hence in any [[linearly distributive category]].  The essential point is that the monoidal structure used for the monoid structure could be different from the monoidal structure used for the comonoid structure, i.e. we could have $\mu:A\otimes A \to A$ but $\delta :A \to A \parr A$.  The compatibility between $\otimes$ and $\parr$ in a linearly distributive category (or between their "[[multicategory|multicategorical]]" analogues in a polycategory) is precisely what is required to write down the composites involved in the Frobenius laws.  For instance, we can have

$$ A\otimes A
\xrightarrow{1_A \otimes \delta}
A \otimes (A \parr A)
\xrightarrow{lin-distrib}
(A \otimes A) \parr A
\xrightarrow{\mu \parr 1_A}
A\parr A
$$

and one of the Frobenius laws says that this composite is equal to

$$ A \otimes A \xrightarrow{\mu} A \xrightarrow{\delta} A\parr A. $$

This is analogous to how a [[bimonoid]] can be defined in any [[duoidal category]].  In fact, it is a sort of [[microcosm principle]]; it is shown in [(Egger2010)](#Egger2010) that Frobenius monoids in the linearly distributive category [[Sup]] are precisely [[star-autonomous category|*-autonomous]] cocomplete [[posets]] (and hence, in particular, linearly distributive).

In polycategorical language we can give another [[unbiased]] definition of a  commutative Frobenius monoid: it is equipped with exactly one morphism $\overset{n}{\overbrace{(A,A,\dots,A)}} \to \overset{m}{\overbrace{(A,A,\dots,A)}}$ of each possible (two-sided) arity, such that any (symmetric) polycategorical composite of two such morphisms is equal to another such.  The monoid structure consists of the morphisms of arity $(2,1)$ and $(0,1)$, while the comonoid structure is the morphisms of arity $(1,2)$ and $(1,0)$, and the Frobenius relations say that three ways to compose these to produce a morphism of arity $(2,2)$ are equal.  (The morphism of arity $(0,0)$ is the composite $\epsilon\eta$; no axiom is required on it, because in a polycategory there is no other morphism $()\to ()$ to compare it to.)  In other words, the free symmetric polycategory containing a commutative Frobenius monoid is the [[terminal object|terminal]]  symmetric polycategory.  In this way Frobenius algebras are to polycategories in the same way that monoids are to multicategories.

+--{: .query}
[[Mike Shulman]]: I have not carefully checked the above statement, but it seems that the Frobenius laws should suffice to manipulate any such composite into any other.  Personal communications from other people who should know are in agreement.
=--


## Related concepts

* [[Frobenius monad]]

* [[Calabi-Yau algebra]]

* [[hypergraph category]]

* [[Frobenius pseudomonoid]]

## References ##

Frobenius algebras were introduced by [[Brauer]] and Nesbitt and were named after [[Ferdinand Frobenius]].

See for instance

* {#Eilenberg1955} [[Samuel Eilenberg]], [[Tadasi Nakayama]], _On the dimension of modules and algebras. II. Frobenius algebras and quasi-Frobenius rings_, _Nagoya Math. J._ **9** (1955) 1-16 &lbrack;[web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.nmj/1118799677)&rbrack;


* [[Marcelo Aguiar]] (2000), _A note on strongly separable algebras_, Bolet&#237;n de la Academia Nacional de Ciencias (C&#243;rdoba, Argentina), special issue in honor of Orlando Villamayor, **65**, 51--60.  ([pdf](http://www.math.cornell.edu/~maguiar/strongly.pdf))
{#Aguiar2000}

* [[Andrew Baker]], _Frobenius algebras_ 2010 ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/Frobenius-talk.pdf))

On the role of Frobenius algebras in [[2d TQFT]]:

* {#Abrams1996} [[Lowell Abrams]] , _Two-dimensional topological quantum field theories and Frobenius algebra_, _Jour. Knot. Theory and its Ramifications_ **5**, 569--587 (1996) ([ps](http://home.gwu.edu/~labrams/docs/tqft.ps))

* {#BaezTWF} [[John Baez]], This Week's Finds in Mathematical Physics, [week268](http://math.ucr.edu/home/baez/week268.html) and [week299](http://math.ucr.edu/home/baez/week299.html).

* {#Kock2004} [[Joachim Kock]], *Frobenius Algebras and 2d Topological Quantum Field Theories*, Cambridge U. Press (2004) &lbrack;[doi:10.1017/CBO9780511615443](https://doi.org/10.1017/CBO9780511615443), [webpage](http://mat.uab.cat/~kock/TQFT.html), [course notes pdf](http://mat.uab.es/~kock/TQFT/FS.pdf), [[Kock-FrobAlgTQFT-short.pdf:file]]&rbrack;

* {#Kock2006} [[Joachim Kock]], Remarks on the history of the Frobenius equation (2006) &lbrack;[web](http://mat.uab.es/~kock/TQFT.html#history)&rbrack;

* {#Lauda2006} [[Aaron Lauda]], Frobenius algebras and ambidextrous adjunctions, *Theory and Applications of Categories* **16** (2006) 84-122 &lbrack;[tac:16-04](http://tac.mta.ca/tac/volumes/16/4/16-04abs.html), [arXiv:math/0502550](http://arxiv.org/abs/math/0502550)&rbrack; 

  > (relating to [[ambidextrous adjunctions]] and [[Frobenius monads]])

* {#Lauda2008} [[Aaron Lauda]], [[Hendryk Pfeiffer]], Open-closed strings: two-dimensional extended TQFTs and Frobenius algebras, _Topology Appl._ **155** (2005) 623-666. &lbrack;[arXiv:0510664](http://arxiv.org/abs/math/0510664)&rbrack;


For applications in proof theory of classical and [[linear logic]] or linguistics:

* [[Martin Hyland]],  _Abstract Interpretation of Proofs: Classical Propositional Calculus_, pp. 6-21 in Marcinkowski, Tarlecki (eds.),  _Computer Science Logic (CSL 2004)_, LNCS **3210** Springer Heidelberg 2004. ([preprint](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2004/aap04.pdf))

* [[Richard Garner]], _Three investigations into linear logic_ , PhD report  Cambridge 2006. ([pdf](http://comp.mq.edu.au/~rgarner/Thesis/Smith-Knight-Essay.pdf))

* D. Kartsaklis, M. Sadrzadeh, S. Pulman,  [[Bob Coecke]], _Reasoning about meaning in natural language with compact closed categories and Frobenius algebras_ (2014). ([arXiv:1401.5980](https://arxiv.org/abs/1401.5980))

Frobenius algebras in linearly distributive categories are discussed in

* [[Jeff Egger]], *The Frobenius relations meet linear distributivity*, 2010 [TAC](http://tac.mta.ca/tac/volumes/24/2/24-02abs.html)
 {#Egger2010}

See also

* Aurelio Carboni (1991), Matrices, relations, and group representations, _Journal of Algebra_ **136** 2, 497--529.  ([pdf](https://www.sciencedirect.com/science/article/pii/002186939190057F))

* [[Bertfried Fauser]], _Some Graphical Aspects of Frobenius Structures_,  preprint (2012).  [arXiv:1202.6380](http://arxiv.org/pdf/1202.6380v1) 

* {#Lack2004} [[Stephen Lack]] (2004), Composing PROPs, _Theory and Applications of Categories_ **13**, 147--163.  ([web](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html))

* [[F. W. Lawvere]], _Ordinal Sums and Equational Doctrines_, pp. 141-155 in Eckmann (ed.), _Seminar on Triples and Categorical Homology Theory_, LNM **80** Springer Heidelberg 1969. ([TAC Reprint of vol. 80](http://www.tac.mta.ca/tac/reprints/articles/18/tr18.pdf)) 

* {#PastroStreet2008} Craig Pastro and [[Ross Street]], _Weak Hopf monoids in braided monoidal categories_, 2008, [arXiv:0801.4067](https://arxiv.org/abs/0801.4067)

* {#Rosebrugh2005} R. Rosebrugh, N. Sabadini and R.F.C. Walters (2005), Generic commutative separable algebras and cospans of graphs, _Theory and Applications of Categories_ **15** (Proceedings of CT2004), 164--177.  ([web](http://www.tac.mta.ca/tac/volumes/15/6/15-06abs.html))

* {#Street2004} [[Ross Street]] (2004), Frobenius monads and pseudomonoids, _J. Math. Phys._ **45**.  ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.91.2686))

* R. F. C. Walters, R. J. Wood, _Frobenius objects in Cartesian cicategories_, TAC **20** no. 3 (2008) 25--47. ([pdf](http://www.tac.mta.ca/tac/volumes/20/3/20-03.pdf))


category: algebra

[[!redirects Frobenius algebra]]
[[!redirects Frobenius algebras]]
[[!redirects Frobenius monoid]]
[[!redirects Frobenius monoids]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

There are many notions of a character for an algebraic structure, often topologized. 

### Character of a group
 {#CharacterOfAGroup}

For [[groups]], there are two different, but related, concepts which are both often just referred to as *characters* of a group:

1. *[multiplicative group characters](#MultiplicativeCharacterOfAGroup)*,

1. *[characters of linear representations of a group](#CharacterOfALinearRepresentation)*.

Here the first notion is the special case of the second notion for *1-[[dimension of a vector space|dimensional]]* [[linear representations]]. Since for [[abelian groups]] *all* [[irreducible representations]] over the [[complex numbers]] are 1-dimensional, in this case both notions agree, but in general they do not.

#### Multiplicative character of a group
 {#MultiplicativeCharacterOfAGroup}

A _multiplicative character_ on a ([[discrete group|discrete]]) [[group]] $G$ (a _[[group character]]_) is a [[group homomorphism]] from $G$ to the [[group of units]] $k^\times$ of the [[ground field]] $k$:

$$
  \chi
  \;\colon\;
  G 
    \longrightarrow 
  k^\times
$$


Since the [[codomain]] $k^\times$ is an [[abelian group]] we have that 

1. such a [[group homomorphism]] is [[invariant]] under [[conjugation]], so that a group character descends to a [[function]] on the [[set]] of [[conjugacy classes]] of elements in $G$.

1. the collection of characters is itself an [[abelian group]] under pointwise multiplication, this is called the _[[character lattice]]_ $Hom(G,k^\times)$ of the group. Similarly the **cocharacter lattice** is $Hom(k^\times, G)$.

For more see at _[[group character]]_.

For [[topological groups]] one considers [[continuous map|continuous]] characters. Specifically, for a [[locally compact Hausdorff]] group $G$ (often further assumed to be an [[abelian group]]), a __character__ of $G$ is a continuous homomorphism to the [[circle]] group $\mathbb{R}/\mathbb{Z}$. If $G$ is [[profinite group|profinite]], then this is the same as an continuous homomorphism to the [[discrete space|discrete]] group $\mathbb{Q}/\mathbb{Z}$.  (See [MO](http://mathoverflow.net/questions/86089/two-definitions-of-character-of-topological-groups).)


#### Character of a linear representation of a group
 {#CharacterOfALinearRepresentation}

In [[representation theory]], one defines the _[[character of a linear representation]]_ $\rho\colon G\to End(V)$ to be the [[group character]] on $G$ given by $g \mapsto Tr \rho(g)$, whenever the [[trace]] in $V$ makes sense (e.g. when $V$ is [[finite-dimensional vector space|finite-dimensional]]).  Since such a function is [[invariant]] under [[conjugation action|conjugation]], one may equivalently consider it a function on the set of [[conjugacy classes]] of elements in $G$.

Sometimes we also extend a character linearly to the [[linear span|free vector space]] on the set of conjugacy classes.  This version of the character can be identified with the [[bicategorical trace]] of the identity map of the representation, considered as a $k[G]$-$k$-module.

There is a different notion of an _infinitesimal character_ in [[Harish–Chandra theory]] and also a notion of the _formal character_.

There are important formulas concerning characters in representation theory, like [[Weyl character formula]], Kirillov character formula, Demazure character formula and so on.  There is also a formula for the [[induced character]] of an [[induced representation]].

### Left and right characters on a ring over a ring

Let $A$ be a unital, not necessarily commutative, [[ring]] (or, more generally, $k$-algebra for $k$-commutative); then a monoid in a category of $A$-bimodules (which are respectively also compatibly $k$-modules), is called an $A$-ring. In other words an $A$-ring $B$ is an object in the [[coslice category]] $A\Ring$; it is thus a ring $B$ equipped with multiplication $\mu_B$ and a map $\eta: A\to B$ of rings. 

A __left character__ of an $A$-ring $(B,\mu_B,\eta_B)$ is a map $\chi:B\to A$ such that 

(i) (left $A$-linearity) 
$\chi(\eta(a)b) = a\chi(b)$ for all $a\in A$, $b\in B$ 

(ii) (associativity) $\chi(b b') = \chi(b (\eta\circ\chi)(b'))$ for all $b,b'\in B$

(iii) (unitality) $\chi(1_B) = \chi(1_A)$ 

where we denoted multiplication in $A$ and in $B$ by concatenation. The conditions on $\chi$ can be restated as 
the requirement that the map $B\otimes A\to A$ given by 
$b\otimes a\mapsto \chi(b\eta(a))$ is a $B$-action extending 
the left regular $A$-action (i.e. the multiplication on $A$ 
considered as a left action).

Dually, a __right character__ of an $A$-ring $(B,\mu_B,\eta_B)$ is a map $\chi:B\to A$ such that 

(i) (right $A$-linearity) 
$\chi(b\eta(a)) = \chi(b)a$ for all $a\in A$, $b\in B$ 

(ii) (associativity) $\chi(b b') = \chi((\eta\circ\chi)(b) b')$ for all $b,b'\in B$

(iii) (unitality) $\chi(1_B) = \chi(1_A)$ 

This is in turn equivalent to extending the right regular action of $A$ to the action of $B$ on $A$.


### Character of a topological space

The character $\chi(X,x)$ of a [[topological space]] $X$ at a point $x$ is the minimal cardinality of a local basis of neighborhoods of point $x$ (local [[topological basis|basis of topology]] on $X$) if it is infinite and aleph zero otherwise. The character of a topological space is the supremum of $\chi(X,x)$ when $x$ runs through $X$. 

## Properties

* [[characters are cyclotomic integers]]

## Examples
 {#Examples}

* [[character table of 2D4=Dic2=Q8]]

* [[character table of 2T]]

* [[character table of 2O]]

* [[character table of 2I]]

* [[character table of GL(2,3)]]



## Related concepts

* [[irreducible character]]

* [[Weyl character formula]]

* [[Kac character formula]]

* [[Kac-Weyl character]]

* [[Cheeger-Simons differential character]]

* [[Chern root]], [[splitting principle]]

* [[character ring]]

* [[table of marks]]

## References

Character rings of [[compact Lie groups]] are discussed in 

* [[Graeme Segal]], _The representation ring of a compact Lie group_, Publications Math&#233;matiques de l'Institut des Hautes &#201;tudes Scientifiques
January 1968, Volume 34, Issue 1, pp 113-128 ([NUMDAM](http://archive.numdam.org/numdam-bin/fitem?id=PMIHES_1968__34__113_0))

* Masaru Tackeuchi, _A remark on the character ring of a compact Lie group_, J. Math. Soc. Japan Volume 23, Number 4 (1971), 555-705 ([Euclid](http://projecteuclid.org/euclid.jmsj/1259849785))

* Troels Roussauc Johansen, _Character Theory for Finite Groups and Compact Lie Groups_ [pdf](http://www.math.upb.de/~johansen/character-theory.pdf)

Discussion in the more general context of [[equivariant cohomology|equivariant]] [[complex oriented cohomology theory]] ([[transchromatic character]]) is in 

* [[Michael Hopkins]], [[Nicholas Kuhn]], [[Douglas Ravenel]], _Generalized group characters and complex oriented cohomology theories_, J. Amer. Math. Soc. 13 (2000), 553-594 ([publisher](http://www.ams.org/journals/jams/2000-13-03/S0894-0347-00-00332-5/), [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/hkr.pdf))

for review see

* {#Raksit15} Arpon Raksit, _Characters in global equivariant homotopy theory_, 2015 [pdf](http://web.stanford.edu/~arpon/math/files/senior-thesis.pdf)


Examples of [[characters of linear representations]] of [[finite groups]] are discussed and listed at 

* {#Montaldi08} James Montaldi, _[representations](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/Representations)_, 2008


[[!redirects character]]
[[!redirects characters]]

[[!redirects character ring]]
[[!redirects character rings]]





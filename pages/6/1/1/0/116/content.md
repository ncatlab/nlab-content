
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

## Definition ##

Classically, a **group** is a [[monoid]] in which every element has an [[inverse]] (necessarily unique). When written with a view toward [[group objects]] (see Internalization below), one should rather say that a group is a monoid together with an inversion operation. 

An **[[abelian group]]** is a group in which moreover the order in which two elements are multiplied is irrelevant.

## Delooping ##

To some extent, a group "is" a [[groupoid]] with a single object, or more precisely a [[pointed object|pointed]] groupoid with a single object.

The [[delooping]] of a group $G$ is a [[groupoid]] $\mathbf{B} G$ with 

* $Obj(\mathbf{B}G) = \{\bullet\}$ 

* $Hom_{\mathbf{B}G}(\bullet, \bullet) = G$.

Since for $G, H$ two groups, [[functors]] $\mathbf{B}G \to \mathbf{B}H$ are canonically in bijection with group homomorphisms $G \to H$, this gives rise to the following statement:

Let [[Grpd]] be the 1-[[category]] whose objects are [[groupoids]] and whose [[morphisms]] are [[functors]] (discarding the [[natural transformations]]). Let [[Grp]] be the category of groups. Then the [[delooping]] functor

$$
  \mathbf{B} : Grp \to Grpd
$$

is a [[full and faithful functor]]. In terms of this functor we may regard groups as the full [[subcategory]] of groupoids on groupoids with a single object.

It is in this sense that a group really is a groupoid with a single object.

But notice that it is unnatural to think of [[Grpd]] as a 1-category. It is really a [[2-category]], namely the sub-2-category of [[Cat]] on groupoids.

And the category of groups is _not_ equivalent to the full sub-2-category of the 2-category of groupoids on one-object groupoids. 

The reason is that two functors:

$$
  \mathbf{B}f_1, \mathbf{B}f_2 : \mathbf{B}G \to \mathbf{B}H
$$ 

coming from two group homomorphisms $f_1, f_2 : G \to H$ are related by a [[natural transformation]] $\eta_h : \mathbf{B}f_1 \to \mathbf{B}f_2$ with single component $\eta_h : \bullet \mapsto h \in Mor(\mathbf{B} H)$ for each element $h \in H$ such that the homomorphisms $f_1$ and $f_2$ differ by the [[inner automorphism]] $Ad_h : H \to H$

$$
  (\eta_h : \mathbf{B}f_1 \to \mathbf{B}f_2)
  \Leftrightarrow 
  (f_2 = Ad_h \circ f_1)
  \,.
$$

To fix this, look at the category of [[pointed object|pointed]] groupoids with [[pointed functor|pointed functors]] and pointed natural transformations.  Between group homomorphisms as above, only identity transformations are pointed, so $Grp$ becomes a full sub-$2$-category of $Grpd_*$ (one that happens to be a $1$-[[1-category|category]]).  (Details may be found in the appendix to [[Lectures on n-Categories and Cohomology]] and should probably be added to [[pointed functor]] and maybe also [[k-tuply monoidal n-category]].)


## Generalizations

### Internalization 

A **[[group object]]** [[internalization|internal to]] a [[category]] $C$ with finite [[product|products]] is an object $G$ together with maps $mult:G\times G\to G$, $id:1\to G$, and $inv:G\to G$ such that various diagrams expressing associativity, unitality, and inverses commute.

Equivalently, it is a functor $C^{op}\to Grp$ whose underlying functor $C^{op} \to Set$ is [[representable functor|representable]].

For example, a group object in [[Diff]] is a [[Lie group]].  A group object in [[Top]] is a [[topological group]].  A group object in [[Sch/S]] (the category or [[relative schemes]]) is an $S$-[[group scheme]].  And a group object in $CAlg^{op}$, where [[CAlg]] is the category of [[commutative algebras]], is a (commutative) [[Hopf algebra]].

A group object in [[Grp]] is the same thing as an abelian group (see [[Eckmann-Hilton argument]]), and a group object in [[Cat]] is the same thing as an [[internal category]] in [[Grp]], both being equivalent to the notion of [[crossed module]]. 

### In higher categorical and homotopical contexts

Internalizing the notion of _group_ in [[higher category theory|higher categorical]] and [[homotopy theory|homotopical]] contexts yields various generalized notions. For instance

* a [[2-group]] is a group object in [[Grpd]]

* an [[n-group]] is a group object internal to [[n-groupoid]]s

* an [[∞-group]] is a [[group object in an (∞,1)-category]].

* a [[loop space]] is a group object in [[Top]]

* generally there is a notion of [[groupoid object in an (infinity,1)-category|group object in an (infinity,1)-category]].

And the notion of [[loop space object]] and [[delooping]] makes sense (at least) in any [[(infinity,1)-category]].

Notice that the relation between group objects and deloopable objects becomes more subtle as one generalizes this way. For instance not every [[groupoid object in an (infinity,1)-category|group object in an (infinity,1)-category]] is [[delooping|deloopable]]. But every group object in an [[(infinity,1)-topos]] is.


### Weakened axioms

Following the practice of [[centipede mathematics]], we can remove certain properties from the definition of group and see what we get:

* remove inverses to get [[monoids]], then remove the identity to get [[semigroups]];
* or remove associativity to get [[loop (algebra)|loops]], then remove the identity to get [[quasigroups]];
* or remove all of the above to get [[magma|magmas]];
* or instead allow (in a certain way) for the binary operation to be partial to get [[groupoids]], then remove inverses to get [[categories]], and then remove identities to get [[semicategory|semicategories]]
* etc.

## Examples

### Special types and classes

* [[simple group]]

* [[finite group]], [[progroup]]

  * [[classification of finite simple groups]]

  * [[sporadic finite simple groups]]

* [[abelian group]]

  * [[finite abelian group]]

* [[divisible group]]

* [[acyclic group]]

* [[topological group]]

  * [[discrete group]]

  * [[Kac-Moody group]]

* [[Lie group]]

* [[group of Lie type]]

### Concrete examples

Standard examples of [[finite group]]s include

* [[group of order 2]] $\mathbb{Z}_2$

* [[symmetric group]] $\Sigma_n$

* [[cyclic group]]

* [[braid group]] $Br_n$

* [[Monster group]]

Standard examples of non-finite groups include

* group of [[integer]]s $\mathbb{Z}$ (under [[addition]]);

* group of [[real number]]s without 0 $\mathbb{R}\setminus \{0\}$ under [[multiplication]].

* [[Prüfer group]]

Standard examples of [[Lie groups]] include

* [[orthogonal group]]

* [[unitary group]]

* [[Spin group]], [[spin^c group]]

Standard examples of [[topological group]]s include

* [[string group]]

### Counterexamples

For more see [[counterexamples in algebra]].

1. A non-[[abelian group|abelian]] [[group]], all of whose [[subgroup]]s are [[normal subgroup|normal]]:

   $$
   Q \coloneqq \langle a, b | a^4 = 1, a^2 = b^2, a b = b a^3 \rangle
   $$

1. A [[finitely presented group|finitely presented]], infinite, [[simple group]]

   [[Thomson's group]] T.

1. A [[group]] that is not the [[fundamental group]] of any [[3-manifold]].

   $$
   \mathbb{Z}^4
   $$

1. Two [[finite group|finite]] non-[[isomorphism|isomorphic]] groups with the same [[order profile]].

   $$
   C_4 \times C_4, \qquad C_2 \times \langle a, b, | a^4 = 1, a^2 = b^2, a b = b a^3 \rangle
   $$

1. A counterexample to the converse of [[Lagrange's theorem]].

   The [[alternating group]] $A_4$ has order $12$ but no [[subgroup]] of order $6$.

1. A [[finite group]] in which the product of two [[commutator]]s is not a commutator.

   $$
   G = \langle (a c)(b d), (e g)(f h), (i k)(j l), (m o)(n p), (a c)(e g)(i k), (a b)(c d)(m o), (e f)(g h)(m n)(o p), (i j)(k l)\rangle \subseteq S_{16}
   $$

## Related concepts

* [[2-group]]

* [[n-group]]

* [[∞-group]]

* [[monoid]], [[monoid object]],

* **group**, [[group object]]

  * [[discrete group]]

    * [[order of a group]]
  
      * [[p-primary group]]

    * [[finite group]], [[profinite group]]

  * [[subgroup]]

    * [[torsion subgroup]]

    * [[stabilizer]],  [[centralizer]], [[normalizer]]

  * [[isogeny]]

  * [[coset]], [[coset space]]

  * [[abelian group]], [[anabelian group]], 

    * [[group completion]]

  * [[group commutator]], [[commutator subgroup]], [[abelianization]]

  * [[group character]]

  * [[group cohomology]]

  * [[group extension]]

  * [[normed group]], [[bornological group]]

  * [[topological group]], [[Lie group]], 

  * [[loop group]]

  * [[cogroup]]

  * is a commutative pregroup as mentioned in [[pregroup grammar]]

* [[ring]], [[ring object]]

* [[automorphism group]], [[automorphism 2-group]], [[automorphism ∞-group]],

  * [[group of bisections]]

* [[center]], [[center of an ∞-group]],

* [[inner automorphism group]]

* [[outer automorphism group]], [[outer automorphism ∞-group]]

* [[group presentation]]


## References

The original article that gives a definition equivalent to the modern definition of a group is

* [[Heinrich Weber]], Beweis des Satzes, dass jede eigentlich primitive quadratische Form unendlich viele Primzahlen darzustellen fähig ist. Mathematische Annalen 20:3 (1882), 301–329.  [doi](http://dx.doi.org/10.1007/bf01443599).


[[!redirects groups]]

category: group theory
#Idea#

A _category of fibrant objects_ is a [[category with weak equivalences]] equipped with extra structure somewhat weaker than that of a [[model category]]. 

The extra structure of fibrations _and_ cofibrations in a [[model category]] is, while convenient if it exists, not carried by many [[category with weak equivalences|categories with weak equivalences]] which still admit many constructions in [[homotopy theory]]. These are notably categories of [[presheaf|presheaves]] with values in a [[model category]]. 

A _category with fibrant objects_ is essentially like a [[model category]] but with all axioms concerning the cofibrations dropped, while at the same time assuming that all object are fibrant (hence the name). It turns out that this is sufficient for many useful constructions. In particular, it is sufficient for giving a convenient construction of the [[homotopy category]] in terms of [[span]]s of length one. This makes categories of fibrant objects useful in [[homotopical cohomology theory]].

#Definition#

A **category with fibrant objects** $C$ is a [[category with weak equivalences]] equipped with a further subcollection of its collection of morphisms called _fibrations_. (As usual, those morphisms which are both weak equivalences and fibrations are called _acyclic fibrations_.) 

This data has to satisfy the following properties:

* $C$ has finite [[product]]s;

* $C$ has a [[terminal object]];

* fibrations are preserved under [[pullback]];

* acyclic fibrations are preserved under [[pullback]];

* for every object there exists a [[path object]];

* all objects are _fibrant_, i.e. all morphisms to the terminal object are fibrations.


#Example#

* The tautological example is the [[full subcategory]] of any [[model category]] on all objects which are fibrant. 

* The category of [[sheaf|sheaves]] with values in [[simplicial set|simplicial sets]] which are [[stalk]]wise [[Kan complex|Kan complexes]] with fibrations and weak equivalences those morphisms of sheaves which are [[stalk]]wise fibrations and weak equivalences in the [[model structure on simplicial sets]].


#Useful properties of categories of fibrant objects#

In a category of fibrant objects, the following is true:

## Pullback of weak equivalences ##

While weak equivalences are not preserved generally under pullback,  they are preserved under pullback along fibrations.


## Path objects are replacements ##

For $B$ any object and $B^I$ its path object, the morphisms

$$
  d_0, d_1 : B^I \to B
$$

are acyclic fibrations.

## Factorization lemma ##

Every morphism $a \stackrel{f}{\to} b$ in a category of fibrant objects can be factored as

$$
  \array{
    && c
    \\
    & {}^\pi \swarrow && \searrow^{\hat f}
    \\
    a &&\stackrel{f}{\to}&& b
  }
$$

where 

* $\hat f$ is fibration;

* $\pi$ is 
 
  * an _acyclic_ fibration 

  * which admits a section $s : a \to c$.


This is the analog of the _factorization axiom_ in a [[model category]] which says that every map factors as an acyclic cofibration followed by a fibration.

Notice that this in particular implies that every weak equivalence is given by a span of acyclic fibrations. In the context of [[Lie groupoid]] theory these are known as the [[Morita equivalence]]s between groupoids. (And groupoids indeed form a category of fibrant objects for instance with respect to the Brown-Golasinski [[folk model structure]]).


## The homotopy category ##

The [[homotopy]] category of a category of fibrant objects has a simple characterization:

Let first $\pi C$ be the category with the same objects as $C$ and which $Hom_{\pi C}(A,B)$ equal to the quotient of $Hom_C(A,B)$ by the equivalence relation $f \sim g$ if there is a weak equivalence $t : A' \to A$ such that there is a [[homotopy|right homotopy]] from $f \circ t$ to $g \circ t$.

Then

+-- {: .un_theorem}
###### Theorem

The [[homotopy category]] $Ho_C$ of the category $C$ of fibrant objects is characterized by
$$
  Hom_{Ho_C}(A,B) \simeq colim_{A'} Hom_{\pi C}(A',B)  
  \,,
$$
where the colimit is taken over all weak equivalences $t : A' \to A$.
=--

### Remark ###

By the factorization lemma above (and using 2-out-of-3 valid in any [[category with weak equivalences]]) it follows that inverting just the acyclic fibrations in $C$ is already equivalent to inverting all weak equivalences. This means that the above theorem remains valid if the weak equivalences $t : A' \to A$ are replaced by _acyclic fibrations_.

Using acyclic fibrations here has the advantage that these are preserved under [[pullback]]. This allows to consistently compose spans whose left leg is an acyclic fibration by [[pullback]]. See [[homotopical cohomology theory]] and [[anafunctor]].

A discussion of this point of using weak equivalences versus acyclic fibrations in the construction of the homotopy category is also in Jardine: [Cocycle categories](http://www.math.uiuc.edu/K-theory/0782/).


# Pointed category of fibrant objects #

If the category $C$ of fibrant objects has an initial object which _coincides_ with the terminal object $e$, i.e. a [[zero object]], then $C$ is a [[pointed category]]. In this case we have the following additional concepts and structures.

## Fibers ##

 For $p : Y \to X$ a fibration, the pullback $F$ in

$$
  \array{
     F &\stackrel{i}{\to}& Y
     \\
     \downarrow && \downarrow
     \\
     e &\to& X
  }
$$

is the **fibre** of $p$ and $i$ is the _fibre inclusion_.
(This is the _kernel_ of the morphism $f$ of [[pointed object]]s)


## Loop object ##

For $B$ any object and $B^I$ any of its [[path object]]s, the fiber of $B^I \stackrel{d_0 \times d_1}{\to} B \times B$ is the **loop object** $\Omega^{(I)} B$ of $B$ with respect to the chosen path object. This construction becomes independent up to canonical isomorphism of the chosen path space after mapping to the [[homotopy category]] and hence there is a functor

$$
  \Omega : Ho_C \to Ho_C
$$

which sends any object $B$ of $C$ to its canonical loop object $\Omega B$.

Any loop object $\Omega B$ becomes a group object in $Ho_C$, i.e. a group [[internalization|internal to]] $Ho_C$ in a natural way.






#References#

The notion of _category of fibrant objects_ was introduced and the above results obtained in

* Kenneth S. Brown, _[[BrownAbstractHomotopyTheory.pdf:file]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458 ([[BrownAHT]]).

for application to [[homotopical cohomology theory]].

A review is in [section I.9](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi) of 

* Goerss, Jardine, _Simplicial homotopy theory_ .
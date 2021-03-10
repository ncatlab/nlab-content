
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A *direct category* is a [[category]] in which the morphisms only go in "one direction."

A direct category can be thought of as a category of [[geometric shapes for higher structures]] which includes only the "inclusions of faces," not any "degeneracy" maps.  (The more general notion of [[Reedy category]] can also include degeneracies.)  The objects of a direct category admit no nontrivial automorphisms, but the notion can also be generalized to allow for such automorphisms.

Alternately, a direct category can be thought of as a combinatorial representation of a *single* geometric shape.  In this case, each object is a "face" and each morphism is the inclusion of a lower-dimensional face in a higher-dimensional one.  If $D$ is a direct category regarded as a category *of* geometric shapes, then each $d\in D$ can be represented by the [[slice category]] $D/d$, a direct category regarded as a single geometric shape.  (In general, however, $D/d$ may admit more automorphisms than $d$, so it may need to be equipped with a "labeling" or "orientation" to truly recapture the shape $d$.)

Finally, a direct category can also be thought of as a [[categorification]] of the notion of [[well-founded relation]] from [[posets]] to [[categories]].

## Definition

### Standard definition

A category $D$ is a **direct category** if the following *equivalent* conditions are satisfied.

* $D$ contains no infinite descending chains of nonidentity morphisms $\cdots \to\cdot \to\cdot\to\cdot$ (including cycles of length $\gt 0$).
* The relation $a\prec b$ on $ob(D)$ defined by "there exists a nonidentity morphism from $a$ to $b$" is [[well-founded relation|well-founded]].
* There exists a function $d\colon ob(D)\to Ord$, where $Ord$ is the class of [[ordinals]], such that every nonidentity morphism of $D$ raises the degree.
* There exists an identity-reflecting functor (that is, it maps a morphism to an identity if and only if the morphism is itself an identity) $d : D\to \mathbf{Ord}$, where $\mathbf{Ord}$ is the large poset of ordinals viewed as a category.
* $D$ is a [[Reedy category]] (in particular an _[[elegant Reedy category]]_) in which $D_-$ consists only of identity maps (or equivalently $D_+$ is all of $D$).

In particular, a [[poset]] is a direct category just when its strict order relation $\lt$ is well-founded.  Thus, direct categories can be seen as a categorification of well-founded relations.

If $D^{op}$ is a direct category, then we say that $D$ is an **inverse category**.


### Direct versus one-way categories

Of course, a direct category can have no nonidentity [[endomorphisms]], since any such endomorphism would be a cycle of length 1.  A category with this property is sometimes called a **one-way category**.

A direct category is also necessarily [[skeleton|skeletal]], since any nonidentity isomorphism and its inverse would form a cycle of length 2.  The notion of generalized direct category, below, relaxes this requirement.

Conversely, a skeletal one-way category can have no cycles of nonidentity morphisms of any finite length, since by the one-way property all morphisms in such a cycle would be isomorphisms, hence endomorphisms by skeletality, and hence identities by the one-way property.  Since any infinite chain in a [[finite category]] contains a cycle, we see that

* A finite category is a direct category if and only if it is one-way and skeletal.

Since this condition is self-dual, we also see that

* A finite category is direct if and only if it is inverse.

An infinite category can be one-way and skeletal without being direct or inverse, such as the [[poset]] $\mathbb{Z}$ with its usual ordering.  However, if it additionally has **finite fan-out**, meaning that for each object $x$ there are altogether only finitely many morphisms with [[source]] $x$ (and arbitrary target), then it must be an inverse category, for any infinite non-cyclic chain would induce infinitely many distinct morphisms out of any of its objects by composition.  In [[FOLDS]], skeletal one-way categories with finite fan-out are called **simple categories** and used as signatures; thus

* Any simple category (in the sense of FOLDS) is an inverse category.

However, a category can be inverse without having finite fan-out.  Let $S$ be an infinite set and consider the poset $S \cup \{\infty\}$, with $S$ having the discrete ordering (no nonidentity arrows) and $\infty$ being less than every element of $S$.  This does not have finite fan-out, since $\infty$ is the source of infinitely many distinct arrows, but it is inverse, since there are clearly no chains of nonidentity arrows of length $\gt 1$.

### Allowing automorphisms

Some categories of geometric shapes, such as the [[tree category]] $\Omega$ and the [[cycle category]] $\Lambda$, include automorphisms of their objects.  By analogy with the notion of [[generalized Reedy category]], we can define $D$ to be a **generalized direct category** by replacing "identity" with "isomorphism" in the above definition.  Thereby we obtain the following equivalent conditions for $D$ to be a generalized direct category.

* $D$ contains no infinite descending chains of noninvertible morphisms $\cdots \to\cdot \to\cdot\to\cdot$.
* The relation $a\prec b$ on $ob(D)$ defined by "there exists a noninvertible morphism from $a$ to $b$" is [[well-founded relation|well-founded]].
* There exists a function $d\colon ob(D)\to Ord$, where $Ord$ is the class of [[ordinals]], such that every noninvertible morphism of $D$ raises the degree.
* $D$ is a [[generalized Reedy category]] in which $D_-$ consists only of isomorphisms (or equivalently $D_+$ is all of $D$).

Of course, $\Omega$ and $\Lambda$ are not generalized direct categories themselves, since they have degree-lowering degeneracies as well, but their full subcategories of coface maps are generalized-direct.  More generally:

* If $R$ is any generalized Reedy category, then $R_+$ is a generalized direct category.

## Properties

### Model structures

Every direct category (and every inverse category) is in particular a [[Reedy category]], in fact an _[[elegant Reedy category]]_. Therefore whenever $M$ is a [[model category]] there is a [[Reedy model structure]] on $M^D$.  In the case of direct and inverse categories, these model structures are even easier to describe, since either the latching or the matching objects are degenerate.



## Examples

### Inside the simplex category

The [[wide subcategory]] $\Delta_+$ of the [[simplex category]] on the injective maps is direct. That is, the category with objects being the totally ordered sets $\{0\}, \{0, 1\}, \{0, 1, 2\}...$, and the morphisms being injective order-preserving maps. Its [[presheaves]] are [[semi-simplicial objects]]/[[semi-simplicial sets]] as opposed to [[simplicial objects]]/[[simplicial sets]].

### The direct category of corollas

We now define a "[[universal property|universal]]" generalized direct category which contains "all" [[geometric shapes for higher structures]].  This is based on ([Borisov](#Borisov)).


A functor $f\colon D\to E$ between generalized direct categories is called a **dependency** if it is equivalent to the inclusion of a [[sieve]], or equivalently if it is a [[fully faithful functor]] and a [[discrete fibration]] in the generalized sense of Street.  If $D$ and $E$ are [[skeleton|skeletal]] (as they must be if they are *non-generalized* direct categories), then any dependency must be isomorphic to the inclusion of a sieve.  One also usually works only with skeletal generalized direct categories, although the definition does not require it.

If we regard direct categories as a categorification of well-founded relations, then dependencies are a categorification of injective [[simulation]]s, i.e. the inclusions of initial segments.

Define a **corolla** to be a generalized direct category with a [[weak limit|weakly]] [[terminal object]]; we call this object the **vertex** of the corolla.  If a generalized direct category is finite and skeletal, then it is a corolla if and only if it has a unique object which is not the source of any noninvertible morphism.  Corollas are the direct categories which it is most natural to regard as *single* geometric shapes; other direct categories are more like "pasting diagrams" of geometric shapes.

Let $Corolla$ be the category of [[small category|small]] skeletal corollas and dependencies.

+-- {: .num_theorem #UnivDirect}
###### Theorem
$Corolla$ is a (large) generalized direct category.
=--
+-- {: .proof}
###### Proof
Suppose that $\cdots \overset{d_2}{\to} C_2 \overset{d_1}{\to} C_1 \overset{d_0}{\to} C_0$ is a descending chain of noninvertible dependencies.  Any dependency whose target is a corolla and whose image contains the vertex must be an equivalence, and hence an isomorphism if the corollas are skeletal; thus none of the dependencies $C_{n+1} \to C_{n}$ can have the vertex in their image.  Let $c_n\in C_0$ be the image of the vertex $\star_n \in C_n$ under the composite $d_0\circ \dots \circ d_{n-1}$.  Then we have a noninvertible morphism $c_{n+1} \to c_n$ for each $n$, arising from some map $d_n(\star_{n+1}) \to \star_n$ which exists since $\star_n$ is weakly terminal.  This is a contradiction, since $C_0$ is a generalized direct category.
=--

Of course, the same is true for any subcategory of $Corolla$.  In particular, it is very natural to consider only the category $FinCorolla$ of *finite* corollas, which is moreover essentially small (though not finite).

We next observe that $Corolla$ is the "universal" generalized direct category in a certain sense.  Let $D$ be any generalized direct category; then the slice category $D/d$ is a corolla for any $d\in D$.  Moreover, if $f\colon d\to d'$ is a morphism in $D$ which is [[monomorphism|monic]], then the "composition" functor $\Sigma_f\colon D/d \to D/d'$ is a dependency.  Thus, if every morphism in $D$ is monic, we have a functor $ext_D\colon D \to Corolla$ with $ext_D(d)= D/d$ and $ext_D(f)=\Sigma_f$.

Now if $f,g\colon d\to d'$ are parallel morphisms and $\Sigma_f=\Sigma_g$, then in particular $f = \Sigma_f(id_d) = \Sigma_g(id_d) = g$; thus $ext_D$ is [[faithful functor|faithful]].  Therefore, if $D$ is a direct category in which all morphisms are monic, and in which $D/d \cong D/d'$ implies $d=d'$ (which includes many examples), then $D$ is equivalent to a [[subcategory]] of $Corolla$.

This subcategory of $Corolla$ is usually *not* full, however.  In particular, for $d\in D$ the corolla $D/d$ will generally admit more automorphisms than $d$ has in $D$.  For instance, if $D$ is a non-generalized direct category, then $d$ has no nontrivial automorphisms, whereas $D/d$ generally will.  In particular, if the objects of $D$ have any sort of "orientation" or "labeling," then this information is forgotten by the functor $ext_D$.

## Related concepts

* [[test category]]

* [[filtered category]], [[sifted category]]

## References

* [[Dennis Borisov]], _Comparing definitions of weak higher categories, I_ ([arXiv:0909.2534](http://arxiv.org/abs/0909.2534))
 {#Borisov}
* [[Clark Barwick]], _On Reedy Model Categories_ ([arXiv:0708.2832](https://arxiv.org/abs/0708.2832))
 {#Barwick}


[[!redirects direct category]]
[[!redirects direct categories]]
[[!redirects inverse category]]
[[!redirects inverse categories]]
[[!redirects one-way category]]
[[!redirects one-way categories]]
[[!redirects category with finite fan-out]]
[[!redirects categories with finite fan-out]]
[[!redirects categories with finite fan-outs]]
[[!redirects simple category]]
[[!redirects simple categories]]

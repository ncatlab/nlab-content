

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
  {#LieModels}

Rational homotopy theory is the [[homotopy theory]] of [[rational topological spaces]], hence of rational [[homotopy types]]: [[simply connected topological space|simply connected]] [[topological spaces]] whose [[homotopy groups]] are [[vector spaces]] over the [[rational numbers]]. 

Much of the theory is concerned with [[rationalization]], the process that sends a general homotopy type to its closest rational approximation, in a precise sense. On the level of [[homotopy groups]] this means to retain precisely the non-[[torsion subgroups]] of the homotopy groups. 

Two algebraic models of rational homotopy types exist, via [[differential graded-commutative algebras]] (Sullivan model) and via [[dg-Lie algebras]] (Quillen model).

This way rational homotopy theory connects [[homotopy theory]] and [[differential graded algebra]]. Akin to the [[Dold-Kan correspondence]], the [[Sullivan construction]] in rational homotopy theory connects the conceptually powerful perspective of [[homotopy theory]] with the computationally powerful perspective of [[differential graded algebra]]. 

Moreover, via the [[homotopy hypothesis]] the study of [[topological spaces]] is connected to that of [[∞-groupoids]], so that rational homotopy theory induces a bridge (the [[Sullivan construction]]) between [[∞-groupoids]] and [[differential graded algebra]]. It was observed essentially by ([Henriques 08](Lie+integration#Henriques), [Getzler 09](Lie+integration#Getzler04)) that this bridge is [[Lie integration]] (see there) in the [[∞-Lie theory]] of [[L-∞ algebras]].

$\,$

There are two established approaches in rational homotopy theory for encoding rational homotopy types in terms of [[Lie theory|Lie theoretic data]]:

1. In the **Sullivan approach** ([Sullivan 77](#Sullivan77)) a 1-connected rational space, in its incarnation as a [[simplicial set]],
is turned into something like a piecewise smooth space by [[nerve and realization|realizing]] each abstract $n$-[[simplex]] by the standard $n$-simplex in $\mathbb{R}^n$; and then a [[dg-algebra]] of [[differential form]]s on this piecewise smooth space
is formed by taking on each simplex the dg-algebra of ordinary rational [[polynomial differential forms]] and gluing these dg-algebras all together.

1. In the **Quillen approach** ([Quillen 69](#Quillen69)) the [[loop space]] of the rational space/simplicial set is formed and its [[H-space]] structure strictified to a [[simplicial group]], of which then a [[dg-Lie algebra]] (a strict [[L-infinity-algebra]]) is formed by mimicking the construction of the Lie algebra of a [[Lie group]] from the [[primitive element]]s of its completed [[group ring]]: the group ring of the simplicial group here is a simplicial ring, whose degreewise primitive elements hence yield a [[simplicial Lie algebra]]. The [[Moore complex]] functor maps this to the [[dg-Lie algebra]] functor that models the rational homotopy type in the Quillen approach.


The connection between these two appoaches is discussed in ([Majewski 00](#Majewski00)): The Sullivan dg-algebra of forms is the [[formal dual]] (the [[Chevalley-Eilenberg algebra]]) of an [[L-infinity algebra]] that may be rectified (see at _[[model structure for L-infinity algebras]]_) to a [[dg-Lie algebra]], and that is the one from Quillen's construction.

(Beware that --  while both rational homotopy types as well as $L_\infty$-algebras are presented by [[formal duals]] of [[dg-algebras]] (via [[Sullivan construction]] and via forming [[Chevalley-Eilenberg algebras]], respectively) -- the class of [[weak equivalences]] in the former case strictly includes that in the latter. See [this remark](model+structure+for+L-infinity+algebras#OndgCoAlgWEs) at _[[model structure for L-∞ algebras]]_.)


## Sullivan approach

### Differential forms on topological spaces {#FormsOnTopSpaces}

A central tool in the study of rational topological spaces is an assignment that sends each [[topological space]]/[[simplicial set]] $X$ to a [[dg-algebra]] $\Omega^\bullet_{poly}(X)$ that behaves like the [[deRham complex|deRham dg-algebra]] of a smooth [[manifold]]. Instead of consisting of smooth [[differential forms]], $\Omega^\bullet_{poly}(X)$ consists of _piecewise linear polynomial differential forms_ , in a way described in detail now.

The construction of $\Omega^\bullet_{poly}$ is a special case of the following general construction:


#### Differential forms on presheaves {#FormsOnPresheaves}

See [[differential forms on presheaves]] for more.

Let $C$ be any [[small category]], write $PSh(C) = [C^{op}, Set]$ for its category of [[presheaf|presheaves]] and let

$$
  \Omega^\bullet_C : C^{op} \to dgAlg
$$

be _any_ functor to the category of [[dg-algebra]]s. Following the logic of [[space and quantity]], we may think of the objects of $C$ as being _test spaces_ and the functor $\Omega^\bullet_C$ as assigning to each test space its [[deRham complex|deRham dg-algebra]].

An example of this construction that is natural from the point of view of [[differential geometry]] appears in the study of [[diffeological space]]s, where $C$ is some subcategory of the category [[Diff]] of smooth [[manifold]]s, and $\Omega^\bullet_C$ is the restriction of the ordinary assignment of [[differential form]]s to this. But in the application to topological spaces, in the following, we need a choice for $C$ and $\Omega^\bullet_C$ that is non-standard from the point of view of [[differential geometry]]. Still, it follows the same general pattern.

After postcomposing with the [[forgetful functor]] that sends each [[dg-algebra]] to its underlying [[set]], the functor $\Omega^\bullet_C$ becomes itself a [[presheaf]] on $C$. For $X \in PSh(C)$ any other presheaf, we extend the notation and write 

$$
  \Omega^\bullet_C(X) := Hom_{PSh(C)}(X, \Omega^\bullet_C)
$$

for the [[hom-set]] of presheaves. One checks that this set naturally inherits the structure of a [[dg-algebra]] itself, where all operations are given by applying "pointwise" for each $p : U \to X$ with $U \in C$ the operations in $\Omega^\bullet_C(U)$. This way we get a functor

$$
  \Omega^\bullet_C : PSh(C) \to dgAlg^{op}
$$

to the [[opposite category]] of that of [[dg-algebra]]s. We may think of $\Omega^\bullet_C(X)$ as the deRham complex of the presheaf $X$ as seen by the functor $\Omega^\bullet_C : C \to dgAlg^{op}$.

By [[category theory|general abstract nonsense]] this functor has a [[right adjoint]] $K_C : dgAlg^{op} \to PSh(C)$, that sends a dg-algebra $A$ to the [[presheaf]]

$$
  K_C(A) : U \mapsto Hom_{dgAlg}(\Omega^\bullet_C(U), A)
  \,.
$$

The [[adjunction]]

$$
  \Omega^\bullet_C : PSh(C) \stackrel{\leftarrow}{\to} : dgAlg^{op} : K_C
$$

is an example for the adjunction induced from a [[dualizing object]].


#### Piecewise linear differential forms

For the purpose of rational homotopy theory, consider the following special case of the [above general discussion](#FormsOnPresheaves) of differential forms on presheaves.

Recall that by the [[homotopy hypothesis]] theorem, [[Top]] is equivalent to [[sSet]]. In the sense of [[space and quantity]], a [[simplicial set]] is a "generalized space modeled on the [[simplex category]]": a [[presheaf]] on $\Delta$.

Therefore set in the above $C := \Delta$. 

Now, a simplicial set has no smooth structure in terms of which one could define differential forms globally, but of course each abstract  $k$-[[simplex]] $\Delta[k]$ may be regarded as the standard $k$-simplex $\Delta^k_{Diff}$ in [[Diff]], and as such it supports smooth differential forms $\Omega^\bullet_{deRham}(\Delta^k_{Diff})$.

The functor $\Omega^\bullet_{deRham}( \Delta_{Diff}^{(-)} ) : \Delta^{op} \to dgAlg$ obtained this way is _almost_ the one that -- after fed into the above procedure -- is used in rational homotopy theory.

The only difference is that for the purposes needed here, it is useful to cut down the smooth differential forms to something smaller. Let $\Omega^\bullet_{poly}(\Delta^k_{Diff})$ be the [[dg-algebra]] of **polynomial differential forms** on the standard $k$-simplex. Notice that this recovers all differential forms after tensoring with smooth functions:

$$
  \Omega^\bullet(\Delta^k_{Diff}) =
  C^\infty(\Delta^k_{Diff}) \otimes_{\Omega^0_{poly}(\Delta^k_{Diff})} \Omega^\bullet_{poly}(\Delta^k_{Diff})
  \,.
$$

For more details see

* [[differential forms on simplices]].


### Sullivan models {#SullivanModels}

...See _[[Sullivan model]]_...

### The rationalization adjunction
 {#SullivanRationalizationAdjunction}

So we have a functor $\Omega^\bullet_{polynomial} \colon \Delta \to dgAlg^{op}$. Feeding that into the [above general machinery](#FormsOnPresheaves) produces a pair of [[adjoint functors]]

$$
  (\Omega^\bullet_{poly} \dashv \mathcal{K}_{poly})
  \colon
  sSet 
    \stackrel{
      \overset{\Omega^\bullet_{poly}}{\longrightarrow}
    }{
     \underset{K_{poly}}{\longleftarrow}
    } 
  dgcAlg^{op}
$$

between [[simplicial sets]] and [[dg-algebras]].


+-- {: .num_theorem #SullivanRationalizationAdjunction}
###### Theorem

This is a [[Quillen adjunction]] with respect to the standard [[model structure on simplicial sets]] on the left, and the standard [[model structure on dg-algebras]] on the right.

Moreover, this restricts to an equivalence between simply connected rational homotopy types and (minimal) [[Sullivan algebras]].

=--

([Bousfield-Gugenheim 76, section 8](#BousfieldGugenheim76)) Review includes ([Hess 06, p. 9](#Hess06)).

+-- {: .num_prop #HomotopyGroupsFromSullivanGenerators}
###### Proposition

For $X$ a homotopy type, then 

1.its rational vector space of the rational homotopy group in degree $n$ is spanned by the generators of degree $n$ of its Sullivan model;

1. its rational cohomology is the cochain cohomology of its Sullivan model.

=--

### Examples
 {#SullivanModelExamples}

#### Rational $n$-spheres
  {#SullivanModelRationalSpheres}

We discuss the minimal Sullivan models of [[rational n-spheres]].

The minimal [[Sullivan model]] of a [[sphere]] $S^{2k+1}$ of odd [[dimension]] is the dg-algebra with a single generator $\omega_{2k+1}$ in degre $2k+1$ and vanishing differential

$$
  d \omega_{2k+1} = 0
  \,.
$$


The minimal [[Sullivan model]] of a sphere $S^{2k}$ of even dimension, for $k \geq 1$. is the dg-algeba with a generator $\omega_{2k}$ in degree $2k$ and another generator $\omega_{4k-1}$ in degree $4k+1$ with the differential defined by

$$
  d \omega_{2k}= 0
$$
$$
  d \omega_{4k+1} = \omega_{2k}\wedge \omega_{2k}
  \,.
$$

One may understand this form prop. \ref{HomotopyGroupsFromSullivanGenerators}: an $n$-sphere has rational cohomology concentrated in degree $n$. Hence its Sullivan model needs at least one closed generator in that degree. In the odd dimensional case one such is already sufficient, since the wedge square of that generator vanishes and hence produces no higher degree cohomology classes. But in the even degree case the wedge square $\omega_{2k}\wedge \omega_{2k}$ needs to be canceled in cohomology. That is accomplished by the second generator $\omega_{4k-1}$. 

Again by prop. \ref{HomotopyGroupsFromSullivanGenerators}, this now implies that the rational [[homotopy groups of spheres]] are concentrated, in degree $2k+1$ for the odd $(2k+1)$-dimensional spheres, and in degrees $2k$ and $4k-1$ in for the even $2k$-dimensional spheres. 

For instance the [[4-sphere]] has rational homotopy in degree 4 and 7. The one in degree 7 being represented by the [[quaternionic Hopf fibration]].


## Quillen approach
 {#QuillenApproach}

The following sequence of six consecutive functors, each of which is a [[Quillen equivalence]], takes one from a [[n-connected space|1-connected]] rational space $X$ to a [[dg-Lie algebra]].

One starts with the [[fundamental infinity-groupoid|singular simplicial set]]

$$
  S(X)
$$
 

and throws away all the simplices except the basepoint in degrees $0$ and $1$, to get a [[reduced simplicial set]].  Then one applies the Kan loop group functor (the simplicial analogue of the based [[loop space]] functor, see [here](simplicial+group#AsInfinityGroups)) to $S(X)$, obtaining an a [[simplicial group]]

$$
  G S(X).
$$

Then one forms its [[group ring]]

$$
  \mathbb{Q}[G S(X)]
$$

and completes it with respect to powers of its [[augmentation ideal]], obtaining a "reduced, complete simplicial [[Hopf algebra]]",

$$
  \hat \mathbb{Q}[G S(X)], 
$$

which happens to be cocommutative, since the group ring is cocommutative. Taking degreewise [[primitive element|primitives]], one then gets a reduced simplicial Lie algebra

$$
  Prim(\hat \mathbb{Q}[G  S(X)]).
$$

At the next stage, the [[Moore complex|normalized chains functor]] is applied, to get Quillen's [[dg-Lie algebra]] model of $X$:

$$
  N^\bullet(Prim(\hat \mathbb{Q}[G S(X)])).
$$

Finally, to get a cocommutative dg [[coalgebra]] model for $X$, one uses a slight generalization of a functor first defined by Koszul for computing the homology of a Lie algebra, which always gives rise to a cocommutative dg coalgebra.


One may think of this procedure as doing the following: we are taking the [[Lie algebra]] of the "group" $\Omega X$ which is the [[loop space]] of $X$. From a group we pass to the enveloping algebra, i.e. the algebra of [[distribution]]s supported at the identity, completed. The topological analog of distributions are chains (dual to functions = cochains), so Quillen's completed chains construction is exactly the completed enveloping algebra. From the (completed) enveloping algebra we recover the Lie algebra as its primitive elements. 

## Related concepts

* from the [[nPOV]]: [[rational homotopy theory in an (infinity,1)-topos]].

* [[p-adic homotopy theory]]

* [[real homotopy theory]]

* [[fracture theorem]]

* [[equivariant rational homotopy theory]]

* [[rational equivariant stable homotopy theory]]

## References

The original articles are

* {#Quillen69} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf)) 

* {#Sullivan77} [[Dennis Sullivan]], _Infinitesimal computations in topology_      Publications math&#233;matiques de l' I.H.&#201;.S. tome 47 (1977), p. 269-331. ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))

* {#BousfieldGugenheim76} Bousfield, Gugenheim, _On PL deRham theory and rational homotopy type_ , Memoirs of the AMS, vol. 179 (1976)



Survey and review includes

* {#Hess06} [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]] and J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000. 

* {#Majewski00} Martin Majewski, _Rational homotopy models and uniqueness_ , AMS Memoir (2000):

Review that makes the [[L-infinity algebra]] aspect completely manifest includes

* {#BuijsFelixMurillo12} Urtzi Buijs, [[Yves Félix]], Aniceto Murillo, section 2 of _$L_\infty$-rational homotopy of mapping spaces_ ([arXiv:1209.4756](https://arxiv.org/abs/1209.4756))



More on the relation to Lie theory is in:

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$-algebras_ ([arXiv](http://arxiv.org/abs/math.AT/0404003))


The above description of the Quillen approach draws on blog comments by [[Kathryn Hess]] [here](http://golem.ph.utexas.edu/category/2010/01/this_weeks_finds_in_mathematic_50.html#c030961) and by [[David Ben-Zvi]] [here](http://golem.ph.utexas.edu/category/2010/01/this_weeks_finds_in_mathematic_50.html#c031038).

Discussion from the point of view of [[(∞,1)-category theory]] and [[E-∞ algebras]] is in 

* [[Jacob Lurie]], _Rational and $p$-adic homotopy theory_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XIII.pdf))

An extension of rational homotopy theory to describe (some) non-simply connected spaces is given, using [[derived algebraic geometry]], in

* [[B. Toën]], _Champs affines_, Selecta Math. (N.S.) 12 (2006), no. 1, 39-135.

See in particular Cor. 2.4.11, Cor. 2.5.3 and Cor. 2.5.4, and the MathOverflow answer [MO/79309/2503](http://mathoverflow.net/a/79309/2503) by [[Denis-Charles Cisinski]].

[[!redirects rational homotopy type]]
[[!redirects rational homotopy types]]

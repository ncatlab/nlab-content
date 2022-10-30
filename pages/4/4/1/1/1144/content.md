

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mathematic
+--{: .hide}
[[!include mathematicscontents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

As with many other parts of [[homotopy theory]] one can view _rational homotopy theory_ in two ways:

* either one looks at a subcategory of [[topological space]]s for which a particular [[homotopy functor]] gives exceptionally good results;

* or alternatively one looks at fairly arbitrary nice spaces, but collects up and uses only the information available using some particular type of [[homotopy functor]].

From the first viewpoint, rational homotopy theory studies special [[topological space]]s called **[[rational topological space|rational spaces]]**: simply connected spaces whose homotopy groups are vector spaces over the rational numbers. 

The point of this is that

* every (simply connected) topological space can be _approximated_ by a rational space;

* rational topological spaces are entirely encoded in terms of [[differential graded algebra]].

Alternatively, looking at simply connected spaces, we can concentrate on what happens if we tensor their homotopy groups with the field of rationals. What information can be gleaned from these homotopy functors? The answer is 'an incredible amount' -- namely all non-[[torsion subgroup|torsion]] information -- and results in a _very rich theory_.

In these ways, rational homotopy theory connects and unifies two large areas of mathematics, [[homotopy theory]] and [[differential graded algebra]]. Akin to the [[Dold-Kan correspondence]], the [[Sullivan construction]] in rational homotopy theory connects the conceptually powerful perspective of [[homotopy theory]] with the computationally powerful perspective of [[differential graded algebra]]. 

Moreover, via the [[homotopy hypothesis]] the study of [[topological space]]s is connected to that of [[infinity-groupoid]]s, so that rational homotopy theory induces a bridge between [[infinity-groupoid]]s and [[differential graded algebra]]. It was observed essentially by Ezra Getzler that this bridge is nothing but higher [[Lie theory]] of [[L-infinity-algebra]]s.


## Details

### Rational homotopy types

* [[rational homotopy equivalence]]

* [[rational space]]

* [[rationalization]]

### Lie theoretic models for rational homotopy types {#LieModels}

There are two main approaches in rational homotopy theory for encoding rational homotopy
types in terms of [[Lie theory|Lie theoretic data]]:

1. In the **Sullivan approach** a 1-connected rational space,
in its incarnation as a [[simplicial set]],
is turned into something like a piecewise smooth space by [[nerve and realization|realizing]]
each abstract $n$-[[simplex]] by the standard $n$-simplex in $\mathbb{R}^n$; and
then a [[dg-algebra]] of [[differential form]]s on this piecewise smooth space
is formed by taking on each simplex the dg-algebra of ordinary rational polynomial
forms and gluing these dg-algebras all together.

   This goes back to

   * [[Dennis Sullivan]], _Infinitesimal computations in topology_ 
     Publications math&#233;matiques de l' I.H.&#201;.S. tome 47 (1977), p. 269-331.

1. In the **Quillen approach** the [[loop space]] of the rational space/simplicial set is formed
and its [[H-space]] structure strictified to a [[simplicial group]], of which
then a [[dg-Lie algebra]] (a strict [[L-infinity-algebra]]) is formed by
mimicking the construction of the Lie algebra of a [[Lie group]] from the
[[primitive element]]s of its completed [[group ring]]: the group ring of the
simplicial group here is a simplicial ring, whose degreewise primitive elements
hence yield a [[simplicial Lie algebra]]. The [[Moore complex]] functor maps this
to the [[dg-Lie algebra]] functor that models the rational homotopy type in the
Quillen approach.

   This goes back to ([Quillen 69](#Quillen)).

The connection between these two appoaches is discussed in

* Martin Majewski, _Rational homotopy models and uniqueness_ , AMS Memoir (2000):

the Sullivan dg-algebra of forms is dual to an [[L-infinity algebra]]
and may be strictified to a [[dg-Lie algebra]], and this is equivalent to
the dg-Lie algebra obtained from Quillen's construction.


### Sullivan approach

#### Differential forms on topological spaces {#FormsOnTopSpaces}

A central tool in the study of rational topological spaces is an assignment that sends each [[topological space]]/[[simplicial set]] $X$ to a [[dg-algebra]] $\Omega^\bullet_{poly}(X)$ that behaves like the [[deRham complex|deRham dg-algebra]] of a smooth [[manifold]]. Instead of consisting of smooth [[differential form]]s, $\Omega^\bullet_{poly}(X)$ consists of _piecewise linear polynomial differential forms_ , in a way described in detail now.

The construction of $\Omega^\bullet_{poly}$ is a special case of the following general construction:


##### Differential forms on presheaves {#FormsOnPresheaves}

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


##### Piecewise linear differential forms

For the purpose of rational homotopy theory, consider the following special case of the [above general discussion](#FormsOnPresheaves) of differential forms on presheaves.

Recall that by the [[homotopy hypothesis]] theorem, [[Top]] is equivalent to [[SSet]]. In the sense of [[space and quantity]], a [[simplicial set]] is a "generalized space modeled on the [[simplex category]]": a [[presheaf]] on $\Delta$.

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

So we have a functor $\Omega^\bullet_{polynomial} : \Delta \to dgAlg^{op}$. Feeding that into the [above general machinery](#FormsOnPresheaves) produces a pair of [[adjoint functor]]s

$$
  \Omega^\bullet_{poly} : SSet \stackrel{\leftarrow}{\to} dgAlg^{op} : 
  K_{poly}
  \,.
$$


+-- {: .un_theorem}
###### Theorem

This is a [[Quillen adjunction]] with respect to the standard [[model structure on simplicial sets]] on the left, and the standard [[model structure on dg-algebras]] on the right.

=--

+-- {: .proof}
###### Proof

The original proof in the literature is apparently the one in section 8 of

* Bousfield, Gugenheim, _On PL deRham theory and rational homotopy type_ , Memoirs of the AMS, vol. 179 (1976)

A review is on [page 9](http://arxiv1.library.cornell.edu/PS_cache/math/pdf/0604/0604626v2.pdf#page=9)

of

* [[Kathryn Hess]], _Rational homotopy theory: A brief introduction_ ([pdf](http://arxiv1.library.cornell.edu/PS_cache/math/pdf/0604/0604626v2.pdf))

=--


#### Sullivan models {#SullivanModels}

See [[Sullivan model]].

### Quillen approach

The following sequence of six consecutive functors, each of which is a [[Quillen equivalence]], take one from a [[n-connected space|1-connected]] rational space $X$ to a [[dg-Lie algebra]].

One starts with the [[fundamental infinity-groupoid|singular simplicial set]]

$$
  S(X)
$$
 

and throws away all the simplices except the basepoint in degrees $0$ and $1$.  Then one applies the Kan loop group functor (the simplicial analogue of the based [[loop space]] functor) to $S(X)$, obtaing an honest [[simplicial group]]

$$
  G S(X).
$$

Then one takes the [[group ring]]

$$
  \mathbb{Q}[G S(X)]
$$

and completes it with respect to powers of its augmentation ideal, obtaining a "reduced, complete simplicial [[Hopf algebra]]",

$$
  \hat \mathbb{Q}[G S(X)], 
$$

which happens to be cocommutative, since the group ring is cocommutative. Taking degreewise [[primitive element|primitives]]s, one then gets a reduced simplicial Lie algebra

$$
  Prim(\hat \mathbb{Q}[G  S(X)]).
$$

At the next stage, the [[Moore complex|normalized chains functor]] is applied, to get Quillen's [[dg-Lie algebra]] model of $X$:

$$
  N^\bullet(Prim(\hat \mathbb{Q}[G S(X)])).
$$

Finally, to get a a cocommutative dg [[coalgebra]] model for $X$, one uses a slight generalization of a functor first defined by Koszul for computing the homology of a Lie algebra, which always gives rise to a cocommutative dg coalgebra.


One may think of this procedure as doing the following: we are taking the [[Lie algebra]] of the "group" $\Omega X$ which is the [[loop space]] of $X$. From a group we pass to the enveloping algebra, i.e. the algebra of [[distribution]]s supported at the identity, completed. The topological analog of distributions are chains (dual to functions = cochains), so Quillen's completed chains construction is exactly the completed enveloping algebra. From the (completed) enveloping algebra we recover the Lie algebra as its primitive elements. 


## nPOV

from the [[nPOV]]: [[rational homotopy theory in an (infinity,1)-topos]].

## References

A useful introduction to rational homotopy theory is

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

A standard textbook is

* Y. F&#233;lix, S. Halperin and J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000. 


Early original articles include:

* [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725))
 {#Quillen}



* [[Dennis Sullivan]], _Infinitesimal computations in topology_      Publications math&#233;matiques de l' I.H.&#201;.S. tome 47 (1977), p. 269-331. ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))


More on the relation to Lie theory is in:

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$-algebras_ ([arXiv](http://arxiv.org/abs/math.AT/0404003))


The above description of the Quillen approach draws on blog comments by [[Kathryn Hess]] [here](http://golem.ph.utexas.edu/category/2010/01/this_weeks_finds_in_mathematic_50.html#c030961) and by [[David Ben-Zvi]] [here](http://golem.ph.utexas.edu/category/2010/01/this_weeks_finds_in_mathematic_50.html#c031038).

Discussion from the point of view of [[(∞,1)-category theory]] and [[E-∞ algebras]] is in 

* [[Jacob Lurie]], _Rational and $p$-adic homotopy theory_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XIII.pdf))


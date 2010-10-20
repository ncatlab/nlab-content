
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* automatic tanle of contents goes here
{:toc}

## Idea

The _rough idea_ is (but see the [caveat](#caveat) below) that the term **moduli space** is essentially a synonym for [[representable functor|representing object]] and for [[classifying space]]. People tend to say "classifying space" when in the context of [[topology]], and they tend to say _moduli space_ when in a context of [[complex geometry]] or [[algebraic geometry]]. 

More precisely, when a moduli space actually does exist as an ordinary space (or [[scheme]]), it is called for emphasis a **fine moduli space**. Fine here refers to the completeness of the description, not shared by coarse moduli below.

Those classifying "spaces" that are called moduli spaces are typically [[orbifold]]s, hence modeled not just as spaces but as [[groupoid]]s with extra structure. These are typically conceived as [[stack]]s: these are then called **moduli stack**s. Typically these are demanded to be [[Deligne-Mumford stack]]s. 

So the term _fine moduli space_ mainly indicates that a given object that might be a [[Deligne-Mumford stack]] is actually just a plain [[scheme]]. But there is also the notion of **coarse moduli space**, which is a kind of conceptual hack designed to be able to keep thinking about what really wants to be a [[stack]] still as a plain [[sheaf]].

A coarse moduli space is one that at least has the right underlying [[set]] of points as the _right_ moduli stack has: as long as we don't look at families but just at single things, it does give the right information. From the point of view of [[derived algebraic geometry]], the coarse moduli spaces are 0-truncations of derived moduli stacks when they exist.

### Caveat {#caveat}

But one has to be **careful with this rough idea**: as there is usually some **implicit fine print** in the notion of moduli space: 

while [[classifying space]] is the term typically used for a [[representable functor|representing object]] in a [[homotopy category]], a representing object is usually called a _moduli space_ only if it lives in the "original" category. For more on this see the chapter 

* [... because they have automorphisms](#because) 

below.

## History

The term possibly originates with Riemann, who was the first to study what are now called moduli spaces of (compact) [[Riemann surface]]s. A "modulus" here is meant to be a _parameter_ that parameterizes isomorphism classes of Riemann surfaces.

More precisely, when a moduli space actually does exist as a genuine space (or [[scheme]]), it is called for emphasis a **fine moduli space**. Fine here refers to the completeness of the description, not shared by coarse moduli below.

Those classifying "spaces" that are called moduli spaces are typically [[orbifold]]s, hence modeled not just as spaces but as [[groupoid]]s with extra structure. These are typically conceived as [[stack]]s: these are then called **moduli stack**s. Typically these are demanded to be [[Deligne-Mumford stack]]s. 

So the term _fine moduli space_ mainly indicates that a given object that might be a [[Deligne-Mumford stack]] is actually just a plain [[scheme]]. But there is also the notion of **coarse moduli space**, which is a kind of conceptual hack designed to be able to keep thinking about what really wants to be a [[stack]] still as a plain [[sheaf]]:

## Definition

...

### Coarse moduli space 

A **coarse moduli space** for a [[presheaf]] $(Sch/\mathbb{C})^{op} \to Set$ on complex [[scheme]]s is a [[scheme]] $M \in Sch/\mathbb{C}$ equipped with a morphism 

$$
  \Psi_M : F \to h_M
  \,,
$$ 

where $h$ denotes the [[Yoneda embedding]], such that 

a) $F(Spec(\mathbb{C})) \to h_M(Spec \mathbb{C}) = hom(Spec \mathbb{C}, M)$ is a [[bijection]]
 
b) given $M'$ and $\Psi_{M'} : F \to h_{M'}$ then there exists unique $M \to M'$ such that $\array{ F && \stackrel{\Psi_{M'}}{\to}&& h_{M'} \\ & {}_{\Psi_M}\searrow && \nearrow \\ && h_M} $

So a coarse moduli space is one that at least has the right underlying set of points as the _right_ moduli stack has: as long as we don't look at families but just at single things, it does give the right information. From the point of view of [[derived algebraic geometry]], the coarse moduli spaces are 0-truncations of derived moduli stacks when they exist.


## "... because they have automorphisms." {#because}

A widespread slogan is 

> **Slogan**: A type of objects that has nontrivial [[automorphism]]s cannot have a fine moduli space.

The typical example motivating and illustrating this slogan is the example of [[elliptic curve]]s: from a single [[elliptic curve]] $E$ with a non-trivial automorphism $\alpha : E \to E$ one may build, for instance, the family $\mathcal{E} \to S^1 \times S^1$ of elliptic curves over the torus which is obtained by starting with the trivial family $E \times S^1 \times [0,1] \to S^1 \times [0,1]$ over the cylinder and then by gluing the two ends by identifying the fiber using the automorphism $\alpha$. The resulting family is _locally trivial_ but globally nontrivial. 

Such locally trivial but globally non-trivial families can in principle not be classified by a representing object in the category of spaces that we are working with, as long as the [[Grothendieck topology]] which we use to say what a locally trivial family is is [[subcanonical coverage|subcanonical]]:

for assume that a classifying object $K$ exists in our category and assume that at least one globally nontrivial but locally trivial family $\mathcal{E} \to X$ exists in the category. 

Then by definition of local triviality there exists a covering [[sieve]] $\{U_i \to X\}$ such that the [[pullback]] of $\mathcal{E}$ to each $U_i$ is equivalent to the trivial family over $U_i$. Accordingly, it will be represented by the trivial element in $Hom(U_i, K)$. But if $\{U_i \to X\}$ is a covering [[sieve]] in a subcanonical topology, then it follows from the [[sheaf]] property of the [[representable functor|representable presheaf]] $Hom(-,K)$ that there is a unique element in $Hom(X,K)$ whose restriction to all the $U_i$ represents the trivial family. But the trivial family over $X$ has this property and hence must be that unique element. Accordingly, it would follow that there is no non-trivial family classified by $K$ over $X$, which is a contradiction and shows that the "fine moduli space" $K$ cannot exist under the given assumptions.

Notice well the two assumptions that were made to make this argument work:

1. the topology with which we glue families must be subcanonical: this is the assumption that fails for the situations in which one would speak of [[classifying space]]s instead of moduli spaces: 

   For instance [[vector space]]s do certainly have nontrivial [[automorphism]]s. A (topological, say) family of vector space is a [[vector bundle]]. So a naive application of the above argument might lead one to conclude that there cannot be a classifying space of vector bundles!

   But of course it is a standard fact that there there are [[topological space]]s $\mathcal{B} U(n)$ such that [[homotopy]] classes of continuous maps $X \to \mathcal{B} U(n)$ classify isomorphism classes of rank-$n$ [[vector bundle]]s. But this means that the functor that assigns families of vector bundles to topological space is -- while not [[representable functor|representable]] in [[Top]] -- representable in the [[homotopy category]] $Ho(Top)$

   $$
     Rank n VectBund(X)/iso  \simeq Hom_{Ho(Top)}(X, \mathcal{B} U(n))
     \,.
   $$

   This might make the [[classifying space]] $\mathcal{B} U(n)$ look like something that deserves to be called a fine moduli space. But one should beware that the standard [[Grothendieck topology]] of [[Top]], which is [[subcanonical coverage|subcanonical]] in [[Top]] is not so in $Ho(Top)$: the functor $Hom_{Ho(Top)}(-, \mathcal{B} U(m))$ has a non-standard opinion about what it means to glue two topological spaces to a third one. That's how in $Ho(Top)$ the above argument that "automorphisms prevent a classifying object" breaks down.

   In fact, there is a theorem by Danny Stevenson and [[David Roberts]], extended a theorem by [[John Baez]] and Danny Stevenson  that shows that large classes of [[principal ∞-bundle]]s, even, do have classifying topological spaces in this sense. (See [[classifying space for principal infinity-bundles|classifying spaces for principal ∞-bundles]].) These are objects that not only have automorphisms, but have automorphisms of automorphisms, etc, and hence seem to contradict the above slogan in a maximal way. 

   But these examples also indicate why it may be misguided to think of the "classifying spaces" such as $\mathcal{B} U(n)$ as being moduli spaces in the first place: the [[homotopy category]] $Ho(Top)$ in fact regards its objects -- even though they are presented as [[topological space]]s -- not really as spaces but as the [[∞-groupoid]]s that they are equivalent to under the [[homotopy hypothesis]]. So in that sense objects such as $\mathcal{B} U(n)$ are not classifying spaces, but are classifying [[groupoid]]s after all. 

2. Another situation that makes the above argument break down is if the category of "spaces" that one works with is such that gluing trivial families by nontrivial automorphisms never produces globally nontrivial families. For instance because the category of "spaces" is such that no nontrivial families exist at all. This happens for instance in the case that we take a "space" to be simply a (finite, say) [[set]]. In the category [[Set]] of (finite) sets every fiber bundle $\mathcal{E} \to X$ (i.e. every surjection such that all fivers are isomorphic to a typical fiber $F$ ) are necessarily globally trivial in that they are isomorphic to $F \times X \to X$. And in fact, there _is_ a "fine moduli space" in this context (inside the category of non-necessarily finite sets), namely the set $\mathbb{N}$ of natural numbers: the family $(\mathcal{E} \to X) \in Set$ with typical fiber the $n$-element set is classified by the map that sends all $x \in X$ to $n \in \mathbb{N}$.



## Related entries

* [[Hilbert scheme]]

A bit of elementary exposition of these ideas is at 

* [[basic ideas of moduli stacks of curves and Gromov-Witten theory]]

A blog discussion about the issue of classifying spaces versus moduli spaces is [here]() (where?)


[[!redirects fine moduli space]]
[[!redirects coarse moduli space]]
[[!redirects moduli stack]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A **Street fibration**, or **weak fibration**, is a generalization of a [[Grothendieck fibration]] which obeys the [[principle of equivalence]], i.e. covariant under [[equivalence of categories]].  In [[Cat]], almost all Street fibrations which arise in practice are actually Grothendieck fibrations, so the extra generality is not very useful; since it is also fairly cumbersome, it is rarely used.  However, when working with [[anafunctors]] or internally to a [[bicategory]] (a weak [[2-category]]), one is essentially forced to work with Street fibrations instead; see below.


## Definition

Let $p\colon E\to B$ be a [[functor]].  The notion of when a morphism of $E$ is [[cartesian morphism|cartesian]] is unchanged from the version for [[Grothendieck fibrations]].  However, now we say that $p$ is a **Street fibration** if for any $f:a\to b$ in $B$ and $e\in E_b$ there exists a cartesian $\phi:e'\to e$ and an _isomorphism_ $h:p(e') \cong a$ such that $f\circ h = p(\phi)$.

An [[internalization|internalized]] version of this definition can be given in any [[2-category]]; see [[fibration in a 2-category]].  The above definition corresponds to the special case of the 2-category [[Cat]].


### In terms of adjoint inverses

Back in the 1960s, J. Gray characterized fibrations as the functors $p\colon E\to B$ 
where for every $a \in E$ the [[slice functor]] $p/a \colon E/a \to B/p(a)$ has a [[right
adjoint]] [[right inverse]] $c_a$. One avoids violating the [[principle of equivalence]] if one just requires that $c_a$ is
[[fully faithful functor|full and faithful]], i.e. the [[counit of the adjunction]] $p/a \dashv c_a$ is an isomorphism. Explicating this condition in elementary terms, one arrives at the above definition.

A simpler version of this characterization is the following.

+--{: .un_lemma}
###### Lemma
A functor $p \colon E \to B$ is a [[cleavage|cloven]] Street fibration if and only if the canonical functor $i \colon E \to B/p$ has a right adjoint $r$ in $Cat / B$.
=--
+-- {: .proof }
###### Proof
First, recall that the 2-category $Cat/B$ has objects the functors $C \to B$, as morphisms the triangles
$$\array{C & \xrightarrow{h} & C' \\ & f \searrow \cong \swarrow g &  \\  & B  & }$$
which commute up to specified isomorphism, and as 2-cells the natural transformations $\alpha : h_1 \to h_2$ which commute with the specified isomorphisms (i.e. $ f \xrightarrow{\cong} g h_1 \xrightarrow{g \alpha} g h_2 \xrightarrow{\cong} f$ is the identity).

Next, recall that the [[comma category]] $B/p$ has objects the triples $(x, e, k)$, with $k \colon x \to p(e)$ a morphism in $B$.  Let $\pi \colon B/p \to B$ denote the projection $(x, e, k) \mapsto x$.  The canonical morphism $i\colon p \to B/p$ in $Cat/B$ sends $e\in E$ to the triple $(p(e),e,1_{p(e)})$.

Somewhat imprecisely, seeing both categories $E$ and $B/p$ as sitting over $B$ means that functors between those should be the identity (up to specified isomorphism) on the $b$ component, and natural transformations should have the identity as their $b$ component (modulo the specified isomorphisms).

Now, to give an adjunction $i \dashv r$ in $Cat$, it suffices to give, for each object $k \colon x \to p(e)$ in $B/p$, an object $r(x,e,k) = r(k)$ in $E$ and an arrow $i(r(k)) = (p(r(k)), r(k), 1_{p(r(k))}) \to (x,e,k)$ in $B/p$ that is [[universal arrow|universal]] from $i$ to $k$.  Such an arrow consists of a pair of morphisms $\theta_k\colon p(r(k)) \to x$ in $B$ and $\epsilon_k\colon r(k) \to e$ in $E$ such that
$$
\array{
  p(r(k)) & \overset{1}{\to} & p(r(k)) \\
  \mathllap{\theta} \downarrow & & \downarrow \mathrlap{p(\epsilon_k)} \\
  x & \underset{k}{\to} & p(e)
}
$$
commutes, i.e. such that $p(\epsilon_k) = k \circ \theta_k$.

Note that since $x = \pi(x,e,k)$, the morphisms $\theta$ supply a natural transformation $\theta\colon p r \to \pi$, not necessarily invertible.  By general [[doctrinal adjunction]] arguments, in order for $i \dashv r$ to be an adjunction in $Cat/B$, it is necessary and sufficient that $\theta$ be invertible (and we then use it to make $r$ into a morphism in $Cat/B$).

Now, the universal property of $(\theta_k,\epsilon_k)$ tells us that for any other morphism in $B/p$ from some $i(y)$ to $k$, i.e., for any $y$ and any pair $(f,g)$ making the square
$$
\array{
  p(y) & \stackrel{1}{\to} & p(y) \\
  \mathllap{f} \downarrow & & \downarrow \mathrlap{p(g)} \\
  x & \underset{k}{\to} & p(e)
}
$$
commute, there is a unique map $h \colon y \to r(k)$ in $B$ such that the above square factors in $B/p$ as
$$
\array{
  p(y) & \stackrel{1}{\to} & p(y) \\
  \mathllap{p(h)} \downarrow &  & \downarrow \mathrlap{p(h)} \\
  \mathllap{p(r(k))} & \stackrel{1}{\to} & \mathrlap{p(r(k))}\\
  \mathllap{\theta_k} \downarrow & & \downarrow \mathrlap{p(\epsilon_k)} \\
  x & \underset{k}{\to} & p(e).
}
$$
In other words, the universal property provides a unique $h$ such that $\epsilon_k \circ h = g$ and $\theta_k \circ p(h) = f$, which exactly asserts that $\epsilon_k$ is a [[cartesian arrow]].

Thus, the existence of a right adjoint to $i$ means precisely that for each morphism $k \colon x \to p(e)$, a choice is given of a cartesian lift of $k$ up to isomorphism.  In turn, this means that $p$ is a cloven fibration.
=--

### Other definitions

Most other characterizations of Grothendieck fibrations can also be given in a way which does not violate the [[principle of equivalence]] to characterize Street fibrations.

## Comparison to Grothendieck fibrations

Every Grothendieck fibration is a Street fibration, as is every [[equivalence of categories]] (the latter are not in general Grothendieck fibrations).  Since Street fibrations are closed under composition, any functor equivalent to a Street fibration is also a Street fibration (this is the "covariance" property).  As remarked above, however, almost all functors in [[Cat]] which one wants to treat as "fibrations" are actually Grothendieck fibrations.  Moreover, in $Cat$ every Street fibration is the composite of an equivalence with a Grothendieck fibration: the latter can be taken to be a [[fibrant replacement]] of it in the [[canonical model structure]] on Cat.  (In fact, a Street fibration is a Grothendieck fibration precisely when it is also a [[isofibration]].)

For these reasons, Street fibrations in $Cat$ are little-studied.  The fact that they exist, and that any Street fibration is equivalent to a Grothendieck one, can be useful in assuaging philosophical worries about violation of the [[principle of equivalence]] in the notion of Grothendieck fibration, but in practice in $Cat$ one usually wants to use Grothendieck fibrations.

However, when internalizing in other 2-categories, covariance becomes more important.  This is most obvious when the 2-category in which one wishes to internalize is only a weak 2-category (a [[bicategory]]), in which it does not even make much sense to internalize the notion of Grothendieck fibration.  (This is even the case in [[Cat]] if we define it using [[anafunctors]], as is often important to do in the absence of the [[axiom of choice]].)  However, even when internalizing in a [[strict 2-category]], if the strict 2-category itself is "only defined up to [[biequivalence]]," then one is again compelled to use internal Street fibrations, since they are "covariant under biequivalence" of the containing bicategory, whereas Grothendieck fibrations are not.

For example, this is arguably the case in the 2-category [[Topos]], where we have to make the arbitrary choice of whether to define the [[geometric morphism|morphisms]] to be [[left exact functor|left-exact]] left [[adjoint functor|adjoints]] $f^*$, right adjoints $f_*$ having a left-exact left adjoint, or adjoint pairs $(f^*,f_*)$ in which $f^*$ is left exact.  The three choices give three strict 2-categories which are all biequivalent, but not strictly 2-equivalent; thus it is more sensible to consider internal Street fibrations in $Topos$ than strict Grothendieck ones.


## Properties

Since Street fibrations are the "minimal covariant modification" of Grothendieck ones, any property enjoyed by Grothendieck fibrations which is itself covariant under equivalence will also be possessed by Street fibrations.

One thing to note is that in general, when working with Street fibrations, one must always replace [[fibers]] with [[essential fibers]].  In particular, the lifting property of a Street fibration is insufficient for a morphism $u\colon J\to I$ in $B$ to induce a functor $u^*\colon E^I\to E^J$ between strict fibers, but such a functor is induced between essential fibers.  In this way we can reconstruct a [[pseudofunctor]] $B^{op}\to Cat$ from any Street fibration, and show that the [[2-category]] of Street fibrations is equivalent to that of such pseudofunctors (though not, as in the case of Grothendieck fibrations, [[strict 2-equivalence of 2-categories|strictly 2-equivalent]]).

Just as every Grothendieck fibration is a [[strictly exponentiable functor]], i.e. an [[exponential object|exponentiable morphism]] in the [[strict 2-category]] [[Cat]], every Street fibration is a non-strictly exponentiable functor, i.e. an exponentiable morphism in the weak [[2-category]] Cat.

## Examples

Of course, any Grothendieck fibration is a Street fibration, but the interest is in those which are not Grothendieck.  Some of the applications are internal to 2-categories other than [[Cat]].

* The original motivation was to consider fibrations (and opfibrations, and [[two-sided fibrations]]) in $V Cat^{op}$ as a means to construct [[Prof]].

* Street fibrations in [[Topos]] are discussed in the paper of Johnstone below.

Street fibrations in [[Cat]] also arise in mathematics, though often under different names.  The following examples were pointed out by [[George Janelidze]], [[Steve Lack]], and [[Ross Street]].

* The notion of "admissible object" in [[categorical Galois theory]] can be expressed in terms of a functor being (partially) a Street fibration, not generally Grothendieck.

* Any [[left exact functor|left exact]] (or, more generally, "semi-left exact") [[reflection]] is a Street fibration, not generally Grothendieck.

## References

The notion was originally defined in 

* [[Ross Street]], *Fibrations in bicategories*, Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques, tome 21, no 2 (1980), 111-160.  ([pdf](http://www.numdam.org/article/CTGDC_1980__21_2_111_0.pdf))

although there it was given in a very abstract form.  A more explicit form like that given above can be found in

* Ross Street, *Conspectus of variable categories*, Journal of Pure and Applied Algebra, Volume 21, Issue 3 (1981), 307-338. ([pdf](https://www.sciencedirect.com/science/article/pii/0022404981900219/pdf?md5=3d791b95c31feb34887b5144975c2f02&pid=1-s2.0-0022404981900219-main.pdf))

Some alternate characterizations, and applications in [[Topos]], are discussed in

* [[Peter Johnstone]], *Fibrations and partial products in a 2-category*.


[[!redirects Street fibration]]
[[!redirects Street fibrations]]
[[!redirects weak fibration]]
[[!redirects weak fibrations]]
[[!redirects Street opfibration]]
[[!redirects Street opfibrations]]
[[!redirects weak opfibration]]
[[!redirects weak opfibrations]]

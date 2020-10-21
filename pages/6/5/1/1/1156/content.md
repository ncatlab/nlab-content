

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of **$(\infty,1)$-sheaf** (or _[[∞-stack]]_ or _[[geometric homotopy type]]_) is the analog in [[(∞,1)-category]] theory of the notion of [[sheaf]] ([[geometric type]]) in ordinary [[category theory]].

See [[(∞,1)-category of (∞,1)-sheaves]] for more.

## Definition

Given an [[(∞,1)-site]] $C$, let $S$ be the class of [[monomorphism in an (∞,1)-category|monomorphisms]] in the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ that correspond to [[covering]] [[(∞,1)-sieve]]s

$$
  \eta : U \hookrightarrow j(c)
$$

on objects $c \in C$, where $j$ is the [[(∞,1)-Yoneda embedding]]. 

Then an [[(∞,1)-presheaf]] $A \in PSh_{(\infty,1)}(C)$ is an **$(\infty,1)$-sheaf** if it is an $S$-[[local object]]. That is, if for all such $\eta$ the morphism

$$
  A(c) \simeq PSh_C(j(c),A) \stackrel{PSh_C(\eta,A)}{\to}
  PSh(U,A)
$$

is an [[equivalence in a quasi-category|equivalence]]. For a presheaf $A : C^{\op} \to E$ with values in an arbitrary ∞-category, we say it is a sheaf iff $E(e, A(-))$ is a sheaf for every object $e$ of $E$.

This is the analog of the ordinary sheaf condition for covering sieves. The [[∞-groupoid]] $PSh_C(U,A)$ is also called the [[descent]]-[[∞-groupoid]] of $A$ relative to the covering encoded by $U$.

As in the 1-categorial case, the sheaf condition for a covering sieve can be translated into a condition on a covering family that generates it:

+-- {: .num_defn}
###### Proposition

Let $\{ u_i \to c \}$ be a family of morphisms of $C$ that generate the sieve corresponding to $\eta : U \hookrightarrow j(c)$, and let $r_\bullet : \mathbf{\Delta}^{\op} \to PSh_C$ be the [[groupoid object in an (infinity,1)-category#cech_nerves|Čech nerve]]
of $\amalg_i j(u_i) \to j(c)$.
Then a presheaf $A$ is local with respect to $\eta$ iff the induced map $A(c) \to \lim A(r_\bullet)$ is an equivalence.
=--

Thus, a presheaf $A$ is a sheaf iff every covering sieve contains
a generating family satisfying this condition. Spelling out the description of the Čech nerve, the condition is that we have
$$
  A(c) \simeq \lim\left(
  \prod_i A(u_i)
  \stackrel{\to}{\to}
  \prod_{i,j} PSh_C(j(u_i) \times_{j(c)} j(u_j), A)
  \stackrel{\to}{\stackrel{\to}{\to}}
  \cdots
  \right)
$$
If $C$ has pullbacks, this simplifies to
$$
  A(c) \simeq \lim\left(
  \prod_i A(u_i)
  \stackrel{\to}{\to}
  \prod_{i,j} A(u_i \times_c u_j)
  \stackrel{\to}{\stackrel{\to}{\to}}
  \cdots
  \right)
$$
and furthermore this formulation applies to presheaves with values
in an arbitrary ∞-category.

+-- {: .proof}
###### Proof

Taking colimits of Čech nerve computes $(-1)$-truncations in $(PSh_C)/j(X)$,
so $\colim(r_\bullet)$ is the subobject of $j(c)$ corresponding
to the sieve $\eta$. We have
$$
  PSh_C(\colim(r_\bullet), A) \simeq \lim PSh_C(r_\bullet, A)
$$
and so the theorem follows.

=--


## Terminology

An **($\infty$,1)-sheaf** is also called an [[∞-stack]] with values in [[∞-groupoid]]s. 

The practice of writing "$\infty$-sheaf" instead of [[∞-stack]] is a rather reasonable one, since a [[stack]] is nothing but a _2-sheaf_. 

Notice however that there is ambiguity in what precisely one may mean by an $\infty$-stack: it can be an $(\infty,1)$-sheaf or more specifically a [[hypercomplete]] $(\infty,1)$-sheaf. This is a distinction that only appears in [[(∞,1)-topos]] theory, not in [[(n,1)-topos]] theory for finite $n$.

## Related concepts

* [[sheaf]]

* [[2-sheaf]] / [[stack]]

* **$(\infty,1)$-sheaf** / [[∞-stack]]

  * [[sheaf of spectra]]

  * [[sheaf of L-∞ algebras]]

* [[(∞,2)-sheaf]]

* [[(∞,n)-sheaf]]

[[!include homotopy n-types - table]]


## References

Section 6.2.2 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
 {#Lurie}


[[!redirects (infinity,1)-sheaves]]
[[!redirects infinity-sheaf]]
[[!redirects infinity-sheaves]]
[[!redirects (∞,1)-sheaf]]
[[!redirects (∞,1)-sheaves]]
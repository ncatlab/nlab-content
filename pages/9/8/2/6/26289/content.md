
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Motivation

In [[category theory]], there is one sensible notion of [[limit]], which is defined in terms of [[universal property|universal]] [[cones]]. However, when we move to [[enriched category theory]], such limits (which we now call **conical limits** to distinguish them from more general notions of limits) are no longer sufficient. By "sufficient", we mean here that there are notions in enriched category theory that are limit-like (such as [[powers]]) but that are not examples of conical limits. Furthermore, it is not true that the [[presheaf category|copresheaf construction]] exhibits the free completion under conical limits. This motivates the move to [[weighted limits]], which are the appropriate notion of limit for enriched categories. In particular, the copresheaf construction is the free completion under weighted limits, and powers are examples of weighted limits.

For a general [[monoidal category]] $V$, weighted limits are more general than conical limits. However, when $V = Set$, every weighted limit can be expressed as a conical limit. This is useful, as the conical limits are simpler to describe than weighted limits.

A particular [[base of enrichment]] of interest is $Cat$, so that enriched categories are precisely [[2-categories]]. The appropriate notion of limit for 2-categories is a weighted 2-limit, i.e. the usual notion of weighted limit for enriched categories (see [[2-limit]] for more details). Unlike for $V = Set$, conical 2-limits do not suffice to capture all weighted 2-limits. Intuitively, cones only capture 1-cells, whereas it is also necessary to capture 2-cells for the appropriate notion of 2-limit.

However, it turns out that, just as every weighted limit for $V = Set$ can be reduced to a conical limit, every weighted limit for $V = Cat$ can be reduced to a simpler kind of limit, called a **marked limit**. This is useful, as it makes working with 2-limits easier than working with general weighted limits.

## History and terminology

While the notion of marked 2-limit goes back a long way, for one reason or another they have remained overlooked until recently.

* Marked 2-limits were introduced by [[John Gray]] in [[Adjointness for 2-Categories]] as **cartesian quasi-limits**.
* [[Ross Street]] proved the equivalence between marked 2-limits and weighted 2-limits.
* Szyld studied such 2-limits, calling them **$\sigma$-s-limits**.
* The terminology **marked** appears in [Gagna–Harpaz–Lanari](#GHL22).
* A particular class of marked 2-limits, called **lax normal conical 2-limits**, (which suffices to capture all 2-limits) was studied by Mesiti.

## Definition

Let $F : A \to B$ be a [[2-functor]] between [[2-categories]], and let $A'$ be a locally full sub-2-category of $A$ (alternatively: a class of morphisms of $A$ closed under identities and composition). A **marked-lax limit** of $(A', F)$ is an object $m_l lim (A', F)$ together with a family of isomorphisms
$$B(b, m_l lim (A', F)) \cong [A, B]_{l, A'}(\Delta(b), F)$$
natural in $b \in B$, where $[A, B]_{l, A'}(\Delta(b), F)$ is the 2-category of [[2-functors]] $A \to B$, marked-lax natural transformations ([[lax natural transformations]] $\alpha$ such that $\alpha_f = 1$ if $f \in A'$), and [[modifications]].

## Related pages

* [[2-limit]]
* [[double limit]]
* [[F-category]]
* [[marked simplicial set]]

## References

The concept is introduced in the following, where marked 2-limits are called *cartesian quasi-limits*:

* [[Adjointness for 2-Categories]]

It was generalised in section 0.2 of:

* [[Robert Blackwell]], _Some existence theorems in the theory of doctrines_, PhD thesis, UNSW Sydney, 1976.

The equivalence to weighted 2-limits is first proven in:

* {#StreetLimitsIndexed} [[Ross Street]], _Limits indexed by category-valued 2-functors_ Journal of Pure and Applied Algebra **8**, Issue 2 (1976) pp 149-181. doi:[10.1016/0022-4049(76)90013-X](https://doi.org/10.1016/0022-4049(76%2990013-X)

* M.E. Descotte, [[Eduardo J. Dubuc]], M. Szyld, _Sigma limits in 2-categories and flat pseudofunctors_, (v1: On the notion of flat 2-functors) [arXiv:1610.09429](https://arxiv.org/abs/1610.09429) Adv. Math. __333__ (2018) 266--313

* Martin Szyld. _Lifting PIE limits with strict projections_ (2018), ([arXiv:1809.04712](https://arxiv.org/abs/1809.04712))

* [[Luca Mesiti]], *The 2-Set-enriched Grothendieck construction and the lax normal conical 2-limits* (2023), &lbrack;[arXiv:2302.04566](https://arxiv.org/abs/2302.04566)&rbrack;

On **marked bilimits**:

* {#GHL22} Andrea Gagna, Yonatan Harpaz, and Edoardo Lanari, _Bilimits are bifinal objects_, Journal of Pure and Applied Algebra 226.12 (2022): 107137.

* [[Ivan Di Liberti]], Axel Osmond, *Bi-accessible and bipresentable 2-categories.* &lbrack;[arXiv:2203.07046](https://arxiv.org/abs/2203.07046)&rbrack;

A proof of the equivalence between weighted 2-limits and marked 2-limits is given in the following, as well as a generalisation of these ideas to weighted limits for [[F-categories]]:

* Joanna Ko. _Dotted Limits_ (2023), ([arXiv:2306.01625](https://arxiv.org/abs/2306.01625))

[[!redirects marked 2-limits]]
[[!redirects marked limit]]
[[!redirects marked limits]]
[[!redirects marked 2-colimit]]
[[!redirects marked 2-colimits]]
[[!redirects marked colimit]]
[[!redirects marked colimits]]

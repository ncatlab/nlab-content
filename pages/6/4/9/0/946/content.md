
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# The specialisation topology
* table of contents
{: toc}

## Idea

The __specialisation topology__, also called the __Alexandroff topology__, is a natural structure of a [[topological space]] induced on the underlying [[set]] of a [[preordered set]].  This is similar to the [[Scott topology]], which is however coarser.

Spaces with this topology, called _Alexandroff spaces_ and named after [[Paul Alexandroff]] (Pavel Aleksandrov), should not be confused with _[[Alexandrov spaces]]_ (which arise in [[differential geometry]] and are named after [[Alexander Alexandrov]]).


## Definition

+-- {: .num_defn}
###### Definition

Let $P$ be a [[preordered set]].

Declare a [[subset]] $A$ of $P$ to be an _[[open subset]]_ if it is upwards-closed.  That is, if $x \leq y$ and $x \in A$, then $y \in A$.  

This defines a [[topology]] on $P$, called the **specialization topology** or **Alexandroff topology**.
=--

+-- {: .num_remark}
###### Remark

One may also use the convention that the open sets are the downwards-closed subsets; this is the specialisation topology on the [[opposite category|opposite]] $P^\op$.
=--


## Examples

* [[Sierpinski space]] is the poset of [[truth values]] with the specialisation topology.


## Properties

### General

+-- {: .num_prop}
###### Proposition

Every [[finite topological space]] is an Alexandroff space.

=--

+-- {: .num_prop}
###### Proposition

A [[preorder]] $P$ is a [[partial order|poset]] if and only if its specialisation topology is $T_0$.
=--

+-- {: .num_prop}
###### Proposition

A [[function]] between preorders is order-preserving if and only if it is a [[continuous map]] with respect to the specialisation topology.  
=--


### Alexandroff topological spaces

+-- {: .num_defn}
###### Definition

An **Alexandroff space** is a [[topological space]] for which arbitrary (as opposed to just finite) [[intersections]] of [[open subsets]] are still open.

Write 

$$
  AlexTop \hookrightarrow Top
$$

for the [[full subcategory]] of [[Top]] on the Alexandroff spaces.
=--

+-- {: .num_prop}
###### Proposition

Every Alexandroff space is obtained by equipping its [[specialization order]] with the Alexandroff topology.
=--

+-- {: .num_cor}
###### Corollary

The specialization topology embeds the category $\Pros$ of preordered sets [[full subcategory|fully-faithfully]] in the category [[Top]] of topological spaces.  

$$
  Proset \hookrightarrow Top
  \,.
$$

If we restrict to a [[finite set|finite]] underlying set, then the categories $\Fin\Pros$ and $\Fin\Top$ of finite prosets and [[finite topological spaces]] are [[equivalence of categories|equivalent]] in this way.

=--


### Alexandroff locales
 {#AlexandrovLocales}

+-- {: .num_defn}
###### Definition

Write $AlexLocale$ for the non-[[full subcategory|full]] [[subcategory]] of [[Locale]] whose

* [[object]]s are __Alexandroff locales__, that is locales of the form $Alex P$ for $P\in Poset$ with $Open(Alex(P)) = UpSets(P)$.
Equivalently, Alexandroff locales can be defined as [[locales]]
that admit a [[base]] consisting of supercompact opens,
i.e., opens $a$ for which any open cover of $a$ contains $a$ itself.

* [[morphisms]] are those morphisms of locales $f\colon Alex P \to Alex Q$, for which the dual [[inverse image]] morphism of [[frames]] $f^*\colon UpSet(Q) \to UpSet(P)$ has a [[left adjoint]] $f_!\colon UpSet(P) \to UpSet(Q)$.
=--

This appears as ([Caramello, p. 55](#Caramello)).

+-- {: .num_remark}
###### Remark

By the definition of the [[2-category]] [[Locale]] (see there), this means that $AlexPoset$ consists of those morphisms which have _right_ adjoints in [[Locale]].
=--

+-- {: .num_prop}
###### Proposition

The functor $Alex\colon Poset \to Locale$ factors through $AlexLocale$ and exhibits an [[equivalence of categories]]
$$
  Alex\colon Poset \stackrel{\simeq}{\to} AlexLocale.
$$
The inverse functor $$AlexLocale\to Poset$$
sends a locale $L$ to the [[poset]] of supercompact elements of $L$ (defined above)
and morphism $f\colon L\to L'$ to the restriction of $f_!$
to supercompact elements (which are preserved by $f_!$).
=--

This appears as ([Caramello, theorem 4.2](#Caramello)).

+-- {: .num_prop}
###### Proposition


The category of Alexandroff locales is equivalent to that of [[completely distributive lattice|completely distributive]] [[algebraic lattice]]s. 
=--

This appears as ([Caramello, remark 4.3](#Caramello)).


## Related concepts

* [[order topology]]

* [[Scott topology]]


## References

* Wikipedia (English), [Alexandrov topology](http://en.wikipedia.org/wiki/Alexandrov_topology)

The original article is

* [[Paul Alexandroff]], _Diskrete R&#228;ume_ ([web](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=5579&option_lang=eng)) (1973)

Details on Alexandroff spaces are in

* F. Arenas, _Alexandroff spaces_, Acta Math. Univ. Comenianae Vol. LXVIII, 1 (1999), pp. 17&#8211;25 ([pdf](http://www.emis.de/journals/AMUC/_vol-68/_no_1/_arenas/arenas.pdf))

* Timothy Speer, _A Short Study of Alexandroff Spaces_ ([arXiv:0708.2136](http://arxiv.org/abs/0708.2136))

A useful discussion of the abstract relation between posets and Alexandroff [[locales]] is in section 4.1 of

* [[Olivia Caramello]], _A topos-theoretic approach to Stone-type dualities_ ([arXiv:1103.3493](http://arxiv.org/abs/1103.3493))
 {#Caramello}

See also around page 45 in

*  [[Peter Johnstone]], _[[Stone Spaces]]_

A discussion of [[abelian sheaf cohomology]] on Alexandroff spaces is in 

* Morten Brun, Winfried Bruns, Tim R&#246;mer, _Cohomology of partially ordered sets and local cohomology of section rings_ Advances in Mathematics 208 (2007) 210&#8211;235 ([pdf](http://www.home.uni-osnabrueck.de/wbruns/brunsw/pdf-article/BrunBrunsRoemer.published.pdf)) 


[[!redirects specialization topology]]
[[!redirects specialization topologies]]
[[!redirects specialisation topology]]
[[!redirects specialisation topologies]]
[[!redirects Alexandroff topology]]
[[!redirects Alexandroff topologies]]
[[!redirects Alexandrov topology]]
[[!redirects Alexandrov topologies]]

[[!redirects Alexandroff space]]
[[!redirects Alexandroff spaces]]

[[!redirects Alexandroff locale]]
[[!redirects Alexandroff locales]]
[[!redirects Alexandrov locale]]
[[!redirects Alexandrov locales]]

[[!redirects completely distributive algebraic lattice]]
[[!redirects completely distributive algebraic lattices]]
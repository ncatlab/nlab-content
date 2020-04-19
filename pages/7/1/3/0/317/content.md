+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The __terminal category__ or __trivial category__ or __final category__ is [[generalized the|the]] [[terminal object]] in [[Cat]].  It is the unique (up to isomorphism) [[category]] with a single [[object]] and a single [[morphism]], necessarily the [[identity morphism]] on that object. It is often denoted $1$ or $\mathbf{1}$ or $\ast$.

In [[enriched category theory]], often instead of the terminal category one is interested in the [[unit enriched category]].


## Properties

A [[functor]] from the terminal category $1$ to any [[category]] $C$ is [[equivalence|equivalently]] an [[object]] of $C$.  More generally, the [[functor category]] $[1, C] \simeq C$ from the terminal category to $C$ is canonically [[equivalence of categories|equivalent]] (in fact, isomorphic) to the category $C$ itself.

The terminal category is a [[discrete category]] that, as a [[set]], may be called the _singleton_.  As a [[subset]] of the singleton, it is in fact a [[truth value]], true ($\top$).  In general, all of these (and their analogues in [[higher category theory]] and [[homotopy theory]]) may be called the [[point]].

So far we have interpreted "terminal" as referring to the 1-category $Cat$.  If instead we interpret "terminal" in the [[2-limit|2-categorical]] sense, then any category [[equivalence of categories|equivalent]] to the one-object-one-morphism category described above is also terminal.  A category is terminal in this sense precisely when it is [[inhabited set|inhabited]] and [[indiscrete category|indiscrete]].  For such a category $1$, the functor category $[1,C]$ is equivalent, but not isomorphic, to $C$.


+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a [[category]].

1. The following are equivalent:

   1. $\mathcal{C}$ has a [[terminal object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[right adjoint]]

      $$
        \ast 
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \mathcal{C}
      $$

    Under this equivalence, the [[terminal object]] is identified with the image under the right adjoint of the unique object of the [[terminal category]].

1. Dually, the following are equivalent:

   1. $\mathcal{C}$ has an [[initial object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[left adjoint]]

      $$
        \mathcal{C}
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \ast
      $$

    Under this equivalence, the [[initial object]] is identified with the image under the left adjoint of the unique object of the [[terminal category]].

=--


+-- {: .proof}
###### Proof

Since the unique [[hom-set]] in the [[terminal category]] is [[generalized the|the]] [[singleton]], the hom-isomorphism characterizing the [[adjoint functors]] is directly the [[universal property]] of an [[initial object]] in $\mathcal{C}$
 
$$
  Hom_{\mathcal{C}}( L(\ast) , X )
  \;\simeq\;
  Hom_{\ast}( \ast, R(X) ) 
  =
  \ast 
$$

or of a [[terminal object]]

$$
  Hom_{\mathcal{C}}( X , R(\ast) )
  \;\simeq\;
  Hom_{\ast}( L(X), \ast ) = \ast
  \,,
$$

respectively.

=--


## Related concepts

* [[initial category]]

* [[point]]

[[!redirects terminal categories]]

[[!redirects trivial category]]
[[!redirects trivial categories]]

[[!redirects final category]]
[[!redirects final categories]]

[[!redirects terminal groupoid]]
[[!redirects terminal groupoids]]



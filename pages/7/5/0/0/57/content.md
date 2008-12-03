#Idea#

Given an [[L-infinity algebroid|Infinity-Lie algebroid]] (for instance a Lie algebra, or a [[Lie algebroid]] or an [[L-infinity algebra]]) $\mathfrak{g}$ and given a $d$-dimensional manifold $P^d$ diffeomorphic to the $d$-dimensional disk $D^d$, let a **$d$-path in $\mathfrak{g}$** be a morhism of [[L-infinity algebroid]]s
$$
  \Sigma : T P^d \to \mathfrag{g}
  \,,
$$ 
where $T P^d$ denotes the _tangent Lie algebroid_ of $P^d$ (see the list of examples [[Lie algebroid|here]]).

By restricting such morphisms to parts of the boundary of $P^d$, the collections of all such $L_\infty$-algebroid $d$-paths naturally arrange themselves in diagrams of the form
$$
  S^\bullet(\mathrak{g})
  :=
  (
  \cdots 
  \to
  Hom_{L_\infty Alg}(T P^2, \mathfrak{g})
  \to
  Hom_{L_\infty Alg}(T P^1, \mathfrak{g})
  \to
  Hom_{L_\infty Alg}(T P^0, \mathfrak{g})
  )
  \,.
$$

In particular

* if $P^d = \Delta^d$ is the standard $d$-simplex, $d$-paths in $\mathfrak{g}$ naturally form a [[simplicial set]];

* if $P^d = D^d$ is the standard $d$-disk, $d$-paths in $\mathfrak{g}$ naturally form a [[globular set]].

Notice that morphisms of $L_\infty$-algebroids are, essentially by [[L-infinity algebroid|definition]] dual to morphisms of [[L-infinity algebroid|qDGCA]]s, so that the above can be equivalently rewritten as
$$
  S^\bullet(\mathrak{g})
  :=
  (
  \cdots 
  \to
  Hom_{qDGCAs}(CE(\mathfrak{g}), \Omega^\bullet(P^2))
  \to
  Hom_{qDGCAs}(CE(\mathfrak{g}), \Omega^\bullet(P^1))
  \to
  Hom_{qDGCAs}(CE(\mathfrak{g}), \Omega^\bullet(P^0))
  )
  \,.
$$

Here we used that the Chevalley-Eilenberg algebra of the tangent Lie algebroid is the deRham complex of differential forms, see the list of examples [[Lie algebroid|here]].

In this form these graded (simplicial/globular) sets associated to a [[L-infinity algebroid|qDGCA]] have been familiar as the [[Sullivan construction]] in [[rational homotopy theory]] since the late 1960s. In this context the interpretation of [[L-infinity algebroid|qDGCA]]s as Chevalley-Eilenberg algebras of $L_\infty$-algebroids is not usually mentioned, however, instead these differential algebras are thought of, equivalently, as models for deRham algebras of certain spaces.

But with the interpretation of qDGCAs as $L_\infty$-algebroids in hand, it is natural to ask for extra properties and structure on $S^\bullet(\mathfrak{g})$ that would allow to interpret $S^\infty(\mathfrak{g})$ as the graded set underlying an [[infinity-groupoid]].

This step, obvious as it may be with hindsight, was only made a few years ago. The general idea is roughly described (apparenntly first?) in

* Pavol &#352;evera, _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080)).

Of course one wants to regard in this context $S^\bullet(\mathfrak{g})$ not just as a graded _set_ but as a graded _space_. In

* Ezra Getzler, _Lie theory for nilpotent L-infinity algebras_, ([arXiv](http://arxiv.org/abs/math/0404003))

this $S^\bullet(\mathfrak{g})$ was realized 

* as [[internalization|internal to]] $Manifolds$ for the case that $\mathfrak{g}$ is a nilpotent $L_\infty$-algebra;

* as having the property of being a [[Kan-complex]].

This then makes $S^\bullet(\mathfrak{g})$ a _Lie $\infty$-groupoid_, which is regarded as the structure which _Lie-integrates_ $\mathfrak{g}$ in the context of [[Lie theory]].

Various variations of this theme are possible: in

* Andr&#233; Henriques, _Integrating $L_\infty$ algebras_,([arXiv](http://arxiv.org/abs/math.AT/0603563))

$S^\bullet(\mathfrak{g})$ is realized [[internalization|internal to ]] [[Banach manifold]]s, for $\mathfrak{g}$ an $L_\infty$-algebra.

Of course the properties of this general construction are best studied and understood for $\mathfrak{g}$ a Lie $n$-algebroid for low $n$. For $n=1$ this reproduces ordinary [[Lie theory]] and in particular [[Lie's three theorems]].


#Remark#

There is a way to understand [[Lie integration]] as being about forming fundamental $\infty$-groupoids of certain [[generalized smooth spaces]]. This is described here:

[[Schreiber:Lie theory|Lie theory]] in [Urs Schreiber's private $n$Lab area](http://ncatlab.org/schreiber/show/HomePage)
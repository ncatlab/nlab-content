
<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Given an $L_\infty$-[[Lie infinity-algebroid|algebroid]] (for instance a Lie algebra, or a [[Lie algebroid]] or an $L_\infty$-[[L-infinity-algebra|algebra]]) $\mathfrak{g}$ and given a $d$-dimensional manifold $P^d$ diffeomorphic to the $d$-dimensional disk $D^d$, let a **$d$-path in $\mathfrak{g}$** be a morhism of $L_\infty$-[[Lie infinity-algebroid|algebroid]]s
$$
  \Sigma : T P^d \to \mathfrak{g}
  \,,
$$ 
where $T P^d$ denotes the _tangent Lie algebroid_ of $P^d$ (see the list of examples [[Lie algebroid|here]]).

By restricting such morphisms to parts of the boundary of $P^d$, the collections of all such $L_\infty$-algebroid $d$-paths naturally arrange themselves in diagrams of the form

$$
  S^\bullet(\mathfrak{g})
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

Notice that morphisms of $L_\infty$-algebroids are, essentially by [[Lie infinity-algebroid|definition]], dual to morphisms of [[Lie infinity-algebroid|qDGCA]]s, so that the above can be equivalently rewritten as

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

Here we used that the Chevalley&#8211;Eilenberg algebra of the tangent Lie algebroid is the deRham complex of differential forms, see the list of examples [[Lie algebroid|here]].

In this form these graded (simplicial/globular) sets associated to a [[Lie infinity-algebroid|qDGCA]] have been familiar as the [[Sullivan construction]] in [[rational homotopy theory]] since the late 1960s. In this context the interpretation of [[Lie infinity-algebroid|qDGCA]]s as Chevalley&#8211;Eilenberg algebras of $L_\infty$-algebroids is not usually mentioned, however, instead these differential algebras are thought of, equivalently, as models for deRham algebras of certain spaces.

But with the interpretation of qDGCAs as $L_\infty$-algebroids in hand, it is natural to ask for extra properties and structure on $S^\bullet(\mathfrak{g})$ that would allow to interpret $S^\infty(\mathfrak{g})$ as the graded set underlying an [[infinity-groupoid]].

This step, obvious as it may be with hindsight, was only made a few years ago. The general idea has been described  first in the article

* Pavol &Scaron;evera, _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080)).

Of course one wants to regard in this context $S^\bullet(\mathfrak{g})$ not just as a graded _set_ but as a graded _space_. In

* Ezra Getzler, _Lie theory for nilpotent L-infinity algebras_, ([arXiv](http://arxiv.org/abs/math/0404003))

this $S^\bullet(\mathfrak{g})$ was realized 

* as [[internalization|internal to]] [[Diff]] for the case that $\mathfrak{g}$ is a nilpotent $L_\infty$-algebra;

* as having the property of being a [[Kan complex]].

This then makes $S^\bullet(\mathfrak{g})$ a _Lie $\infty$-groupoid_, which is regarded as the structure which _Lie-integrates_ $\mathfrak{g}$ in the context of [[Lie theory]].

Various variations of this theme are possible: in

* Andr&eacute; Henriques, _Integrating $L_\infty$ algebras_,([arXiv](http://arxiv.org/abs/math.AT/0603563))

(whose origin possibly preceeds that of the previous article)
$S^\bullet(\mathfrak{g})$ is realized [[internalization|internal to]] [[Banach manifold]]s, for $\mathfrak{g}$ an $L_\infty$-algebra.

## The main technical issue: truncation and quotienting

The main technical point in these constructions is to ensure that the general construction can be realized internal to a category of well-behaved spaces. In particular, usually one wants to integrate a Lie $n$-algebroid to a Lie $n$-groupoid, which means that $S^\bullet(\mathfrak{g})$ has to be _truncated_ after degree $n$ and _quotienting_ out $(n+1)-cells$ by replacing the space of $n$-paths $S^n(\mathfrak{g})$ in the $L_\infty$-algebroid with the _quotient space_ $S^n(\mathfrak{g})/S^{n+1}(\mathfrak{g})$ of $n$-paths modulo $(n+1)$-dimensional homotopy.

By the old [[dichotomy between nice objects and nice categories]], the more well-behaved a space is the less likely is this quotient still to be well behaved. 

One can 

* either carefully try to cut down $S^\bullet(\mathfrak{g})$ to something small and well behaved (this is the strategy in Getzler's work [#](http://arxiv.org/abs/math/0404003));

* or one realizes these quotients as suitable [[generalized smooth space|generalized spaces]] (this is the strategy in Zhu's work [[Lie theory for stacky Lie groupoids|#]]).


##Lie integration in low categorical dimension##

Unsurprisingly, the properties of this general construction are best studied and understood for $\mathfrak{g}$ a Lie $n$-algebroid for low $n$. For $n=1$ it reproduces ordinary [[Lie theory]] and in particular [[Lie's three theorems]] (see there for details), at least if one passes to [[generalized smooth space]]s.



## Remark

There is a way to understand [[Lie integration]] as being about forming fundamental $\infty$-groupoids of certain [[generalized smooth space]]s. This is described at
[[Schreiber:Lie theory|Lie theory]] in the [private $n$Lab area](http://ncatlab.org/schreiber/show/HomePage).
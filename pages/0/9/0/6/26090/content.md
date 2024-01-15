
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



* table of contents
{: toc}

## Idea

A *clan* in the sense of [Joyal 2017, Def. 1.1.1](#Joyal17) (previously: *category with [[display maps]]* &lbrack;[Taylor 1987, §4.3.2](#Taylor87)&rbrack;, or *display category* &lbrack;[Taylor 1999, §8.3](#Taylor99)&rbrack;, a non-strict notion of [[contextual categories]]) is a minimum notion of [[fibration category]] providing [[categorical semantics for dependent types]] modelling (just) [[context extension]] and [[dependent pair type]]-[[type formation|formation]] (but not necessarily, say, [[function types]] or [[identity types]]):

## Definition

A clan is a [[category]] with a [[terminal object]] equipped with a sub-[[class]] $Fib \subset Mor$ of its [[morphisms]], to be called the *[[fibrations]]* and serving the role of [[display maps]], such that:

1. every [[isomorphism]] is in $Fib$,

1. for every [[object]] $X$ the [[terminal object|terminal map]] $X \to \ast$ is in $Fib$ (hence all objects are [[fibrant object|fibrant]], cf. *[[category of fibrant objects]]*),

1. for $f \in Fib$ and $h$ any [[cospan|coincident]] morphism, the [[base change]] ([[pullback]])  $h^\ast f$ exits and is in $Fib$ (this interprets [[context extension]])

1. for composable $f,g \in Fib$ also their [[composition]] $g \circ f \in Fib$ (this interprets [[dependent pair type]]-[[type formation]])



## Related concepts

* [[fibration category]]

* [[category of fibrant objects]]

* [[categorical semantics of dependent types]]

  * [[tribe]]

  * [[type-theoretic model category]]


## References

The definition of *categories with [[display maps]]* and their role as [[categorical semantics for dependent types]] is due to

* {#Taylor87} [[Paul Taylor]], §4.3.2 in: *Recursive Domains, Indexed Category Theory and Polymorphism*, Cambridge (1983-7) &lbrack;[[Taylor-IndexedCategoryTheory.pdf:file]]&rbrack;

being a non-strict version of [[contextual categories]]:

* {#Taylor99} [[Paul Taylor]], §8.3 in: _[[Practical Foundations of Mathematics]]_, Cambridge University Press (1999) &lbrack;[webpage](http://www.paultaylor.eu/~pt/prafm/index.html)&rbrack;

The terminology "clan" for this notion is due to:

* {#Joyal17} [[André Joyal]], _Notes on Clans and Tribes_ &lbrack;[arxiv:1710.10238](https://arxiv.org/abs/1710.10238)&rbrack;

but the general notion of [[categorical semantics of dependent types]] is classical, going back at least to [Seely 1984](relation+between+type+theory+and+category+theory#Seely84b) and  [Hofmann 1997](categorical+semantics+of+dependent+type+theory#Hofmann97).

The type-theory-literature traditionally refers to such categories generically as *[[display map]]/[[fibration categories]] with such-and-such types*, eg. 

[North 2019, Rem. 2.4](#North19):

> The definitions in this section are relatively standard in the literature. A display map category which models [[dependent pair type|$\Sigma$-types]] coincides with Joyal’s notion of *clan*, and a display map category which models [[dependent pair type|$\sum$-types]] and [[dependent function type|$\prod$-types]] coincides with his notion of *$\pi$-clan*.

* {#North19} [[Paige Randall North]], *Identity types and weak factorization systems in Cauchy complete categories*, Mathematical Structures in Computer Science **29** 9 (2019) 1411-1427 &lbrack;[doi:10.1017/S0960129519000033](https://doi.org/10.1017/S0960129519000033), [arXiv:1901.03567](https://arxiv.org/abs/1901.03567)&rbrack;







[[!redirects clans]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Serre-Swan theorem_ identifies suitable [[modules]] over an [[algebra of functions]] on some [[space]] with the modules of [[sections]] of [[vector bundles]] over that space and thereby identifies these modules with vector bundles themselves.

Together with theorems like _[[Gelfand duality]]_, the Serre-Swan theorem is a central part of the [[Isbell duality|general duality]] between [[geometry]] and [[algebra]].
In particular it may serve to generalize the notion of vector bundle from standard [[geometry]] to more exotic forms of geometry, such as [[noncommutative geometry]].

## Statement

There are two different original theorems of the same intuitive spirit which are usually jointly called the **Serre-Swan theorem**, the first one is in [[algebraic geometry]], the second in [[topology]]:

1) **Serre's theorem** ([Serre 55](#Serre55)): let $R$ be a commmutative unital [[Noetherian ring]] (in particular, the [[structure sheaf|coordinate ring]] of an [[affine variety]] over a [[field]]), then the [[category]] of finitely-generated _[[projective module|projective]] $R$-[[modules]] is [[equivalence of categories|equivalent]] to the category of [[algebraic vector bundles]] (= [[covering|locally]] [[free module|free]] [[sheaves]] of [[structure sheaf]]-[[modules]] of constant finite [[rank]]) on $Spec R$.

2) **Swan's theorem** ([Swan 62](#Swan)): Given a [[Hausdorff space|Hausdorff]] [[compact space]] $X$, the [[category]] of [[finitely generated module|finitely generated]] [[projective modules]] over the [[continuous function|continuous]]-[[function algebra]] $C(X)$ is [[equivalence of categories|equivalent]] to the category of finite-[[rank]] [[vector bundles]] on $X$, where the equivalence is established by sending a vector bundle to the its module of continuous [[sections]].

But there are also various variations of these theorems, for instance to [[differential geometry]]:

3) **[[smooth Serre-Swan theorem]]** ([Nestruev 03, 11.33](#Nestruev03)) For $X$ a [[smooth manifold]] with $\mathbb{R}$-algebra of [[smooth functions]] $C^\infty(X)$ there is an [[equivalence of categories]] between that of finite [[rank]] smooth [[vector bundles]] over $X$ and [[finitely generated objects|finitely generated]] [[projective modules]] over $C^\infty(X)$.


A general statement of the Serre-Swan theorems over [[ringed spaces]] is in ([Morye](#Morye)).

If one drops the condition that the [[sheaf of modules]] over the [[structure sheaf]] of a [[ringed space]] is [[covering|locally]] [[free module|free]], and allows it instad to be just _locally [[presentable module|presentable]]_, then one arrives at the notion of [[quasicoherent sheaf of modules]]. Here the Serre-Swan theorem serves to clarify in which sense precisely these are generalizations of [[vector bundles]].

The condition that the modules be [[projective module|projective]] can also naturally be relaxed.
In [[higher geometry]] the Serre-Swan theorem becomes not only more general but also conceptually simpler: if instead of [[modules]] one considers [[chain complexes]] of modules ([[(∞,1)-modules]]) then under mild assumptions (see at _[[projective resolution]]_) every chain complex of modules is [[equivalence|equivalent]] ([[quasi-isomorphism|quasi-isomorphic]]) to a chain complex of [[projective modules]], and hence this condition in the statement of the traditional Serre-Swan theorem becomes automatic. Or in other words, the non-projective modules also do correspond to [[vector bundles]], but to [[chain complexes]] of vector bundles (only that the [[chain homology]] of the complex is not itself a vector bundle again in this case). See at _[[(∞,1)-vector bundle]]_ for more on this.

## Applications

### To K-theory

The Serre-Swan theorem serves to relate [[topological K-theory]] with [[algebraic K-theory]]. (...)



## Related concepts

* [[Gelfand duality]]

* [[operator K-theory]] 

* [[Quillen-Suslin theorem]]

* [[smooth Serre–Swan theorem]]

* [[duality between geometry and algebra]]

[[!include Isbell duality - table]]


## References

The two original articles are

* {#Serre55} [[Jean-Pierre Serre]], _Faisceaux algebriques coherents_, Annals of Mathematics 61 (2): 197&#8211;278 (1955)
 

* {#Swan} [[Richard Swan]], _Vector bundles and projective modules_, Trans. AMS __105__ (2): 264&#8211;277 (1962)
 

A textbook account in the context of [[differential geometry]] is in 

* {#Nestruev03} [[Jet Nestruev]], _Smooth manifolds and observables_, Graduate texts in mathematics, 220, Springer-Verlag, ISBN 0-387-95543-7 (2003)
 

A general account of Serre-Swan-type theorems over [[ringed spaces]] is in 

* {#Morye} [[Archana Morye]], _Note on the Serre-Swan Theorem_ ([arXiv:0905.0319](http://arxiv.org/abs/0905.0319))
 

A textbook account on the use of the theorem in [[K-theory]] is for instance

* [[Max Karoubi]], _$K$-theory. An introduction_, Grundlehren der Mathematischen Wissenschaften, Band __226__, Springer 1978. xviii+308 pp. 


[[!redirects Serre–Swan theorem]]
[[!redirects Serre--Swan theorem]]
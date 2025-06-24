
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

3) **[[smooth Serre-Swan theorem]]** ([Nestruev 02, 11.33](#Nestruev02)) For $X$ a [[smooth manifold]] with $\mathbb{R}$-algebra of [[smooth functions]] $C^\infty(X)$ there is an [[equivalence of categories]] between that of finite [[rank]] smooth [[vector bundles]] over $X$ and [[finitely generated objects|finitely generated]] [[projective modules]] over $C^\infty(X)$.


A general statement of the Serre-Swan theorems over [[ringed spaces]] is in [Morye 2017](#Morye17).

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

* [[modules over a ring are equivalent to quasicoherent sheaves over its spectrum]]

* [[duality between geometry and algebra]]


[[!include Isbell duality - table]]


## References

The two original articles:

* {#Serre55} [[Jean-Pierre Serre]], §50 in: *Faisceaux algebriques coherents*, Annals of Mathematics **61** 2 (1955) 197-278  &lbrack;[jstor:1969915](https://www.jstor.org/stable/1969915)&rbrack;
 
* {#Swan} [[Richard Swan]], *Vector bundles and projective modules*, Trans. AMS **105** 2 (1962) 264-277 &lbrack;[doi:10.2307/1993627](https://doi.org/10.2307/1993627)&rbrack;
 

A textbook account in the context of [[differential geometry]]:

* {#Nestruev02} [[Jet Nestruev]]: *Smooth manifolds and Observables*, Graduate Texts in Mathematics **220** Springer (2002, 2020) &lbrack;ISBN:0-387-95543-7, [doi:10.1007/978-3-030-45650-4](https://doi.org/10.1007/978-3-030-45650-4), [book webpage](https://diffiety.mccme.ru/books/nestrspr.htm),  <a href="https://nzdr.ru/data/media/biblio/kolxoz/M/MD/MDdg/Nestruev%20J.%20Smooth%20Manifolds%20and%20Observables%20(ISBN%200387955437)(Springer,%202003)(224s)_MDdg_.pdf">pdf</a>&rbrack;

See also

* G. Sardanashvily, _Remark on the Serre-Swan theorem for non-compact manifolds_, [arXiv](https://arxiv.org/abs/math-ph/0102016).

For the case of Hilbert bundles, see

* Jens Kaad, _A Serre–Swan theorem for bundles of bounded geometry_, Journal of Functional Analysis 265:10 (2013), 2465-2499.  [arXiv](https://arxiv.org/abs/1302.3310), [doi](https://doi.org/10.1016/j.jfa.2013.06.005).



A general account of Serre-Swan-type theorems over [[ringed spaces]] is in 

* [[Archana S. Morye]]: *Note on the Serre‐Swan theorem*, Mathematische Nachrichten **286** 2-3 (2013) 272-278  &lbrack;[arXiv:0905.0319](http://arxiv.org/abs/0905.0319), [doi:10.1002/mana.200810263](https://doi.org/10.1002/mana.200810263)&rbrack;

* {#Morye17} [[Archana S. Morye]]: *The Serre-Swan Theorem for Ringed Spaces*, in: *Analytic and Algebraic Geometry*, Springer (2017) 207-223 &lbrack;[doi:10.1007/978-981-10-5648-2_1](https://doi.org/10.1007/978-981-10-5648-2_13)&rbrack;

A textbook account on the use of the theorem in [[K-theory]] is for instance

* [[Max Karoubi]], _$K$-theory. An introduction_, Grundlehren der Mathematischen Wissenschaften, Band __226__, Springer 1978. xviii+308 pp. 


[[!redirects Serre–Swan theorem]]
[[!redirects Serre--Swan theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given an [[adjoint pair]] of [[functors]] $(f^\ast \dashv f_\ast)$ or $(f_! \dashv f^\ast)$ between two [[monoidal categories]] such that $f^\ast$ is a [[strong monoidal functor]], then the _projection morphism_ is the canonical [[natural transformation]] of the form

$$
  B \otimes f_\ast A \longrightarrow f_\ast (f^\ast B \otimes A)
$$

or 

$$
  f_! (f^\ast B \otimes A) \longrightarrow  B \otimes f_! A 
$$

respectively. If these morphisms are [[equivalences]] then one often calls them the **projection formula** or the **reciprocity** relation.

## Examples

Examples include the [[six operations]] setup in [[Grothendieck context]] and [[Wirthmüller context]], respectively (in a [[transfer context]] both pushforward maps satisfy their projection formula). In particular in [[representation theory]] and in [[formal logic]] reciprocity is also called _[[Frobenius reciprocity]]_, see there for more.

For more examples see also at MO _[Where do all the projection formulas come from?](http://mathoverflow.net/q/67228/381)_

## Related concepts

* [[monoidal adjunction]]

* [[dependent linear type theory]]

* [[Frobenius reciprocity]], [[Beck-Chevalley condition]]

## References

Discussion in a context of [[formal logic]]:

* [[Bill Lawvere]], p. 6 in: _[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970) 1-14 &lbrack;[pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf)&rbrack;


Discussion in [[real cohomology]] for [[integration of differential forms]]:

* [[Raoul Bott]], [[Loring Tu]], Prop. 6.15 in: _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/978-1-4757-3951-0](https://link.springer.com/book/10.1007/978-1-4757-3951-0))

Discussion in the context of [[Grothendieck's yoga of six functors]]:

* [[Martin Gallauer]], p. 11 of *An introduction to six-functor formalism*, lecture at *[The Six-Functor Formalism and Motivic Homotopy Theory](https://sites.google.com/view/summer-school-motivic/home)*, Università degli Studi di Milano (Sept. 2021) &lbrack;[arXiv:2112.10456](https://arxiv.org/abs/2112.10456), [pdf](https://homepages.warwick.ac.uk/staff/Martin.Gallauer/docs/m6ff.pdf)&rbrack;

A general abstract account is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_, Theory and Applications of Categories , Vol. 11, 2003, No. 4, pp 107-131. ([TAC](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 {#May05}

For the [[Grothendieck context]] of [[quasicoherent sheaves]] in [[E-infinity geometry]] the projection formula appears as remark 1.3.14 in 

* [[Jacob Lurie]], _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

See also 

* MathOverflow, _[Where do all the projection formulas come from?](http://mathoverflow.net/q/67228/381)_

* MathOverflow, _[Ubiquity of the push-pull formula](http://mathoverflow.net/q/18799/381)_

[[!redirects reciprocity]]

[[!redirects projection formulas]]
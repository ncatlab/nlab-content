
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

> under construction


#Contents#
* table of contents
{:toc}

## Idea

Central aspects of _finite_ [[quantum mechanics]] (with finite-dimensional [[space of states|state space]], notably for [[tensor products]] of [[qbit]] states) and [[quantum computation]] follow formally from the formal properties of the [[category]] [[Hilb|FinHilb]] of [[finite-dimensional vector space|finite-dimensional]] [[Hilbert spaces]]. These properties are axomatized by saying that [[Hilb]] is an example of a _[[†-compact category]]_.

Conversely, much of finite quantum mechanics and quantum computation can be formulated in _any_ &#8224;-compact category, and general reasoning about &#8224;-compact categories themselves yields results about quantum mechanics and quantum computation.

A transparent [[string diagram]] calculus in &#8224;-compact categories as exposed in ([Coecke, Kindergarten quantum mechanics](#CoeckeKindergarten)) provides an intuitive and powerful tool for reasoning in $\dagger$-compact categories.


## Quantum mechanical concepts in $\dagger$-compact categories

Let $(C,\otimes,I, \dagger)$ be a [[†-compact category]].

We list various concepts in quantum mechanics and their corresponding incarnation in terms of structures in $C$.

### Classical measurement outcomes

An [[observable]] in quantum mechanics formulated on a [[Hilbert space]] is modeled by a [[self-adjoint operator]], and the classical measurement outcomes of this operator provide, at least under some assumptions, an [[orthogonal basis]] on the [[Hilbert space]].

That, more abstractly, the notion of orthogonal basis of an object can be phrased intrinsically inside any suitable $\dagger$-compact category is the point made in ([CoeckePavlovicVicary](#CoeckePavlovicVicary)). 


### Complex phases

The underlying "algebra of quantum amplitudes" of the corresponding quantum mechanical system is the [[endomorphism]] [[monoid]] of the tensor unit

$$
  \mathbb{C}_C = End_C(I)
  \,.
$$


In ([Vicary](#Vicary)) it is shown that in $\dagger$-compact categories with all finite limits over certain "tree-like" diagrams compatible with the $\dagger$-structure, this $\mathbb{C}_C$ has the properties that

* it is a [[field]] of characteristic 0 with involution $\dagger$;

* the subfield $\mathbb{R}_C$ fixed under $\dagger$ is [[order]]able.

If furthermore every bounded sequence of measurements in $C$ with values in $\mathbb{R}_C$ has a least upper bound, then it follows that this field coincides with the [[complex number]]s 

$$
  \mathbb{C}_C = \mathbb{C}
$$

and moreover

$$
  \mathbb{R}_C = \mathbb{R}
  \,.
$$



### Completely positive maps {#ComplPosMaps}

The behaviour of [[quantum channel]]s and _completely positive maps_ has an elegant categorical description in terms of $\dagger$-compact categories. See ([Selinger](#SelingerPositive) and [Coecke](#CoeckePositive)).


## Quantum logic

[[symmetric monoidal categories|Symmetric monoidal categories]] such as [[†-compact categories]] have as [[internal logic]] a fragment of [[linear logic]] and as [[type theory]] a flavor of [[linear type theory]]. In this fashion everything that can be formally said about quantum mechanics in terms of [[†-compact categories]] has an equivalent expression in [[formal logic]]/[[type theory]]. It has been argued ([Abramsky-Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06)) that this [[linear logic]]/[[linear type theory]] of quantum mechanics is the correct formalization of "[[quantum logic]]". An exposition of this point of view is in ([Baez-Stay 09](#BaezStay09)).


## Related concepts

* [[order-theoretic structure in quantum mechanics]]

* [[linear logic]], [[linear type theory]], [[quantum logic]], [[quantum computing]]

* [[JBW-algebraic quantum mechanics]]

* [[tensor network]], [[string diagram]]

## References
 {#References}

The idea that the natural language of [[quantum mechanics]] and [[quantum computation]] is that of [[†-compact categories]] became popular with the publication

* {#AbramskyCoecke} [[Samson Abramsky]], [[Bob Coecke]], _A categorical semantics of quantum protocols_ , Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) ([arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130))

with an expanded version in 

* {#AbramskyCoecke08} [[Samson Abramsky]], [[Bob Coecke]], _Categorical quantum mechanics_, in _Handbook of Quantum Logic and Quantum Structures vol II_, Elsevier, 2008 ([arXiv:0808.1023](http://arxiv.org/abs/0808.1023))
 

A fairly comprehensive account of the underlying theory of [[string diagrams]] is in

* {#Selinger} [[Peter Selinger]], _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))


A pedagogical exposition of the graphical calculus is in

* {#CoeckeKindergarten} [[Bob Coecke]], _Kindergarten quantum mechanics_ ([arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032))


* {#CoeckePicturalism} [[Bob Coecke]], _Quantum Picturalism_ ([arXiv:0908.1787](http://arxiv.org/abs/0908.1787))


More basic introductions are in

* {#CoeckeIntroducing} [[Bob Coecke]], _Introducing categories to the practicing physicist_ ([arXiv:0808.1032](http://arxiv.org/abs/0808.1032))


* {#CoeckePractising} [[Bob Coecke]], _Categories for the practising physicist_ ([arXiv:0905.3010](http://arxiv.org/abs/0905.3010))

* {#HeunenVicary12} [[Chris Heunen]], [[Jamie Vicary]], _Lectures on categorical quantum mechanics_, 2012 ([pdf](https://www.cs.ox.ac.uk/files/4551/cqm-notes.pdf))


A comprehensive collection of basics and of recent developments is in 

* [[Bob Coecke]], [[Ross Duncan]], _Interacting Quantum Observables: Categorical Algebra and Diagrammatics_ ([arXiv:0906.4725](http://arxiv.org/abs/0906.4725))

The formalization of orthogonal bases in $\dagger$-compact categories is in 

* {#CoeckePavlovicVicary} [[Bob Coecke]], [[Dusko Pavlovic]], [[Jamie Vicary]], _A new description of orthogonal bases_ ([arXiv:0810.0812](http://arxiv.org/abs/0810.0812))


The role of [[complex numbers]] in general $\dagger$-compact categories is discussed in

* {#Vicary} [[Jamie Vicary]], _Completeness of $\dagger$-categories and the complex numbers_ ([arXiv:0807.2927](http://arxiv.org/abs/0807.2927)) 


[[quantum operation|Completely positive maps]] in terms of $\dagger$-categories are discussed in

* {#SelingerPositive} [[Peter Selinger]], _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))


* {#CoeckePositive} [[Bob Coecke]], _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 


The relation to [[quantum logic]]/[[linear logic]] has been expolred in 

* {#AbramskyDuncan05} [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_ ([arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114))
 

* {#Duncan06} [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf), [slides](http://www.cs.ox.ac.uk/people/ross.duncan/talks/2005/pps-22-05-2005.pdf))
 

An exposition along these lines is in

* {#BaezStay09} [[John Baez]], [[Mike Stay]], _Physics, topology, logic and computation: a rosetta stone_, [arxiv/0903.0340](http://arxiv.org/abs/0903.0340); in "New Structures for Physics", ed. Bob Coecke, Lecture Notes in Physics __813__, Springer, Berlin, 2011, pp. 95-174
 

[[!redirects finite quantum mechanics in terms of †-compact categories]]

[[!redirects quantum mechanics in terms of †-compact categories]]
[[!redirects quantum mechanics in terms of dagger-compact categories]]


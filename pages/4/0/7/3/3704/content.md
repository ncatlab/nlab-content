
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
* automatic table of contents goes here
{:toc}

## Idea

Crucial aspects of [[quantum mechanics]] and [[quantum computation]] follow formally from the formal properties of the [[category]] [[Hilb]] of [[Hilbert space]]s. These properties are axomatized by saying that [[Hilb]] is an example of a [[†-compact category]].

Conversely, much of quantum mechanics and quantum computation can be formulated in _any_ &#8224;-compact category, and general reasoning about &#8224;-compact categories themselves yields results about quantum mechanics and quantum computation.

A nice [[string diagram]] calculus in &#8224;-compact categories as exposed in ([Coecke, Kindergarten qunatum mechanics](#CoeckeKindergarten)) provides an intuitive and powerful tool for reasoning in $\dagger$-compact categories.


## Quantum mechanical concepts in $\dagger$-compact categories

Let $(C,\otimes,I, \dagger)$ be a [[†-compact category]].

We list various concepts in quantum mechanics and their corresponding incarnation in terms of structures in $C$.

### Classical measurement outcomes

An [[observable]] in quantum mechanics formulated on a [[Hilbert space]] is modeled by a [[self-adjoint operator]], and the classical measurement outcomes of this operator provide, at least under some assumptions, an [[orthogonal basis]] on the [[Hilbert space]].

That, more abstractly, the notion of orthognal basis of an object can be phrased intrinsically inside any suitable $\dagger$-compact category is the point made in ([CoeckePavlovicVicary](#CoeckePavlovicVicary))


### Complex phases

The underlying "algebra of quantum amplitudes" of the corresponding quantum mechanical system is the [[endomorphism]] [[monoid]] of the tensor unit

$$
  \mathbb{C}_C = End_C(I)
  \,.
$$


In ([Vicary](#Vicary)) it is shown that in $\dagger$-compact categories with all finite limits over certain "tree-like" diagrams compatible with the $\dagger$-structure, this $\mathbb{C}_C$ has the properties that

* it is a [[field]] of characteristic 0 with involution $\dagger$;

* the subfield $\mathbb{R}_R$ fixed under $\dagger$ is [[order]]able.

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



## References

The idea that the natural language of [[quantum mechanics]] and [[quantum computation]] is that of [[†-compact categories]] became popular with the publication

* [[Samson Abramsky]] and [[Bob Coecke]], _A categorical semantics of quantum protocols_ , Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) ([arXiv](http://arxiv.org/abs/quant-ph/0402130))
{#AbramskyCoecke}

A fairly comprehensive account of the underlying formalism is in

* Peter Selinger, _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))
{#Selinger}

A pedagogical exposition of the graphical calculus is in

* [[Bob Coecke]], _Kindergarten quantum mechanics_ ([arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032))
{#CoeckeKindegarten}

* [[Bob Coecke]], _Quantum Picturalism_ ([arXiv:0908.1787](http://arxiv.org/abs/0908.1787))
{#CoeckePicturalism}

More basic introductions are in


* [[Bob Coecke]], _Introducing categories to the practicing physicist_ ([arXiv:0808.1032](http://arxiv.org/abs/0808.1032))
{#CoeckeIntroducing}

* [[Bob Coecke]], _Categories for the practising physicist_ ([arXiv:0905.3010](http://arxiv.org/abs/0905.3010))
{#CoeckePractising}

The formalization of orthogonal bases in $\dagger$-compact categories is in 

* [[Bob Coecke]], [[Dusko Pavlovic]], [[Jamie Vicary]], _A new description of orthogonal bases_ ([arXiv:0810.0812](http://arxiv.org/abs/0810.0812))
{#CoeckePavlovicVicary}

The role of comoplex numbers in general $\dagger$-compact categories is discussed in

* [[Jamie Vicary]], _Completeness and the complex numbers_ ([arXiv:0807.2927](http://arxiv.org/abs/0807.2927)) 
{#Vicary}

Completely positive maps in terms of $\dagger$-categories are discussed in

* [[Peter Selinger]], _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))
{#SelingerPositive}


* [[Bob Coecke]], _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 
{#CoeckePositive}

[[!redirects quantum mechanics in terms of †-compact categories]]

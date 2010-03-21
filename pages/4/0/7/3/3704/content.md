<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


> under construction


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Crucial aspects of [[quantum mechanics]] and [[quantum computation]] follow formally from the formal properties of the [[category]] [[Hilb]] of [[Hilbert space]]s. These properties are axomatized by saying that [[Hilb]] is an example of a [[†-compact category]].

Conversely, Much of quanrtum mechanics and quantum computation can be formulated in _any_ &#8224;-compact category, and general reasoning about &#8224;-compact categories themselves yields results about quantum mechanics and quantum computation.

A nice [[string diagram]] calculus in &#8224;-compact categories as exposed in

* [[Bob Coecke]], _Kindergarten quantum mechanics_ ([arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032))

provides an intuitive and powerful tool for reasoning in $\dagger$-compact categories.



## Quantum mechanical concepts in $\dagger$-compact categories

Let $(C,\otimes,I, \dagger)$ be a $\dagger$-compact category.

We list various concepts in quantum mechanics and their corresponding incarnation in terms of structures in $C$.

### Complex phases

The underlying "algebra of quantum amplitudes" of the corresponding quantum mechanical system is the [[endomorphism]] [[monoid]] of the tensor unit

$$
  \mathbb{C}_C = End_C(I)
  \,.
$$


In 

* [[Jamie Vicary]], _Completeness and the complex numbers_ ([arXiv:0807.2927](http://arxiv.org/abs/0807.2927)) 

it is shown that In $\dagger$-compact categories with all finite limits over certain "tree-like" diagrams compatible with the $\dagger$-structure, this $\mathbb{C}_C$ has the properties that

* it is a [[field]] of characteristic 0 with involution $\dagger$;

* the subfield $\mathbb{R}_R$ fixed under $\dagger$ is orderable.

If furthermore every bounded sequence of measurements in $C$ with values in $\mathbbf{R}_C$ has a least upper bound, then it follows that this coincides with the [[complex number]]s and the [[real number]]s 

$$
  \mathbb{C}_C = \mathbb{C}
$$

$$
  \mthbb{R}_C = \mathbb{R}
  \,.
$$



### Completely positive maps

The behaviour of [[quantum channel]]s and _completely positive maps_ has an elegant categorical descriptin in terms of $\dagger$-compact categories

* [[Peter Selinger]], _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))

* [[Bob Coecke]], _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 


### More

## References

The idea that the natural language of [[quantum mechanics]] and [[quantum computation]] is that of [[†-compact categories]] became popular with the publication

* [[Samson Abramsky]] and [[Bob Coecke]], _A categorical semantics of quantum protocols_ , Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) ([arXiv](http://arxiv.org/abs/quant-ph/0402130))

A fairly comprehensive account of the underlying formalism is in

* Peter Selinger, _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))

A pedagogical exposition of the graphical calculus is in

* [[Bob Coecke]], _Kindergarten quantum mechanics_ ([arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032))

[[!redirects quantum mechanics in terms of †-compact categories]]

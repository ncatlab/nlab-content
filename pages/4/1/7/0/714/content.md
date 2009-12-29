# $\dagger$-categories
* tic
{: toc}


## Idea

The definition of a [[category]] effectively enforces an ordering on the "0-faces" -- the source and target objects -- of every 1-cell (every morphism). In many cases this is essential, in that there is no way to regard the generic morphism $a \stackrel{f}{\to} b$ in the generic category as a morphism from $b$ to $a$ instead.

But there are many categories for which this is not the case, where every morphism naturally only comes with the information of an unordered pair $\{a,b \}$ of objects, without any prejudice on which is to be regarded as source and which as target. An important general example is:

* the category $Spans(C)$ of [[span|spans]] in a category $C$ with pullbacks, or [[duality|dually]], the category $CoSpans(C)$ of [[cospan|cospans]] in a category $C$ with pushouts.

More concrete examples are:

* categories of [[cobordism]]s (but notice that cobordisms are naturally regarded as [[cospan]]s which makes this a special case of the above example);

* the category [[Hilb]] of Hilbert spaces, where for every linear map $f : H_1 \to H_2$ we also have the adjoint map (in the sense of Hilbert spaces, not in the categorical sense) $f^\dagger : H_2 \to H_1$ (but notice that according to [[groupoidification]] this is also essentially to be regarded as a special case of categories of spans).

A _dagger structure_ on a category is extra structure which encodes the idea of _removing_ the ordering information on the 0-faces of 1-cells in a category: it is is a contravariant functor which sends every morphism $f : a \to b$ to a morphims going the other way, $f^\dagger : b \to a$.

The notation and terminology here is motivated from the example [[Hilb]] of Hilbert spaces, where $f^\dagger$ is traditionally the notion for the adjoint of a linear map $f$.  The canonical dagger-structure on [[Hilb]] and on [[nCob]] is crucial in [[FQFT|quantum field theory]] where it is used to encode the idea of **unitarity**:

a _unitary_ [[FQFT|functorial QFT]] of dimension $n$ is supposed to be a functor $n Cob \to Hilb$ which respects the dagger-structure on both sides.

## Definition

A **dagger category** is a [[category]] $C$ equipped with a contravariant functor
$$
  \dagger : C \to C
$$
which is the identity on objects, and which satisfies $\dagger \circ \dagger = \mathrm{id}_C$.

Note that regarded as an extra structure on categories, a dagger structure is [[evil]], since it imposes equations on objects.

## Examples

* The category [[Rel]] of sets and [[relations]] is a dagger category, taking dagger as relational converse.

* More generally, let $C$ be a category with [[pullbacks]] and let $Span_1(C)$ be the 1-category of [[spans]] up to isomorphism: its morphisms are spans with one leg labeled as source, the other labeled as target. Then the functor $\dagger : Span_1(C)^{op} \to Span_1(C)$ which just exchanges this labeling is a dagger-structure on $Span_1(C)$.

* $\mathcal{R}(G)$, the category of unitary [[representation]]s of a (discrete) [[group]] $G$ and intertwining maps, is a dagger category. For an intertwiner $\phi : R \rightarrow S$, let $\phi^\dagger : S \rightarrow R$ be the adjoint of $\phi$ in [[Hilb]].


## Underlying groupoid

For the purpose of considering what makes two objects of a $\dagger$-category [[equivalence|equivalent]], one should not consider all [[isomorphism]]s (invertible morphisms) but rather all **unitary isomorphisms**: those morphisms $f$ whose adjoint is their inverse.

For example, in $Hilb$, there are many invertible linear operators, but only those of norm $1$ (the invertible isometries) are unitary.

The unitary isomorphisms form a [[groupoid]], which may be regarded as the _[[core]]_ of the $\dagger$-category.


## References

The concept of $\dagger$-category is discussed here:

* S. Abramsky and B. Coecke, A categorical semantics of quantum protocols, _Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04)_, IEEE Computer Science Press (2004).  [arXiv](http://arxiv.org/abs/quant-ph/0402130)

and further abstracted in:

* P. Selinger, Dagger compact closed categories and completely positive maps, _Proceedings of the 3rd International Workshop on Quantum Programming Languages_, Chicago, June 30&#8211;July 1, 2005. [web](http://www.mscs.dal.ca/~selinger/papers.html#dagger)

The importance of $\dagger$-categories in quantum theory is discussed here:

* [[John Baez]], Quantum quandaries: a category-theoretic perspective, in _Structural Foundations of Quantum Gravity_, eds. Steven French, Dean Rickles and Juha Saatsi, Oxford U. Press, 2006, pp. 240--265.  See especially Section 3: The $\star$-category of Hilbert spaces.  ([web](http://math.ucr.edu/home/baez/quantum/node3.html))

Note that in older literature, the term "$\star$-category"  or "star-category" is sometimes used instead of $\dagger$-category.

Certain specially nice $\dagger$-categories, such as $C^*$-categories and [[modular tensor category|modular tensor categories]], play an important role in topological quantum field theory and the theory of quantum groups:

* J&#252;rg Fr&#246;hlich and Thomas Kerler, _Quantum Groups, Quantum Categories, and Quantum Field Theory_, Springer Lecture Notes in Mathematics 1542, Springer-Verlag, Berlin, 1991. 

* Bojko Bakalov and Alexander Kirillov, Jr., _Lectures on Tensor Categories and Modular Functors_, American Mathematical Society, Providence, Rhode Island, 2001.
([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html))


[[!redirects dagger-categories]]
[[!redirects dagger category]]
[[!redirects dagger categories]]
[[!redirects †-category]]
[[!redirects †-categories]]
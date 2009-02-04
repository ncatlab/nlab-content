#Idea#

The definition of a [[category]] effectively enforces an ordering on the "0-faces" -- the source and target objects -- of every 1-cell (every morphism). In many cases this is essential, in that there is no way to regard the generic morphism $a \stackrel{f}{\to} b$ in the generic category as a morphism from $b$ to $a$ instead.

But there are many categories for which this is not the case, where every morphism naturally only comes with the information of an unordered pair $\{a,b \}$ of objects, without any prejudice on which is to be regarded as source and which as target. An important general example is

* the category $Spans(C)$ of [[span]]s in a category $C$ with pullbacks and, [[duality|dually]] the category $CoSpans(C)$ of [[cospan]]s in a category $C$ with pushouts.

More concrete examples are

* categories of [[cobordism]]s (but notice that cobordisms are naturally regarded as [[cospan]]s which makes this a special case of the above example);

* the category [[Hilb]] of Hilbert spaces, where for every linear map $f : H_1 \to H_2$ we also have the adjoint map (in the sense of Hilbert spaces, not in the categorical sense) $f^\dagger : H_2 \to H_1$ (but notice that according to [[groupoidification]] this is also essentially to be regarded as a special case of categories of spans).

A _dagger structure_ on a category is extra structure which encodes the idea of _removing_ the ordering information on the 0-faces of 1-cells in a category: it is is a contravariant functor which sends every morphism $f : a \to b$ to a morphims going the other way, $f^\dagger : b \to a$.


The notation and terminology here is motivated from the example [[Hilb]] of Hilbert spaces, where $f^\dagger$ is traditionally the notion for the adjoint of a linear map $f$.  The canonical dagger-structure on [[Hilb]] and on [[nCob]] is crucial in [[FQFT|quantum field theory]] where it is used to encode the idea of **unitarity**:

a _unitary_ [[FQFT|functorial QFT]] of dimension $n$ is supposed to be a functor $n Cob \to Hilb$ which respects the dagger-structure on both sides.


#Definition#

A **dagger category** is a [[category]] $C$ equipped with a contravariant functor
$$
  \dagger : C \to C
$$
which is the identity on objects, and which satisfies $\dagger \circ \dagger = \mathrm{id}_C$.

#Examples#

* Let $C$ be a category with pullbacks and let $Span_1(C)$ be the 1-category of [[span]]s up to isomorphism: its morphisms are spans with one leg labeled as source, the other labeled as target. Then the functor $\dagger : Span_1(C)^{op} \to Span_1(C)$ which just exchanges this labeling is a dagger-structure on $Span_1(C)$.

#References#

The formalizaiton of the $\dagger$-operation was first proposed in

* S. Abramsky and B. Coecke, _A categorical semantics of quantum protocols_, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) ((arXiv)[http://arxiv.org/abs/quant-ph/0402130])

and further abstracted in

* P. Selinger, _Dagger compact closed categories and completely positive maps_, Proceedings of the 3rd International Workshop on Quantum Programming Languages, Chicago, June 30&#8211;July 1, 2005 ((web)[http://www.mscs.dal.ca/~selinger/papers.html#dagger])
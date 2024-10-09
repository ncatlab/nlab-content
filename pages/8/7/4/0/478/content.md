
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In natural language, the definite article ('the' in English) is generally used only for nouns which are uniquely characterized by context.  Hence we have "the Moon" and "the book I was just reading," but only "a car" or "a wild late-night party." (Sometimes "the book I was just reading" is abbreviated to "the book", but it should be clear from context that only one book could be meant.) Philosophers call this use of the definite article to pick out an individual [[definite description]].

In [[mathematics]], and especially in [[category theory]], [[homotopy theory]]/[[homotopy type theory]] and generally in [[higher category theory]], it is common to use "the" more generally for [[objects]]/[[types]] which are characterized only up to [[coherence|coherent]] [[isomorphism]]/[[equivalence in an (infinity,1)-category|equivalence]]: Such need not actually be unique, but any two of them are [[isomorphism|isomorphic]] or more generally [[coherence|coherently]] [[equivalence in homotopy type theory|equivalent]] in an [[essentially unique]] way (meaning that the [[∞-groupoid]] of all such objects is [[contractible space|contractible]]).

For example, one speaks (assuming that any exists) of "the" [[terminal object]] of a category, "the" [[Cartesian product]] of two objects, "the" [[adjoint functor|left adjoint]] of a functor, and so on.  Outside of pure [[category theory]] we have examples such as "the" Dedekind-complete ordered field (the field of [[real numbers]]).



## Formalization

The notion of a "generalized the" can be formalized and treated uniformly in [[homotopy type theory]]. Here one may define an [[introduction rule]] for *the* as follows:

$$
  (A:Type),((a,p):IsContr(A)) \vdash (the(A,a,p):A).
$$

Here the [[term]] $(a,p)$ is one witness for the [[contractible type|contractibility]] of the [[type]] $A$. Then we have $the(A,a,p)=a:A$.

Since $IsContr(A)$ is itself [contractible](contractible+type#properties_18), we could say that $(a,p)$ is *the* witness for the contractibility of the type $A$, which may explain why we do not generally mention it.

If we wish to extend this treatment to types which are [[propositions]], we might call such types $FactThat(P)$, for some statement $P$. Then if $P$ holds, we can introduce a term $the(FactThat(P))$.


## References

The term "generalized the" was introduced by [[James Dolan]] and may first appear in print here:

* [[John Baez]], *Higher-dimensional algebra II: 2-Hilbert spaces*, Adv. Math. 127 (1997), 125-189.  ([arXiv:q-alg/9609018](http://arxiv.org/abs/q-alg/9609018))

Quoting:

> Given a tensor product of the 2-Hilbert spaces $H$ and $H'$, we often write its underlying 2-Hilbert space as $H \otimes H'$. This notation may tempt one to speak of ‘the’ tensor product of $H$ and $H'$, which is is legitimate if one uses the generalized ‘the’ as advocated by Dolan [7]. In a set, when we speak of ‘the’ element with a given property, we implicitly mean that this element is unique.  In a category, when we speak of ‘the’ object with a given property, we merely mean that this object is unique up to isomorphism — typically a specified isomorphism. Similarly, in a 2-category, when we speak of ‘the’ object with a given property, we mean that this object is unique up to equivalence — typically an equivalence that is specified up to a specified isomorphism. This is the sense in which we may refer to ‘the’ tensor product of $H$ and $H'$. The generalized ‘the’ may be extended in an obvious recursive fashion to $n$-categories.

Discussion in [[homotopy type theory]]:

* [[David Corfield]], _Expressing 'The Structure of' in Homotopy Type Theory_, Synthese 197, 681–700 ([doi:10.1007/s11229-017-1569-7](https://doi.org/10.1007/s11229-017-1569-7), [pdf](https://ncatlab.org/davidcorfield/show/Expressing+%27The+Structure+of%27+in+Homotopy+Type+Theory)), revised and expanded as Chapter 3 of [Modal Homotopy Type Theory: The Prospect of a New Logic for Philosophy](https://ncatlab.org/davidcorfield/show/Modal+Homotopy+Type+Theory).


[[!redirects the]]
[[!redirects generalised the]]
[[!redirects generalized the]]

[[!redirects unique]]
[[!redirects unique up to]]
[[!redirects unique up to unique isomorphism]]
[[!redirects unique up to unique coherent isomorphism]]
[[!redirects unique up to unique equivalence]]
[[!redirects unique up to unique coherent equivalence]]

[Spanish Version](https://chicksgold.com/blog/generalized-the) by [ChicksGold](https://chicksgold.com).

# Contents
* table of contents
{: toc}

## Idea

In natural language, the definite article ('the' in English) is generally used only for nouns which are uniquely characterized by context.  Hence we have "the United States of America" and "the book I was just reading," but only "a car" or "a wild late-night party." (Sometimes "the book I was just reading" is abbreviated to "the book", but it should be clear from context that only one book could be meant.) Philosophers call this use of the definite article to pick out an individual [[definite description]].

In [[mathematics]], and especially in [[category theory]], [[homotopy theory]] and [[higher category theory]], it is common to use "the" more generally for something which is characterized uniquely up to unique [[coherence|coherent]] [[isomorphism]] (that is, a unique isomorphism appropriate given the context).  

Thus, for instance, we speak (assuming that any exists) of "the" [[terminal object]] of a category, "the" [[product]] of two objects, "the" [[adjoint functor|left adjoint]] of a functor, and so on.  Outside of pure [[category theory]] we have examples such as "the" Dedekind-complete ordered field (the field of [[real numbers]]).

In [[higher category theory]], we extend this usage to objects that are characterized uniquely up to unique coherent [[equivalence]].  Of course, by "unique equivalence" we mean "unique up to 2-equivalence," and so on.  A more [[homotopy theory|homotopy-theoretic]] way to say this is that _the space ($\infty$-[[infinity-groupoid|groupoid]]) of all such objects is [[contractible space|contractible]]_.


## Formalization

The notion of a "generalized the" can be formalized and treated uniformly in [[homotopy type theory]]. Here one can define an [[natural deduction|introduction rule]] for *the* as follows:

$$
  (A:Type),((a,p):IsContr(A)) \vdash (the(A,a,p):A).
$$

Here the [[term]] $(a,p)$ is one witness for the [[contractible type|contractibility]] of the [[type]] $A$. Then we have $the(A,a,p)=a:A$.

Since $IsContr(A)$ is itself [contractible](contractible+type#properties_18), we could say that $(a,p)$ is *the* witness for the contractibility of the type $A$, which may explain why we do not generally mention it.

If we wish to extend this treatment to types which are [[propositions]], we might call such types $FactThat(P)$, for some statement $P$. Then if $P$ holds, we can introduce a term $the(FactThat(P))$.


## References

* [[David Corfield]], _Expressing 'The Structure of' in Homotopy Type Theory_, [pdf](https://ncatlab.org/davidcorfield/show/Expressing+%27The+Structure+of%27+in+Homotopy+Type+Theory), revised as Chapter 4 of _Modal Homotopy Type Theory: The Prospect of a New Logic for Philosophy_.

The term "generalized the" was introduced by James Dolan and may first appear in print here:

* [[John Baez]], Higher-dimensional algebra II: 2-Hilbert spaces, Adv. Math. 127 (1997), 125-189.  ([arxiv](http://arxiv.org/abs/q-alg/9609018))

Quoting:

> Given a tensor product of the 2-Hilbert spaces $H$ and $H'$, we often write its underlying 2-Hilbert space as $H \otimes H'$. This notation may tempt one to speak of ‘the’ tensor product of $H$ and $H'$, which is is legitimate if one uses the generalized ‘the’ as advocated by Dolan [7]. In a set, when we speak of ‘the’ element with a given property, we implicitly mean that this element is unique.  In a category, when we speak of ‘the’ object with a given property, we merely mean that this object is unique up to isomorphism — typically a specified isomorphism. Similarly, in a 2-category, when we speak of ‘the’ object with a given property, we mean that this object is unique up to equivalence — typically an equivalence that is specified up to a specified isomorphism. This is the sense in which we may refer to ‘the’ tensor product of $H$ and $H'$. The generalized ‘the’ may be extended in an obvious recursive fashion to $n$-categories.


[[!redirects the]]
[[!redirects generalised the]]
[[!redirects generalized the]]

[[!redirects unique]]
[[!redirects unique up to]]
[[!redirects unique up to unique isomorphism]]
[[!redirects unique up to unique coherent isomorphism]]
[[!redirects unique up to unique equivalence]]
[[!redirects unique up to unique coherent equivalence]]


# Higher doctrines
* table of contents
{: toc}

## Doctrinal logic

The notion of logical [[theory]] in categorical logic, that is given by a 2-category of categories with additional structures, due to Lawvere and Ehresmann, may be straightforwardly generalized using the metalanguage of higher and homotopical (multi)-categories, in a way that is directly inspired by the Baez--Dolan categorification method.

This setting, combined with a higher Yoneda lemma, is very natural to treat the semantics of mathematical theories in a coordinate free fashion, characterizing a theory by its universal property. This gives unicity statements.

The main problem of the notion of higher doctrine, is to find a proper notion of syntax for the doctrines in play, that allows one to define the notion of _coherent theory_. This problem is already solved for 2-doctrines by Ehresmann's notion of sketches, and may be solved by using higher monads, or other descriptions of higher homotopical categories by [[generators and relations]]. This main problem is presently solved only in particular cases.

When combined with the _axiom of choice_ and the categorification of classical methods of mathematical logic given by [[model theory]] (following Goedel's groundbreaking work), this formalism can be used to prove general existence results, for the models of coherent theories in doctrines with good finiteness properties. An example of this general approach is given by Deligne's theorem about the existence of enough points for a coherent topos.
Remark that if one does not want to ground the categorical metalanguage on set theory, one may also formulate a doctrinal axiom of choice, once defined a precise notion of coherent theory:

+-- {: .un_axiom}
###### Doctrinal axiom of choice
Every coherent theory has at least a model.
=--

Basing mathematics on this ground, one can define the notion of
<strong>well posed mathematical problem</strong>,
generalizing Hadamard's approach to the partial differential systems of mathematical physics: a mathematical problem/theory is well posed if it has a unique solution.

Remark that showing that a mathematical problem is well posed in the above sense may be a bit harder than solving it directly by hand, but both actions are homotopically equivalent, in the sense of doctrinal logic, as you may be able to prove it, with some unworthy efforts.

This modest program of generalizing model theory methods to higher doctrines may be put at the heart of a categorical foundation of mathematics, a la Lawvere, but with a more concrete flavor, since the methods also allow to prove existence results (for objets, theories, and even proofs), under finiteness (coherence) hypothesis.

Remark that this abstract nonsense  may also be pedagogically very helpful to understand on a conceptual way the recent and numerous applications of higher categorical methods in mathematics and physics.

## Definition and challenges

Suppose given a metalanguage of homotopical higher (and even multi-) categories, that we will call simply higher categories.

+-- {: .un_defn}
###### Definition
A __doctrine__ $D$ is an $(n+1)$-category whose objects are $n$-categories equipped with some specified finitary structure.  A theory of type $D$ is an object $T$ of $D$. A model for a theory of type $D$ in another one is a morphism
$$M\colon T_1 \to T_2.$$
=--

The main challenges of higher doctrine theory are the following:

* Define a precise notion of (possibly homotopical) syntax for a given theory
(analog of a site underlying a topos, or of a sketch underlying a theory a la Ehresmann). This is what it meant by the generators and relations data.

* Basing on the above, give a precise definition of coherent theory (finiteness property for the syntax) in a given doctrine.

* Prove that, under the set theoretic axiom of choice and the formalization of higher categories through set theoretical methods (i.e., by one of the standard delooping machines), the doctrinal axiom of choice is true.

## Examples

It may be interesting to show that these methods can be used to study concrete mathematical problems:

1. A good testing example is the following: prove that the problem of proving the representability of the projective space $P^1$ (or grassmanians) is well posed, by showing that it is the unique (by Yoneda) model of a coherent theory (the theory of lines in the affine space of the big Zariski topos on rings) in a well chosen doctrine.

2. Another example is: prove that the fixed point theorem in functional analysis of Banach spaces is the solution of a well posed mathematical problem (or more specifically, that the limit of a cauchy filter in a complete uniform structure, &#224; la Bourbaki, is an existing model of a theory associated to the uniform space, that is coherent by completeness of the uniform structure).

3. Show that compactness arguments in analysis (those saying that one can extract a convergent subsequence from a sequence on a compact topological space) may be formalized by saying that the subsequence is a model of a theory associated to the topological space, that is coherent because of its
compactness.

## References

* See the Section [[doctrine]] for historical background and refined definitions in lower dimension, and

* [[Frédéric Paugam]], *A Categorical Toolbox*, chapter 1 of: *Towards the mathematics of quantum field theory*, Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge / A Series of Modern Surveys in Mathematics, vol 59. Springer, Cham. ([doi:10.1007/978-3-319-04564-1_2](https://doi.org/10.1007/978-3-319-04564-1_2))

[[!redirects higher doctrine]]
[[!redirects higher doctrines]]
[[!redirects Higher doctrine]]
[[!redirects Higher doctrines]]

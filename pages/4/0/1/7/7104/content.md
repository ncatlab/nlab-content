# Higher doctrines
* table of contents
{: toc}

The notion of logical theory in categorical logic, that is given by a 2-category of categories with additional structures, due to Lawvere and Ehresmann, may be straightforwardly generalized using the metalanguage of higher and homotopical (multi)-categories, in a way that is directly inspired by the Baez-Dolan categorification method.

This setting, combined with a higher Yoneda lemma, is very natural to treat the semantics of mathematical theories in a coordinate free fashion, characterizing a theory by its universal property. This gives unicity statements.

The main problem of the notion of higher doctrine, is to find a proper notion of syntax for the doctrines in play, that allows one to define the notion of _coherent theory_. This problem is already solved for 2-doctrines by Ehresmann's notion of sketches, and may be solved by using higher monads, or other descriptions of higher homotopical categories by generators and relations. This main problem is presently solved only in particular cases.

When combined with the _axiom of choice_ and the categorification of classical methods of mathematical logic given by [[model theory]] (following Goedel's groundbreaking work), this formalism can be used to prove general existence results, for the models of coherent theories in doctrines with good finiteness properties. An example of this general approach is given by Deligne's theorem about the existence of enough points for a coherent topos.
Remark that if one does not want to ground the categorical metalanguage on set theory, one may also formulate a doctrinal axiom of choice, once defined a precise notion of coherent theory:

**Doctrinal axiom of choice:** Every coherent theory has at least a model.

Basing mathematics on this ground, one can easily define the notion of **well posed mathematical problem**, generalizing Hadamard's approach to the partial differential systems of mathematical physics: a mathematical problem/theory is well posed if it has a unique solution.

This vast program of generalizing model theory methods to higher doctrines may be put at the heart of a categorical foundation of mathematics, a la Lawvere, but with a more concrete flavor, since the methods also allow to prove existence results (for objets, theories, and even proofs), under finiteness (coherence) hypothesis.

Remark that this abstract nonsense  may also be pedagogically very useful to understand on a conceptual way the recent and numerous applications of higher categorical methods in mathematics and physics.

Suppose given a metalanguage of homotopical higher (and even multi-) categories, that we will call simply higher categories.

**Definition:** A _doctrine_ $D$ is a higher category. A theory of type $D$ is an object $T$ of $D$. A model for a theory of type $D$ in another one is a morphism
$$M:T_1\to T_2.$$

The main challenges of higher doctrine theory are:
* Define a precise notion of syntax for a given theory (analog of a site underlying a topos, or of a sketch underlying a theory a la Ehresmann).
* basing on the above, give a precise definition of coherent theory (finiteness property) in a given doctrine.
* Prove that, under the set theoretic axiom of choice and the formalization of higher categories through set theoretical methods, the doctrinal axiom of choice is true.
* Show that these methods can be used to study concrete mathematical problems:
1. A good testing example is the following: prove that the problem of proving the representability of the projective space $P^1$ (or grassmanians) is well posed, by showing that it is the unique model of a theory (the theory of lines in the Zariski topology on rings) in a well chosen doctrine.
2. Another example is: prove that the fixed point theorem in functional analysis of Banach spaces  is the solution of a well posed mathematical problem (or more specifically, that the notion of complete uniform structure, &#224; la Bourbaki, can be formalized as the notion of coherence of a well whosen theory).
3. Show that compactness arguments in analysis (those saying that one can extract a subsequence from a sequence on a compact topological space) can be formalized by saying that the subsequence is a model of a coherent theory associated to the compact topological space.

***References***

* See the Section [[doctrine]] for historical background and refined definitions in lower dimension, and

* [[Frédéric Paugam]]: Chapter 1 of
[Towards the mathematics of quantum field theory](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf).
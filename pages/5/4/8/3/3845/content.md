
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Given an ordinary [[category]] $C$, a pasting diagram in $C$ is a sequence of composable morphisms in $C$

$$
  a_1 \stackrel{f_1}{\to} a_2 \stackrel{f_2}{\to}
  \cdots
  \stackrel{f_n}{\to} a_{n+1}
  \,.
$$

We think of these arrows as not yet composed, but _pasted_ together at their objects, such as to form a composable sequence, and then say the _value_ of the sequence is the composite morphism in $C$. Or, we could say that a pasting diagram is a specified decomposition of whatever morphism $f$ it evaluates to, thus breaking down $f$ into morphisms $f_i$ which, in practice, are usually "more basic" than $f$ relative to some type of structure on $C$. For example, if $C$ is a [[monoidal category]], the $f_i$ might be instances of associativity isomorphisms. 

Pasting decompositions become more elaborate in higher categories. An example of a pasting diagram in a (let's say strict) 2-category is a pasting of two squares 

$$
  \array{
    a &\to& b &\to& c
    \\
    \downarrow &\swArrow& \downarrow &\swArrow& \downarrow
    \\
    d &\to& e &\to& f
  }
  \,.
$$

To evaluate this diagram as a single 2-morphism, we read this diagram explicitly as the vertical composite of the 2-morphism

$$
  \array{
    a &\to& b &\to& c
    \\
    && \downarrow &\swArrow& \downarrow
    \\
     && e &\to& f
  }
$$

with the 2-morphism

$$
  \array{
    a &\to& b && 
    \\
    \downarrow &\swArrow& \downarrow && 
    \\
    d &\to& e &\to& f
  }
  \,.
$$

(Notice that the two halves of the boundary of each of these two 2-morphisms are themselves 1-dimensional pasting diagrams.) Similarly, there can be situations where one pastes together other shapes (triangles, pentagons, etc.), and there may be multiple paths on the way to resolving the diagram into a single 2-morphism, but the idea is that all such paths evaluate to the same 2-morphism, at least in a strict 2-category. General theorems which refer to the uniqueness of pastings are called _pasting theorems_. 

On the other hand, the following diagram is _not_ a pasting diagram: 

$$
  \array{
    a &\to& b &\to& c
    \\
    \downarrow &\neArrow& \downarrow &\swArrow& \downarrow
    \\
    d &\to& e &\to& f
  }
  \,.
$$

Thus, formal definitions of pasting diagram include conditions which impose a consistent "directionality" of the cells so they can be pasted together.

In an [[n-category]] a pasting diagram is similarly a collection of [[k-morphism|n-morphisms]] with a prescribed way how they are to fit together at their boundaries. There are a number of ways of formalizing pasting diagrams, depending partly on the constituent shapes one allows, and also on the technical hypotheses that allow proofs of pasting theorems, which include directionality conditions but usually also "loop-freeness" conditions to ensure there exists a unique way to resolve or evaluate the diagram. (N.B.: usually a completely unambiguous evaluation is only possible in a strict $n$-category; in a weak $n$-category, one allows uniqueness up to a "contractible space of choices".) 

Despite some technical differences among the formalizations, the core idea throughout is that the overall geometric shapes of pasting diagrams should be (contractible) $n$-dimensional polyhedra, broken down into smaller polyhedral cells which come equipped with directionality or orientations, that can be sensibly pasted together as in the above descriptions once the cells have been assigned values in an $n$-category. 

## Notions of pasting diagrams 

Various formalisms for pasting diagrams have been proposed. They include 

* [[pasting scheme|pasting schemes]] (Johnson) 

* [[parity complex|parity complexes]] (Street) 

* [[directed complex|directed complexes]] (Steiner) 

* [[generalized parity complex|generalized parity complexes]] (Forest)

* [[regular directed complex|regular directed complexes]] (Hadzihasanovic)

Each of these formalisms involve graded sets $\{C_n\}_{n \geq 0}$ together with maps $\partial^+_n: C_{n+1} \to P(C_n)$, $\partial^-_n: C_{n+1} \to P(C_n)$. This goes under various names; here we call it a **parity structure**. It should be thought of as assigning to each "cell" of dimension $n+1$ a collection of positive boundary cells and negative boundary cells in dimension $n$. The formalisms above are distinguished by the choice of axioms on parity structures, but there is definite kinship among them. 

Also related are various notions of categories of shapes, including 

* [[test category]] 

* [[direct category]] 

* [[compositions in cubical sets]]

## Examples

* [[Toda bracket]]

## Related concepts

* [[pasting law]] for [[pullbacks]]/[[homotopy pullbacks]]

## References

The notion of pasting in a [[2-category]] was introduced in

* [[Jean Benabou]], _Introduction to bicategories_, Reports of the Midwest Category Seminar, Lecture Notes in Mathematics, **47**, 1967. ([doi:10.1007/BFb0074299](https://doi.org/10.1007/BFb0074299))

A reasonably self-contained, formal, and illustrated seven-page introduction to pasting diagrams in the context of weak 2-categories, and their relation to [[string diagrams]] is given in Section A.4 of: 

* [[Chris Schommer-Pries]], _The Classification of Two-Dimensional Extended Topological Field Theories_, 2011. ([arXiv:1112.1000v2](https://arxiv.org/abs/1112.1000v2))

A survey discussion of pasting in [[2-categories]] is in 

* [[John Power]], _2-Categories_ ([pdf](http://www.brics.dk/NS/98/7/BRICS-NS-98-7.pdf))

from definition 2.10 on. Details are in

* [[John Power]], _A 2-categorical pasting theorem_ , Journal of Algebra, **129**, 1990. &lbrack;<a href="https://doi.org/10.1016/0021-8693(90)90229-H">doi:10.1016/0021-8693(90)90229-H</a>&rbrack;

Dominic Verity gave a bicategorical pasting theorem in 

* [[Dominic Verity]], _Enriched categories, internal categories, and change of base_, PhD thesis, Cambridge University, 1992. Reprinted in TAC ([link](http://www.tac.mta.ca/tac/reprints/articles/20/tr20abs.html)). 

A definition and discussion of pasting diagrams in [[strict omega-categories]] is in

* [[Sjoerd Crans]], _Pasting presentation for Omega-categories_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.4342))

* [[Sjoerd Crans]], _Pasting schemes for the monoidal biclosed structure on $\omega$-$\mathbf{Cat}$_ ([web](http://home.tiscali.nl/secrans/papers/thten.html), [ps](http://home.tiscali.nl/secrans/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

The notion of pasting scheme used by Crans was introduced by Johnson, 

* [[Michael Johnson]], _The combinatorics of n-categorical pasting_, Journal of Pure and Applied Algebra, **62**, 1989. &lbrack;<a href="https://doi.org/10.1016/0022-4049(89)90136-9">doi:10.1016/0022-4049(89)90136-9</a>&rbrack;

Other notions of pasting presentations have been given by Street and by Steiner: 

* [[Ross Street]], _Parity complexes_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, **32**, 1991. ([link](http://www.numdam.org/item/?id=CTGDC_1991__32_4_315_0)) 

* [[Ross Street]], _Parity complexes : corrigenda_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, **35**, 1994. ([link](http://www.numdam.org/item/?id=CTGDC_1994__35_4_359_0))

* [[Richard Steiner]], _The algebra of directed complexes_, Applied Categorical Structures, **1**, 1993. ([doi:0.1007/BF00873990](https://doi.org/10.1007/BF00873990))

These notions were compared, and a new generalized one introduced, in

* [[Simon Forest]], _Unifying notions of pasting diagrams_, Higher Structures, **6**, 2022 ([arxiv:1903.00282](https://arxiv.org/abs/1903.00282), [doi:10.21136/HS.2022.01](https://doi.org/10.21136/HS.2022.01))

Another recent approach is: 

* [[Amar Hadzihasanovic]], _Combinatorics of higher-categorical diagrams_, 2024 ([link](https://arxiv.org/abs/2404.07273))

For an online link to the notion of directed complex, see 

* [[Sjoerd Crans]] and [[Richard Steiner]], _Presentations of omega-categories by directed complexes_, Journal of the Australian Mathematical Society, **63**, 1997. ([doi:10.1017/S1446788700000318](https://doi.org/10.1017/S1446788700000318))

There is also

* [[Michael Makkai]], _Computads and 2 dimensional pasting diagrams_ ([pdf](http://www.math.mcgill.ca/makkai/2dcomputads/2DCOINS1.pdf))

For a cubical approach to multiple compositions and other references see the paper 

* [[Philip J. Higgins]], _Thin elements and commutative shells in cubical omega-categories_, Theory and Applications of Categories, **14**, 2005. ([link](http://www.tac.mta.ca/tac/volumes/14/4/14-04abs.html))

A formal approach to [[pasting diagrams]] in [[Gray categories]]:

* {#DiVittorio2023} [[Nicola Di Vittorio]], _A Gray-categorical pasting theorem_, Theory and Applications of Categories **39** 5 (2023) 150-171 &lbrack;[tac:39-05](http://www.tac.mta.ca/tac/volumes/39/5/39-05abs.html)&rbrack;

[[!redirects pasting diagrams]]
[[!redirects pasting]]
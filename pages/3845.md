
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

Each of these formalisms involve graded sets $\{C_n\}_{n \geq 0}$ together with maps $\partial^+_n: C_{n+1} \to P(C_n)$, $\partial^-_n: C_{n+1} \to P(C_n)$. This goes under various names; here we call it a **parity structure**. It should be thought of as assigning to each "cell" of dimension $n+1$ a collection of positive boundary cells and negative boundary cells in dimension $n$. The formalisms above are distinguished by the choice of axioms on parity structures, but there is definite kinship among them. 

Also related are various notions of categories of shapes, including 

* [[test category]] 

* [[direct category]] 

* [[compositions in cubical sets]]

## Related concepts

* [[pasting law]] for [[pullbacks]]/[[homotopy pullbacks]]

## References

The notion of pasting in a [[2-category]] was introduced in

* [[Jean Benabou]], _Introduction to bicategories_ , in _Lecture Notes in Mathematics_ Vol. 47, pp. l-77, Springer-Verlag, New York/Berlin, (1967)

A reasonably self-contained, formal, and illustrated seven-page introduction to pasting diagrams in the context of weak 2-categories, and their relation to [[string diagrams]] is given by [[Chris Schommer-Pries]] in Section A.4 of "The Classification of Two-Dimensional Extended Topological Field Theories", arXiv:1112.1000v2.

A survey discussion of pasting in [[2-categories]] is in 

* [[John Power]], _2-Categories_ ([pdf](http://www.brics.dk/NS/98/7/BRICS-NS-98-7.pdf))

from definition 2.10 on. Details are in

* [[John Power]], _A 2-categorical pasting theorem_ , Journal of Algebra
Volume 129, Issue 2, March 1990, Pages 439-445 

Dominic Verity gave a bicategorical pasting theorem in 

* [[Dominic Verity]], Enriched categories, internal categories, and change of base, PhD thesis, Cambridge University, 1992. Reprinted in TAC ([link](http://www.tac.mta.ca/tac/reprints/articles/20/tr20abs.html)). 

A definition and discussion of pasting diagrams in [[strict omega-categories]] is in

* [[Sjoerd Crans]], _Pasting presentation for Omega-categories_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.4342))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-$\mathbf{Cat}$_ ([web](http://home.tiscali.nl/secrans/papers/thten.html), [ps](http://home.tiscali.nl/secrans/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

The notion of pasting scheme used by Crans was introduced by Johnson, 

* [[Michael Johnson]], The combinatorics of categorical pasting, J. Pure Appl. Alg. 62 (1989), 211-225. 

Other notions of pasting presentations have been given by Street and by Steiner, 

* Street, Parity complexes, Cahiers Top. G&#233;om Diff. Cat&#233;goriques 32 (1991), 315-343. ([link](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1991__32_4/CTGDC_1991__32_4_315_0/CTGDC_1991__32_4_315_0.pdf)) Corrigenda, Cahiers Top. G&#233;om Diff. Cat&#233;goriques 35 (1994), 359-361. ([link](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1994__35_4/CTGDC_1994__35_4_359_0/CTGDC_1994__35_4_359_0.pdf))

* Richard Steiner, The algebra of directed complexes, Appl. Cat. Struct. 1 (1993), 247-284. 

These notions were compared, and a new generalized one introduced, in

* Simon Forest, _Unifying notions of pasting diagrams_, [arxiv:1903.00282](https://arxiv.org/abs/1903.00282)

For an online link to the notion of directed complex, see 

* [[Sjoerd Crans]] and Richard Steiner, Presentations of omega-categories by directed complexes, Journal of the Australian Mathematical Society (Series A), (1997), 63 : pp 47-77. ([link](http://journals.cambridge.org/download.php?file=%2FJAZ%2FJAZ1_63_01%2FS1446788700000318a.pdf&code=d96423d28d8595ef0e528452fc6608c7))

There is also

* [[Michael Makkai]], _Computads and 2 dimensional pasting diagrams_ ([pdf](http://www.math.mcgill.ca/makkai/2dcomputads/2DCOINS1.pdf))

For a cubical approach to multiple compositions and other references see the paper 

*  Philip J. Higgins, Thin elements and commutative shells in cubical omega-categories, Theory and Applications of Categories, Vol. 14, 2005, No. 4, pp 60-74. ([link](http://www.tac.mta.ca/tac/volumes/14/4/14-04abs.html))

[[!redirects pasting diagrams]]
[[!redirects pasting]]
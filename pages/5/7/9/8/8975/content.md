#Contents#
* table of contents
{:toc}

## Idea

In the theory of [[programming languages]], the idea that procedures may be modelled as mathematical [[functions]] is useful for compositional reasoning, but at first seems to rule out programming with more sophisticated control structures which can actually be very useful in practice.  For example, we might want to write an integer division routine which raises an exception on division-by-zero, or a procedure that lazily computes the first satisfying assignment to a boolean formula while giving the user the ability to query to obtain additional ones.

Now, an "impure" functional language such as OCaml lets us do some of this directly.  For example, we can write the following code for integer division:

    let divide : int -> int -> int =
      fun x y -> if y == 0 then raise Division_by_zero else x / y

However, it should be said that the type ascription "<code>int -> int -> int</code>" is a bit misleading here (or at least open to misinterpretation), since <code>divide</code> cannot actually be modelled as a set-theoretic function of type $\mathbb{Z} \to \mathbb{Z} \to \mathbb{Z}$.

_Continuation-passing style_ (or CPS) is a very general technique that allows one to express many different seemingly "non-functional" patterns of control flow within the confines of pure functional programming.  The basic idea is that a procedure in CPS takes an additional argument (often named "$k$") representing the _continuation_, a functional abstraction of the context in which the procedure is used (or "the rest of the computation").  Whenever a procedure in "direct style" would return a value ($v$), the corresponding procedure in CPS instead invokes the continuation with that value ($k(v)$).  However, it is the fact that the procedure has explicit access to the continuation which also allows for the possibility of exceptional behaviors, typically by throwing away the continuation or by invoking it more than once.

To transform the example above into continuation-passing style, first we must fix an "answer type", that is, the return type of the continuation. In this case, to allow for the possibility of raising a division-by-zero error, the answer type should be a [[pointed type]].  For example, we could take

    type ans = int option

Now, our division routine can be written as follows in CPS:

    let divide_cps : int -> int -> (int -> ans) -> ans =
      fun x y k -> if y == 0 then None else k (x / y)

Observe that we have replaced the (somewhat misleading) original type

    divide : int -> int -> int

by the more complicated type

    divide_cps : int -> int -> (int -> ans) -> ans

This may be recognized as a form of [[double negation translation]], and indeed under [[propositions as types]], the classical negative translations correspond to different forms of continuation-passing style transformations.  Under this correspondence, the "answer type" corresponds to the type of [[false|absurdity]] $\bot$, but as the above example shows, we almost never want the answer type to be [[empty type|empty]].  As such, CPS translation is best understood in terms of the negative translations from [[classical logic]] into [[minimal logic]], where the type of falsehood $\bot$ behaves like a fixed atomic proposition.

## Continuation semantics

Whereas "continuation-passing style" refers to a programming technique, the term "continuation semantics" refers to a certain way of assigning [[denotational semantics]] to programs, originally in the context of [[domain theory]] [(Strachey & Wadsworth 1974)](#StracheyWadsworth74).  The two are very closely related, though, especially if one views the meaning function &#10214;-&#10215; in a denotational semantics as a "definitional interpreter" in the sense of [(Reynolds 1972)](#Reynolds72).  In that case, giving a continuation semantics for a language corresponds to writing the definitional interpreter in continuation-passing style.


## Related concepts

* [[continuation monad]]

* [[programming language]]

* [[functional programming]]

* [[Yoneda lemma]]

* [[negative translation]]

* [double-negated principle of excluded middle](excluded+middle#DoubleNegatedPEM)

* [[monad (in computer science)]]

## References

Some early and historical references for continuations and continuation-passing style include:

* {#Reynolds72} [[John C. Reynolds]]. Definitional interpreters for higher-order programming languages. In _Proceedings of the ACM National Conference_, 1972. ([pdf](http://surface.syr.edu/cgi/viewcontent.cgi?article=1012&context=lcsmith_other))

* {#StracheyWadsworth74} Christopher Strachey and C. P. Wadsworth. Continuations: A Mathematical Semantics for Handling Full Jumps, Technical Monograph PRG-11, Oxford, 1974. ([pdf](http://repository.readscheme.org/ftp/papers/plsemantics/oxford/strachey-continuations.PDF))

* {#Reynolds74} [[John C. Reynolds]]. On the Relation Between Direct and Continuation Semantics.  Second Colloquium on Automata, Languages, and Programming, Saarbrucken, July 29 - August 2, 1974. ([pdf](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2287&context=compsci))

* {#Plotkin75} [[Gordon Plotkin]]. Call-by-name, call-by-value, and the lambda-calculus. _Theoretical Computer Science_ 1 (1975), 125-159. ([pdf](http://homepages.inf.ed.ac.uk/gdp/publications/cbn_cbv_lambda.pdf))

* [[John C. Reynolds]]. The Discoveries of Continuations. _LISP and Symbolic Computation_ 6 (1993), 233-247. ([pdf](http://www.math.bas.bg/bantchev/place/iswim/conti-disco.pdf))

Other references include:

* [[Hayo Thielecke]]. _Categorical Structure of Continuation Passing Style_. PhD thesis, University of Edinburgh, 1997. ([pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-376/ECS-LFCS-97-376.pdf)) 

* [[Josh Berdine]], [[Peter O'Hearn]], [[Uday Reddy]], [[Hayo Thielecke]]. Linear Continuation-Passing. _Higher-Order and Symbolic Computation_ 15 (2002), 181-208. ([pdf](http://research.microsoft.com/pubs/64171/LinCP.pdf))

* [[Ulrich Schöpp]]. On the Relation of Interaction Semantics to Continuations and Defunctionalization. _Logical Methods in Computer Science_ Vol.10(4:10)2014, 1-41. ([pdf](http://arxiv.org/pdf/1410.4980.pdf))

* Wikipedia, _[Continuation-passing style](http://en.wikipedia.org/wiki/Continuation-passing_style)_

For the connection between CPS and the [[Yoneda lemma]], see 

* Ralf Hinze, Daniel W. H. James, _Reason Isomorphically!_, secions 3-4, [pdf](http://www.cs.ox.ac.uk/ralf.hinze/publications/WGP10.pdf)

* Mike Stay, _The Continuation Passing Transform and the Yoneda Embedding_, [blog post](https://golem.ph.utexas.edu/category/2008/01/the_continuation_passing_trans.html)

[[!redirects continuation passing style]]

[[!redirects continuation-passing]]
[[!redirects continuation passing]]

#Contents#
* table of contents
{:toc}

## Idea

The **de re/ de dicto** distinction has different meanings, as explained in ([SEP](#SEP)), but it typically concerns the two readings that are possible in sentences where a [[modal operator]] or propositional attitude verb is applied to a claim about some subject. For example, consider

* I believe that the person downstairs is my mother

The usual _de dicto_ reading would express my strong hunch about the person who is downstairs that she is my mother. The _de re_ reading would take the expression 'the person downstairs' to designate the person who is actually there, for example, it may in fact be my father. This would entail that I am crazy enough to believe my father to be my mother.

Similarly in the case of [[modal logic]], we could consider a statement such as

+ Someone is necessarily the monarch of this country

_De dicto_ this means that it has to be the case at this time that there be a monarch (as soon as one monarch dies, their successor becomes monarch). On the other hand, _de re_ this means that some specific individual has to be monarch. This reading leads to a false claim since that person might in fact not have been monarch. They might, say, have abdicated earlier or have been killed by their uncle when a child.

## Formalization in modal logic

In [[modal logic]] a [[proposition]] involving the consecutive application of a [[modal operator]] and an [[existential quantifier]] is called 

* _de dicto_ if the modal operator is applied after the quantifier

  $\Box \underset{x \colon X}{\exists} A(x)$;

* _de re_ if it is the other way around

  $\underset{x \colon X}{\exists} \Box A(x)$;

Hence a difference between de dicto and de re statements is related to the failure of a [[modal operator]] to commute with [[base change]].

However, according to the treatment at [necessity and possibility](necessity+and+possibility#InFirstOrderLogicAndTypeTheory), these modalities operate on world dependent types:

$$
  (\underset{W}{\lozenge} \dashv \underset{W}{\Box})
  \coloneqq
  \left(
     \left(
     W^\ast \circ \underset{w\colon W}{\exists}
     \right)
     \dashv
     \left(
     W^\ast \circ \underset{w\colon W}{\forall}
     \right)
  \right)
  \;\colon\;
  \mathbf{H}_{/W}
    \longrightarrow
  \mathbf{H}_{/W}
  \,.
$$

Then, _de dicto_, I could mean by  $\Box \underset{x \colon X}{\exists} A(x)$ that we have a world-dependent type $X(w)$, and then put $\Box_W \underset{x \colon X(w)}{\exists} A(w, x)$. But this $A$ is a dependent type $w: W, x:X(w) \vdash A(w, x):Prop$.

However, _de re_, I need to have world-independent $X$, to allow the modal operator $\Box_W: \mathbf{H}/(X \times W) \to \mathbf{H}/(X \times W)$ and then $\underset{x \colon X}{\exists}: \mathbf{H}/(X \times W) \to \mathbf{H}/W$.

## Related concepts

* [[Barcan formula]]

## References

* {#SEP} Stanford Encyclopedia of Philosophy, _[The De Re/De Dicto Distinction](http://plato.stanford.edu/entries/prop-attitude-reports/dere.html)_

* Wikipedia, _[De dicto and de re](https://en.wikipedia.org/wiki/De_dicto_and_de_re)_


Detailed discussion of compatibility of [[modal operators]] with [[base change]] in a [[hyperdoctrine]] is in

* {#MakkaiReyes95} [[Michael Makkai]], [[Gonzalo Reyes]], section 4 of _Completeness results for intuitionistic and modal logic in a categorical setting_, Annals of Pure and Applied Logic 72 (1995) 25-101

Related comments are in 

* {#Law91a} [[William Lawvere]], _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in A. Carboni, M. Pedicchio, G. Rosolini, _Category theory_ , [[Como|Proceedings of the International Conference held in Como 1990]], 213&#8211;236, Lecture Notes in Math. __1488__, Springer (1991)

For an attempt to represent the kinds of _opaque_ contexts considered here using the [[reader monad]], see

* Gianluca Giorgolo, Ash Asudeh, _Monads as a Solution for Generalized Opacity_, Proceedings of the EACL 2014 Workshop on Type Theory and Natural Language Semantics (TTNLS), pp. 19-27. ([pdf](http://users.ox.ac.uk/~cpgl0036/pdf/giorgolo-asudeh-eacl2014.pdf))

[[!redirects de dicto and de re]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A Moufang loop is a set with a [[binary operation]] that is similar to that of a [[group]], but does not require [[associativity]]. Making this precise is a little fiddly.

## Definition

A **Moufang loop** is a set $Q$ with a binary operation $\cdot\colon Q\times Q \to Q$ (a [[magma]]) with two-sided unit $e$ such that left and right multiplication, $y\cdot -\colon Q \to Q$ and $-\cdot x\colon Q \to Q$ respectively, are [[isomorphisms]] (i.e. it is a unital [[quasigroup]] or _[[loop (algebra)|loop]]_) and such that the _Moufang identities_ hold:

* $(u v)(w u) = (u(v w))u = u((v w)u)$ 

* $((u v)u)w = u(v(u w))$

* $((u v)w)v = u(v(w v))$

One may consider the weaker analogous structure without unit $e$, the Moufang quasigroup, but the Moufang identities, by a result of [[Kenneth Kunen]] imply that the quasigroup is a loop.

## Properties

Every element in a Moufang loop has a multiplicative inverse; a priori there are only left and right inverses, but these coincide by the Moufang identities.

Since right and left multiplication give isomorphisms of the underlying set, one can 'divide' by any element of the Moufang loop, on the right or on the left (recall we are not assuming commutativity). Thus one can define a Moufang loop as a set together with a multiplication as above, together with right and left division operations $/, \backslash \colon Q\times Q \to Q$, again satisfying the Moufang identities. Thus Moufang loops are algebras for a [[Lawvere theory]], and thus can be defined [[internalization|internal]] to any category with [[finite products]].

Moufang loops are _[[power-associative algebra|power-associative]]_, in that any bracketing of a string consisting of copies of the same element multiply to a unique element. In fact, more is true, in that any two elements generate a genuine group; that is, Moufang loops are _[[alternative algebra|alternative]]_.


## Examples

* Any group is a Moufang loop.

* The non-zero [[octonions]] form a Moufang loop, as does the multiplicatively closed subset of octonions of norm 1 (which form the [[7-sphere]]). The invertible elements in any alternative ring or [[alternative algebra]] form a Moufang loop. 

* The basis octonions, $1,e_1,\ldots,e_7$ and their additive inverses $-1,-e_1,\ldots,-e_7$ form a finite Moufang loop of order 16 (compare with the case of the quaternions, where the basis elements and their inverses form a group of order 8, the [[quaternion group]] $Q_8$).

* There is a finite Moufang loop of order $2^{13}$ which [[John Conway]] used to construct the [[Monster group]]. This Moufang loop is a central extension by $\mathbb{Z}/2$ of the [[binary Golay code]], an abelian group of order $2^{12}$, see ([Hsu](#Hsu)). This is a special case of a [[code loop]], which is a specific sort of Moufang loop.

## References

Related concepts in $n$Lab: [[quasigroup]], [[Bol loop]], [[composition algebra]], [[identities of Bol-Moufang type]]

* Wikipedia: [Moufang loop](http://en.wikipedia.org/wiki/Moufang_loop)

* [[eom]]: [Moufang loop](http://www.encyclopediaofmath.org/index.php?title=M/m065050)

* R. Moufang, _Zur Struktur von Alternativk&#246;rpern_, Math. Ann. __110__ (1935) 416&#8211;430 ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002277301))

* Tim Hsu, _Explicit constructions of code loops as centrally twisted products_, Math. Proc. Cambridge Philos. Soc. __128__ (2000), no. 2, 223&#8211;232 ([journal](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=37707&fulltextType=RA&fileId=S030500419900403X) or [preprint](http://www.math.sjsu.edu/~hsu/pdf/tp.pdf))
{#Hsu}

* [[Kenneth Kunen]], _Moufang quasigroups_, J. Algebra __183__:1 (1996) 231&#8211;234 [doi](http://dx.doi.org/10.1006/jabr.1996.0216)
* E. N. Kuz'min, , Algebra i Logika __10__ (1) (1971), pp. 3&#8211;22, in Russian [pdf](), English translation: _On a relation between Malcev algebras and analytic Moufang loops_, Algebra Logic __10__ (1972), pp. 1&#8211;14

[[!redirects Moufang loops]]
[[!redirects Moufang quasigroup]]
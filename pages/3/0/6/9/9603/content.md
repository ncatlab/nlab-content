
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

A [[loop (algebra)|loop]] is a set with a [[binary operation]] that is similar to that of a [[group]], but does not require [[associativity]].  A *Moufang loop* $Q$ is one for which so-called monotopies act transitively, where a **monotopy** is a bijection $\gamma : Q \to Q$ such that there exist bijections $\alpha, \beta \colon Q \to Q$ such that

$$ u v = w \quad \implies \quad \alpha(u) \beta(v) = \gamma(w) .$$

This conceptual definition was given by [Conway & Smith 2003](#ConwaySmith2003), who prove that it is equivalent to a more commonly used definition in terms of two equational laws called the _Moufang identities_.

## Definition

A **loop** is a set $Q$ with a binary operation $\cdot\colon Q\times Q \to Q$ (a [[magma]]) with two-sided unit $e$ such that left and right multiplication, $y\cdot -\colon Q \to Q$ and $-\cdot x\colon Q \to Q$ respectively, are [[bijections]] (i.e. it is a unital [[quasigroup]]).   A **Moufang loop** is a loop such that the **Moufang identities** hold:

* $(u v)(w u) = (u(v w))u = u((v w)u)$ 

These identities imply others, including

* $((u v)u)w = u(v(u w))$

* $((u v)w)v = u(v(w v))$

the so-called **alternative** laws

* $(u u) v = u (u v) $

* $(u v) v = (u v) v$

and the **flexible** law

* $(u v) u = u (v u) $

As emphasized by [Conway & Smith 2003](#ConwaySmith2003), in a Moufang loop every element has a left and right inverse and these agree.  Furthermore we have these identities

* $u (v w) = (u v u)(u^{-1} w) $

* $(v w) u = (v u^{-1}) (u w u) $

which say how to left or right multiply a product by an element $u$.  (The products $u v u$ and $u w u$ are unambiguous thanks to the alternative law.)

One may consider the weaker analogous structure without unit $e$, the Moufang quasigroup, but the Moufang identities, by a result of [Kunen 1996](#Kunen1996) imply that the quasigroup is a loop.

## Properties

Every element in a Moufang loop has a multiplicative inverse; a priori there are only left and right inverses, but these coincide by the Moufang identities.

Since right and left multiplication give isomorphisms of the underlying set, one can 'divide' by any element of the Moufang loop, on the right or on the left (recall we are not assuming commutativity). Thus one can define a Moufang loop as a set together with a multiplication as above, together with right and left division operations $/, \backslash \colon Q\times Q \to Q$, again satisfying the Moufang identities. Thus Moufang loops are algebras for a [[Lawvere theory]], and thus can be defined [[internalization|internal]] to any category with [[finite products]].

Moufang loops are _[[power-associative algebra|power-associative]]_, in that any bracketing of a string consisting of copies of the same element multiply to a unique element. In fact, more is true, in that any two elements generate a genuine group; that is, Moufang loops are _[[alternative algebra|alternative]]_.


## Examples

* Any group is a Moufang loop.

* The non-zero [[octonions]] form a Moufang loop, as does the multiplicatively closed subset of octonions of norm 1 (which form the [[7-sphere]]). The invertible elements in any alternative ring or [[alternative algebra]] form a Moufang loop. 

* The basis octonions, $1,e_1,\ldots,e_7$ and their additive inverses $-1,-e_1,\ldots,-e_7$ form a finite Moufang loop of order 16 (compare with the case of the quaternions, where the basis elements and their inverses form a group of order 8, the [[quaternion group]] $Q_8$).

* There is a finite Moufang loop of order $2^{13}$ which [[John Conway]] used to construct the [[Monster group]]. This Moufang loop is a central extension by $\mathbb{Z}/2$ of the [[binary Golay code]], an abelian group of order $2^{12}$, see ([Hsu](#Hsu)). This is a special case of a [[code loop]], which is a specific sort of Moufang loop.

## Related concepts

* [[quasigroup]]

* [[code loop]]

* [[Bol loop]]

* [[identities of Bol-Moufang type]]

* [[composition algebra]]



## References

The original article:

* {#Moufang1935} [[Ruth Moufang]]: *Zur Struktur von Alternativkörpern*, Math. Ann. **110** (1935) 416430 &lbrack;[doi:10.1007/BF01448037](https://doi.org/10.1007/BF01448037), [eudml:159732](https://eudml.org/doc/159732), [gdz:GDZPPN002277301](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002277301)&rbrack;

Early further discussion:

* {#Kunen1996} [[Kenneth Kunen]]: _Moufang quasigroups_, J. Algebra __183__ 1 (1996) 231-234 &lbrack;[doi:10.1006/jabr.1996.0216](http://dx.doi.org/10.1006/jabr.1996.0216)&rbrack;

Monographs:

* {#ConwaySmith2003} [[John Conway]], [[Derek Smith]], *Moufang Loops*, chapter 7 in: _On Quaternions and Octonions: Their Geometry, Arithmetic and Symmetry_, A K Peters/CRC Press (2003) &lbrack;[ISBN:9781568811345](https://www.routledge.com/On-Quaternions-and-Octonions/Conway-Smith/p/book/9781568811345), [doi:10.1201/9781439864180](https://doi.org/10.1201/9781439864180)&rbrack;

See also:

* Wikipedia: *[Moufang loop](http://en.wikipedia.org/wiki/Moufang_loop)(

* [[eom]]: *[Moufang loop](http://www.encyclopediaofmath.org/index.php?title=M/m065050)*


Further discussion:

* E. N. Kuz'min, Algebra i Logika __10__ (1) (1971) 3-22  English translation: _On a relation between Malcev algebras and analytic Moufang loops_, Algebra Logic __10__ (1972) 1-14

* {#Hsu} Tim Hsu, _Explicit constructions of code loops as centrally twisted products_, Math. Proc. Cambridge Philos. Soc. __128__ 2 (2000) 223-232 &lbrack;[doi:10.1017/S030500419900403X](https://doi.org/10.1017/S030500419900403X)&rbrack;


[[!redirects Moufang loops]]
[[!redirects Moufang quasigroup]]
This is a sub-entry of 

* [[gerbe]] .

#Idea#

Recall that [[principal bundle]]s are classified by [[nonabelian cohomology]] in degree 1 with coefficients in a [[group]] $G$.

A central motivation for the introduction of the notion of [[gerbe]] was to find an analog of this statement for [[nonabelian cohomology]] in degree 2.

The basic theorem of Giraud's theory of [[gerbe]]s says that in the sense of [[gerbe (as a stack)]], gerbes $G$-gerbes are classified by [[nonabelian cohomology]] (usually realized as nonabelian [[Čech cohomology]], see there for more details) with coefficients in the [[strict 2-group]] $AUT(G) = Aut_{Grpd}(\mathbf{B}G)$.

#References#

For instance in 

* Breen _Notes on 1- and 2-gerbes_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0611/0611317v2.pdf)) 

this is section 5 _cocycles and coboundaries for gerbes_ .

The cocycle description itself is equation (5.1.10), the classification theorem is mentioned and referenced on the bottom of page 14.

Or 

* Ieke Moerdijk _Introduction to the language of gerbes and stacks_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0212/0212266v1.pdf)) 

discusses the &#268;ech-cocycle description of gerbes from page 16 on, and the classification theorem appears as theorem 3.1 on p. 21.

The statement is originally due to Giraud's work 

* Giraud, _Cohomologie non-ab&#233;lienne

In 

* Brylinski _Loop spaces, characteristic classes and geometric quantization_

the cocycle description of gerbes is extracted in chapter 5.2 _Sheaves of groupoids and gerbes_ and the classification theorem is theorem 5.2.8 on p. 200, 201.

The discussion of cocycles for gerbes is traditionally complicated by the fact that general sheaves of groups are used, instead of just a group, then there is the discussion of band, etc., all of which somewhat contributes to tending to hide a simple idea behind non-essential technical details. 

Another thing that gerby tradition has is to express in linear formulas or rectangular diagrams what is intrinsically a nice geometric higher dimensional structure. The funny-looking nonabelian cocycle for a gerbe is really just a tetrahedron (the 3-simplex, since we are talking about a 2-cocycle) in $\mathbf{B} AUT(G)$.

This may be helpful, since it makes at once clear a lot of structure, such as for instance the nature of coboundaries. One can find these tetrahedra drawn in joint work [[John Baez]] and [[Urs Schreiber]], for instance the gerbe 2-cocycle tetrahedron is the title piece of 

* [[John Baez]], _Namboodiri lecture slides: Higher Categories, Higher Gauge Theory, III ([pdf](http://math.ucr.edu/home/baez/namboodiri/nam3.pdf))

This recalls the theorem in question on slide 10.

Finally, gerbes, in as far as they are nonabelian, are really objects associated to [[principal 2-bundle]]s. The cocycle description of principal 2-bundles is more transparent, conceptually,  as it is the 2-bundle that is associated by abstract nonsense to the 2-cocycle, whereas the gerbe comes from that only after some fiddling (see [[gerbe (general idea)]]).

Accordingly, the nonabelian &#268;ech cocycles in question here are discussed at length and in detail in the literature on [[principal 2-bundle]]s by Toby Bartels, Igor Bakovi&#263; and Christoph Wockel. 

Nonabelian &#268;ech cocycles as therefore are naturally expressed $n$-functors out of &#268;ech $n$-groupoids.

This is described in some detail for instance in 

* [[Urs Schreiber]], [[Konrad Waldorf]], _Connections on non-abelian gerbes and their cohomology_ ([arXiv](http://arxiv.org/abs/0808.1923))

Another discussion more in the style of the [[Lie groupoid]] community is in section 2 of 

* Ginot, Sti&#233;non, _$G$-gerbes, principal 2-group bundles and characteristic classes_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.1238v2.pdf))

Giraud's gerbes as being the objects classified by [[nonabelian cohomology]] are recovered from general principles:

* [[Alexander Campbell]], _A higher categorical approach to Giraud's non-abelian cohomology_, PhD thesis, Macquarie University (2016) &lbrack;[hdl:1959.14/1261186](http://hdl.handle.net/1959.14/1261186)&rbrack;

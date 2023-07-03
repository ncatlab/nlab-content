## Idea

While for finite $m$, $m$-jets of a scheme of finite type (over an algebraically closed field of characteristic $0$) are represented by a scheme, the $m$-[[jet scheme]], the (inverse) limit of $m$-jet schemes is not 
of finite type; this is the arc space.

## Motivation

The arc space (and the jet schemes) of a variety $X$ gives information about the singular locus $X_{sing}$.

## Definition

Let $k$ be the algebraically closed field, $Sch/k$ the category of schemes over $k$ and $X$ an object in $Sch/k$. The presheaf
$$
(Sch/k)^{op}\to Set\,\,\,\,\,\,\,\,\,\,
 Y\mapsto (Sch/k) (Y\times_k k[t]/t^{m+1},X)
$$
is representable by a $k$-scheme of finite type $X_m$ the $m$-jet scheme. 
For $s\geq 1$, the canonical maps $k[t]/t^{m+1}\to k[t]^{m+s+1}$ induces maps
$(Sch/k) (Y\times_k k[t]/t^{m+s+1},X)\to (Sch/k)(Y\times_k k[t]/t^{m+1},X)$,
what is
$(Sch/k) (Y,X_{m+1})\to (Sch/k) (Y, X_m)$ hence also on representing objects
$X_{m+1}\to X_m$. The limit is the __arc space__ $X_\infty = lim_m X_m$ of $X$
and it comes along with natural projections $X_\infty\to X_m\to X$ (under some
assumptions each of the maps is locally trivial).

## Properties

If $X$ is a scheme of finite type over $k$ then there is a bijection 

$$
(Sch/k) (Y,X_\infty) \cong (ind-Sch/k) (Y\hat\times_{Spec k} Spec k[[t]],X)
$$

natural in $Y$ in $Sch/k$, where $Y\hat\times_k k[[t]]$ is the formal completion of
$Y$ along subscheme $Y\times_{Spec k} \{0\}$.1

## Literature

Related $n$Lab entries include [[singularity]], [[loop space]], [[jet space]], [[motivic integration]]

Early ideas appeared in

* J. Nash Jr., _Arc structure of singularities_, Duke Math. J.,
81 (1995), 31&#8211;38.

and its appearance in motivic integration stems from

* [[M. Kontsevich]], lecture on motivic integration, Orsay, December 7, 1995.

For basic lectures see

* M. Musta&#355;&#462;, _Spaces of arcs in birational geometry_, [pdf](http://www.math.lsa.umich.edu/~mmustata/lectures_arcs.pdf)
* M. Popa, 571 Ch. 5. _Jet schemes and arc spaces_, [pdf](http://homepages.math.uic.edu/~mpopa/571/chapter5.pdf)


For surveys, see
-
* Jan Denef, Francois Loeser, _Geometry on arc spaces of algebraic varieties_, Proceedings of 3rd ECM, Barcelona, July 10-14, 2000, [math.AG/0006050](http://arxiv.org/abs/math/0006050)
* L. Ein, M. Musta&#355;&#462;, _Jet schemes and singularities_, Algebraic geometry-
Seattle 2005, 505&#8211;546, Proc. Sympos. Pure Math. 80, Part 2, Amer. Math. Soc.,
Providence, RI, 2009 [MR2483946](http://www.ams.org/mathscinet-getitem?mr=2483946)

There are connections to combinatorics and representation theory, see

* Clemens Bruschek, Hussein Mourtada, Jan Schepers, _Arc spaces and the Rogers&#8211;Ramanujan identities_, The Ramanujan Journal 30:1 (2013) 9-38

A survey

* Tommaso de Fernex, _The space of arcs of an algebraic variety_, [arxiv/1604.02728](http://arxiv.org/abs/1604.02728)

Other papers

* J. Denef, F. Loeser, _Germs of arcs on singular algebraic varieties and motivic
integration_, Invent. Math. 135 (1999), 201&#8211;232.
* S Ishii, J Koll&#225;r, _The Nash problem on arc families of singularities, _
Duke Math. J., 120 (2003) 601&#8211;620 [math.AG/0207171](http://arxiv.org/abs/math/0207171)
* Shihoko Ishii, _The arc space of a toric variety_, [doi](http://dx.doi.org/10.1016/j.jalgebra.2003.12.015) [arxiv/0312324](http://arxiv.org/abs/math/0312324)
* L Ein, R Lazarsfeld, M Musta&#355;&#462;, _Contact loci in arc spaces_, Comput. Math. and [math.AG/0303268](http://arxiv.org/abs/math/0303268) 
* M Musta&#355;&#462;, _Jet schemes of locally complete intersection canonical singularities_, with an appendix by David Eisenbud and Edward Frenkel, Invent. Math., 145 (2001) 397&#8211;424; _Singularities of pairs via jet schemes_, J. Amer. Math. Soc., 15 (2002) 599&#8211;615
* Cobo Pablos, H. and Gonz&#225;lez P&#233;rez, Pedro Daniel (2012) Motivic Poincar&#233; series, toric singularities and logarithmic Jacobian ideals. Journal of algebraic geometry, 21 (3). pp. 495-529 [pdf](http://www.ams.org/journals/jag/2012-21-03/S1056-3911-2011-00567-5/S1056-3911-2011-00567-5.pdf)
* Dave Anderson, Alan Stapledon, _Arc spaces and equivariant cohomology_, Transformation Groups 18:4 (2013) 931-969
* J. Nicaise, _Arcs and resolution of singularities_, Manuscr. Math. 116: pp. 297-322 (2005)
* W. Veys, _Arc spaces, motivic integration and stringy invariants_, in
Singularity theory and its applications, Adv. Stud. Pure Math. 43, Math. Soc. Japan, Tokyo (2006) 529-572

See also Corollary 4.4 in

* Bhargav Bhatt, _Algebraization and Tannaka duality_, [arXiv/1404.7483](http://arxiv.org/abs/1404.7483)

## Related entries

[[Greenberg scheme]]
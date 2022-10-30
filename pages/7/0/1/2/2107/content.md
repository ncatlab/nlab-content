
#Contents#
* automatic table of contents goes here
{:toc}

## Motivation

Sometimes in the place where we expect [[Lie algebra]]s, some noncommutative phenomena occur and we need to drop out the requirement of antisymmetry of the brackets. 

[[Jean-Louis Loday]] introduced Leibniz algebras, because of considerations in [[algebraic K-theory]]. Roughly speaking the [[Lie algebra homology]] is related to the appearance of cyclic homology (as it is manifest in the original work of Tsygan and then of Loday-Quillen). 

* [[Jean-Louis Loday]], [[Daniel Quillen]], _Cyclic homology and the Lie algebra homology of matrices_, 	Comm. Math. Helv. __59__, n. 1, 565-591 (1984), [doi](http://dx.doi.org/10.1007/BF02566367)

Lie algebra homology involves the [[Chevalley-Eilenberg chain complex]], which in turns involves the exterior powers of the Lie algebra. Loday found that there is a noncommutative generalization where roughly speaking one has the tensor and not the exterior powers of the Lie algebra in the complex; this new complex defines the __Leibniz homology__ of Lie algebras. The Leibniz homology is related to the [[Hochschild homology]] the same way the Lie algebra homology is related to the cyclic homology. 

* C. Cuvier, _Homologie de Leibniz et homologie de Hochschild_, C.R. Acad. Sci. Paris, Ser. A-B313, 569-572 (1991)

In fact this new complex for Leibniz homology further generalizes to the case of Leibniz algebras, where it computes certain [[Tor]] groups for corepresentations of Leibniz algebras. 

## Definition

Given a [[commutative unital ring]] $k$ (usually a [[field]]), a Lebniz $k$-algebra $A$ is a particular kind of [[nonassociative algebra]] over $k$ which is somewhat more general than a [[Lie algebra]] over $k$.

A __left Leibniz $k$-algebra__ is $k$-[[module]] $L$ equipped with a bracket, which is a $k$-linear map $[,]:A\otimes A \to A$ satisfying the __left Leibniz identity__

$$ [a, [b,c]] = [[a,b],c]+[b,[a,c]] $$

In other words, the left $ad$-map, $a \mapsto (ad_l a = [a,-]:L\to L)$ is a [[derivation]] of $L$ as a nonassociative algebra. Similarly, there are right Leibniz algebras, for which the right $ad$-map $ad_r :a\mapsto [-,a]:L\to L$ is a derivation. In the presence of antisymmetry, the left Leibniz identity is equivalent to the [[Jacobi identity]], though this is not true in general; thus a Lie algebra is precisely an antisymmetric (or alternating) Leibniz algebra.

## Relation to Lie algebras in Loday-Pirashvili category

There is a remarkable observation of Loday and Pirashvili that in the [[Loday–Pirashvili tensor category]] of linear maps with (exotic) "infinitesimal tensor product", the category of internal Lie algebras has the category of, say left, Leibniz $k$-algebras as a full subcategory.  

## Terminology

Some people dislike the term (left/right) Leibniz algebra (which is allegedly due to Loday), and prefer other names, including 'Loday algebras' and many longer descriptive names.  

## Corepresentation, representation, crossed module

Both a representation and a corepresentation of a right Leibniz $k$-algebra $\mathfrak{g}$ involve a $k$-module $M$ and two $k$-linear maps "actions" $M\otimes\mathfrak{g}\to M$ and $\mathfrak{g}\otimes M\to M$  with 3 axioms. 

For representations:

$$[m, [x, y]] = [[m, x], y] - [[m, y], x]$$
$$[x, [a, y]] = [[x, m], y] - [[x, y], m]$$
$$[x, [y, m]] = [[x, y], m] - [[x, m], y]$$

for $x,y\in\mathfrak{g}$ and for $m\in M$. 

For corepresentatons:

$$[[x, y], m] = [x, [y, m]] - [y, [x, m]] $$
$$[y, [a, x]] = [[y, m], x] - [m, [x, y]] $$
$$[[m, x], y] = [m, [x, y]] - [[y, m], x].$$

If the two "actions" are symmetric, i.e. $[x,m] + [m,x] = 0$ for all $m\in M$, $x\in\mathfrak{g}$ then all the 6 axioms of representation or corepresentation are equivalent. If $M$ is underlying a Leibniz algebra then an action of $\mathfrak{g}$ on $M$ is by definition symmetric, hence all the 6 equivalent conditions hold. 

A map $t : \mathfrak{g}\to\mathfrak{b}$ together with an action of $\mathfrak{b}$ on $\mathfrak{g}$ is a Leibniz crossed module if

$$
t([b,g])= [b,t(g)],\,\,\,t([g,b])=[t(g),b],\,\,\,\, for all\,\,\, b\in\mathfrak{b}, g' \in\mathfrak{g}$$

$$
[g, t(g')] = [g, g'] = [t(g), g'],\,\,\,\, for all\,\,\, g, g' \in\mathfrak{g}
$$

## Abelian extensions

Abelian extension of right Leibniz algebras is a split short exact sequence of $k$-modules

$$ 0\to M \to \mathfrak{h}\to \mathfrak{g}\to 0 $$

where the mapping $\mathfrak{h}\to\mathfrak{g}$ is a morphism of Leibniz algebras, and $M$ is equipped with induced action of $\mathfrak{g}$. The isomorphisms of extensions of $\mathfrak{g}$ by $M$ with fixed action are defined as usual. This way we obtain a set of equivalence classes $Ext(\mathfrak{g},M)$. To classify the extensions one looks for compatible Leibniz brackets on $M\oplus \mathfrak{g}$. The general form of a bracket is

$$ [(m_1,x_1),(m_2,x_2)] = ([m_1, x_2] + [x_1, m_2] + f(x_1, x_2), [x_1, x_2]),$$

where $f(x_1,x_2)$ satisfy the following 2-cocycle identity:

$$
[x, f(y, z)] + [f(x, z), y] - [f(x, y), z] =
f([x, y], z) - f([x, z], y) - f(x, [y, z]) 
$$

The extension is __split__ in the category of Leibniz algebras if $f$ is a *boundary* i.e. there exists a $k$-module map $g:\mathfrak{g}\to M$ such that 

$$
f(x, y) = [x, g(y)] + [g(x), y] - g([x, y]), \,\,\,x,y,\in\mathfrak{g}
$$

As for the Lie algebras, the group of abelian extensions agrees with the 2-cohomology $HL^2(\mathfrak{g},M)$. 

A $k$-linear __derivation__ of a right Leibniz algebra $\mathfrak{g}$ with values in its representation $M$ is a $k$-linear map satisfying the Leibniz property with respect to the bracket:

$$
\delta([x,y]) = [\delta(x),y]+[x,\delta(y)]
$$

Such derivations form a $k$-module $Der(\mathfrak{g},M)$. 

## Homology and cohomology

The homology and cohomology of Leibniz algebra $\mathfrak{g}$ with abelian $k$-module of coefficients, which is a corepresentation $A$ in the case of homology and a representation $M$ in the case of cohomology: 

$$ HL_*(\mathfrak{g},A) = Tor^{U\mathfrak{g}}_*(U(\mathfrak{g}_{Lie}),A) ,$$

$$ HL^*(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(U(\mathfrak{g}_{Lie}),A) $$

where $U(\mathfrak{g}_{Lie})$ is the universal enveloping of the maximal Lie algebra quotient $\mathfrak{g}_{Lie}$ of $\mathfrak{g}$ and $U\mathfrak{g}$ is the universal enveloping of a Leibniz algebra $\mathfrak{g}$. 

Fopr $n\geq 0$, the $n$-cocycles are elements in $C^n(\mathfrak{g}, M) = Hom_k(\mathfrak{g}^{\otimes n}, M)$, satisfying the corresponding abelian cocycle condition determined by the differential 

$$ d^n : C^n(\mathfrak{g}, M)\to C^{n+1}(\mathfrak{g}, M) $$

$$ (d^n f) (x_1, . . . , x_{n+1}) = [x_1,f(x_2,\ldots,x_{n+1})] +\sum_{n+1}^{i=2} (-1)^i [f(x_1,\ldots, \hat{x}_i, \ldots, x_{n+1}), x_i] $$

Notice a difference from the Lie algebra cocycles where instead of a tensor power we have an external power. Then $HL^*(\mathfrak{g},M) = H^*(C^*(\mathfrak{g}, M),d^*)$. 

There are standard interpretations of cocycles in low dimensions. For example for $n=0$, $HL^0(\mathfrak{g}, M)$ is the submodule of invariants.
For $n=1$ there is a natural projection $Der(\mathfrak{g},M)\to HL^1(\mathfrak{g},M)$ whose kernel is generated by inner derivations. 

## The related kinds of algebras

The Leibniz operad is quadratic Koszul algebra whose Koszul dual operad is called the operad of dual Leibniz algebras
or of [[Zinbiel algebra]]s, see there. 

## Literature 

* [[Jean-Louis Loday]], [[Teimuraz Pirashvili]], _Universal enveloping algebras of Leibniz algebras and (co)homology_, Math. Ann. __296__, 139-158 (1993), [pdf](http://www-irma.u-strasbg.fr/~loday/PAPERS/LodayPira1993%28Leibniz%29.pdf)
* J-L. Loday, _Algebraic K-theory and the conjectural Leibniz K-theory_, K-Theory 09/2003; 30(2):105-127, [pdf](http://www-irma.u-strasbg.fr/~loday/PAPERS/2003Loday%28LeibnizConj%29.pdf) [doi](http://dx.doi.org/10.1023/B:KTHE.0000018382.90150.ce)
* [[Jean-Louis Loday]], [[Teimuraz Pirashvili]], _The tensor category of linear maps_, Georg. Math. J. vol. 5, n.3 (1998) 263--276.
* Jerry M. Lodder, _Leibniz homology, characteristic classes and K-theory, [K-theory archive/0493](http://www.math.uiuc.edu/K-theory/0493); _Leibniz cohomology and the calculus of variations_, [arXiv:math/9808036](http://arxiv.org/abs/math/9808036)

A generalization of [[Lie integration]] to conjectural Leibniz groups has been conjectured by [[J-L. Loday]]. A local version via local Lie [[rack]]s has been proposed in

* Simon Covez, _The local integration of Leibniz algebras_, [arXiv:1011.4112](http://arxiv.org/abs/1011.4112); _On the conjectural cohomology for groups_, [arXiv:1202.2269](http://arxiv.org/abs/1202.2269); 
_L'int&#233;gration locale des alg&#232;bres de Leibniz_, Thesis (2010), [pdf](http://tel.archives-ouvertes.fr/docs/00/49/54/69/PDF/THESE_Simon_Covez.pdf)

This is partly based on earlier insights of Kinyon and Weinstein:

* Michael K. Kinyon, _Leibniz algebras, Lie racks, and digroups_, J. Lie Theory __17__:1 (2007) 099--114, [arxiv:math.GR/0403509](http://arxiv.org/abs/math/0403509)

* Simon Covez, _On the conjectural Leibniz cohomology for groups_, Journal of K-theory __10__:03, Dec 2012, pp 519-563 [doi](http://dx.doi.org/10.1017/is011011011jkt195)

[[!redirects Leibniz algebras]]
[[!redirects Loday algebra]]
[[!redirects Leibniz rule]]
[[!redirects Leibniz rules]]
[[!redirects Leibniz identity]]
[[!redirects Leibniz identities]]

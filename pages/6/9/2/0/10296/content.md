# Dual gebras
* table of contents
{: toc}

## What is this entry about

Following Serre, [[gebra]] is a common term for [[associative algebra]]s and coassociative [[coalgebra]]s (also called cogebras), and sometimes more involved variants and combinations, like [[bialgebra]]s (also, more properly, called bigebras) and (co)rings. 

When working over a field, finite dimensional algebras are duals to finite dimensional cogebras. When the dimension is infinite, even for algebraic duals, the situation is more complicated. This entry should eventually sort out these issues (for now only the simplest
cases are discussed). 

## Algebraic dual

For a commutative ring $k$, a coassociative 
$k$-coalgebra $(C,\Delta)$ and an associative $k$-algebra $(A,m)$
the $k$-module $Hom_k(C,A)$ is equipped with an associative __convolution product__ $\star$ given by 
$(f\star g)(c) = m(f\otimes g)(\Delta(c))$. 
In particular, for $k$ a field, 
the algebraic dual $C^*:= Hom_k(C,k)$ of
a $k$-coalgebra $C$ is an associative algebra, called its __dual coalgebra__ whose product is also often referred to as convolution.
Correspondence $C\mapsto C^*$ extends to a contravariant functor
$Cog_k\to Alg_k$, where for $f:C\to D$, $f^*:D^*\to C^*$ is simply the transpose, hence $f^*(d^*)(c) = d^*(f(c))$. 

Now for a $k$-algebra $(A,m)$, its algebraic dual $A^*$ is _not_ necessarily a coalgebra; namely the natural candidate for the 
comultiplication $\Delta$ is the transpose operator $m^*: A^*\to (A\otimes A)^*$ of the multiplication $m: A\otimes A\to A$. 
There is a canonical injection 
$A^*\otimes A^*\to (A\otimes A)^*$; over a field $k$ it is an isomorphism (hence taken as an identification) iff $A$ is finite dimensional over $k$. In topological cases (e.g., if $A$ is filtered with filtered pieces finite-dimensional), one can replace the tensor product with some completed tensor product $\hat\otimes$ and define a topological comultiplication $m^*:A^*\to A^*\hat\otimes A^*$. In algebraic situation, one usually employs so called finite dual which is the maximal subspace $A^\circ$ for which $m^*$ factors through
$A^\circ\otimes A^\circ$. 

## Finite dual

If $k$ is a field, the finite dual functor $()^\circ:Alg_k\to Cog_k$ is the [[left adjoint functor]] to the algebraic dual as a functor $()^*:Cog_k\to Alg_k$.  $A^\circ\subset A^*=Hom_k(A,k)$ as a vector spaces (actually as functors $Alg_k\to Vec_k$, $()^\circ$ is a [[subfunctor]] of $()^*:Alg_k\to Vec_k$). For a concrete construction
below, the statement of adjointness is Theorem 1.5.22 in Dascalescu et al. 

We say that a subspace $W$ of a vector space $V$ is of finite codimension if $V/W$ is of finite dimension. As a vector subspace of 
$A^*$, 

$$
A^\circ = \{ f\in A^* \, | \, Ker(f)\, \text{contains an ideal of finite codimension in}\, A\}
$$

There are several other characterizations of the finite dual. Alternative terminologies are restricted dual and Hopf dual. 

## Actions on duals

We define here left actions &#8640; (or in LaTeX $\rightharpoonup$), &#8641; (LaTeX $\rightharpoondown$) and right actions &#8637; (LaTeX $\leftharpoondown$), &#8636; (LaTeX $\leftharpoonup$).

(Montgomery 1.6.5) If $C$ is a coalgebra, and $C^*$ the dual algebra, then $C^*$ acts from the left on $C$ by the transpose to the left multiplication

$$
\langle g, c &#8636; f\rangle = \langle f g, c\rangle
$$

or equivalently by the formula

$$
f &#8636; c \coloneqq \langle f, c_{(1)}\rangle c_{(2)},
$$

where the [[Sweedler notation]] has been used.

Similarly for the right-hand action:

$$
f &#8640; c \coloneqq \langle f, c_{(2)}\rangle c_{(1)},
$$

or

$$
\langle g, f &#8640; c\rangle = \langle f, c_{(2)}\rangle
\langle g, c_{(1)}\rangle = \langle g f, c\rangle
$$

According to the suggestion of Nichols, one reads $f$&#8640;$c$
as "$f$ hits $c$" and $f$&#8636;$c$ as "$f$ is hit by $c$". 

Similarly (cf. Montgomery 1.6.6), if $A$ is an algebra and $A^*$ its algebraic dual, one also defines harpoon actions as transposes to left and right multiplications, for example for right multiplication

$$
\langle h &#8636; f, k\rangle = \langle f, k h\rangle.
$$

Now, if $f\in A^\circ$ is in finite dual, then $\Delta(f)$ makes sense, hence, in Sweedler notation, 
$h$&#8640;$f=\langle f_{(2)}, h\rangle f_{(1)}$.

We also define here left and right coadjoint actions and coactions, cf. Majid. 

One should also treat rationality: a module is rational if it corresponds to a comodule of the finite dual coalgebra. 

## Paired bialgebras

For [[bigebra]]s (and [[Hopf algebra]]s n particular) 
one may consider the duality pairings which are 
compatible with their structure.

Two $k$-bigebras $B$ and $H$ are __paired__ 
if there is a bilinear map
$\langle,\rangle: B\otimes H\to k$ such that for all $a,b\in B$ and $h,g\in H$ the equations

$$
\langle a b, h\rangle = \langle a\otimes b,\Delta h\rangle,
\,\,\,\,\,\,\,\,\,\,\langle 1_B,h\rangle = \epsilon(h),
$$
$$
\langle \Delta a, h\otimes g\rangle = \langle a, h g\rangle,
\,\,\,\,\,\,\,\,\,\,\epsilon(a) = \langle a, 1_H\rangle
$$

They are a __strictly dual pair of bigebras__ if the pairing is also nondegenerate. If $B$ and $H$ are paired then one can quotient out [[biideal]]s $J_B\subset B$, $J_H\subset H$ of all those elements in each of them which pair as zero with all elements in the other bigebra; the quotients $B'$ and $H'$ will then be strictly paired bigebras.  

See also [[dual bialgebra]].

## Dual rings of corings

Let $A$ be a $k$-algebra and $C$ an $A$-[[coring]]. The left dual ${}* C$ of $C$ is defined by
$$
{}* C = {}_A Hom(C,k) 
$$
where ${}_A Hom(-,-)$ denotes the $k$-module of morphisms of left $A$-modules, with associative multiplication 
$$
(f\star g)(c) = g(c_{(1)},f(c_{(2)})).
$$

$A$ is a sub-$k$-algebra of ${}^* C$ via $i:A\hookrightarrow {}^* C$, $i(a)(c)=\epsilon(c)\cdot_A a$, that is ${}^* C$ is an $A$-ring (see [[ring over a ring]]).

The right dual $C^*$ is defined by
$$
C^* = Hom_A(C,k)
$$
where $Hom_A(-,-)$ denotes the $k$-module of morphisms of right $A$-modules, with the associative multiplication 
$$
(f\star g)(c) = f(g(c_{(1)}),c_{(2)}).
$$

$A$ is a sub-$k$-algebra of $C^*$ via $j:A\hookrightarrow C^*$, $j(a)(c)= a\cdot_A\epsilon(c)$.

## Literature

Related $n$Lab entries: [[dual]], [[Heisenberg double]], [[gebra]]

Quite detailed treatment of duality of gebras is in

* Sorin D&#259;sc&#259;lescu, Constantin N&#259;st&#259;sescu, Serban Raianu, _Hopf algebras: an introduction_, Marcel & Dekker 2000

and the entire Chapter VI (titled $()^\circ$) of

* [[Moss E. Sweedler]], _Hopf algebras_, Benjamin, N.Y. 1969

Other sources are

* [[Susan Montgomery]], _Hopf algebras and their actions on rings_, AMS 1994, 240 pp.
* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge Univ. Press
* Eiichi Abe, _Hopf algebras_, Cambridge Tracts in Mathematics 74, 1977

and for gebras with involution 

* A. van Daele, _Dual pairs of Hopf $\ast$-algebras_,  Bull. London Math. Soc. (1993) 25 (3): 209--230 [doi](https://doi.org/10.1112/blms/25.3.209)

Hit-actions are recently studied in

* M. Cohen, S. Westreich, _Hit-actions and commutators for Hopf algebras_, Bull. Math. Soc. Sci. Math. Roumanie __56__(104) No. 3, 2013, 299--313 [pdf](http://ssmr.ro/bulletin/pdf/56-3/articol_4.pdf)

[[Cartier duality]] and related earlier issues on [[linearly compact vector space]]s due Dieudonn&#233; are in the first chapter of 

* [[Jean Dieudonné]], _Introduction to the theory of formal groups_, Marcel Dekker, New York 1973.

Some newer applications are in

* Lowell Abrams, [[Charles Weibel]], _Cotensor products of modules_, [math.RA/9912211](https://arxiv.org/abs/math/9912211)

Duality of dg-algebras vs. dg-coalgebras is studied recently in great detail in

* [[Mathieu Anel]], [[André Joyal]], _Sweedler Theory for (co)algebras and the bar-cobar constructions_, 260 pp. [arxiv/1309.6952](https://arxiv.org/abs/1309.6952); cf. also Boston 2012 [slides](http://thales.math.uqam.ca/~anelm/mat/doc/boston.pdf)

Some special cases of finite duals are treated in

* Stephen Donkin, _On the Hopf algebra dual of an enveloping algebra_, Math. Proc. Camb. Phil. Soc. (1982), 91, 215-224, [doi](https://doi.org/10.1017/S0305004100059260)
* Jahn Astrid, _The finite dual of crossed products_, thesis, [pdf](http://theses.gla.ac.uk/6158/1/2015jahnphd.pdf)
* MathOverflow: [Hopf algebra duality and algebraic groups](http://mathoverflow.net/questions/31237/hopf-algebra-duality-and-algebraic-groups)

Duals of corings are used in

* [[Stefaan Caenepeel]], D. Quinn, S. Raianu, _Duality for finite Hopf algebras explained by corings_, Appl. Categor. Struct. 14 (2006) 531--537 [doi](https://doi.org/10.1007/s10485-006-9046-3)

Duals of [[Hopf algebroid]]s (under certain conditions) are studied in

* [[Peter Schauenburg]], _The dual and the double of a Hopf algebroid are Hopf algebroids_, Appl. Categ. Struct. __25__ (2017) 147--154 [doi](https://doi.org/10.1007/s10485-015-9418-7) [arXiv:1504.05057](https://arxiv.org/abs/1504.05057)

category: algebra

[[!redirects dual gebras]]
[[!redirects Hopf pairing]]
[[!redirects dual bialgebra]]
[[!redirects dual Hopf algebra]]
[[!redirects finite dual]]
[[!redirects restricted dual]]
[[!redirects Hopf dual]]

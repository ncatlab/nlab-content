## Motivation

The original motivation was the functorial Maschke's theorem over rings and its various cousins: namely the classical Maschke's theorem about finite group rings over fields, generalizes to the statements that when the order of the group is invertible in the ground ring then the spliting of an exact sequence of $kG$-module can be obtained functorially from its spliting as an exact sequence of 
$k$-modules.
Functors similar to the forgetful functor ${}_k Mod\to {}_{kG}Mod$ in a sense of 
having such a functorial Maschke's property are abstracted into the notion of a separable functor.

Similar phenomena appear in the study of ring extensions $f: R\to S$: such a ring extension is separable iff the extension of scalars $M\mapsto S\otimes_R M$ is a separable functor. 

## Definition

Let $F:C\to D$ be a functor. There is a corresponding (bi)natural transformation with components
$$
\mathcal{F}_{x,y} = C(x,y)\to D(Fx,Fy),\,\,\,\,(x\stackrel{f}\to y)\mapsto (Fx\stackrel{Ff}\to Fy).
$$
We way that $F$ is a separable functor if $\mathcal{F}$ splits (i.e. $\mathcal{F}_{x,y}$ has a section natural in $x$ and $y$).

## Properties

__Rafael's theorem.__ Let $F\dashv G$ be a pair of adjoint functors. Then $F$ is separable iff the unit $\eta:1\to GF$ has a section (= a natural transformation $\nu$ which is its right inverse, $\nu\circ\eta = 1$). $G$ is separable iff the counit $\epsilon:FG\to 1$ has a retraction (= a natural transformation $\zeta$ which is its left inverse, $\eta\circ\zeta =1$). 

## Generalization for $S$-categories

[[Tomasz Brzezinski]]

## Literature

Separable functors were defined in 

* C. N&#259;st&#259;sescu, M. van den Bergh, [[F. van Oystaeyen]], _Separable functors applied to graded rings_, J. Algebra __123__ (1989), 397-413, <a href="http://dx.doi.org/10.1016/0021-8693(89)90053-7">[doi]</a>.

Now there is a monograph available:

* S. Caenepeel, G. Militaru, S. Zhu, _Frobenius and separable functors for generalized module categories and nonlinear equations_, Lec. Notes in Math. __1787__, Springer 2002. xiv+354 pp. 

Other references

* M. D. Rafael, _Separable functors revisited_, Comm. in Algebra __18__ (1990), 1445-1459.

* S. Caenepeel, B. Ion, G. Militaru, _The structure of Frobenius algebras and separable algebras_,  $K$-Theory __19__ (2000),  no. 4, 365--402. 

* J. G&#243;mez-Torrecillas, _Separable functors in [[corings]]_, 
Int. J. of Math. and Math. Sci. __30__ (2002), 4, Pages 203-225, [doi](http://dx.doi.org/10.1155/S016117120201270X), [pdf](http://www.emis.de/journals/HOA/IJMMS/Volume30_4/225.pdf)

* A. Ardizzoni, _Separable functors and [[formal smoothness]]_,  J. K-Theory  1  (2008),  no. 3, 535--582, [math.QA/0407095](http://arxiv.org/abs/math.QA/0407095), [doi](http://dx.doi.org/10.1017/is007011015jkt012), [MR2009k:16069](http://www.ams.org/mathscinet-getitem?mr=2009k:16069)

[[!redirects separable functors]]
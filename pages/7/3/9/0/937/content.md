Given any category $C$, one can define the [[arrow category]] $\Arr(C)$ of $C$, whose objects are morphisms in $C$ and whose morphisms are commutative squares. If $C$ is the category of [[vector space]]s (or some other $k$-linear [[closed monoidal category|closed]] [[symmetric monoidal category]] with [[equalizer]]s) one can define the _infinitesimal_ or _Loday--Pirashvili_ (LP) tensor product on the category of arrows, as well as an inner hom, equipping the category $\mathrm{Arr} C$ with a structure of a $k$-linear closed symmetric monoidal category.

The LP-tensor product is
$$(f:V_1\to V_0)\otimes (g:W_1\to W_0):= (V_0\otimes g + f\otimes W_0: V_0\otimes W_1 \oplus V_1\otimes W_0\to V_0\otimes W_0).$$ 
This is a truncation of the tensor product of [[chain complex]]es where $V_1\otimes W_1$ is dropped.

The inner hom is rather interesting:
$\mathbf{Hom}(f,g) = (p:\mathrm{Hom}_1(f,g)\to\mathrm{Hom}_0(f,g))$, where $\mathrm{Hom}_0(f,g)$ is the equalizer of two morphisms
$$
\mathrm{hom}(V_0,W_0)\oplus\mathrm{hom}(V_1,W_1)\to\mathrm{hom}(V_1,W_0),
$$
namely precomposing the first summand with $f$ and postcomposing the second summand with $g$ (where $\mathrm{hom}$ is the ordinary [[hom-set|inner hom]] in $C$), and where $\mathrm{Hom}_1(f,g)$ is the equalizer of two morphisms 
$$\mathrm{Hom}_0(f,g)\oplus\mathrm{hom}(V_0,W_1)\to \mathrm{Hom}_0(f,g),$$ 
namely the identity and the map which replaces the lower component with the postcomposition by $g$ applied on $\mathrm{hom}(V_0,W_1)$ and keeps the upper component.
Finally, $p$ is the natural projection.

In the case of vector spaces this means that we have diagonal lifts in squares such that the lower square commutes but not necessarily the upper, i.e. $\mathrm{Hom}(f,g)$ is the space consisting of all triples $(u_1,u_0,\phi)$ where $u_1:V_1\to W_1$, $u_0:V_0\to W_0$ and $\phi:V_0\to W_1$
such that $g\circ u_1= u_0\circ f$ and $u_0=g\circ\phi$ while one does *not* require $\phi\circ f=u_1$.

There are a number of remarkable functors relating [[internalization|internal]] algebras in LP, [[Lie algebra]]s in LP etc., to or from some other categories of algebras. For example the categories of left [[Leibniz algebra]]s and of right Leibniz algebras embed as full subcategories into the category of internal Lie algebras in LP. This embedding has an [[adjunction|adjoint]].
Notice that because of truncation, being a Lie algebra in LP is a bit less than a (strict) $2$-[[Lie n-algebra|Lie algebra]] (a requirement in degree $2$ is dropped). 

See J-L. Loday, T. Pirashvili, The tensor category of linear maps, Georg. Math. J. vol. 5, n.3 (1998) 263--276.
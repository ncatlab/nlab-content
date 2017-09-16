Given any category $C$, one can define the category of arrows $\mathrm{Arr} C$ whose objects are morphisms in $C$ and morphisms in $\mathrm{Arr} C$ are commutative squares. If $C$ is the category of vector spaces (or some other $k$-linear closed symmetric monoidal category with equalizers) one can define infinitesimal or Loday-Pirashvili (LP) tensor product on the category of arrows and inner hom, equipping the category $\mathrm{Arr} C$ with a structure of $k$-linear closed symmetric monoidal category. 

LP-tensor product  
$$(f:V_1\to V_0)\otimes (g:W_1\to W_0):= (V_0\otimes g + f\otimes W_0: V_0\otimes W_1 \oplus V_1\otimes W_0\to V_0\otimes W_0).$$ 

This tensor product is a truncation of the tensor product of chain complexes where $V_1\otimes W_1$ is dropped. 

Inner hom is rather interesting:
$\mathbf{Hom}(f,g) = (p:\mathrm{Hom}_1(f,g)\to\mathrm{Hom}_0(f,g))$, where $\mathrm{Hom}_0(f,g)$ is the equalizer of two morphisms
$$
\mathrm{hom}(V_0,W_0)\oplus\mathrm{hom}(V_1,W_1)\to\mathrm{hom}(V_1,W_0),
$$
namely precomposing the first summand with $f$ and postcomposing the second summand with $g$ (where $\mathrm{hom}$ is the ordinary inner hom in $C$), and where
$\mathrm{Hom}_1(f,g)$ is the equalizer of two morphisms 

$$\mathrm{Hom}_0(f,g)\oplus\mathrm{hom}(V_0,W_1)\to \mathrm{Hom}_0(f,g),$$ 

namely the identity and the map which replaces lower component with the postcomposition by $g$ applied on $\mathrm{hom}(V_0,W_1)$ and keeps the upper component.
Finally, $p$ is the natural projection.

In the case of vector spaces this means that we have diagonal lifts in squares such that lower square commutes and upper not necessarily, i.e. $\mathrm{Hom}(f,g)$ is the space consisting of all triples $(u_1,u_0,\phi)$ where $u_1:V_1\to W_1$, $u_0:V_0\to W_0$ and $\phi:V_0\to W_1$
such that $g\circ u_1= u_0\circ f$ and $u_0=g\circ\phi$ while one does NOT require $\phi\circ f=u_1$.

There is a number of remarkable functors relating internal algebras in LP, Lie algebras in LP etc. to or from some other categories of algebras. For example the categories of left Leibniz algebras and of right Leibniz algebras embed as full subcategories into the category of internal Lie algebras in LP. This embedding has an adjoint.
Notice that because of truncation being a Lie algebra in LP is a bit less than a (strict) 2-Lie algebra (a requirement in degree $2$ is dropped). 

See J-L. Loday, T. Pirashvili, The tensor category of linear maps, Georg. Math. J. vol. 5, n.3 (1998) 263-276.
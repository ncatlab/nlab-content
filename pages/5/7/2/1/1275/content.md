Given a monoidal category $\mathcal{M}$ and a coalgebra $C$ in $\mathcal{M}$ denote by $\mathcal{M}^{C}$ ($ resp. {}^{C}\mathcal{M}$)
the category of right (resp. left) ${C}$-comodules; similarly for an algebra $E$, denote by ${}_E\mathcal{M}$ (resp. $\mathcal{M}_E$) the category of left $E$-modules
(right $E$-modules); if the monoidal category is [[symmetric monoidal category|symmetric]] or there is instead an appropriate [[distributive law]], then there are extensions of this notation to bimodules, bicomodules, relative [[Hopf module]]s, entwined modules etc. e.g. ${}_E\mathcal{M}^B$ for left-right relative $(E,B)$-Hopf modules where $E$ is a $B$-comodule algebra over a bialgebra $B$. 

Let $k$ be a commutative unital [[ring]], and let $\mathcal{M}$ be $k$-linear with (in particular it has zero morphisms). Given a coalgebra $C$ in $\mathcal{M}$, a left $C$-[[comodule]] $(N,\rho_N:N\to N\otimes C)$, a right $C$-comodule $(M,\rho_M:M\to C\otimes M)$, their
__cotensor product__ is an object in $\mathcal{M}$ given by
$$
N \Box M  :=
\mathrm{ker} (\rho_N \otimes \mathrm{id}_M - \mathrm{id}_N \otimes \rho_M ).
$$
If equalizers exist in $\mathcal{M}$, this formula extends to a bifunctor
$${}\Box = \Box^{C} :
\mathcal{M}^{C} \times {}^{C}\mathcal{M} \rightarrow \mathcal{M}.$$
If $B$ is a bialgebra in $\mathcal{M}$ and $E$ is a right $B$-comodule algebra then the same formula defines a bifunctor
$$\Box : {}_{E}\mathcal{M}^{B} \times {}^{B}\mathcal{M} \rightarrow
{}_{E}\mathcal{M}.$$ 

Let now $\mathcal{M}=({}_k\mathrm{Mod},\otimes_k)$ be the symmetric monoidal category of $k$-modules.

Let $D$ be another $k$-coalgebra, with coproduct $\Delta_C$.
If $D$ is [[flat module|flat]] as a $k$-module
(e.g. $k$ is a field),
and $N$ a left $D$- right $C$-bicomodule,
then the cotensor product $N \Box M$ is a $D$-subcomodule of
$N \otimes_k M$. In particular, under the flatness assumption, if $\pi : D \rightarrow C$ is a surjection of
coalgebras then $D$ is a left $D$- right $C$-bicomodule
via $\Delta_D$ and $(\id \otimes \pi) \circ \Delta_D$
respectively, hence $\mathrm{Ind}^D_C := D \Box^C -$
is a functor from left $C$- to left
$D$-comodules called the [[induced comodule|induction]] functor for left comodules from $C$ to $D$. 

Cotensor products in [[noncommutative geometry]] appear in the role of space of sections of a associated vector bundles of [[quantum principal bundle]]s (which in affine case correspond to [[Hopf-Galois extension]]s). See e.g.

* S. Majid, Foundations of quantum groups theory, 2nd extended edition, paperback, Cambridge Univ. Press 2000.

For a nonaffine extension of the sections of associated quantum vector bundle, using [[localization]] theory see

* Z. &#352;koda, Coherent states for Hopf algebras,
Lett. Math. Phys. 81 (2007), no. 1, 1--17. [arXiv:math.QA//0303357](http://front.math.ucdavis.edu/0303.5357)

In Hopf algebra theory, cotensor products appear as early as in 

* John W. Milnor, John C. Moore, On the structure of Hopf algebras.  Ann. of Math. (2)  81  1965 211--264.

The authors mention that they learned the notion from Mac Lane who knew it earlier in more general contexts. An important problem is that the cotensor product of bicomodules is in general (even for $\mathcal{M}={}_k\mathrm{Mod}$) *not associative*, even up to an isomorphism. Cotensor products play a prominent role in various treatments of Galois theory in noncommutative geometry; a particularly geometric approach is within a version of [[noncommutative algebraic geometry]] based on usage of monoidal categories, as sketched in 

* [[Tomasz Maszczyk]], Noncommutative geometry through monoidal categories I, [arXiv:0707.1542](http://front.math.ucdavis.edu/0707.1542)
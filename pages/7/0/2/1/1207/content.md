Measuring of coalgebras of algebra morphisms and algebras was introduced by Sweedler in

* [[M. E. Sweedler]], __Hopf algebras__, Mathematics Lecture Note Series, Benjamin 1969.

Given a commutative ring $k$, a $k$-coalgebra $(C,\Delta_C,\epsilon)$ and $k$-algebras $(A',\mu',\eta')$ and $(A,\mu,\eta)$, a __$C$-measuring__ from $A'$ to $A$ is a $k$-linear map $f: C\to Mod_k(A',A)$ such that
$$
ev\circ (f\otimes\mu_{A'}) = \mu_A\circ (ev\otimes ev)\circ(f\otimes A'\otimes f\otimes A')\circ (C\otimes \tau_{A',C}\otimes A')\circ (\Delta_C\otimes A'\otimes A') : C\otimes A'\otimes A'\to A,
$$
and $f\circ \eta' = \eta\circ\epsilon_C:C\to A$ where $\tau$ is the transposition of factors and $ev$ the evaluation of a map. In Sweedler notation, the requirements on $f$ are
$f(c)(a\cdot_{A'} b) = f(c_{(1)})(a)\cdot_A f(c_{(2)})(b)$
and $f(c)(1_{A'}) = \epsilon(c)1_{A}$.

We can instead of $f:C\to Mod_k(A',A)$ consider its adjoint map $\tilde{f}:C\otimes A'\to A$ and the convolution algebra $Mod_k(C,A)$.
Then, $f$ is a measuring (or some say taht $\tilde{f}$ is a measuring iff the other adjoint $\tilde{f}^*: A'\to Mod_k(C,A)$ is a map of algebras. 

As a special case, we can consider the case of the identity map $A\overset{A}\to A$ and talk about a $C$-measuring of a monoid $A$, including in the general case of a symmetric monoidal category $D$ with unit $\mathbf{1}$, symmetry $\tau$, left and right unit coherences $l$ and $r$,
a map $\triangleright : C\otimes A\to A$ of a (counital) is a __measuring__ of the comonoid $C$ on a (unital) monoid $(A,\mu_A,\eta_A)$, or we say that $C$ *measures* $A$ if 
$$
C\triangleright \mu_A = \mu_A\circ(\triangleright \otimes \triangleright)\circ (C\otimes \tau\otimes A)\circ (\Delta_C\otimes A\otimes A) : C\otimes A\otimes A\to A,
$$
and
$$
\triangleright \circ (C\otimes \eta) = \eta\circ r_C\circ (\epsilon\otimes \mathbf{1}): C\otimes \mathbf{1}\to A.
$$
In Sweedler notation, we also write $c\triangleright (ab) = 
\sum (c_{(1)}\triangleright a)(c_{(2)}\triangleright b)$ and
$c\triangleright 1_A = \epsilon(c) 1_A$. Note that $C$ is not a monoid so a measuring is not an action (although the notation may suggest this). However if $C$ is a bialgebra, we may consider when it is an action.
A [[Hopf action]] is a measuring which is also an action of a <em> bimonoid </em> $B=(C,\Delta_C,\epsilon,\mu_C,\eta_C)$. In other words, $A$ is a monoid in the monoidal category of $B$-modules (also called $B$-module monoid or $B$-[[module algebra]]). 

Measurings of algebras by bialgebras are used to define the (cocycled) [[crossed product algebra]]s, see also [[cleft extension]] (of an algebra by a bialgebra). For measurings and module algebras see

* S. Montgomery, Hopf algebras and their actions on rings, CBMS 82, AMS 1993.

* A. Klimyk, K. Schm&#252;dgen, _Quantum groups and their representations_, Springer, 1997;

and for (co)module (co)algebras and generalizations see also

* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge University Press 1995, 2000.

There are also more elaborate versions of measurings, which play role in a Galois theory, see 

* [[Tomasz Brzeziński]], _On modules associated to coalgebra Galois extensions, J. Algebra, 215, no. 1, 1999, 290-317.

Other works include

* [[Martin Hyland|M. Hyland]], I. Lo'pez Franco, C. Vasilakopoulou, _Hopf measuring comonoids and enrichment_, Proc. Lond. Math. Soc. (3) 115:5 (2017) 1118--1148

If $U$ and $V$ are $k$-algebras measured by a $k$-coalgebra $C$ and $M$ is a $U$-$V$-bimodule, then we say that $M$ is measured by $C$, if there is a $k$-bilinear map $\triangleright_M:C\otimes M\to M$ such that for all $u\in U$, $v\in V$, $m\in M$, $c\in C$,

$$
c\triangleright (u m v) = \sum (c_{(1)}\triangleright_U u) (c_{(2)}
\triangleright_M m)(c_{(3)}\triangleright_V v)
$$

If $C$ is in addition a $k$-bialgebra and $\triangleright_U,\triangleright_V,\triangleright_M$ actions of $H$, we say that a measuring is __Hopf action__ of $C$ on the $U$-$V$-bimodule $M$. 
For Hopf actions on bimodules, one can define a 
bimodule version of a (Hopf) [[smash product algebra]], see [[zoranskoda:Hopf smash product bimodule]].

There is a dual notion of a comeasuring, see

* [[Mitsuhiro Takeuchi]], _Matched pairs of groups and bismash products of hopf algebras_, Comm. Alg. __9__:8 (1981) 841--882 [doi](https://doi.org/10.1080/00927878108822621) 

See also related $n$Lab page [[measuring coalgebra]] about the related enrichment (in the cocommutative case) and wikipedia:[measuring coalgebra](https://en.wikipedia.org/wiki/Measuring_coalgebra) which has a bit of both.

Given an algebra $A$ and a coalgebra $C$, a map 
$\rho:C\to A\otimes C$ 
is a left __$A$-comeasuring__ of $C$ if
$$
\sum c^A\otimes c^C_{(1)} \otimes c^C_{(2)}
= \sum (c_{(1)})^A (c_{(2)})^A\otimes c_{(1)}^C\otimes c_{(2)}^C
$$
and $(A\otimes\epsilon)\circ\rho = \epsilon$,
where we denote $\rho(c) = \sum c^A\otimes c^C$ and $\Delta(c) = \sum c_{(1)}\otimes c_{(2)}$.
If $A$ is a bialgebra then $A$-comeasurings of coalgebras (with additional data) appear in the definition of (cocycle) cross coproduct coalgebras.

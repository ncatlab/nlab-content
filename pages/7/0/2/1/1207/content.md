In a strict symmetric monoidal category $D$ with unit $\mathbf{1}$, symmetry $\tau$, left and right unit coherences $l$ and $r$, a map $\triangleright : C\otimes A\to A$ of a (counital) comonoid $(C,\Delta_C,\epsilon)$ on a (unital) monoid $(A,\mu_A,\eta_A)$ is a __measuring__, or we say that $C$ *measures* $A$ if 
$$
C\triangleright \mu_A = \mu_A\circ(\triangleright \otimes \triangleright)\circ (C\otimes \tau\otimes A)\circ (\Delta_C\otimes A\otimes A) : C\otimes A\otimes A\to A,
$$
and
$$
\triangleright \circ (C\otimes \eta) = \eta\circ r_C\circ (\epsilon\otimes \mathbf{1}): C\otimes \mathbf{1}\to A.
$$
In Sweedler notation, we also write $c\triangleright (ab) = 
\sum (c_{(1)}\triangleright a)(c_{(2)}\triangleright b)$ and
$c\triangleright 1_A = \epsilon(c) 1_A$.
A [[Hopf action]] is a special case of measuring which is also an action of a <em> bimonoid </em> where $B=(C,\mu_C)$. In other words, $A$ is a monoid in the monoidal category of $B$-modules (also called $B$-module monoid or $B$-[[module algebra]]). Measurings are used to define the (cocycled) [[crossed product algebra]]s, see also [[cleft extension]] (of an algebra by a bialgebra). For measurings and module algebras see

* S. Montgomery, Hopf algebras and their actions on rings, CBMS 82, AMS 1993.

* A. Klimyk, K. Schm&#252;dgen, _Quantum groups and their representations_, Springer, 1997;

and for (co)module (co)algebras and generalizations see also

* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge University Press 1995, 2000.

There are also more elaborate versions of measurings, which play role in a Galois theory, see 

* [[Tomasz Brzeziński]], _On modules associated to coalgebra Galois extensions, J. Algebra, 215, no. 1, 1999, 290-317.

If $U$ and $V$ are $k$-algebras measured by a $k$-coalgebra $C$ and $M$ is a $U$-$V$-bimodule, then we say that $M$ is measured by $C$, if there is a $k$-bilinear map $\triangleright_M:C\otimes M\to M$ such that for all $u\in U$, $v\in V$, $m\in M$, $c\in C$,

$$
c\triangleright (u m v) = \sum (c_{(1)}\triangleright_U u) (c_{(2)}
\triangleright_M m)(c_{(3)}\triangleright_V v)
$$

If $C$ is in addition a $k$-bialgebra and $\triangleright_U,\triangleright_V,\triangleright_M$ actions of $H$, we say that a measuring is __Hopf action__ of $C$ on the $U$-$V$-bimodule $M$. 
For Hopf actions on bimodules, one can define a 
bimodule version of a (Hopf) [[smash product algebra]], see [[zoranskoda:Hopf smash product bimodule]].
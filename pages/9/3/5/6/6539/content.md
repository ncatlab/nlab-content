See also [[dual gebra]] for a more general entry.

## Definition

Given a field $k$, a $k$-vector space pairing between $k$-bialgebras $H$ and $K$  such that 

$$
\langle h\otimes h', \Delta_K k\rangle = \langle h h', k\rangle
$$

$$
\langle \Delta_H h, k\otimes k' \rangle = \langle h, k k'\rangle
$$

$$
\langle h, 1_K\rangle = \epsilon_H(h),
\,\,\,\,\,
\langle 1_H, k\rangle = \epsilon_K(k).
$$

(where on the left hand side $\langle,\rangle$ denotes the map $H\otimes H\otimes K\otimes K\to k$ given by
$\langle h\otimes h', k\otimes k'\rangle = \langle h,k\rangle \langle h',k' \rangle$), is called the __bialgebra pairing__.  

The bialgebra pairing which is __perfect__ (nondegenerate in each variable) as a $k$-vector space pairing (i. e. if $\langle h, K\rangle = 0$ implies that $h$ is $0$ and $\langle H,k\rangle$ implies that $k$ is $0$) is called the bialgebra duality. 

## Finite duals 

As stated in [[dual gebra]], for an algebra $A = (A,m)$, a finite (or restricted or Hopf) dual is the subspace
$$ A^\circ = \{f\in A^* | \exists ideal I\subset Ker(f)\subset A, dim(A^*/I)\lt\infty \}\subset A^*.$$ 
Then $f\in A^\circ$ iff $m^*(f)\subset A^*\otimes A^*$ which is iff $m^*(f)\subset A^\circ\otimes A^\circ$, see [Sweedler1969](Sweedler1969). This subspace is consequently a coalgebra, via the corestriction of $m^*:A^*\to (A\otimes A)^*$. If $A$ is a bialgebra (Hopf algebra) then $A^\circ$ is such as well.
We can say this differently: If $H$ is a bialgebra (resp. Hopf algebra) then its finite dual $H^\circ$ has a unique structure of a bialgebra (resp. Hopf algebra) such that
the evaluation is a bialgebra pairing. 

A general pairing $\langle -,-\rangle : H\otimes K\to K$
of vector spaces underlying Hopf algebras $H$ and $K$ is
a bialgebra pairing iff the induced map $H\to K^\circ$, $h\mapsto \langle h, -\rangle$
is a bialgebra map. 

## Hopf algebra case

If $H$ and $K$ are Hopf algebras then the bialgebra pairing is a Hopf pairing if $\langle h, S k \rangle = \langle S h, k\rangle$. This is however, automatic. 

## Literature

* {#Sweedler1969} [[Moss E. Sweedler]], $()^\circ$, Chapter VI in _Hopf algebras_, Benjamin, N.Y. 1969

* MO: [is-a-bialgebra-pairing-of-hopf-algebras-automatically-a-hopf-pairing](https://mathoverflow.net/questions/20666/is-a-bialgebra-pairing-of-hopf-algebras-automatically-a-hopf-pairing), [dual-of-a-hopf-algebra](https://math.stackexchange.com/questions/3324098/dual-of-a-hopf-algebra), [hopf-dual-of-the-hopf-dual](https://mathoverflow.net/questions/308374/hopf-dual-of-the-hopf-dual), [on-reflexive-bialgebras](https://mathoverflow.net/questions/357738/on-reflexive-bialgebras)
* Stephen Donkin, _On the Hopf algebra dual of an enveloping algebra_, Math. Proc. Camb. Phil. Soc. __91__ (1982) 215-224
* R. G. Heyneman, [[David E. Radford]], _Reflexivity and coalgebras of finite type_,J. Alg. __28__ (1974) 215-246 [pdf](https://core.ac.uk/download/pdf/82125553.pdf)

category: algebra

[[!redirects dual Hopf algebra]]
[[!redirects Hopf algebra dual]]
[[!redirects bialgebra dual]]
[[!redirects bialgebra pairing]]
[[!redirects Hopf algebra pairing]]
[[!redirects Hopf pairing]]

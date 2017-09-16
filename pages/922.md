#Definition#
Let $(C,d_C)$ be a dg-coalgebra with comultiplication $\Delta$ and $(A,d_A)$ a dg-algebra with multiplication $\mu$. A twisting cochain is a morphism $\tau:C\to A[1]$ such that the following [[ Maurer-Cartan equation
| Maurer-Cartan equation]] holds:
$$d_A\circ\tau+\tau\circ d_C+\mu\circ(\tau\otimes\tau)\circ\Delta = 0.$$

#Relation to the adjunction bar-cobar#
Let $\mathrm{Cogc}$ be the category of cocomplete dg-co(al)gebras and $\mathrm{Alg}$ the category of dg-algebras. There is a bar-construction functor $B :\mathrm{Alg}\to\mathrm{Cogc}$ which is a right adjoint to the cobar-construction functor $\Omega:\mathrm{Cogc}\to\mathrm{Alg}$. Starting from a map $f\in\mathrm{Cogc}(C,BA)$ one constructs a twisting cochain $\tau_f$ by postcomposing $f: C\to BA$ by the natural projection $BA\to A[1]$; the Maurer-Cartan equation for $\tau_f$ translates to saying that $f$ is a chain map, $d_{BA}\circ f = f\circ d_C$. One then replaces $\tau_f$ by the composition of the natural map $\Omega C\to C[-1]$ and $\tau_f[-1]:C[-1]\to A$ to obtain a morphism $f':\Omega C\to A$. The Maurer-Cartan equation for $\tau$ is equivalent also to saying that $f'$ is a chain map, i.e. $d_A\circ f'=f'\circ d_{\Omega C}$.

#Some usages of twisting cochain#

Twisting cochain is a datum used to define the [[twisted tensor product| twisted tensor product]] $L\otimes_\tau M$ for any right $C$-comodule $L$ and any left $A$-comodule $M$,
as well as the [[twisted module of homomorphisms|twisted module of homomorphisms]] $\mathrm{Hom}_\tau(N,P)$ where $N$ is a left $C$-dg-comodule and $P$ a left $A$-dg-module.

There are variants of the notion of twisting cochain in a variety of other contexts.


This is about a famous theorem from

* Jean Benabou, Jacques Roubaud, _Monades et descente_, C. R. Acad. Sc. Paris, t. 270 (12 Janvier 1970), Serie A, 96--98

(_Zoran_: a file with my few years old English translation will be posted and linked in few days or weeks) 

relating the [[descent]] via [[Grothendieck fibration|fibered categories]] and monadic descent. 

By a definition, a functor $P:F\to A$ is a Grothendieck cofibration (or nowdays opfibration) if $P^{op}:F^{op}\to A^{op}$ is a fibration; a functor $P:F\to A$ is a __bifibration__ if $P$ is both Grothendieck cofibration and fibration (no additional compatibility asked!). Thus we can talk about cartesian and cocartesian arrows in $F$.

In a bifibered category, automatically for any morphism $a:A_1\to A_0$ in the base the inverse image functor $a^*:F(A_0)\to F(A_1)$ is right adjoint to the direct image functor $a_*:F(A_1)\to F(A_0)$; with unit $\eta^a : Id_{F(A_1)} \to a^* a_*$ and counit $\epsilon^a : a_* a^* \to Id_{F(A_0)}$. (This is contrary to the usual geometric conventions where inverse image is the left adjoint, but this is a matter of taking some opposites of the categories in the motivating examples.) This [[adjunction]] generates a [[monad]] $\mathbf{T}^a=(T^a,\mu^a,\eta^a)$ in the usual vein: $T^a = a^* a_* : F(A_1)\to F(A_1)$, $\mu^a = a^* \epsilon^a a_* : T^a \circ T^a \to T^a$. Denote by $F^a$ the [[Eilenberg-Moore category]] $F(A_1)^{\mathbf{T}^a}$ of modules (algebras) over the monad $\mathbf{T}^a$, by  $U^{\mathbf{T}} : F^a \to F(A_1)$
the canonical forgetful functor and by $\Phi^a : F(A_0) \to F^a$ the canonical comparison functor.

One assumes that $A$ has fibered products and an important additional assumption on $P$, nowdays called __Beck-Chevalley property__, and in the paper Chevalley property, making $P$ into a Chevalley functor:
For each commutative square
$$\array{
N_0 \stackrel{\chi'}\leftarrow & N_1\\
\downarrow^{k_0}& \downarrow^{k_1}\\
M_0\stackrel{\chi}\leftarrow & M_1
}$$
in $F$ such that its image in $A$ is a cartesian square, if $\chi$ and $\chi'$ are cartesian then $k_1$ is cocartesian.

Denote $A_2 :=A_1\times_{A_0}A_1$ the pullback fo $a$ along itself, with the canonical projections $a_1,a_2:A_2\to A_1$. Considering the lift of the cartesian square defining $A_2$ to $F$ in such a way that $a_1$ is lifted to cartesian and $a_2$ to cocartesian arrow and $a$ to a cocartesian arrow, then by the universality there is a lift of $a$ completing the square; by the Beck-Chevalley it is cartesian. Together with the isomorphism given by adjunction this gives a morphism

$$
K^a: Hom_{F(A_2)}(a_1^*(M_1),a_2^*(M_1))\to Hom_{F(A_1)}(T^a(M_1),M_1).
$$ 

One checks that an invertible morphism $\phi:a_1^*(M_1)\to a_2^*(M_1)$ satisfies the cocycle equation (making it into a descent datum) iff $K^a(\phi)$ is an action of $\mathbf{T}^a$ on $M_1$; similarly for the unitality axiom. 

Denote by $Desc(a)$ the category of descent data for fibration $P$ along morphism $a$; it comes with canonical functors $\Psi^a:F(A_0)\to Desc(a)$ and $U^a:Desc(a)\to F(A_1)$. 

__Benabou-Roubaud theorem__ asserts that this induces an equivalence of categories between $Desc(a)$ and $F^a$ satisfying in addition some naturality properties, including that it commutes appropriately with the canonical functors to the fibers $F(A_0)$ and $F(A_1)$. Combining this theorem with Beck's monadicity theorems it becomes a practical tool for establishing a descent property in bifibration with variants in some other setup (to be covered later).  
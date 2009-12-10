This is about a famous theorem from

* Jean Benabou, Jacques Roubaud, _Monades et descente_, C. R. Acad. Sc. Paris, t. 270 (12 Janvier 1970), Serie A, 96--98

>_Zoran_: a file with my few years old English translation will be posted and linked in few days or weeks

relating [[descent]] via [[Grothendieck fibration|fibered categories]] to monadic descent. 

By a definition, a functor $P:F\to A$ is a [[Grothendieck opfibration]] if $P^{op}:F^{op}\to A^{op}$ is a [[Grothendieck fibration]], and a functor $P:F\to A$ is a __bifibration__ if $P$ is both a Grothendieck opfibration and fibration (no additional compatibility asked!). Thus we can talk about [[cartesian morphism|cartesian]] and [[cocartesian morphism|cocartesian]] arrows in $F$.

In a bifibered category, automatically for any morphism $a:A_1\to A_0$ in the base, the "inverse image" (or "pullback" or "restriction") functor $a^*:F(A_0)\to F(A_1)$ is right adjoint to the "pushforward" functor $a_!:F(A_1)\to F(A_0)$; with unit $\eta^a : Id_{F(A_1)} \to a^* a_!$ and counit $\epsilon^a : a_! a^* \to Id_{F(A_0)}$.

(Note that in topos theory and algebraic geometry, functors $a^*$ called "inverse images" usually have *right* adjoints $a_*$.  This situation can be reconciled with the setup of bifibrations either by taking fiberwise opposites, so that left and right adjoints are switched, or by taking opposites of both the base and total categories, so that the direct and inverse images are switched.  However, there are also many bifibrations arising in other contexts in which $a^*$ has both a left adjoint $a_!$ *and* a right adjoint $a_*$, although the latter cannot then be described cleanly in fibrational terms.)

In any case, the [[adjunction]] $a_!\dashv a^*$ generates a [[monad]] $\mathbf{T}^a=(T^a,\mu^a,\eta^a)$ in the usual way: the functor is $T^a = a^* a_!\colon  F(A_1)\to F(A_1)$, the multiplication is $\mu^a = a^* \epsilon^a a_!\colon  T^a \circ T^a \to T^a$, and the unit is just the unit of the adjunction.  Denote by $F^a$ the [[Eilenberg–Moore category]] $F(A_1)^{\mathbf{T}^a}$ of modules (algebras) over the monad $\mathbf{T}^a$, with canonical forgetful functor $U^{\mathbf{T}} \colon  F^a \to F(A_1)$ and canonical comparison functor $\Phi^a : F(A_0) \to F^a$.

Now we assume that $A$ has [[pullbacks]], and that $P$ satisfies what is nowadays called the **Beck-Chevalley property**, namely that for each commutative square
$$\array{
N_0 \stackrel{\chi'}\leftarrow & N_1\\
^{k_0}\downarrow& \downarrow^{k_1}\\
M_0\stackrel{\chi}\leftarrow & M_1
}$$
in $F$ such that its image in $A$ is a [[pullback]] square, if $\chi$ and $\chi'$ are cartesian then $k_1$ is cocartesian.

+--{: .query}
[[Mike Shulman]]: Is that really correct?  I would have thought it would be "if $\chi$ and $\chi'$ are cartesian and $k_1$ is opcartesian, then $k_0$ is also opcartesian.
=--

An equivalent way to state the condition is that for any pullback square
$$\array{x & \overset{a}{\to} & y\\
  ^c\downarrow && \downarrow^d\\
  z& \underset{b}{\to} & w}$$
in $A$, the canonical transformation $c_! a^* \to b^* d_!$ is an isomorphism.   In the Benabou-Roubad paper this is called the *Chevalley property* and said to make $P$ into a *Chevalley functor*.


Denote by $A_2 :=A_1\times_{A_0}A_1$ the pullback of $a$ along itself, with the canonical projections $a_1,a_2\colon A_2\to A_1$.  Now consider the lift of the cartesian square defining $A_2$ to $F$ in such a way that $a_1$ is lifted to a cartesian arrow, $a_2$ to a cocartesian arrow, and $a$ to a cocartesian arrow.  Then by the universality there is a lift of $a$ completing the square, and by the Beck-Chevalley property it is cartesian. Together with the isomorphism given by adjunction this gives a morphism

$$
K^a: Hom_{F(A_2)}(a_1^*(M_1),a_2^*(M_1))\to Hom_{F(A_1)}(T^a(M_1),M_1).
$$ 

One checks that an invertible morphism $\phi\colon a_1^*(M_1)\to a_2^*(M_1)$ satisfies the cocycle equation (making it into a descent datum) iff $K^a(\phi)$ is an action of $\mathbf{T}^a$ on $M_1$, and similarly for the unitality axiom.

Denote by $Desc(a)$ the category of descent data for the fibration $P$ along the morphism $a$; it comes with canonical functors $\Psi^a\colon F(A_0)\to Desc(a)$ and $U^a\colon Desc(a)\to F(A_1)$.

Finally, the __Benabou-Roubaud theorem__ asserts that this induces an equivalence of categories between $Desc(a)$ and $F^a$.  In addition, this equivalence satisfies some naturality properties, including that it commutes appropriately with the canonical functors to the fibers $F(A_0)$ and $F(A_1)$. Combining this theorem with Beck's [[monadicity theorem]], it becomes a practical tool for establishing a descent property in bifibrations, with variants in some other setups (to be covered later).


[[!redirects Benabou–Roubaud theorem]]
[[!redirects Benabou--Roubaud theorem]]

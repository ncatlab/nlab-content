##Definition##

Given a (counital coassociative) $k$-[[coalgebra]] $(C,\Delta,\epsilon)$, a $k$-linear __coderivation__ is a $k$-module map $ D : C\to C$ satisfying the co-Leibniz rule

$$
\Delta \circ D = (D\otimes id + id \otimes D)\circ\Delta : C\to C\otimes C
$$

If the [[commutative ring]] $k$ is a [[field]] and $C$ is finite-dimensional, then the transposes of the coderivations on $C$ are the [[derivations]] of the $k$-algebra $Hom_k(C,k)$. With proper care of continuity conditions, this correspondence generalizes to other (for example infinite-dimensional) contexts. 


##Examples##

The left translations of the elements of the [[universal enveloping algebra]] $H=U(L)$ of a [[Lie algebra]] $L$ on itself $L_h (g) = h g$ restricts to an action of $L$ on $U(L)$ by coderivations:
$$\Delta (h) = 1\otimes h + h \otimes 1,$$
hence
$$(L_h \otimes 1 + 1 \otimes L_h)(\Delta (g)) = \Delta(h)\cdot\Delta(g) = \Delta(h g) = (\Delta \circ L_h)(g).$$


[[!redirects coderivations]]
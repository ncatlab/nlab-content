
&lbrack;xyz&rbrack;

For any [[category]] $C$, there exists a [[covariant functor]] $Aut : Core(C) \to Grp$ from the [[core groupoid|core]] to [[Grp]], which maps each object $A$ to an automorphism group $Aut(A)$ and each morphism $f$ to a conjugate as follows.

$$
\begin{array}{rl}
\mathrm{Aut}(f) : \mathrm{Aut}(A) & \longrightarrow \mathrm{Aut}(B) \\
a & \mapsto f \circ a \circ f^{-1} \\
\end{array}
$$

The [[contravariant functor|contravariant form]] can be obtained by changing the order of the conjudate as $f^{-1} \circ a \circ f$.
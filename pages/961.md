In a [[finitely complete category]] $C$, a **congruence** on an object $X$ is an [[internalization|internal]] [[equivalence relation]] on $X$.

To be precise, this consists of a [[subobject]] $R\stackrel{(p_1,p_2)}\hookrightarrow X \times X$ equipped with the following maps:
* internal [[reflexive relation|reflexivity]]: $r: X \to R$ which is a section both of $p_1$ and of $p_2$;
* internal [[symmetric relation|symmetry]]: $s: R \to R$ which interchanges $p_1$ and $p_2$, namely $p_1\circ s = p_2$ and $p_2\circ s = p_1$;
* internal [[transitive relation|transitivity]]: $t: R \times_X R \to R$; where with the notation for the projections in the cartesian square
$$\array{
R \times_X R & \stackrel{q_2}\rightarrow & R\\
\downarrow^{q_1} && \downarrow^{p_1}\\
R & \stackrel{p_2}\rightarrow & X
}$$
the following holds: $p_1\circ q_1 = p_1\circ t$ and $p_2\circ q_2 = p_2\circ t$. 

Any [[kernel pair]] is a congruence; a congruence which is the kernel pair of some morphism is called **effective**.  The [[coequalizer]] of a congruence is called a **[[quotient object]]**.  An effective congruence is always the kernel pair of its quotient if that quotient exists; the quotient of an effective congruence is an **effective quotient**.  A [[regular category]] is called an [[exact category]] if every congruence is effective.

# Examples #

An [[equivalence relation]] is precisely a congruence in [[Set]].

The eponymous example is congruence modulo $n$ (for a fixed [[natural number]] $n$), which is a congruence on $\mathbf{N}$ in the category of [[rig]]s.
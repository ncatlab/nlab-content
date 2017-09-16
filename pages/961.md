In a [[finitely complete category]] $C$, a **congruence** on an object $X$ is an [[internalization|internal]] [[equivalence relation]] on $X$.

To be precise, this consists of a [[subobject]] $E$ of $X \times X$ equipped with the following maps:
* internal [[reflexive relation|reflexivity]]: $r: X \to R$;
* internal [[symmetric relation|symmetry]]: $s: R \to R$;
* internal [[transitive relation|transitivity]]: $t: R \times_X R \to R$
such that some diagrams commute that I haven\'t drawn yet.

Any [[kernel pair]] is a congruence; a congruence which is the kernel pair of some morphism is called **effective**.  The [[coequalizer]] of a congruence is called a **[[quotient object]]**.  An effective congruence is always the kernel pair of its quotient if that quotient exists; the quotient of an effective congruence is an **effective quotient**.  A [[regular category]] is called an [[exact category]] if every congruence is effective.

# Examples #

An [[equivalence relation]] is precisely a congruence in [[Set]].

The eponymous example is congruence modulo $n$ (for a fixed [[natural number]] $n$), which is a congruence on $\mathbf{N}$ in the category of [[rig]]s.
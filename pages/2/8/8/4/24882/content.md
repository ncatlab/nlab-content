+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

# Idea

_Adámek's fixed point theorem_ gives a method to construct an [[initial algebra of an endofunctor]] by "iterating" the functor.

## Construction 

This theorem is attributed to [[Jiří Adámek]] but note that the same construction for set-functors already appeared in ([Pohlova,1973](#Pohlova))).

+-- {: .num_theorem #AdameksTheorem }
######Theorem (Ad&#225;mek)

Let $C$ be a category with an [[initial object]] $0$ and [[transfinite composition]] of length $\omega$, hence [[colimits]] of sequences $\omega \to C$ (where $\omega$ is the first infinite [[ordinal]]), and suppose $F: C \to C$ preserves colimits of C$\omega$-chains. Then the colimit $\gamma$ of the chain 

$$0 \overset{i}{\to} F(0) \overset{F(i)}{\to} \ldots \to F^{(n)}(0) \overset{F^{(n)}(i)}{\to} F^{(n+1)}(0) \to \ldots$$ 

carries a structure of initial $F$-algebra. 
=-- 

+-- {: .proof}
###### Proof

The $F$-algebra structure $F\gamma \to \gamma$ is inverse to the canonical map $\gamma \to F\gamma$ out of the colimit (which is invertible by the hypothesis on $F$). The proof of initiality may be extracted by dualizing the corresponding proof given at [[terminal coalgebra]]. 
=--

This approach can be generalized to the [[transfinite construction of free algebras]].

## Related entries

* [[Kleene's fixed point theorem]] is precisely the [[de-categorification]] of this theorem to [[posets]]/[[preorders]].

## References

* {#Pohlova} Věra Pohlová. "On sums in generalized algebraic categories." Czechoslovak Mathematical Journal 23.2 (1973): 235-251. <http://eudml.org/doc/12718>.
* Jiří Adámek. "Free algebras and automata realizations in the language of categories." Commentationes Mathematicae Universitatis Carolinae 15.4 (1974): 589-602.
* Jiří Adámek, Věra Trnková. Automata and algebras in categories. Vol. 37. Springer Science & Business Media, 1990.
## Idea

Curry's paradox is a version of [[Russell's paradox]] that does not involve the use of [[negation]].

Russell's paradox is a proof of [[falsehood]], rendering a certain class of formal systems (those including some kind of unlimited [[axiom of comprehension]]) "inconsistent" in the sense that they prove false, which by the law of [[ex falso quodlibet]] entails that they prove anything at all.  Curry's paradox is a *direct* proof of "anything at all" without the detour through falsehood.  Thus, it applies more generally than Russell's paradox, e.g. to theories lacking a notion of "false", or to [[paraconsistent logic|paraconsistent]] theories whose notion of "false" does not satisfy ex falso quodlibet.

Curry's paradox does, however, still depend on the structural rule of [[contraction rule|contraction]].  Thus, it can be avoided by systems based on [[linear logic]].

## Argument

Let $P$ be any statement at all, and consider the set

$$ C = \{ x \mid (x\in x) \Rightarrow P \}. $$

Then if $C\in C$, by definition we have $(C\in C) \Rightarrow P$, and hence by [[modus ponens]] we have $P$.  Therefore, $(C\in C) \Rightarrow P$.  But by definition this means that $C\in C$, and therefore (as we just proved) $P$.

Note that, if [[negation]] is defined as $\neg P = (P \Rightarrow \bot)$ for some notion of [[falsehood]] $\bot$, then Russell's paradox is the special case of Curry's paradox for $P=\bot$.
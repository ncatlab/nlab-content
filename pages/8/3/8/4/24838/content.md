## Idea

Rule C is a formal analogue in predicate logic of making a (single) choice when reasoning (in a line of logical proof). Thus, if one has a premise that $(\exists x)\phi(x)$ then one introduces a new
constant $b$ ("chosen $x$") and states $\phi(b)$. Then one
continues proof and finally arrives at a new theorem not containing $b$.

A basic metatheorem is that if a theorem not containing such a $b$ is provable with rule $C$ then it is provable without rule $C$, written $P \vdash_C Q$ then $P\vdash Q$.

## Literature

It seems that the rule is introduced in VI.7 of

* [[J. Barkley Rosser]], _Logic for mathematicians_, 1954

and is now more widely known from 2.6 in 

* Elliott Mendelson, _Introduction to mathematical logic_, Chapman and Hall 1964, 1979, 1987, 1997

See also a comment about the proof of the basic metatheorem at 

* math.stackexchange:[confusion-about-steps-of-proof-of-rule-c](https://math.stackexchange.com/questions/4115567/confusion-about-steps-of-proof-of-rule-c)

category: logic
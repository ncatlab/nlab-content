# Weak excluded middle

* table of contents
{: toc}

## Definition

In [[logic]], the principle of **weak excluded middle** says that for any [[proposition]] $P$ we have $\neg P \vee \neg\neg P$.

This follows from the full principle of [[excluded middle]], which says that for any $Q$ we have $Q \vee \neg Q$ (take $Q = \neg P$).  Thus, in [[classical mathematics]] weak excluded middle is just true.  But in [[constructive mathematics]] (i.e. [[intuitionistic logic]]), it is a weaker assumption than full excluded middle.

## Equivalent forms

### De Morgan's Law

In intuitionistic logic, **de Morgan's law** often refers to the one of [[De Morgan duality|de Morgan's four laws]] that is *not* an intuitionistic tautology, namely $\neg (P \wedge Q) \to (\neg P \vee \neg Q)$ for any $P,Q$.

+-- {: .un_theorem}
###### Theorem
De Morgan's law is equivalent to weak excluded middle.
=--
+-- {: .proof}
###### Proof
If de Morgan's law holds, then since $\neg (P \wedge \neg P)$, we have $\neg P \vee \neg\neg P$, as desired.  Conversely, if weak excluded middle holds and we have $\neg (P\wedge Q)$, then from weak excluded middle we get $\neg P \vee \neg\neg P$ and $\neg Q \vee \neg\neg Q$ which give four cases.  In three of those cases $\neg P \vee \neg Q$ holds, while in the fourth we have $\neg\neg P$ and $\neg\neg Q$, which together imply $\neg\neg(P\wedge Q)$, contradicting the assumption of $\neg (P\wedge Q)$; so the fourth case is impossible.
=--

[[!redirects principle of weak excluded middle]]
[[!redirects law of weak excluded middle]]
[[!redirects weak principle of excluded middle]]
[[!redirects weak law of excluded middle]]
[[!redirects weak PEM]]
[[!redirects weak LEM]]

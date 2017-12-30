# Double-negation shift

* table of contents
{:toc}

## Definition

In [[logic]], the principle of **double-negation shift** (**DNS**) is the statement that for any [[predicate]] $P$, the following holds:

$$ (\forall x, \neg\neg P(x)) \to \neg\neg\forall x, P(x). $$

Of course, this is a tautology in [[classical logic]] where [[double negation]] $\neg\neg$ is the identity, but in [[constructive mathematics]] this is not provable (although its [[converse]] is).

It is provable even constructively, though, if the domain of [[quantifier|quantification]] of the variable $x$ is [[finite set|finite]].  In general, the principle of double-negation shift can be considered a property of this domain, which holds automatically for finite sets, and might hold for some other sets but not for others.  Sometimes by "double-negation shift" is meant specifically the version for the domain $\mathbb{N}$ of [[natural numbers]].

## Equivalence to double-negated PEM

The principle of double-negation shift (over arbitrary domains) is equivalent to the double-negation of the universally-quantified principle of [[excluded middle]]:

$$\neg\neg \forall Q, (Q \vee \neg Q). $$

Since $\forall Q, \neg\neg(Q \vee \neg Q)$ is a constructive tautology, the above double-negated PEM follows from DNS with domain $Prop$ and $P(Q) = (Q\vee\neg Q)$.  Conversely, if double-negated PEM holds, then to prove any negated goal like $\neg\neg\forall x, P(x)$ we may assume full PEM, i.e. classical logic, in which case DNS holds.

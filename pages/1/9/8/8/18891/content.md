# Double-negation shift

* table of contents
{:toc}

## Definition

In [[logic]], the principle of **double-negation shift** (**DNS**), also known as the **Kuroda Principle**, is the statement that for any [[predicate]] $P$, the following holds:

$$ (\forall x, \neg\neg P(x)) \to \neg\neg\forall x, P(x). $$

Of course, this is a tautology in [[classical logic]] where [[double negation]] $\neg\neg$ is the identity, but in [[constructive mathematics]] this is not provable (although its [[converse]] is).

It is provable even constructively, though, if the domain of [[quantifier|quantification]] of the variable $x$ is [[finite set|finite]].  In general, the principle of double-negation shift can be considered a property of this domain, which holds automatically for finite sets, and might hold for some other sets but not for others.  Sometimes by "double-negation shift" is meant specifically the version for the domain $\mathbb{N}$ of [[natural numbers]].

## Equivalence to double-negated PEM

The principle of double-negation shift (over arbitrary domains) is equivalent to the double-negation of the universally-quantified principle of [[excluded middle]]:

$$\neg\neg \forall Q:\Omega, (Q \vee \neg Q). $$

Since $\forall Q, \neg\neg(Q \vee \neg Q)$ is a constructive tautology, the above double-negated PEM follows from DNS with domain $Prop$ and $P(Q) = (Q\vee\neg Q)$.  Conversely, if double-negated PEM holds, then to prove any negated goal like $\neg\neg\forall x, P(x)$ we may assume full PEM, i.e. classical logic, in which case DNS holds.

## Validity in toposes

The interpretation of the predicate $(Q : \Omega | Q\vee\neg Q)$ in an elementary topos $\mathcal{E}$ is the subobject $[t,f] : 1+1=2\to\Omega$. Thus, $\neg\neg \forall Q:\Omega, Q \vee \neg Q $ holds in $\mathcal{E}$ precisely if there exists a subterminal $U\to 1$ such that $\neg\neg U \cong\id_1$ and 
$$(*) \qquad\quad (\Omega\times U\to\Omega)\subseteq(2\to\Omega).$$ 
If $\mathcal{E}$ is the topos of sheaves on a locale $X$, the subterminals correspond to the opens of the locale, and $(*)$ holds for an open $U\in O(X)$ precisely if $U\subseteq V\vee\neg V$ for all $V\in O(X)$ with $V\subseteq U$. This means precisely that $U$ is boolean as an open sublocale, so double negation shift holds in ${Sh}(X)$ precisely if $X$ has a dense boolean open sublocale. If $X$ is (the set of opens in) a $T_0$-space, the booleanness condition is equivalent to discreteness, so double negation shift holds in the sheaf topos precisely if $X$ has a dense discrete open subspace. A non-trivial example satisfying $T_2$ is the 1-point compactification of an infinite set, and the real line is a counterexample (since a dense discrete open would be non-empty, and each of its element would be an isolated point, contradicting connectedness of $\mathrm{R}$).

In the case of a *presheaf topos*, say on a small category $\mathrm{C}$, truth values are precisely sieves in $\mathrm{C}$, i.e. sets of objects $U$ such that for every morphism $f: A\to B$, $B\in U$ implies $A\in U$. In this situation, $(*)$ is equivalent to $\mathrm{C}/A\simeq 1$ for all $A\in U$. From this it can be deduced that double negation shift holds in presheaves over $\mathrm{C}$ if and only if for every $A\in\mathrm{C}$ there exists an $f:B\to A$ with $\mathrm{C}/B\simeq 1$.

DNS holds in every Kripke model with finite frame; see [here](https://plato.stanford.edu/entries/logic-intuitionistic/).
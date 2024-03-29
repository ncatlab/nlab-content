
# Contents
* table of contents
{: toc}

## Idea 

**Double negation translation** is a method for converting [[propositions]] [[valid]] in [[classical logic]] into propositions valid in [[intuitionistic logic]]. It can be used to establish relative consistency results. For example, it may be possible to show that the proof of a [[contradiction]] in a classical theory could be translated to the proof of a contradiction in a constructive theory. [[Kurt Gödel]] used this technique to show that [[Peano arithmetic]] and [[Heyting arithmetic]] are equiconsistent.

Double negation translation was discovered independently by a number of mathematicians including [[Kurt Gödel]], [[Gerhard Gentzen]], and [[Andrey Kolmogorov]], and is also called the __G&#246;del--Gentzen negative translation__.


## Construction 

The traditional descriptions are highly syntactic, but can be motivated by recalling some conceptual relationships between [[Boolean algebras]] (which are algebras for classical propositional logic) and [[Heyting algebras]] (which are algebras for intuitionistic propositional logic). 


### Propositional case 

Recall from the article [[Heyting algebra]] that the [[left adjoint]] $F$ to the [[forgetful functor]] 

$$U \colon Bool \to Heyt$$ 

is given objectwise by taking a Heyting algebra $L$ to the poset $L_{\neg\neg}$ of [[regular elements]] $x \in L$, i.e., those that are fixed by [[double negation]]: $x = \neg \neg x$. It was shown that $L_{\neg\neg}$ is a Boolean algebra, and $\neg \neg \colon L \to L_{\neg\neg}$ is a Heyting algebra homomorphism which is universal among Heyting algebra maps $L \to U B$ into Boolean algebras. 

In particular, if $Heyt(S)$ is the free Heyting algebra on a set of [[variables]] $S$, it follows by composing left adjoints 

$$Set \stackrel{free}{\to} Heyt \stackrel{F}{\to} Bool$$ 

that $Heyt(S)_{\neg\neg}$ is the free Boolean algebra on $S$. 

Furthermore, it was shown in [[Heyting algebra]] that for Heyting algebras $L$, 

* $\neg\neg \colon L \to L$ preserves finite [[meets]]; 

* $\neg\neg \colon L \to L$ preserves the [[implication]] operation $\Rightarrow$. 

Consequently, the inclusion of regular elements $L_{\neg\neg} \to L$ also preserves meets and implications, __strictly__. This gives the following result. 

+-- {: .num_thm} 
###### Glivenko's Theorem 
If $p \Rightarrow q$ is a [[tautology]] in classical propositional logic, then $(\neg \neg p) \Rightarrow (\neg \neg q)$ is a tautology in intuitionistic propositional logic, and conversely. 
=-- 

+-- {: .proof} 
###### Proof 
Here $p$ and $q$ are [[term]] expressions in variables $x_i \in S$ over the signature $(0, 1, \vee, \wedge, \Rightarrow)$. To say $p \Rightarrow q$ is a classical tautology means that $1 \leq (p \Rightarrow q)$ holds when interpreted in $Bool(S)$. But since $Bool(S) = Heyt(S)_{\neg\neg}$, this is equivalent to saying that 

$$1 \leq \neg\neg(p \Rightarrow q) = (\neg\neg p) \Rightarrow (\neg\neg q)$$

when interpreted in $Heyt(S)$, which is to say that $(\neg \neg p) \Rightarrow (\neg\neg q)$ is an intuitionistic tautology. 
=-- 

Continuing this thought: the join $\vee$ in $Bool(S) = Heyt_{\neg\neg}$ is computed as 

$$a \vee_{Bool} b = \neg\neg(a \vee_{Heyt} b)$$ 

since $\neg\neg \colon Heyt(S) \to Heyt(S)_{\neg\neg}$ preserves joins (it is a left adjoint). Putting all this together, because $\neg\neg \colon Heyt(S) \to Heyt(S)_{\neg\neg}$ preserves Heyting algebra structure, we arrive at the following syntactic translation. 

+-- {: .un_def #defn}
###### Definition 
The double-negation translation $p \mapsto p^{N}$ on term expressions in the theory of Heyting algebras $L$ is defined by induction as follows. 

* $x^N = \neg\neg x$ for variables $x$. 

* $0^N = 0$ (since $\neg\neg \colon L \to L$ preserves $0$)

* $1^N = 1$ (since $\neg\neg \colon L \to L$ preserves $1$)

* $(p \wedge q)^N = p^N \wedge q^N$ (since $\neg\neg \colon L \to L$ preserves the meet operation) 

* $(p \Rightarrow q)^N = p^N \Rightarrow q^N$ (since $\neg\neg \colon L \to L$ preserves the implication operation)

* $(p \vee q)^N = \neg\neg(p^N \vee q^N)$. 
=-- 

Thus, by Glivenko's theorem, $p$ is a classical tautology if and only if $p^N$ is an intuitionistic tautology. This result may be extended to theories as well: suppose $L$ is an intuitionistic theory or Heyting algebra, given by a presentation as a coequalizer in $Heyt$: 

$$Heyt(T) \stackrel{\to}{\to} Heyt(S) \to L.$$ 

Then, since the functor $L \mapsto L_{\neg\neg}$ is a left adjoint, it takes this coequalizer to a coequalizer 

$$Bool(T) \stackrel{\to}{\to} Bool(S) \to L_{\neg\neg}$$ 

so that an term expression $p$ is a theorem in the classical theory $L_{\neg\neg}$ if and only if $p^N$ is a theorem in the intuitionistic theory $L$. 


### First-order case 

Double negation translation for a formula, $\phi$, of a [[first-order language]] is defined inductively by the following clauses:

* $\phi^N = \neg \neg \phi$, for atomic $\phi$.

* $(\phi \wedge \psi)^N = \phi^N \wedge \psi^N$.

* $(\phi \vee \psi)^N = \neg(\neg \phi^N \wedge \neg \psi^N)$ (or equivalently, $\neg \neg (\phi^N \vee \psi^N)$)

* $(\phi \to \psi)^N = \phi^N \to \psi^N$.

* $(\neg \phi)^N = \neg \phi^N$.

* $(\forall x \phi)^N = \forall x \phi^N$.

* $(\exists x \phi)^N = \neg \forall x \neg \phi^N$ (or equivalently, $\neg \neg \exists x \phi^N$).


### Higher-order case

The basic idea here is that any [[topos]] $E$ gives rise to a [[Boolean topos]] $E_{\neg\neg}$.


## References

Informal exposition of a tiny aspect of this double negation business is in 

* [[Andrej Bauer]], _[Intuitionistic mathematics for physics](http://math.andrej.com/2008/08/13/intuitionistic-mathematics-for-physics/)_, 2008

[[!redirects double negation translation]]
[[!redirects double negation translations]]
[[!redirects double-negation translation]]
[[!redirects double-negation translations]]
[[!redirects negative translation]]
[[!redirects negative translations]]

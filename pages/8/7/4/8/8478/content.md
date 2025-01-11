
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Sequent#
* table of contents
{:toc}


## Idea

In formal [[logic]] a _sequent_ ([Gentzen 35](#Gentzen), [Martin-L&#246;f 83](#Martin-L&#246;f)) or _hypothetical judgement_ ([Pfenning, Davies 00](Pfenning-Davies)) is an expression in the [[metalanguage]] 
which is a string of symbols of the form

$$
  Antecedent \vdash Succedent
$$

where 

1. $Antecedent$ are symbols indicating [[judgements]] called the _[[antecedents]]_ or _[[context]]_, 

1. $Succedent$ are symbols indicating [[judgements]] called the _[[succedents]]_ or (if it is just a single judgement) the _[[consequent]]_

1. the **consequence sign** or **turnstile**-symbol "$\vdash$" expresses that $Succedent$ is a _consequence_ of $Antecedent$:

   " $Antecedent$ yields $Succedent$."

   or

   "With $Antecedent$ the $Succedent$ can be [[proof|proven]]."

   or

   "$Antecedent$, con-sequent-ly $Succedent$."

   Or similar. 

Historically the "consequence" here was early on transmuted to "sequenz" ([Gentzen](#Gentzen)) and then later to "sequent". See the section _[History](#History)_ below.

In systems of [[formal logic]] such as [[natural deduction]]/[[type theory]] such sequents express rules for explicit _symbol manipulation_ admitted in the system rather than formal [[implications]] _within_ the system. The latter instead are expressed by [[terms]] of [[function type]] $t : \phi \to \psi$. But the [[term introduction rule]] for terms of function types say that given one, one is allowed to get the other.

Typically one allows a list of expressions on both sides of the turnstile-symbols as in

$$
 Antec_1, \cdots, Antec_k \vdash Succ_1, \cdot, Succ_l
$$

often abbreviated as

$$
  \vec Antec \vdash \vec Succ
$$

in which case on the left a [[conjunction]] of the [[antecedents]] and on the right a [[disjunction]] of [[succedents]] is understood, as in

"If $Antec_1$ and $Antec_2$... are given then one of $Succ_1, \cdots, Succ_l$ is a consequence".

An **[[intuitionistic logic|intuitionistic]] sequent** has at most one succedent, which is then called the **[[consequent]]**.  Often "intuitionistic sequent" is used to mean one with *exactly* one succedent, although technically it would make more sense to call those [[minimal logic|minimal]] sequents.

Another variant is that in some frameworks the [[antecedent]] and [[succedent]] displayed are required to be [[propositions]] and the [[free variables]] of the [[context]] are instead displayed beneath the turnstile as in 

$$
  \vec \phi(x)\, true \vdash_{\vec x} \vec \psi(x) \, true
  \,.
$$

If the framework regards [[propositions as types]] then this is the same as writing

$$
  \vec x. \vec \phi(x) \vdash \vec \psi(x)
  \,.
$$

Finally one can of course consider sequences of sequents

$$
  (\Gamma_1 \vdash \Delta_1), \cdots, (\Gamma_n \vdash \Delta_n)
$$

and if these are read [[disjunction|disjunctively]] it is like a higher-order sequent without [[antecedent]] and called a *[[hypersequent]]*.

Rules for formal manipulation of sequents are called _[[sequent calculi]]_ or _[[deduction calculi]]_. See there for more details.

## Definition

The precise nature of sequents has been formalized differently in different systems of [[formal logic]]. We discuss a few

### Intuitionistic sequents

(...) ([Martin-L&#246;f](#Martin-L&#246;f)) (...)

### Gentzen's sequents

(...) ([Gentzen](#Gentzen)) (...)

### Sequents in focalized calculi

(...) [Simmons](#Simmons) (...)

## Semantics

We discuss aspects of the [[categorical semantics]] of sequents, hence their interpretation when the ambient formal logic is regarded as the [[internal language]] of a [[category]].

### In homotopy type theory

Under the [[categorical semantics]] of [[homotopy type theory]]
sequents in the type theory pretty accurately correspond to 
[[morphisms]] in the [[(∞,1)-topos]]. We indicate how this works, first for type declarations, then for terms of [[dependent types]].

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Write $Type \in \mathbf{H}$ for the [[universe in a topos|internal universe]] of  [[small objects]] of $\mathbf{H}$, called the _[[object classifier]]_. 

This is defined as the [[representable functor|representing object]]
for the [[core]] of the [[small object|small]] [[codomain fibration]], exhibited by an  [[equivalence of ∞-groupoids]]

$$
  name
  :
  Core(\mathbf{H}_{/X})^{small} \stackrel{\simeq}{\to} \mathbf{H}(X,Type)
  \,.
$$

This equivalence sends an $X$-family $(E \to X) \in \mathbf{H}_{/X}$ to its "name", denoted

$$
  X \stackrel{\vdash E}{\to} Type
  \,,
$$

which is the morphism characterized by fitting into an
[[(∞,1)-pullback|∞-pullback]] square of the form

$$
  \array{
     E &\to& \widehat{Type}
     \\
     \downarrow &\swArrow& \downarrow
     \\
     X &\underset{\vdash E}{\to}& Type
  }
  \,,
$$

If here we simply replace, notationally, the arrow "$\to$" by the turnstile "$\vdash$", display a generic [[generalized element]] $x$ of $X$ and then write $E(x)$ to highlight the dependence of the [[fibers]] of $E$ on $x$ in $X$, then the symbols "$X \stackrel{\vdash E}{\to} Type$" become the 
sequent "$x : X \vdash E(x) : Type$".
This sequent is the [[syntax]] of which the morphism is the [[categorical semantics]]. 

Similarly, if $X \stackrel{t}{\to}_X E$
is a [[section]] of $E$ over $X$, hence 
a [[generalized element]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/X}$,
then by replacing the arrow-symbol by a
 turnstile-symbol we get "$x : X \vdash t(x) : E(x)$".
This is the sequent for the [[term]] $t$ of the [[dependent type]] $E$.

In summary we have under the [[relation between category theory and type theory]] the notational correspondence:

**morphisms to sequents.**

| $\,$ | [[types]] | [[terms]] |
|--|--|--|
| [[(∞,1)-topos theory|∞-topos theory]] | $\;\;\;\;X \stackrel{\vdash \;\;\;\;E}{\to} \;\;\Type$ | $\;\;\;\;X \stackrel{\vdash \;\;\;t}{\to} {}_X \;\;E$ |
|[[homotopy type theory]] | $x : X \vdash E(x) : Type$ | $x : X \vdash t(x) : E(x) $ |


## History
 {#History}

The notion of sequent was introduced in section 2.3 of ([Gentzen 1935](#Gentzen)) (called _Sequenz_ there). In ([Martin-L&#246;f 1984, pages 29-30](#Martin-L&#246;f)) it says

> The forms of hypothetical judgement $[$ have $]$ the form

>$A_1 true, \cdots, A_n true \vdash A prop$

>which says that $A$ is a proposition under the assumptions that $A_1, \cdots, A_n$ are all true, and, on the other hand, the form

> $A_1 true, \cdots, A_n true \vdash A true$

> which says that the proposition A is true under the assumptions that $A_1, \cdots, A_n$ are all true. Here I am using the vertical bar for the relation of logical consequence, that is, for what Gentzen expressed by means of the arrow $\to$ in his sequence calculus, and for which the double arrow $\Rightarrow$ is also a common notation. It is the relation of logical consequence, which must be carefully distinguished from implication. What stands to the left of the consequence sign, we call the hypotheses, in which case what follows the consequence sign is called the thesis, or we call the **judgements that precede the consequence sign** the antecedents and the **judgement that follows after the consequence sign** the consequent. This is the terminology which Gentzen took over from the scholastics, except that, for some reason, he changed consequent into succedent and consequence into sequence, Ger. Sequenz, usually improperly rendered by sequent in English.


## Related concepts

* [[sequent calculus]]

* [[cut rule]]

[[!include logic symbols -- table]]

## References

In Section 2.3 of

* [[Gerhard Gentzen]], _Untersuchungen &#252;ber das logische Schließen I_, Mathematische Zeitschrift 39:1 (1935). [doi](https://doi.org/10.1007/BF01201353).
 {#Gentzen}

what today is called a _sequent_ is introduced under _Sequenz_ (Ger: _sequence_), apparently derived from _Konsequenz_ (Ger: _consequence_) and denoted by a single arrow "$\to$". 

In the lectures 

* {#Martin-L&#246;f83}
 [[Per Martin-Löf]]: *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[[MartinLofOnTheMeaning96.pdf:file]]&rbrack;
 

where the author provides a modern foundation for logic based on a clear separation of the notions of [[judgment]] and [[proposition]] (see at [[Martin-Löf dependent type theory]]) the author says (pages 29-30) that "the forms of hypothetical judgements that I shall need" are [[Gentzen]]'s sequents without the symmetry between [[antecedent]] and [[succedent]] that Gentzen used.

Referring explicitly to these lectures, these are are then just called _hypothetical judgements_ in section 3 of

* [[Frank Pfenning]], Rowan Davies, _A judgemental reconstruction of modal logic_ (2000) ([pdf](http://www.cs.cmu.edu/~fp/papers/mscs00.pdf))
 {#Pfenning-Davies}

In section D1.1 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ 

sequents are introduced in the context of a basic introduction to [[formal logic]]. There the the notation $\phi \vdash_{\vec c} \psi$ is used where $\phi$ is required to be a [[proposition]] and the [[context]] [[variables]] $\vec x$ are typeset below the turnstile. From the [[categorical semantics]] in section D1.2 it is clear that in the sense of [[dependent type theory]] these variables are to stand to the left of the turnstile.

See also 

* Robert J. Simmons, _Structural focalization_ ([arXiv:1109.6273](http://arxiv.org/abs/1109.6273))
 {#Simmons}

[[!redirects sequents]]

[[!redirects turnstile]]

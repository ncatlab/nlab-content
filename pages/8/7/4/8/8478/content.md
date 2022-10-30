
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In formal [[logic]] a _sequent_ is an expression in the metalanguage 
which is a string of symbols of the form

$$
  Ctxt \vdash Jdgmt
$$

where 

1. $Ctxt$ are symbols indicating a [[judgement]] called the _[[context]]_ or the _[[antecedent]]_, 

1. $Jdgmt$ are symbols indicating a [[judgement]] calld the _[[succedent]]_

1. the **consequence sign** or **turnstile**-symbol "$\vdash$" expresses that $Jdgmt$ is a _consequence_ of $Ctxt$

   " $Ctxt$ yields $Jdgmt$."

   or

   "In $Ctxt$ the $Jdgmt$ can be proven."

   or

   "$Ctxt$, con-sequent-ly $Jdgmt$."

   Or similar. 

Historically the "consequence" here was early on transmuted to "sequenz" ([Gentzen](#Gentzen)) and then later to "sequent". See the section _[History](#History)_ below.

In systems of [[formal logic]] such as [[natural deduction]]/[[type theory]] such sequents express rules for explicit _symbol manipulation_ admitted in the system rather than formal implications _within_ the system, which instead are expressed by [[terms]] of [[function type]] $t : \phi \to \psi$. But the [[term introduction rule]] for terms of function types say that given one, one is allowed to get the other.



## Semantics

We discuss aspects of the [[categorical semantics]] of sequents, hence their interpretation when the ambient formal logic is regarded as the [[internal language]] of a [[category]].

### In homotopy type theory

Under the [[categorical semantics]] of [[homotopy type theory]]
sequents in the type theory pretty accurately corrsepond to 
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

## References

In section 2.3

* [[Gerhard Gentzen]]  _Untersuchungen &#252;ber das logische Schlie&#223;en I_ _Mathematische Zeitschrift_ 39(1), Springer-Verlag 1935. &lt;http://dx.doi.org/10.1007/BF01201353>.
 {#Gentzen}

what today is called a _sequent_ is introduced under _Sequenz_ (Ger: _sequence_), apparently derived from _Konsequenz_ (Ger: _consequence_) and denoted by a single arrow "$\to$". 

A historical remark on how this turned into the modern _sequents_ is on pages 29-30 of

* [[Per Martin-Löf]], _On the meaning of logical constants and the justifications of the logical laws_, leture series in Siena (1983) ([web](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))
 {#Martin-L&#246;f83}



[[!redirects sequents]]

[[!redirects turnstile]]

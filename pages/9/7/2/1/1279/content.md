
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Sequent calculus
* table of contents
{: toc}

## Idea

A sequent calculus is a [[deductive system]] for [[predicate logic]] (or something similar) in which the basic [[judgment]] is a [[sequent]]
$$ \phi_1, \phi_2, \ldots \vdash \psi_1, \psi_2, \ldots ,$$
expressing the idea that some statement $\psi_i$ must be true if every statement $\phi_i$ is true.  The original sequent calculi were developed by [[Gerhard Gentzen]] in 1933 building on anticipatory ideas by [[Paul Hertz]].

A central property of sequent calculi, which distinguishes them from systems of [[natural deduction]], is that it allows an easier analysis of proofs: the [subformula property](#subformulaprop) that it enjoys allows easy [[induction]] over proof-steps. The reason is roughly that, using the language of [[natural deduction]], in sequent calculus "every rule is an [[introduction rule]]" which introduces a term on _either_ side of a [[sequent]] with no [[elimination rules]]. This means that working backward every "un-application" of such a rule makes the sequent necessarily simpler.


## Definitions

We will start with an arbitrary [[signature (in logic)|signature]] $\Sigma$; the simplest case (for [[propositional logic]]) uses the empty signature (with no [[types]]).  We will assume unlimited [[variables]] for [[propositions]] and unlimited variables for each type.

+-- {: .num_remark}
###### Warning

We will be defining several terms below; but keep in mind that these are definitions *for sequent calculus*, since these terms may also be used more generally.
=--

+-- {: .num_defn}
###### Definition

A __[[context]]__ over $\Sigma$ is a (finite) [[list]] $\vec{x}\colon \vec{T}$ or
$$ x_1\colon T_1, x_2\colon T_2, \ldots ,$$
where the $x_i$ are [[variables]] and the $T_i$ are (formulas for) [[types]] over $\Sigma$.
=--

For the empty signature, the only context is empty; if $\Sigma$ consists of a single type, then a context is effectively a list of variables.

+-- {: .num_defn}
###### Definition

Given a context $\Gamma$ over $\Sigma$, a __cedent__ in $\Gamma$ over $\Sigma$ is simply a [[list]] $\vec{\phi}$ or
$$ \phi_1, \phi_2, \ldots $$
of (formulas for) [[propositions]] in $\Gamma$ over $\Sigma$.
=--

(Recall that a proposition in the context $\Gamma$ allows the variables introduced by $\Gamma$, but no others, to be free variables.  Such a proposition in context is also called a [[predicate]].)

+-- {: .num_defn}
###### Definition

A __sequent__ over $\Sigma$ consists of a context $\Gamma$ over $\Sigma$ and two cedents in $\Gamma$, called the __[[antecedent]]__ and the __[[succedent]]__.  This is written
$$ \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi} ,$$
where $\vec{x}\colon \vec{T}$ is the context $\Gamma$, with the antecedent on the left and the succedent on the right.
=--

+-- {: .num_remark}
###### Warnings

If $\Sigma$ has a single type (a so-called 'untyped' signature) and one tacitly assumes that the single type is [[inhabited type|inhabited]], then one may (up to equivalence in a certain sense) reconstruct the context of any sequent from the cedents, by examining which variables appear; this is even possible if $\Sigma$ has more than one type (all assumed inhabited), although more difficult if certain abuses of notation are used.  Then the context can be ignored.  This is not really the right way to do things, but (especially for untyped signatures) it is traditional.

Confusingly, the cedents are sometimes also called 'contexts'; then one speaks of the __left context__ (the antecedent), the __right context__ (the succedent).  This is most easily done when ingoring what we have been calling the context; I\'m not even sure what term would then be used for that context (maybe the __type context__?).  See also also the [interpretation of sequents as hypothetical judgements](sequent#Gentzen2MartinLof) (which I hope to write soon), which shows how the type context, antecedent, and succedent are all used to form the context of a related [[hypothetical judgement]].

One also sometimes uses 'antecedent' or 'succedent' for an *individual* proposition on the relevant side of the sequent; see also the use of 'consequent' in [minimal sequents](#minimaletc) below.
=--

+-- {: .num_defn}
###### Definition

A __[[theory]]__ over $\Sigma$ is an arbitrary [[subset|set]] of sequents over $\Sigma$, called the __[[axioms]]__ of the theory.
=--

We will explain below how the sequent calculus may be used to prove [[theorems]] from the axioms; each theorem will also be a sequent.

We may also consider particular kinds of sequents or theories, by form or content.

+-- {: .num_defn #minimaletc}
###### Definitions (by form)

A __closed sequent__ is one in which the context is empty; a __closed theory__ is one in which every sequent is closed.

An __intuitionistic sequent__ is one in which the succedent consists of at most one proposition; an __intuitionistic theory__ is one in which every sequent is intuitionistic.

A __minimal sequent__ is one in which the succedent consists of exactly one proposition (then called the __[[consequent]]__); a __minimal theory__ is one in which every sequent is minimal.

A __dual-intuitionistic sequent__ is one in which the antecedent consists of at most one proposition; a __dual-intuitionistic theory__ is one in which every sequent is dual-intuitionistic.
Who will be sworn in as POTUS on 01
A __dual-minimal sequent__ is one in which the antecedent consists of exactly one proposition; a __dual-minimal theory__ is one in which every sequent is dual-minimal.

A __classical sequent__ is simply a sequent, emphasising that we are not restricting to (dual)-intuitionistic or (dual)-minimal sequents; similarly, a __classical theory__ is any theory.
=--

These (except the first) are so-called because of their relationship to [[intuitionistic logic]], [[minimal logic]], [[classical logic]], etc.  Any of these [[logics]] may be presented using any sort of sequent, but Gentzen\'s original sequent calculi presented each logic using only corresponding sequents.

+-- {: .num_defn}
###### Definitions (by content)

A __regular sequent__ is one in which every proposition is given by a formula in [[regular logic]]; a __regular theory__ is one in which every sequent is regular.

A __coherent sequent__ is one in which every proposition is given by a formula in [[coherent logic]]; a __coherent theory__ is one in which every sequent is coherent.
=--

Obviously, this list could be continued.


## Rules of proof

The basic building blocks of a proof in sequent calculus are **[[rule of inference|inference rules]]** or **rewrite rules**, which are rules for inferring the validity of certain sequents from other sequents.  One writes

$$
  \frac{\vec{\sigma}}{\tau}
$$

where $\vec{\sigma}$ is a (possibly empty) [[list]] of sequents and $\tau$ is a single sequent, to indicate that from the validity of the sequents in $\vec{\sigma}$ that of $\tau$ may be inferred, or that $\vec{\sigma}$ may be _rewritten_ to $\tau$.

A **[[deduction|derivation]]** or **proof tree** is a compound of rewrite rules, such as

$$
  \frac{\frac{\sigma_1 \;\; \sigma_2}{\sigma_3} \;\; \sigma_4 }{\sigma_5}
  \,.
$$

We will give the rules in several classes.

+-- {: .num_defn}
###### Rules (structural rules)

The **[[identity rule]]** is
  $$
    \frac{}{\alpha \vdash_{\vec{x}\colon \vec{T}} \alpha}
     \,,
  $$
stating that, in any context $\Gamma$, any proposition in $\Gamma$ follows from itself, always.

The **[[substitution rule]]** is
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}
    }{
      \vec{\phi}[\vec{s}/\vec{x}] \vdash_{\vec{y}\colon \vec{U}} \psi[\vec{s}/\vec{x}]
    }
    \,,
  $$
or
  $$
    \frac{
      \vec{\phi} \vdash_{\Gamma} \vec{\psi}
    }{
      a^*\vec{\phi} \vdash_{\Delta} a^*\vec{\psi}
    }
    \,,
  $$
  where $a$ is any [[interpretation]] of $\Gamma$ in $\Delta$.  Explicitly, such an interpretation is a list $\vec{s}$ of [[terms]] (of the same length as the list which is the context $\Gamma$), where each term $s_i$ is a term over $\Sigma$ of type $T_i$ in the context $\Delta$.  Then $a^*\phi$, or $\phi[\vec{s}/\vec{x}]$, is obtained from $\phi$ by substituting each $s_i$ for the corresponding $x_i$, and $a^*\vec{\phi}$ (and $a^*\vec{\psi}$) are obtained by applying this substitution to every proposition in the list.  Of course, this rule is vacuous if $\Sigma$ has no terms.

The **[[cut rule]]** is
  $$
    \frac{
      (\vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha) \;\;\; (\alpha, \vec{\chi} \vdash_{\vec{x}\colon \vec{T}} \vec{\omega})
    }{
      \vec{\phi}, \vec{\chi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \vec{\omega}
   }\,;
  $$
the proposition $\alpha$ has been 'cut'.

The __[[exchange rules]]__ are
  $$
    \frac{
      \vec{\phi}, \alpha, \beta, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}, \vec{\omega}
    }{
      \vec{\phi}, \beta, \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}, \vec{\omega}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi}, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}, \alpha, \beta, \vec{\omega}
    }{
      \vec{\phi}, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}, \beta, \alpha, \vec{\omega}
    }
    \,;
  $$
more generally, we may apply any [[permutation]] of the antecedent and succedent (because every permutation is a [[composite]] of [[transposition]]s).

The __[[weakening rules]]__ are
  $$
    \frac{
      \vec{\phi}, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }{
      \vec{\phi}, \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \vec{\chi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha, \vec{\chi}
    }
    \,;
  $$
more generally, we may insert any sequence of propositions anywhere in the antecedent and succedent.

The __[[contraction rules]]__ are
  $$
    \frac{
      \vec{\phi}, \alpha, \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }{
      \vec{\phi}, \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
  $$
and
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha, \alpha, \vec{\chi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha, \vec{\chi}
    }
    \,;
  $$
in the absence of the exchange rule, it is important that we can remove duplications only one proposition at a time (as shown here) and only if they are adjacent (as shown here).
=--

Some or all of these rules may be dropped in a [[substructural logic]].  However, even so, the first three rules can generally be proved (except for the identity rule for atomic propositions); see [[cut elimination]].

+-- {: .num_defn }
###### Rules (logical rules)

The **[[truth]] rule** is
  $$
    \frac{
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \top, \vec{\chi}
    }
    \,;
  $$
that is, any sequent is valid if the necessarily true statement is in the succedent.

[[de Morgan duality|Dually]], the **[[falsehood]] rule** is
  $$
    \frac{
    }{
      \vec{\phi}, \bot, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,;
  $$
that is, any sequent is valid if the necessarily false statement is in the antecedent.

The **binary [[conjunction]] rules** are
  $$
    \frac{
      \vec{\phi}, \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }{
      \vec{\phi}, \alpha \wedge \beta, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi}, \beta, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }{
      \vec{\phi}, \alpha \wedge \beta, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,
  $$
on the left and
  $$
    \frac{
      (\vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha, \vec{\chi})
        \;\;\;
      (\vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \beta, \vec{\chi})
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha \wedge \beta, \vec{\chi}
    }
    \,
  $$
on the right.

Dually, the **binary [[disjunction]] rules** are
  $$
    \frac{
      (\vec{\phi}, \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi})
        \;\;\;
      (\vec{\phi}, \beta, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi})
    }{
      \vec{\phi}, \alpha \vee \beta, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,
  $$
on the left and
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha, \vec{\chi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha \vee \beta, \vec{\chi}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \beta, \vec{\chi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha \vee \beta, \vec{\chi}
    }
    \,
  $$
on the right.

The **[[negation]] rules** are
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \alpha, \vec{\psi}
    }{
      \vec{\phi}, \neg{\alpha} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi}, \alpha \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \neg{\alpha}, \vec{\psi}
    }
    \,;
  $$
in other words, a proposition may be moved to the other side if it is replaced by its negation.

The **[[conditional]] rules** are
  $$
    \frac{
      (\vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \alpha)
        \;\;\;
      (\beta \vdash_{\vec{x}\colon \vec{T}} \vec{\psi})
    }{
      \vec{\phi}, \alpha \to \beta \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi}, \alpha \vdash_{\vec{x}\colon \vec{T}} \beta, \vec{\psi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \alpha \to \beta, \vec{\psi}
    }
    \,.
  $$

Dually, the **[[relative complement]] rules** are
  $$
    \frac{
      \vec{\phi}, \alpha \vdash_{\vec{x}\colon \vec{T}} \beta, \vec{\psi}
    }{
      \vec{\phi}, \alpha \setminus \beta \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}
    }
    \,
  $$
and
  $$
    \frac{
      (\vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \alpha)
        \;\;\;
      (\beta \vdash_{\vec{x}\colon \vec{T}} \vec{\psi})
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \alpha \setminus \beta, \vec{\psi}
    }
    \,.
  $$

The **[[equality]] rules** are
  $$
    \frac{
      (\vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \alpha[s/y])
        \;\;\;
      (\alpha[t/y] \vdash_{\vec{x}\colon \vec{T}} \vec{\psi})
    }{
      \vec{\phi}, (s = t) \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}
    }
    \,,
  $$
where $s$ and $t$ are any [[terms]] of the same [[type]] $U$ in the context $\vec{x}\colon \vec{T}$ and $\alpha$ is a proposition in the context $(\vec{x}\colon \vec{T}, y\colon U)$, and
  $$
    \frac{
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, (s = s)
    }
    \,,
  $$
where $s$ is any [[term]] of any type in the context $\vec{x}\colon \vec{T}$.

One could (but rarely does) introduce dual [[apartness]] rules.

The **[[universal quantification]] rules** are
  $$
    \frac{
      \vec{\phi}, \alpha[s/y], \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }{
      \vec{\phi}, \forall(y\colon U) \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,,
  $$
where $s$ is a term of type $U$ in the context $\vec{x}\colon \vec{T}$ and $\alpha$ is a proposition in the [[extended context]] $(\vec{x}\colon \vec{T}, y\colon U)$, and
  $$
    \frac{
      \vec{\phi}[\hat{y}] \vdash_{\vec{x}\colon \vec{T}, y\colon U} \vec{\psi}[\hat{y}], \alpha, \vec{\chi}[\hat{y}]
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \forall(y\colon U) \alpha, \vec{\chi}
    }
    \,,
  $$
where $\phi[\hat{y}]$ is the proposition in the context $(\vec{x}\colon \vec{T}, y\colon U)$ produced by [[weakening rule|weakening]] (in the type context) the proposition $\phi$ in the context $\vec{x}\colon \vec{T}$ (and similarly for a list of propositions).

Dually, the **[[existential quantification]] rules** are
  $$
    \frac{
      \vec{\phi}[\hat{y}], \alpha, \vec{\psi}[\hat{y}] \vdash_{\vec{x}\colon \vec{T}, y\colon U} \vec{\chi}[\hat{y}]
    }{
      \vec{\phi}, \exists(y\colon U) \alpha, \vec{\psi} \vdash_{\vec{x}\colon \vec{T}} \vec{\chi}
    }
    \,
  $$
and
  $$
    \frac{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \alpha[s/y], \vec{\chi}
    }{
      \vec{\phi} \vdash_{\vec{x}\colon \vec{T}} \vec{\psi}, \exists(y\colon U) \alpha, \vec{\chi}
    }
    \,.
  $$
=--

We have written the rules _additively_, which works best when using (dual)-intuitionistic or (dual)-minimal sequents, but it is also possible to write them in a slightly different _multiplicative_ manner.  This makes a difference if some of the [[weakening rule]] and [[contraction rule]] are abandoned; [[linear logic]] uses both rules but for different connectives.  Similarly, we have written the rules to apply as much as possible without the [[exchange rule]], but the remaining asymmetries (in the rules for $\neg$, $\to$, $\setminus$, and $=$) mean that these diverge into left and right operations in [[noncommutative logic]].  (Compare the difference between [[left duals]] and [[right duals]] in a non-[[symmetric monoidal category|symmetric]] [[monoidal category]].)

Gentzen originally did not include $\top$ or $\bot$, but if $\top$ is defined as $\alpha \to \alpha$ for any atomic $\alpha$ and $\bot$ is defined as $\neg{\top}$, then their rules can be proved.  Similarly, he did not use $\setminus$; we may define $\alpha \setminus \beta$ to mean $\alpha \wedge \neg{\beta}$.  It would also be possible to leave out $\to$, defining $\alpha \to \beta$ as $\neg{\alpha} \vee \beta$.  With or without these optional operations and rules, the resulting logic is [[classical logic|classical]].

If we use only those rules that can be stated using intuitionistic sequents, then the result is [[intuitionistic logic]]; this is again true with or without $\top$, $\bot$, or $\setminus$.  However, if we leave out $\to$, then we cannot reconstruct it; the definition of $\to$ using $\neg$ and $\vee$ is not valid intuitionistically.  On the other hand, if we include $\bot$ (and optionally $\top$) but leave out $\neg$ and $\setminus$, then we get intuitionistic logic using all (classical) sequents except the right conditional rule, which must remain intuitionistic.  (Conversely, we could get classical logic using only intuitionistic sequents and adding the law of [[excluded middle]] as an axiom.)

If we use only those rules that can be stated using minimal sequents (so necessarily leaving out $\setminus$), then the result is still intuitionistic logic; but if we also leave out $\bot$, then the result is [[minimal logic]].  Dual results hold for dual-intuitionistic and dual-minimal sequents.


## Cut-free proofs
{#subformulaprop}

The [[cut rule]] expresses the composition of proofs.  Gentzen's main result ([Gentzen, Haupsatz](#Gentzen)) is that any derivation that uses the cut rule can be transformed into one that doesn't -- the _[[cut-elimination theorem]]_.  This yields a [[normalization]] algorithm for proofs, which provided much of the inspiration behind [[Lambek]]'s approach to categorical logic.  Similarly, any derivation that uses the identity rule can be transformed into one that uses it only for atomic propositions (those provided by the signature $\Sigma$ and equality).

The most important property of cut-free proofs is that every formula occurring anywhere in a proof is a subformula of a formula contained in the conclusion of the proof (the [[subformula property]]).  This makes induction over proof-trees much more straightforward than with [[natural deduction]] or other systems.

See [[cut elimination]].


## Related entries

* [[natural deduction]]

* [[cut rule]]

* [[Paul Hertz]]

## References

For the basic definition of bi-minimal sequents see for instance def. D1.1.5 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

and section D1.3 for sequent calculus.

Sequent calculus was introduced by Gerhard Gentzen in his 1933 thesis 

* [[Gerhard Gentzen]]  _Untersuchungen &#252;ber das logische Schlie&#223;en I_ _Mathematische Zeitschrift_ 39(1), Springer-Verlag 1935. &lt;http://dx.doi.org/10.1007/BF01201353>.
 {#Gentzen}

as a formal system for studying the properties of proof systems presented in the style of [[natural deduction]] (also introduced by Gentzen).  It has since been widely adopted over natural deduction in [[proof theory]].


The article

* Wikipedia, _[Sequent calculus](http://en.wikipedia.org/wiki/Sequent_calculus)_

provides a good summary.  So does

* [Sequent Calculus Primer](http://sakharov.net/sequent.html)

In 

* St&#233;phane Lengrand,  Roy Dyckhoff, James McKinna, _A Sequent Calculus for Type Theory_ ([inria](http://hal.inria.fr/hal-00150286/), [pdf](http://138.251.206.45/~rd/publications/42070441.pdf))

is discussion of a sequent calculus for [[type theory]].


[[!redirects sequent calculus]]
[[!redirects sequent calculi]]
[[!redirects sequent calculuses]]


# Quantifiers
* table of contents
{: toc}

## Idea

A quantifier is an operation in [[logic]] that moves a statement from one [[context]] to a related context.

## Definitions

### Quantification in first-order logic

In [[first-order logic]], we have two basic quantifiers, each of which moves a [[predicate]] on one type to a [[proposition]] (a predicate on no types), or more generally moves a predicate on $n + 1$ types to a predicate on $n$ types.

Given a predicate $P$ on a type $T$, the __[[universal quantification]]__ of $P$, denoted $\forall\, x\colon T, P(x)$ (and with many variations in punctuation), is intended to be [[true]] if and only if $P(a)$ is true for every possible element $a$ of $T$.  Similarly, the __[[existential quantification]]__ of $P$ (also called its __particular quantification__), denoted $\exists\, x\colon T, P(x)$, is intended to be true if and only if $P(a)$ is true for at least one element $a$ of $T$.  However, it is quite possible that $P(a)$ may be provable (in a given context $\Gamma$) for every *term* $a$ of type $T$ that *can actually be constructed* (in $\Gamma$), yet $\forall\, x\colon T, P(x)$ cannot be proved; conversely, it is quite possible that $\exists\, x\colon T, P(x)$ can be proved (in a given context) but $P(a)$ cannot be proved for any term $a$ of type $T$ that can actually be constructed.

Therefore, we must define the quantifiers more carefully; one way to do this is as follows:

*  $Q \vdash_{\Gamma}\forall\, x\colon T, P(x)$ if and only if $Q \vdash_{\Gamma, x\colon T} P(x)$;
*  $\exists\, x\colon T, P(x) \vdash_{\Gamma} Q$ if and only if $P(x) \vdash_{\Gamma, x\colon T} Q$.

Here, $\Gamma$ is an arbitrary context, and $\Gamma, x\colon T$ is that context supplemented by a free variable $x$ of type $T$.  Note that $Q$ is (a priori) a statement in the context $\Gamma$ but also needs to make sense in the context $\Gamma, x\colon T$; therefore, our logic needs an appropriate [[weakening rule]] for this to make sense.  This definition also presumes that a statement (in any given context) can be identified precisely by placing it within the [[poset]] of statements (in that context) under entailment ($\vdash$), which is true for ordinary first-order logic.

From this definition, one can derive rules for the quantifiers in [[sequent calculus]] and [[natural deduction]].


### Quantification in first-order logic with equality

If all of our types have an [[equality predicate]], then we can construct some fancier quantifiers.

Given a predicate $P$ on a type $T$ with equality, the __[[uniqueness quantifier]]__ of $P$, denoted $\exists!\, x\colon T, P(x)$, may defined in terms of the universal and existential quantifiers as

$$ \exists!\, x\colon T, P(x) \;\equiv\; \exists\, x\colon T, P(x) \wedge \forall\, y\colon T, P(y) \Rightarrow (x = y) .$$

The intended interpretation is that $\exists!\, x\colon T, P(x)$ is true iff $P(a)$ is true for *exactly* one element $a$ of $T$.

Given a natural number $n$, we can similarly write down quantifiers to say that $P$ holds for exactly $n$ elements, at most $n$ elements, at least $n$ elements, etc. (These all require [[negation]] and therefore there are some slight variations possible when using [[intuitionistic logic]].)

With these examples, one can see quite readily that quantification is about saying how often a statement is true, that is *quantifying* it.

### Lawvere quantifiers: Quantification as adjunction
 {#LawvereQuantifier}

Given two contexts $\Gamma$ and $\Delta$ and an interpretation $f\colon \Gamma \to \Delta$, we obtain an operation $f^*\colon Prop_\Delta \to Prop_\Gamma$ from the propositions in $\Delta$ to the propositions in $\Gamma$.  If this operation has a [[right adjoint]], then this right adjoint is the __[[universal quantifier]]__ along $f$; if it has a [[left adjoint]], then this is the __[[existential quantifier]]__ along $f$.  The ordinary quantifiers in first-order logic are simply special cases of this where $f$ is given by weakening.

To bring this down to earth, let $S$ and $T$ be [[sets]] and let $f\colon S \to T$ be a [[function]].  We will think of each set as defining a context with one free variable for an element of that set; then the propositions in one of those contexts correspond to the [[subsets]] of the corresponding set.  In this way, we are looking at $f^*\colon \mathcal{P}T \to \mathcal{P}S$, the [[preimage]] map between [[power sets]] (often denoted $f^{-1}$).  Then the adjoints $\forall_f$ and $\exists_f$ are maps from $\mathcal{P}S \to \mathcal{P}T$ as follows:

*  $\forall_f\, A \coloneqq \{ y\colon T \;|\; \forall\, x\colon S,\; f(x) = y \;\Rightarrow\; x \in A \}$;

*  $\exists_f\, A \coloneqq \{ y\colon T \;|\; \exists\, x\colon S,\; f(x) = y \;\wedge\; x \in A \}$.

Note that $\exists_f A$ is simply the [[image]] of $f$ restricted to $A$.  Accordingly, one often denotes $\exists_f$ as $f_!$ (if not simply $f$).  When using this notation, one can also denote $\forall_f$ as $f_*$.

When $f$ is the unique function from a set $X$ to the terminal set, $\mathcal{P}1$ is the two-element set and an object in $\mathcal{P}X$ is a predicate on $X$.  The adjoints then map a predicate $Q$ to a truth value:

* $\exists x \in X$ such that $Q(x)$;

* $\forall x \in X, Q(x).$

### Guarded quantification: quantifying over subtypes {#Guarded} 

Recall that, given a [[type]] $T$ and a [[predicate]] $Q$ on $T$, the __[[subtype]]__ of $T$ defined by $Q$ is, or would be, a type $S$ whose elements ([[terms]]) $x$ are thought of as elements ([[terms]]) of $T$ such that $Q(x)$ holds. But many [[type theories]] do not include sub-[[type formation]] among their rules.  However, we can mimic quantification over subtypes by using so-called 'guarded' quantifiers.

Specifically, given a type $T$, a predicate $Q$ on $T$, and a predicate $P$ on $T$, the __guarded quantifications__ of $P$ relative to $Q$ are these [[propositions]]:

*  $\underset{x\colon T}{\forall}
   \big( Q(x) \Rightarrow P(x) \big)$,


*  $\underset{x\colon T}{\exists}
   \big( Q(x) \wedge P(x) \big)$.

We have already had an example of these on this page, in the discussion of the Lawvere quantifiers along a function ([above](#LawvereQuantifier)).

When the notation for $Q$ makes the type $T$ obvious, and especially when the variable appears only at beginning in this notation, it is quite common to suppress mention of $T$ and write "$\forall Q(x), P(x)$" and "$\exists Q(x), P(x)$".  This is particularly common in untyped theories where the domain type "$T$" would be notationally suppressed anyway; for example, this is almost always how one writes guarded quantifiers in [[material set theory]].


### Bounded quantification: Size issues and predicativity

When [[type theory]] is used as a [[foundation of mathematics]], we have a freely generated [[universe]] of types (see also at _[[type of types]]_) and can also consider quantification over these. Similarly, when [[set theory]] is used as a foundation, we have a type of all sets and can consider quantification over this type. Such quantification is called __unbounded__ and often forbidden in the [[axiom of separation]] (if it can be stated in the language at all), especially in [[predicative mathematics]] but also in some impredicative foundations, such as [[ETCS]]. Even if we allow unbounded quantification, if we wish to refer to large objects using the language of [[proper classes]], this introduces the possibility of quantification over all classes, and this is forbidden even in [[ZFC]] and [[SEAR]] (although it is allowed in Morse--Kelley class theory).

In contrast, quantification over variables from *small* types (for a suitable notion of smallness) is called __bounded quantification__. 

In the usual formulations of [[material set theory]], there is only one type (the type of sets), which is not small.  However, we can consider quantification over small subtypes using the trick of guarded quantification (above).  So the axiom of separation in so-called 'bounded' variations of ZFC allows only statements in which all quantifiers are guarded by a set.

In classical mathematics, at least, formulas with unbounded quantifiers can be classified into the [[Lévy hierarchy]], whose bottom level $\Delta_0$ consists of the formulas with only bounded quantifiers.

### Internalised quantifiers

... [[Heyting category]] ...


### Categorified quantifiers

... [[dependent product]] ... [[dependent sum]] ...


## Examples

* [[existential quantifier]], [[dependent sum]]

* [[universal quantifier]], [[dependent product]]

* [[uniqueness quantifier]]

## Related concepts
 {#RelatedConcepts}

* [[de dicto and de re]]

* [[Lévy hierarchy]]

* [[elimination of quantifiers]]

* [[generalized quantifier]]


## References

General linguistical and philosophical discussion is in 

* [Quantifiers and quantification](https://plato.stanford.edu/entries/quantification) in Stanford Encyclopedia of Philosophy

The identification of universal/existential quantification with [[adjoints]] of [[substitution]]/[[context extension]] ([[dependent product]]/[[dependent sum]]) originates around

* [[William Lawvere]], *Adjointness in Foundations*, Dialectica **23** (1969) 281-296, 

  reprinted in: Reprints in Theory and Applications of Categories **16** (2006) 1-16 &lbrack;[tac:tr16](https://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html), [pdf](https://www.emis.de/journals/TAC/reprints/articles/16/tr16.pdf)&rbrack;

* [[William Lawvere]],  *Quantifiers and sheaves*, Actes Congrès intern. Math. **1** (1970) 329-334 &lbrack;[pdf](https://raw.githubusercontent.com/mattearnshaw/lawvere/master/pdfs/1970-quantifiers-and-sheaves.pdf), [[Lawvere-QuantifiersAndSheaves.pdf:file]]&rbrack;

A definition of guarded and bounded quantification for the membership relation could be found in 

* [[Michael Shulman]] (2018). Comparing material and structural set theories. [arXiv:1808.05204](https://arxiv.org/abs/1808.05204).

[[!redirects quantifier]]
[[!redirects quantifiers]]
[[!redirects quantification]]
[[!redirects quantifications]]

[[!redirects Lawvere quantifier]]
[[!redirects Lawvere quantifiers]]
[[!redirects Lawvere quantification]]
[[!redirects Lawvere quantifications]]

[[!redirects guarded quantifier]]
[[!redirects guarded quantifiers]]
[[!redirects guarded quantification]]
[[!redirects guarded quantifications]]

[[!redirects bounded quantifier]]
[[!redirects bounded quantifiers]]
[[!redirects bounded quantification]]
[[!redirects bounded quantifications]]
[[!redirects quantifier]]

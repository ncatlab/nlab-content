
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

__Intuitionistic logic__ was introduced by [[Arend Heyting]] as a [[logic]] for [[Brouwer]]\'s [[intuitionistic mathematics]].  It applies more generally to [[constructive mathematics]] and so may also be called __constructive logic__.

Beware the terminological ambiguity: Some people insist that "intuitionistic logic" refers to Brouwerian intuitionism, which includes axioms that contradict classical logic; but other people use "intuitionistic" to mean the same as what in other contexts is called "constructive", i.e. mathematics without the [[principle of excluded middle]] or the [[axiom of choice]] but nothing added that contradicts them.  Some people (particularly material set theorists) use "constructive" to mean *predicative* constructive and "intuitionistic" to mean impredicative constructive.


## Idea

### General

Intuitionistic logic is most easily described as [[classical logic]] without the [[principle of excluded middle]] ($\vdash A \vee \neg{A}$) or the [[double-negation]] rule ($\neg\neg{A} \vdash A$).  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for [[classical logic]] (with $\neg$ but not $\bot$) and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ may contain *at most one* formula, or by starting with [[sequent calculus]] with $\bot$ and restricting to such sequents where $\Delta$ must contain *exactly one* formula.

### Constructive interpretation of connectives
 {#ConstructiveInterpretationOfConnectives}

The *intuitionistic interpretation* of the [[logical connectives]] is such that the resulting [[proposition]] is regarded as [[true]] if it is possible to [[constructive mathematics|construct]] a [[proof]] of its [[assertion]]. 

Notably, to assert a [[logical disjunction]] ("or") or an [[existential quantification]] ("exists") is taken to mean to prove one of the instances, so that there is no intuitionistic existence statement without construction of an example (the "disjunction property", see [below](#DisjunctionProperty)).

This constructive interpretation of logical truth is the crux of the rejection of the [[principle of excluded middle]], for it implies that to prove $P \vee (\not P)$ (which may superficially/classically seem tautologous) one must prove $P$ or one must prove $\not P$ --- but neither proof may be known (e.g. if $P$ = [[Riemann hypothesis]]). 

(Here the classical mathematician is regarded as "idealistic" in their assumption that either case must hold, even if it is impossible to tell which one.)

From [Bridges (1999), p. 96](#Bridges99):

\begin{imagefromfile}
    "file_name": "Bridges-IntuitInterpOfConnectives.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


An analogous discussion for [[inference rules]] in [[intuitionistic type theory]] is given in [Martin-Löf (1996, Lec 3)](#MartinLöf96).


## Properties

### Double negation
 {#DoubleNegation}

The [[double negation translation]] says that a [[proposition]] $P$ is provable in [[classical logic]] precisely if its [[double negation]] $\not \not P$ is provable in constructive logic.

### Disjunction property
 {#DisjunctionProperty}

Unlike classical logic, intuitionistic logic has the
_disjunction-_ and _existence_ properties (cf. [above](#ConstructiveInterpretationOfConnectives)): any [[proof]] of
$\vdash A \vee B$ must contain a proof of either $\vdash A$ or $\vdash B$, and similarly any proof of $\vdash \exists x.\,F(x)$ must
construct a term $t$ and a proof of $\vdash F(t)$.  These
properties are what justify our calling intuitionistic
logic 'constructive'.

On the other hand, (classical) [[Peano arithmetic]] is
conservative over (intuitionistic) [[Heyting arithmetic]] when
restricted to $\Pi^0_1$ formulas; that is, formulas of the
form $\forall x\colon N.\, \exists y\colon N.\, F(x,y)$.  Roughly speaking,
classical logic can be just as 'constructive' as
intuitionistic logic as far as proving the totality of
functions $\mathbb{N} \to \mathbb{N}$ is concerned.

## Classicality principles

The principle of [[excluded middle]] is not provable in intuitionistic logic, and if we assume it then the logic becomes [[classical logic]].  But there are other principles that are provable classically but not intuitionistically, but which are weaker than full PEM, such as

* various [[omniscience principles]] such as LPO and LLPO
* the [[double-negation shift]]
* [[de Morgan's law]], i.e. [[weak excluded middle]]
* the [[world's simplest axiom of choice]]

## Related concepts

* [[BHK interpretation]]

[[!include categories and logic - table]]

## References

Original articles:

* {#Heyting1930} [[Arend Heyting]], *Die formalen Regeln der intuitionistischen Logik. I, II, III.* Sitzungsberichte der Preußischen Akademie der Wissenschaften, Physikalisch-Mathematische Klasse (1930) 42-56, 57-71, 158-169.

See also:

* Wikipedia, *[Intuitionistic logic](https://en.wikipedia.org/wiki/Intuitionistic_logic)*

The intuitionistic interpretation of the logical connectives is reviewed 

in the context of [[constructive analysis]] in:

* {#Bridges99} [[Douglas Bridges]], p. 96 of: *Constructive mathematics: a foundation for computable analysis*, Theoretical Computer Science **219** 1–2 (1999) 95-109 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00285-0">doi:10.1016/S0304-3975(98)00285-0</a>&rbrack;

and in the context of [[intuitionistic type theory]] in:

* {#MartinLöf96} [[Per Martin-Löf]], *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf), [[MartinLofOnTheMeaning96.pdf:file]]&rbrack;
 

The observation that the [[poset]] of [[open subsets]] of a [[topological space]] (the [[internal logic]] of the [[sheaf topos]]) serves as a model for [[intuitionistic logic]] is apparently originally due to

* {#Tarski} [[Alfred Tarski]], _Der Aussagenkalk&#252;l und die Topologie_, Fundamenta Mathematicae 31 (1938), pp. 103-134.
 

A textbook account in the context of [[programming languages]] is in section 30 of

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_


[[!redirects intuitionistic logic]]
[[!redirects Intuitionistic logic]]

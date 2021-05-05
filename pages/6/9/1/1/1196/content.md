
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


## Definition

Intuitionistic logic is most easily described as [[classical logic]] without the [[principle of excluded middle]] ($\vdash A \vee \neg{A}$) or the [[double-negation]] rule ($\neg\neg{A} \vdash A$).  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for classical logic (with $\neg$ but not $\bot$) and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ may contain *at most one* formula, or by starting with sequent calculus with $\bot$ and restricting to such sequents where $\Delta$ must contain *exactly one* formula.


## Properties

### Double negation
 {#DoubleNegation}

The [[double negation translation]] says that a [[proposition]] $P$ is provable in [[classical logic]] precisely if its [[double negation]] $\not \not P$ is provable in constructive logic

### Disjunction property

Unlike classical logic, intuitionistic logic has the
_[[disjunction property|disjunction]]_ and _[[existence property|existence]]_ properties: any [[proof]] of
$\vdash A \vee B$ must contain a proof of either $\vdash A$ or
$\vdash B$, and similarly any proof of $\vdash \exists x.\,F(x)$ must
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

## References

The observation that the [[poset]] of [[open subsets]] of a [[topological space]] (the [[internal logic]] of the [[sheaf topos]]) serves as a model for [[intuitionistic logic]] is apparently originally due to

* [[Alfred Tarski]], _Der Aussagenkalk&#252;l und die Topologie_, Fundamenta Mathematicae 31 (1938), pp. 103-134.
 {#Tarski}

A textbook account in the context of [[programming languages]] is in section 30 of

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_


[[!redirects intuitionistic logic]]
[[!redirects Intuitionistic logic]]
[[!redirects constructive logic]]
[[!redirects constructivist logic]]

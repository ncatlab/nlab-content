
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

__Intuitionistic logic__ was introduced by [[Arend Heyting]] as a [[logic]] for [[Jan Brouwer]]\'s [[intuitionistic mathematics]].  It applies more generally to [[constructive mathematics]] and so may also be called __constructive logic__.


## Definition

Intuitionistic logic is most easily described as [[classical logic]] without the principle of the [[excluded middle]] ($\vdash A \vee \neg{A}$) or the [[double-negation]] rule ($\neg\neg{A} \vdash A$).  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for classical logic (with $\neg$ but not $\bot$) and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ may contain *at most one* formula, or by starting with sequent calculus with $\bot$ and restricting to such sequents where $\Delta$ must contain *exactly one* formula.


## Properties

Unlike classical logic, intuitionistic logic has the
_[[disjunction property|disjunction]]_ and _[[existence property|existence]]_ properties: any proof of
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


[[!redirects intuitionistic logic]]
[[!redirects Intuitionistic logic]]
[[!redirects constructive logic]]

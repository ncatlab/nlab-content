
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Intuitionistic logic was introduced by Heyting as a
formalism intended to encode Brouwer's [[constructive mathematics|constructivism]].
It is most easily described as [[classical logic]] without
the principle of the [[excluded middle]] $\vdash A \vee \neg{A}$
or the double-[[negation]] rule $\neg\neg{A} \vdash A$.  It
may also be defined by starting with Gentzen\'s [[sequent calculus]] for classical logic (with $\neg$ but not $\bot$) and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ may contain *at most one* formula, or by starting with sequent calculus with $\bot$ and restricting to such sequents where $\Delta$ must contain *exactly one* formula.

## Properties ##

Unlike classical logic, intuitionistic logic has the
_disjunction_ and _existence_ properties: any proof of
$\vdash A\vee B$ must contain a proof of either $A$ or
$B$, and similarly any proof of $\vdash\exists x.F(x)$ must
construct a term $t$ and a proof of $\vdash F(t)$.  These
properties are what justify our calling intuitionistic
logic 'constructive'.

On the other hand, (classical) Peano arithmetic is
conservative over (intuitionistic) Heyting arithmetic when
restricted to $\Pi^0_1$ formulas; that is, formulas of the
form $\forall x:N.\exists y:N.F(x,y)$.  Roughly speaking,
classical logic can be just as 'constructive' as
intuitionistic logic as far as proving the totality of
functions is concerned.

[[!redirects constructive logic]]

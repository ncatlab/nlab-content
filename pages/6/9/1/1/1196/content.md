Intuitionistic logic was introduced by Heyting as a
formalism intended to encode Brouwer's [[constructivism]].
It is most easily described as [[classical logic]] without
the principle of the excluded middle $\vdash A\vee\not A$
or the double-negation rule $\not\not A\vdash A$.  It
may also be defined by means of a [[sequent calculus]]
system where in a sequent $\Gamma\vdash\Delta$, $\Delta$
may contain _at most one_ formula.

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
form $\forall x:N\exists y:N.F(x,y)$.  Roughly speaking,
classical logic can be just as 'constructive' as
intuitionistic logic as far as proving the totality of
functions is concerned.

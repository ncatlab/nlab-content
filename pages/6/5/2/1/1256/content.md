**Coherent logic** is a fragment of (finitary) [[first-order logic]] which allows only the connectives and quantifiers $\wedge$, $\vee$, $\top$, $\bot$, and $\exists$.  A **coherent formula** is a formula in coherent logic.

A **coherent sequent** is a [[sequent]] of the form $\varphi \vdash \psi$, where $\varphi$ and $\psi$ are coherent formulas, possibly with free variables $x_1,\dots,x_n$.  In full first-order logic, such a sequent is equivalent to the single formula $\forall x_1, \dots, \forall x_n (\varphi \Rightarrow \psi)$ (in the empty [[context]]).  Of course, this latter formula is not coherent, but this shows that when we deal with coherent *sequents* rather than merely formulas, it can also be thought of as allowing one instance of $\Rightarrow$ and a string of $\forall$s at the very outer level of a formula.

Coherent logic (including sequents, as above) is the [[internal logic]] of a [[coherent category]].

## Examples

* Any (finitary) [[algebraic theory]] is coherent.

* A good example of a coherent theory that is not [[algebraic theory|algebraic]] (in any of the usual senses, although it comes from algebra) is the theory of a [[local ring]]; a similar example is the theory of a [[discrete field]].

## Variations

* Sometimes coherent logic is called *geometric logic*, but that term now more commonly used for the analogous fragment of infinitary logic which allows disjunctions over arbitrary sets (though still only finitary conjunctions).  See [[geometric logic]].

* Occasionally the existential quantifiers in coherent logic are further restricted to range only over *finitely presented types*.

[[!redirects coherent theory]]
[[!redirects coherent theories]]
[[!redirects coherent formula]]
[[!redirects coherent formulas]]
[[!redirects coherent sequent]]
[[!redirects coherent sequents]]

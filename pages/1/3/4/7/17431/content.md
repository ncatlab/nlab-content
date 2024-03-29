
# Display logic

* table of contents
{:toc}

## Idea

Display logic is a general kind of [[sequent calculus]] containing enough [[structural connectives]] and [[structural rules]] so that every [[logical formula]] appearing in a sequent can be "displayed" all by itself on the left or the right in an equivalent sequent.  This enables a simple formulation of the [[cut rule]].

## Informal Description

In the simplest sort of display logic, the [[antecedent]] and [[consequent]] are lists of formulas, some of which are marked with a star $*$, and there are [[structural rules]] allowing formulas to be moved back and forth between the antecedent and consequent by adding or removing a star:

$$ \frac{\Gamma,A \vdash \Delta}{\Gamma \vdash A*,\Delta} \qquad
 \frac{\Gamma,A* \vdash \Delta}{\Gamma \vdash A,\Delta} $$
$$ \frac{\Gamma \vdash A*,\Delta}{\Gamma,A \vdash \Delta} \qquad
 \frac{\Gamma \vdash A,\Delta}{\Gamma,A* \vdash \Delta} $$

By repeated application, this means that if $A$ appears anywhere in the antecedent --- or in the consequent with a star --- then we can rearrange the sequent to look like $A \vdash \Delta$.   Dually, if $A$ appears anywhere in the consequent, or anywhere in the antecedent with a star, we can rearrange the sequent to look like $\Gamma \vdash A$.  This enables a simple formulation (and proof) of the cut rule:

$$ \frac{\Gamma \vdash A \quad A \vdash \Delta}{\Gamma\vdash \Delta} $$

The general form of display logic allows [[bunches]] as antecedents and consequents.  There are some number of "families" of connectives, each of which comes with a [[structural connective]] for joining formulas in a context, like comma or semicolon, and also a structural connective for "negation" like star, with structural rules like those above formulated for each family.  (Each "comma" also has a corresponding nullary version, i.e. there is one "empty context" for each family.)  The structural comma is internalized on the left by a [[logical conjunction|conjunction]] and on the right by a [[logical disjunction|disjunction]], while the structural negation is internalized on both sides by a [[negation]].

Each family can also have other logical connectives like [[implication]] and [[modal operators]].  The families are distinguished from each other by the *other* structural rules that their commas satisfy; for instance, a "boolean family" satisfies contraction and weakening, while a "[[relevance logic|relevance]]" family satisfies only contraction.

## Properties

Any display logic satisfying a list of eight natural conditions automatically satisfies [[cut admissibility]].

## References

* Nuel D. Belnap, Jr.  *Display logic*, Journal of Philosophical Logic 11 (1982) 375-417.  [PDF](http://www.pitt.edu/~belnap/87displaylogic.pdf)

[[!redirects display logics]]

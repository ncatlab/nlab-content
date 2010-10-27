# The axiom of choice
* tic
{: toc}


## Statement

In its modern form, the axiom of choice in an [[internalization|ambient category]] $A$ says that

* _Every [[epimorphism]] in $A$ splits._

This means: for every [[epimorphism]] $f : A \to B$ there is a morphism $\sigma : B \to A$ (a [[section]]), such that
$$
  (B \stackrel{\sigma}{\to} A \stackrel{f}{\to} B) 
  =
  (B \stackrel{Id_B}{\to} B)
  \,.
$$

If the ambient category is not [[balanced category|balanced]], such as a [[regular category|regular]] or [[coherent category]] which is not a [[pretopos]], it may be more appropriate to replace "epimorphism" by [[regular epimorphism]].

If $A$ is a [[extensive category|superextensive]] [[site]], then the axiom of choice for $A$ may be taken to say that, given any [[cover]]ing family $(p_i: U_i \to X)_i$, there is an appropriate section $X \to \coprod_i U_i$.


## Remarks

* If $A = Sets$ then this reproduces the axiom of choice in its traditional form: an epimorphism $A \to B$ of sets can be regarded as a $B$-indexed [[family of sets]]. The existence of a section is equivalent to a choice of one element in each set of this family.

* Formulated in terms of sections the _axiom of choice_ may look less mysterious than in its original formulation. For instance, it is clear that it fails in contexts such as $A =$ [[Top]] and $A = $[[Diff]], due to the existence of nontrivial topological and smooth fiber bundles.

* When the full axiom of choice it may still be valid for some restricted class of objects $A$ and/or $B$.  An object $B$ such that any epimorphism $A\to B$ splits is called [[projective object|projective]]; this means that one can make choices 'indexed by' $B$.  Dually, an object $A$ such that one can make choices 'with values in' $A$ is called a [[choice object]] (this is not quite equivalent to every epimorphism $A\to B$ splitting).

* In the context of [[constructive mathematics]], the full axiom of choice in $Set$ implies the principle of [[excluded middle]] and so is rejected.  However, weaker forms of choice, such as (in order of increasing strength) [[countable choice]], [[dependent choice]], and [[COSHEP]], are often (if not usually) accepted by constructivists.


## Equivalents 

The following statements are all equivalent to the axiom of choice in $Set$ (although sometimes the proof in one direction requires [[excluded middle]]).  This is a *very* short list; much longer lists can be found elsewhere, such as at [Wikipedia](http://en.wikipedia.org/wiki/Axiom_of_choice#Equivalents).  Some of the statements on this list, though, may be of interest to nLabbers but are not commonly mentioned as equivalents of choice.

* The [[well-ordering theorem]] (that any set can be [[well-order|well-ordered]]),
* [[Zorn's lemma]],
* That ($L =$ [[monomorphism]]s, $R =$ [[epimorphism]]s) is a [[weak factorization system on Set]].
* That [[Set]] is equivalent to its own [[free exact completion]].
* That there exists a [[group]] structure on every inhabited set (see [this MO answer](http://mathoverflow.net/questions/12973/does-every-non-empty-set-admit-a-group-structure-in-zf/12988#12988)).


## Variants

There are a number of weaker axioms which are implied by the full axiom of choice.  Some of these are valid or accepted more generally than the full AC, and/or suffice for some of the usual applications of choice.

* Many applications of choice in [[logic]], [[topology]], and [[algebra]] require only the [[ultrafilter principle]] (UF), or equivalently the *Boolean prime ideal theorem*.

* From the perspective of [[constructive mathematics]], the principle of [[excluded middle]] (EM) may be seen as a form of the axiom of choice; EM is equivalent to the statement that every [[Kuratowski-finite set]] is projective.

* The axioms of [[countable choice]] (CC) and [[dependent choice]] (DC) suffice for many of the usual applications of choice in the analysis of [[separable space]]s.  CC states that the set $\mathbb{N}$ of [[natural number]]s is projective.  DC strenghtens CC by allowing the set of possible choices for $n+1$ to depend on the choice made for $n$.

* The axiom [[COSHEP]], also called the "presentation axiom," says that any set admits a surjection from a projective one (whereas full AC says that all sets are projective).  This implies CC and DC, and is moreover sufficient for the existence of [[projective resolution]]s and cofibrant replacements, as well as the usual theorems in algebra that (for example) [[Mod]] has enough projectives.  For example, see the [[canonical model structure on Cat]].

* The [[axiom of small violations of choice]] (SVC) asserts there is a set $S$ such that every set is a [[subquotient]] of $C\times S$ for some choice set $C$.  Intuitively, this says that the failure of AC is parametrized by a single set.  It can be regarded as a "dual" of COSHEP, since it deals with choice sets rather than projective ones, it implies the existence of (at least some) [[injective resolution]]s, and together with COSHEP and EM it implies full AC.

* The [[axiom of multiple choice]] is a different way of saying that choice is violated in only a small way, which is more "local" than SVC.  It apparently follows from SVC, at least in [[ZF]].

* A still weaker axiom along the lines of "AC fails in only a small way," which is implied by AMC, is [[WISC]], i.e. that for any set $X$, the full subcategory of $Set/X$ consisting of the surjections has a [[weakly initial set]] (under COSHEP it has a single weakly initial object, namely a projective cover of $X$).  Two similar assertions are that the [[free exact completion]] $Set_{ex/lex}$ of $Set$ is a [[topos]] (i.e. that $Set$ has a [[generic proof]]), and that $Set_{ex/lex}$ is [[well-powered category|well-powered]]; both of these imply WISC.

The axiom of choice can also be strengthened in a few ways.

* While the ordinary axiom of choice says that any surjection of sets is split, the *axiom of global choice* says that this is also true for any surjection of [[proper classes]].  (Making this precise requires a bit of work.)  It is equivalent to the existence of a well-ordering of the class of all sets.

* One can also postulate a [[choice operator]], which gives a *specified* way to choose an element from any nonempty set.  This implies global choice, and conversely a choice operator can be defined from any well-ordering of the class of all sets.

Finally, one can instead adopt the *negation* of the axiom of choice, or a strengthened version:

* The assumption that every subset of the [[real line]] has the [[Baire property]] (BP) is consistent with DC but not AC; the same holds for the assumption that every subset of the real line is [[Lebesgue measure|measurable]] (LM) if at least one [[Grothendieck universe]] exists.  These assumptions leads to a very nice setting for analysis called [[dream mathematics]].

* The [[axiom of determinacy]] is a natural statement in [[game theory]] that is consistent with dependent choice; in fact, it implies dependent choices in certain models, such as in the constructible (in the sense of Goedel) closure of the set of reals. However, determinacy contradicts the full AC (for example, it implies that all sets of reals are Lebesgue measurable and have the Baire property, as in the previous entry). 

* Any of the varieties of [[constructive mathematics]] that contradict excluded middle necessarily contradict choice, but they tend to be consistent with COSHEP.


## References

[[HAF|Eric Schechter's analysis book]] surveys several variants of AC and its negation with a view to applications of analysis, including this nice picture:

![a Hasse diagram of variants of AC.](http://www.math.vanderbilt.edu/~schectex/ccc/excerpts/acchart.gif)

(Here, UF, DC, CC, BP, and LM are as defined above.)


## See also

* [[anafunctor]];
* [[foundations]].


category: foundational axiom


[[!redirects Choice]]
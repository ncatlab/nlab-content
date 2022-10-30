
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
{: toc}

## Statement

The axiom of **small violations of choice**, or **SVC**, introduced by Andreas Blass (1979), asserts that

* There exists a set $S$ such that every set is a [[subquotient]] of $A\times S$ for some [[choice set]] $A$.

Note that if $S=1$, then every set is a subquotient of a choice set; but choice sets are closed under subsets and quotients, so this means that every set is choice, i.e. that the [[axiom of choice]] holds.  Thus, SVC is a weakened version of AC; intuitively, it says that "the failure of AC to hold is parametrized by a mere set" (rather than a [[proper class]]).

At least assuming [[classical logic]], it is equivalent to say that every set is a quotient of $A\times S$, for we can extend any function defined on a subset of $A\times S$ to be constant on the complement of this subset.


## Implications

The following statements are all consequences of SVC (some requiring [[excluded middle]]).

* Assuming SVC with $S$, AC holds as soon as $S$ is choice.

* The [[regular extension axiom]] (REA).

* The [[axiom of multiple choice]] (AMC).

* There are "enough highly filtered ordinals," in the sense that for any set $A$, there is a limit [[ordinal]] $\alpha$ such that there is no cofinal function $A\to \alpha$.  (This is actually a consequence of REA.)

* There are enough [[injective object|injective]] [[abelian groups]].

  +--{: .query}
  [[Mike Shulman]]: I wonder whether SVC implies the existence of the full [[injective model structure|model structure on chain complexes]] on chain complexes.
  =--

* The category of [[anafunctors]] between two [[small categories]] is essentially small.

* The (local) [[axiom of small cardinality selection]].


## Models

SVC holds in all "ordinary" [[permutation model|permutation]] and [[symmetric model]]s of [[classical logic|classical]] (material) [[set theory]], as well as in hereditarily-ordinal-definable and [[constructible universe|relatively-constructible]] submodels.  However, it can fail in permutation models over [[proper classes]].

When we move to [[constructive mathematics]], however, SVC quickly becomes unreasonable, because in the absence of LEM there are usually very few choice objects.  In particular, [here](https://mathoverflow.net/a/339314/49) Simon Henry argues that any Grothendieck topos satisfying both SVC and $\neg$LEM (i.e. $\neg \forall P, P\vee \neg P$, which holds in many toposes such as $Sh([0,1])$) is trivial.

## SVC and COSHEP

SVC can be regarded as a sort of "dual" or "complement" to [[COSHEP]], since it deals with choice sets and COSHEP deals with projective sets.  And while COSHEP implies the existence of projective resolutions, SVC implies the existence of (at least some) injective resolutions.

Moreover, at least assuming classical logic, SVC + COSHEP implies AC.  First note that if SVC holds with $S$, then it also holds with $S'$ for any surjection $S'\to S$; thus under SVC + COSHEP we may assume that SVC holds with a projective set $S$.  Let $Z$ be any set, and let $g\colon A\times S \twoheadrightarrow Z^S$ be a surjection, where $A$ is choice.  For each $s\in S$, let $Z_s = \{g(a,s)(s) | a\in A\} \subseteq Z$.  Then each $Z_s$ is a surjective image of $A$, and hence choice.  If each $Z\setminus Z_s$ is nonempty, then (since $S$ is projective) we have a function $f\colon S\to Z$ such that $f(s)\notin Z_s$ for all $s$.  But $g$ is surjective, so there exist $s_0\in S$ and $a_0\in A$ with $g(a_0,s_0) = f$, whence $g(a_0,s_0)(s_0) = f(s_0) \notin Z_{s_0}$, a contradiction.  Thus some $Z_s$ is all of $Z$, and hence $Z$ is choice; so AC holds.


## References

SVC was introduced in the paper

* [[Andreas Blass]], _Injectivity, projectivity, and the axiom of choice_,   Trans. Amer. Math. Soc. **255** (1979), pp 31-59 doi:[10.1090/S0002-9947-1979-0542870-6](https://doi.org/10.1090/S0002-9947-1979-0542870-6)

where most of the above results were proven.  Some others can be found in

* [[Michael Rathjen]], _Choice principles in constructive and classical set theories_, in: Logic Colloquium '02, pp 299-326, Lect. Notes Log., **27**, (2006) ([pdf](http://www1.maths.leeds.ac.uk/~rathjen/acend.pdf))


category: foundational axiom

[[!redirects SVC]]
[[!redirects small violations of choice]]
[[!redirects axiom of small violations of choice]]

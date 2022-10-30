
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Logic
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Mathematical logic_ or _symbolic logic_ is the study of [[logic]] and [[foundations]] of mathematics as, or via, formal systems -- _[[theories]]_ --  such as [[first-order logic]] or [[type theory]].

## Subfields

The classical subfields are

* [[set theory]]

* [[model theory]],

* [[recursion theory]]

* [[proof theory]]

## Category-theoretic logic

By a convergence and unification of concepts that has been named _[[computational trinitarianism]]_, mathematical logic is equivalently incarnated in 

1. [[type theory]]

1. [[category theory]]

1. [[programming theory]]

The logical theory that is specified by and specifies a given [[category]] $\mathcal{C}$ -- called its _[[internal logic]]_, see there for more details and also see [[internal language]], [[syntactic category]].
-- is the one 

* whose [[types]] are the [[objects]] $A$ of $\mathcal{C}$;

* whose [[contexts]] are the [[slice categories]] $\mathcal{C}_{/A}$;

* whose [[propositions]] in context are the [[(-1)-truncated objects]] $\phi$ of $\mathcal{C}_{/A}$;

* whose [[proofs]] $A \vdash PhiIsTrue : \phi $ are the [[generalized elements]] of $\phi$.

Hence pure mathematical logic in the sense of the study of [[propositions]] is identified with [[(0,1)-category theory]]: where one concentrates only on [[(-1)-truncated objects]]. Genuine [[category theory]], which is about [[0-truncated objects]], is the home for logic and [[set theory]], or rather [[type theory]], the 0-truncated objects being the [[sets]]/[[types]]/[[hSet|h-sets]]. 

For instance, 

* [[limits]] and [[colimits]], [[exponentials]], and [[object classifiers]] belong to the [[type theory]];

* while their (-1)-truncation, in this order: [[intersections]]/([[and]]), [[unions]]([[or]]), [[implications]], and [[subobject classifiers]], belong to the logic.

Generally, [[(∞,1)-category theory]], which is about untruncated objects, is the home for logic and types with a [[constructive mathematics|constructive]] notion of [[equality]], the [[identity types]] in [[homotopy type theory]].


[[!redirects symbolic logic]] 


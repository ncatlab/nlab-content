+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[homotopy type theory]], a _suspension type_ of any [[type]] $X$ is the [[pushout type]] of the terminal function $X \to \ast$ (to the [[unit type]]) along itself, hence the pushout of the [[span]] $\ast \longleftarrow X \longrightarrow \ast$.

The [[categorical semantics]] is given by [[suspension objects]] in [[homotopy theory]] (and hence by [[suspension]] of [[topological spaces]] in, say, the [[classical model structure on topological spaces]]). 

## Definition

As a [[higher inductive type]], the suspension $\Sigma A$ of a type $A$ is given by

* A point $\mathrm{N} : \Sigma A$
* A point $\mathrm{S} : \Sigma A$
* A function $merid : A \to (\mathrm{N} =_{\Sigma A} \mathrm{S})$

The resulting [[inference rules]] are the specialization of those of [[pushout types]] (see [there](pushout+type#InferenceRules)).

In [[Coq]] [[pseudocode]] this becomes

    Inductive Suspension (A : Type) : Type
      | north : Suspension A
      | south : Suspension A
      | meridian : A -> Id Suspension A north south

This says that the type is [[dependent type|dependent]] on the type A and inductive constructed from two [[terms]] in the suspension, whose [[semantics|interpretation]] is as the north and south poles of the suspension, together with a term in the [[function type]] from A to the [[identity type]] of paths between these two terms, representing the meridians from the north to the south pole.

## Examples

* The [[two-valued type]] $\mathbf{2}$ is the suspension type of the [[empty type]] $\mathbf{0}$. 

* The [[interval type]] $I$ is the suspension type of the [[unit type]] $\mathbf{1}$. 

* The [[circle type]] $S^1$ is the suspension type of $\mathbf{2}$.

* The homotopical disk type $G_2$ is the suspension type of $I$.

* Homotopical $n$-sphere types of dimension $n:\mathbb{N}$, $S^n$, are suspension types of $S^{n-1}$. 

* Homotopical $n$-[[globe]] types of dimension $n:\mathbb{N}$, $G_n$, are suspension types of $G_{n-1}$.


## Related concepts

* [[suspension object]]

  * **suspension type**, [[reduced suspension type]]

  * [[suspension]], [[reduced suspension]]

* [[homotopy pushout]]

## References

* [[Univalent Foundations Project]], §6.5 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

[[!redirects suspension types]]
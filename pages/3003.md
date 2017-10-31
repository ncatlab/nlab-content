
# Conical spaces
* table of contents
{: toc}

## Idea

A **conical space** is a [[set]] equipped with a notion of taking [[real number|real]]-[[linear combinations]] with [[nonnegative number|nonnegative]] [[coefficients]] of its elements.  

Conical spaces appear prominently in [[microlocal analysis]], where [[wave front sets]] of [[distributions]] are [[disjoint unions]] of (open-)conical spaces; also in [[Lorentzian geometry]] in the guise of open [[past]]/[[future]] [[causal cones]] and [[light cones]]. 

## Definition

### Conical sets

A _conical set_ is a [[module]] of the [[rig]] $\mathbb{R}^+ = {[{0,\infty}[}$: that is, the rig of [[nonnegative number|nonnegative]] [[real numbers]], with ordinary [[addition]] and [[multiplication]] as the rig operations.

Similarly one may consider "open conical sets" which are [[modules]] over the [[rig]] of [[positive number|positive]] [[real numbers]].

### Extended conical sets

An _extended conical space_ is a [[module]] over the [[rig]] $\bar{\mathbb{R}}^+ = [0,\infty]$ of [[nonnegative number|nonnegative]] [[extended real numbers]], with $0 \cdot \infty \coloneqq 0$.  

For purposes of [[constructive mathematics]], one should take $\bar{\mathbb{R}}^+$ to be the space of nonnegative [[lower real numbers]].

Since we have a [[rig]] [[homomorphism]] $\mathbb{R}^+ \hookrightarrow \bar{\mathbb{R}}^+$, every extended conical space has an underlying conical space, and any conical space [[free construction|freely generates]] an extended conical space.  However, there is no direct relationship between [[vector spaces]] and extended conical spaces.

## Examples

### General

The  [[extended positive cone]] of any [[ordered group|ordered]] real [[vector space]] is an extended conical space.

* The [[positive cone]] of any [[ordered group|ordered]] real [[vector space]] is a conical space.


### Relation to vector spaces

Any [[rig]] [[homomorphism]] $A \to B$ gives a '[[restriction of scalars]]' [[functor]] $R\colon B Mod \to A Mod$ and '[[extension of scalars]]' [[functor]] $L \colon A Mod \to B Mod$.  In particular,  the rig homomorphism 

$$
  \mathbb{R}^+ \hookrightarrow \mathbb{R}
$$

produces a pair of [[adjoint functors]] between the [[category of modules]] over $\mathbb{R}$ (that is,  [[real vector spaces]]) and the [[category of modules]] over $\mathbb{R}^+$ (that is, conical spaces).  

In simple English: any real vector space has an [[forgetful functor|underlying]] conical space, and any conical space [[free construction|freely generates]] a real vector space.

## Related concepts

* [[affine space]]

* [[projective space]]

* [[conical singularity]]

## References

See also 

* Wikipedia, _[Conical combination](https://en.wikipedia.org/wiki/Conical_combination)_

[[!redirects conical spaces]]

[[!redirects conical set]]
[[!redirects conical sets]]


[[!redirects extended conical space]]
[[!redirects extended conical spaces]]

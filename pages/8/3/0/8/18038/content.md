+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
The _Keisler-Shelah isomorphism theorem_ characterizes the partially syntactic concept of elementary equivalence in purely semantic form with the help of [[ultrapower|ultrapowers]].

## Statement of theorem 
In practice, the theorem is usually stated as follows: let $A$ and $B$ be [[first-order logic|first-order]] $\mathcal{L}$-[[structures]]. Then $A$ and $B$ are [[elementary equivalence|elementarily equivalent]], written $A \equiv B$, if and only if there is an ultrafilter $\mathcal{U}$ on some index set $I$ such that there is an isomorphism of [[ultrapowers]] $A^{\mathcal{U}} \simeq B^{\mathcal{U}}$.

Keisler proved, assuming [[GCH]], that when $A \models T$ and $B \models T$ have cardinality $\leq 2^{|T|}$ then they have isomorphic $|T|$-indexed ultrapowers. Shelah removed the assumption of GCH at the cost of exhibiting the isomorphism for only $2^{|T|}$-indexed ultrapowers instead.

## Examples
* The [[Ax-Kochen-Ershov theorem]] states that for any non-principal ultrafilter $\mathcal{U}$ on the primes, the valued fields (viewed as structures in [[ACVF]], where $\mathbb{Q}_p$ is the [[p-adic]] field and $\mathbb{F}_p((t))$ is the field of [[formal Laurent series]] over the [[finite field]] $\mathbb{F}_p$)

$$

\displaystyle \prod_{p} \mathbb{Q}_p/\mathcal{U} \equiv \displaystyle \prod_{p} \mathbb{F}_p((t)) / \mathcal{U}

$$

are elementarily equivalent. Assuming the continuum hypothesis (this is an example of where this technical distinction is vital), they are also isomorphic.

## Remarks
* One could view this theorem as a generalization/variant of the [[nonstandard analysis|transfer principle]] from nonstandard analysis: given any two structures with the same theory, there exists a single "nonstandard model" linking the two via their diagonal embeddings into their ultrapowers.

## Related concepts
[[ultraroot]]

[[ultrapower]]

[[ultraproduct]]

[[Los ultraproduct theorem]]

## References
* See e.g. section 10 of [this survey article](https://ms.mcmaster.ca/~hanj18/jessewebpage_files/keisler-ultraproducts.pdf) by H. Jerome Keisler.

[[!redirects Keisler-Shelah theorem]]

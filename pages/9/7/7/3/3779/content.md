
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of [[weak complicial set]] is a model for (the [[omega-nerve]] of) the notion of [[weak ∞-category]]. The **model structure for weak $\omega$-categories** is a [[model category]] structure on the category of [[stratified simplicial set]]s, such that cofibrant-fibrant objects are precisely the [[weak complicial set]]s. This model structure may therefore be understood as a presentation of the [[(∞,1)-category]] of weak $\omega$-categories.

+-- {: .query}

[[Urs Schreiber]]: It would be interesting to see which algebraic definitions of higher categories coul be equipped with a model category structure induced from this model structure for weak complicial sets under the corresponding natural [[nerve and realization]] adjunction, maybe even as a [[transferred model structure]].

For instance I imagine that there is a good cosimplicial [[Trimble n-category|Trimble ∞-category]]

$$
  \Delta \stackrel{O}{\to} Str \omega Cat \stackrel{resolve}{\to} Trimble \omega Cat
  \,,
$$

where the first step is Street's [[oriental]]s and the second step is an embedding that regards a [[strict ∞-category]] as a suitably resolved equivalent Trimble $\omega$-category.

The induced [[nerve and realization]] adjunction

$$
  Trimble \omega Cat \stackrel{\overset{|-|}{\leftarrow}}{\underset{N}{\to}}
  sSet
$$

might maybe even be used to define the [[transferred model structure]] on Trimble $\omega$-catgeories (but I haven't checked at all if the relevant conditions have a chance of being satisfied, though). In any case I would expect that the counit of the adjunction $|N(C)| \to C$ serves as a good (cofibrant) replacement in $Trimble \omega Cat$ for reasonable choices of $Str \omega Cat \stackrel{resolve}{\to} Trimble \omega Cat$.

=--

## References

Section 6 of 

* [[Dominic Verity]], _Weak complicial sets, a simplicial weak omega-category theory. Part I: basic homotopy theory_ ([arXiv:math/0604414](http://arxiv.org/abs/math.CT/0604414)).

[[!redirects model structure for weak ∞-categories]]
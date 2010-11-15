## Definition

Let $C$ be a [[locally cartesian closed category]].  A **polynomial functor** is specified by the data
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z $$
in $C$.  The resulting functor is the composite
$$ C/W \overset{f^*}{\to} C/X \overset{\Pi_g}{\to} C/Y \overset{\Sigma_h}{\to} C/Z. $$
where $\Pi_g$ and $\Sigma_h$ are the [[dependent product]] and [[dependent sum]] operations, right and left adjoint respectively to [[pullback]] functors $g^*$ and $h^*$.

When $W=Z$, this is a **polynomial endofunctor**.

Sometimes this general notion is called a **dependent polynomial functor**, with "polynomial (endo)functor" reserved for the "one-variable" case, when $W=Z=1$ is the [[terminal object]].

If $g$ is an identity, the functor is sometimes called a **linear functor** or a **linear polynomial functor**.  Note that this notion makes sense even if $C$ is not locally cartesian closed; all it needs are [[pullbacks]].  More generally, we can make sense of polynomial functors in any category with pullbacks if we restrict $g$ to be an [[exponentiable morphism]].

## The 2-category of polynomial functors

Any polynomial functor, as defined above, is automatically equipped with a [[tensorial strength]], when the slice categories of $C$ are regarded as tensored over $C$ in the canonical way.  The following theorem is proven in Gambino-Kock:

+--{: .un_theorem}
###### Theorem
There is a [[bicategory]] whose objects are the objects of $C$, whose morphisms from $W$ to $Z$ are diagrams of the form
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z, $$
and whose 2-morphisms are diagrams of the form
$$
\array{ & & X & \to & Y \\
  & \swarrow & \uparrow & & \mathllap{id}\uparrow & \searrow\\
  W && X' \times_{Y'} Y & \to & Y && Z\\
  &\nwarrow & \downarrow & & \downarrow & \nearrow \\
  && X' & \to & Y'. }
$$
This bicategory is equivalent to the 2-category whose objects are slice categories of $C$, whose morphisms are polynomial functors regarded as strong functors, and whose 2-morphisms are strength-respecting natural transformations.
=--

Note that the above bicategory contains, as a locally full sub-bicategory, the usual bicategory of [[spans]].  Thus, as a special case, the bicategory of spans is equivalent to the 2-category of "linear" polynomial functors.  Both of these are instances of [[Lack's coherence theorem]].

## Related pages

* Polynomial endofunctors are important in the definition of [[W-types]] in categories.

* Polynomial functors are a special case of [[parametric right adjoint|parametric right adjoints]].

## References

* [[Nicola Gambino]] and [[Joachim Kock]], *Polynomial functors and polynomial monads*: [arXiv](http://arxiv.org/abs/0906.4931)

[[!redirects polynomial functors]]
[[!redirects polynomial endofunctor]]
[[!redirects polynomial endofunctors]]
[[!redirects dependent polynomial functor]]
[[!redirects dependent polynomial functors]]
[[!redirects linear polynomial functor]]
[[!redirects linear polynomial functors]]

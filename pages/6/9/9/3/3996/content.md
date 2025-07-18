
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Reflection of limits
* table of contents
{: toc}

## Idea

A [[functor]] is said to _reflect_ [[limits]] ([[colimits]]) of a given shape if a [[cone]] ([[cocone]]) is (co-)limiting whenever its image under $F$ is.

## Definition

+-- {: .num_prop #ReflectedLimit}
###### Definition

Let $F\colon C\to D$ be a [[functor]] and $J\colon I\to C$ a [[diagram]].  We say that $F$ **reflects** [[limits]] of $J$ if whenever we have a [[cone]] $\eta\colon const^I_x \to J$ over $J$ in $C$ such that $F(\eta)$ is a [[limit]] of $F\circ J$ in $D$, then $\eta$ was already a limit of $J$ in $C$.

=--

Of course, a functor $F$ reflects a colimit if $F^{op}$ reflects the corresponding limit.

If $F$ reflects all limits or colimits of a given type (i.e. over a given category $I$), we simply say that $F$ reflects that sort of limit (e.g. $F$ reflects products, $F$ reflects equalizers, etc.).

A functor which both reflects *and* preserves limits, and such that limits exist in its domain whenever they do in its codomain, is said to [[created limit|create]] them.


+-- {: .num_remark}
###### Remark

Reflection of limits is distinct from [[preservation of limits]], although there are relationships, e.g prop. \ref{ConservativeFunctors}.

=--


## Examples
 {#Examples}

+-- {: .num_prop }
###### Proposition

A [[faithful functor]] reflects [[epimorphisms]] and [[monomorphisms]].

=--

(The simple proof is spelled out [here](epimorphism#EpimorphismsAreReflectedByFaithfulFunctors) at _[[epimorphism]]_.)


+-- {: .num_example #FullSubcategoryInclusionsReflectCoLimits}
###### Example

A [[fully faithful functor]] (hence a [[full subcategory]] inclusion) reflects all limits and colimits.

=--

This is evident from inspection of the defining [[universal property]].


+-- {: .num_prop #ConservativeFunctors}
###### Proposition

A [[conservative functor]] reflects any limits which exist in its domain and that it [[preserved limit|preserves]].  

=--

+-- {: .proof}
###### Proof

If $J$ in def. \ref{ReflectedLimit} has some limit $\theta$ which is preserved by $F$, then there is a unique induced map $\eta\to\theta$ by the universal property of a limit, which becomes an isomorphism in $D$ since $F(\eta)$ and $F(\theta)$ are both limits of $F\circ J$; hence if $F$ is conservative then it must already have been an isomorphism in $C$, and so $\eta$ was already also a limit of $J$.

=--


## Related pages

* [[preserved limit]]

* **reflected limit**

* [[created limit]]

* [[lifted limit]]

## References

* [[Emily Riehl]], §3.3 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[pdf](https://emilyriehl.github.io/files/context.pdf), [book website](http://www.math.jhu.edu/~eriehl/context/)&rbrack;
  


[[!redirects reflection of limits]]
[[!redirects reflected limits]]
[[!redirects reflected colimit]]
[[!redirects reflected colimits]]
[[!redirects reflection of colimits]]

[[!redirects reflects]]
[[!redirects reflected]]


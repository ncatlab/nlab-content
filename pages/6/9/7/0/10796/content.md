
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A [[topological space]] is called _extremally disconnected_ if the [[closure]] of any [[open subset]] is still an open subset.

=--


## Properties

+-- {: .num_theorem}
###### Theorem (Gleason)

Extremally disconnected topological spaces are precisely the [[projective objects]] in the [[category]] of [[compact topological space|compact]] [[Hausdorff topological spaces]].

=--

See e.g. ([Bhatt-Scholze 13, below theorem 1.8](BhattScholze13))

+-- {: .num_prop}
###### Proposition

For $R$ a [[w-contractible ring]], the [[profinite set]] $\pi_0(Spec R)$
is an extremally disconnected [[profinite set]].

=--

Part of ([Bhatt-Scholze 13, theorem 1.8](#BhattScholze13)).

## The logical side

The extremal disconnectedness of a space is correlated with the property that the frame of its open subsets is a [[De Morgan Heyting algebra]] hence with the validity of the [[De Morgan law]] in logic, since a result by Johnstone says that a topos $Sh(X)$ of sheaves on a space $X$ is a [[De Morgan topos]] precisely when $X$ is extremally disconnected and this implies that all subobject lattices $sub(X)$ are De Morgan Heyting algebras, in particular $sub(1)$ corresponding to the frame of opens of $X$ (cf. [[De Morgan topos]] for details and references).

## Examples

+-- {: .num_example}
###### Example

For $S$ any [[set]] regarded as a [[discrete topological space]],
its [[Stone-Cech compactification]] is extremally disconnected.

=--

(e.g. [Bhatt-Scholze 13, example 2.4.6](#BhattScholze13))

+-- {: .num_example}
###### Counter-Example

The [[profinite set]] underlying the [[p-adic integers]], regarded as a [[Stone space]], is _not_ extremally disconnected.

=--

(e.g. [Bhatt-Scholze 13, example 2.4.7](#BhattScholze13))


## Related concepts

* [[totally disconnected space]]

* [[De Morgan topos]]

## References

* [[Peter Johnstone]], _[[Stone Spaces]]_

Discussion in the context of the [[pro-etale site]] is in

* [[Bhargav Bhatt]], [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 {#BhattScholze13}

The result on projective spaces stems from

* Andrew M. Gleason, _Projective topological spaces_ , Ill. J. Math. **2** no.4A (1958) pp.482-489. ([euclid](https://projecteuclid.org/euclid.ijm/1255454110))

[[!redirects extremally disconnected profinite sets]]

[[!redirects extremally disconnected profinite set]]

[[!redirects extremally disconnected space]]
[[!redirects extremally disconnected spaces]]
[[!redirects extremally disconnected]]

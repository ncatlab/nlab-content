

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One of the basic facts of [[category theory]] is that the order of two [[limits]] (a kind of [[universal construction]]) does not matter, up to [[isomorphism]].

## Statement

+-- {: .num_prop #LimitsCommuteWithLimits}
###### Proposition
**(limits commute with limits)**

Let $\mathcal{D}$ and $\mathcal{D}'$ be [[small categories]] and let $\mathcal{C}$ be a [[category]] which admits [[limits]] of shape $\mathcal{D}$ as well as [[limits]] of shape $\mathcal{D}'$. Then these limits "commute" with each other, in that 
for $F \;\colon\; \mathcal{D} \times {\mathcal{D}'} \to \mathcal{C}$ a [[functor]] (hence a [[diagram]] of shape the [[product category]]), with corresponding [[adjunct]] functors 

$$
  {\mathcal{D}'} 
    \overset{F_{\mathcal{D}}}{\longrightarrow} 
  [\mathcal{D},\mathcal{C}]
  \phantom{AAA}
  {\mathcal{D}} 
    \overset{F_{\mathcal{D}'}}{\longrightarrow} 
  [{\mathcal{D}'},   \mathcal{C}]
$$

we have that the canonical comparison morphism 

\[
  \label{ComparisonMorphismForCommutingLimits}
  lim F \simeq lim_{\mathcal{D}}  (lim_{\mathcal{D}'} F_{\mathcal{D}} )
  \simeq
   lim_{\mathcal{D}'}  (lim_{\mathcal{D}} F_{\mathcal{D}'} )
\]

is an [[isomorphism]].

=--

+-- {: .proof}
######Proof

Since the [[limit]]-construction is the [[right adjoint]] functor to the [[constant functor|constant]] [[diagram]]-functor, this is a special case of _[[right adjoints preserve limits]]_.

=--


See _[[limits and colimits by example]]_ for what formula (eq:ComparisonMorphismForCommutingLimits) says for instance for the special case $\mathcal{C} =$ [[Set]].

+-- {: .num_remark}
###### Remark
**(general non-commutativity of limits with colimits)**

In general limits do _not_ commute with [[colimits]]. But under a number of special conditions of interest they do. Special cases and concrete examples are discussed at _[[commutativity of limits and colimits]]_.

=--

## Related statements

* [[preserved limit]]

* [[adjoints preserve (co-)limits]]

* [[hom-functor preserves limits]]


[[!redirects limits preserve limits]]

[[!redirects colimits commute with colimits]]

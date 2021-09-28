
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Reflexive coequalisers
* table of contents
{: toc}


## Definitions

+-- {: .num_defn}
###### Definition

A **reflexive pair** is a [[parallel pair]] $f,g\colon A\rightrightarrows B$ having a common [[section]], i.e. a map $s\colon B\to A$ such that $f \circ s = g \circ s = 1_B$.  A **reflexive coequalizer** is a [[coequalizer]] of a reflexive pair.  A category **has reflexive coequalizers** if it has coequalizers of all reflexive pairs.

Dually, a reflexive coequalizer in the [[opposite category]] $C^{op}$ is called a __coreflexive equalizer__ in $C$.

=--

+-- {: .num_remark}
###### Remark

Reflexive coequalizers should not be confused with [[split coequalizers]], a distinct concept.

=--

+-- {: .num_example}
###### Example

Any [[congruence]] is a reflexive pair, so in particular any [[quotient object|quotient]] of a congruence is a reflexive coequalizer.

=--

## Properties



+-- {: .num_theorem #LintonTheorem}
###### Theorem

If $T$ is a [[monad]] on a [[cocomplete category]] $C$, then the category $C^T$ of [[Eilenberg-Moore category|Eilenberg Moore algebras]] is cocomplete if and only if it has reflexive coequalizers.  This is the case particularly if $T$ preserves reflexive coequalizers.

=--

This is due to ([Linton](#Linton)). 

+-- {: .proof} 
###### Proof 
Suppose $C^T$ has reflexive coequalizers. Then $C^T$ certainly has coproducts, because if $A_i$ is a collection of $T$-algebras, then we can form the coequalizer in $C^T$ of the reflexive pair 

$$
  \sum_i F U F U A_i 
   \underoverset
     {\sum_i F U \varepsilon A_i} 
     {\sum_i \varepsilon  F U A_i}
     {\rightrightarrows}
  \sum_i F U A_i$$ 

using the fact that the displayed coproducts exist because, for example, 

$$\sum_i F U A_i \cong F(\sum_i U A_i)$$ 

since the left adjoint $F$ preserves coproducts, assumed to exist in $C$. That this reflexive coequalizer is the coproduct $\sum_i A_i$ in $C^T$ is routine. 

Finally, a category with coproducts and reflexive coequalizers is cocomplete. It suffices that general coequalizers exist, but it is easily seen that if 

$$f, g \colon A \stackrel{\to}{\to} B$$ 

is a parallel pair, then the coequalizer of the reflexive pair 

$$A + B \stackrel{\overset{(f, 1_B)}{\to}}{\underset{(g, 1_B)}{\to}} B$$ 

(note both maps are retracts of the inclusion $B \to A + B$) also exists, and gives the coequalizer of the first pair. This completes the proof. 
=-- 


+-- {: .num_prop #PreservingReflectiveCoequalizersInTwoVariables}
###### Proposition

If $F\colon C\times D\to E$ is a [[functor]] of two variables which preserves reflexive coequalizers in each variable separately (that is, $F(c,-)$ and $F(-,d)$ preserve reflexive coequalizers for all $c\in C$ and $d\in D$), then $F$ preserves reflexive coequalizers in both variables together.  

=-- 

+-- {: .num_remark}
###### Remark

This is emphatically *not* the case for arbitrary coequalizers.

=-- 

+-- {: .proof} 
###### Proof 
**of proposition \ref{PreservingReflectiveCoequalizersInTwoVariables}** 
Suppose given two reflexive coequalizers 

$$c_0 \stackrel{\to}{\to} c_1 \to c_2$$ 

$$\,$$ 

$$d_0 \stackrel{\to}{\to} d_1 \to d_2$$ 

and let $c_{i j}$ denote $F(c_i, d_j)$ so that we have a diagram 

$$\array{
c_{0 0} & \stackrel{\to}{\to} & c_{0 1} & \to & c_{0 2} \\
\downarrow \downarrow & & \downarrow \downarrow & & \downarrow \downarrow \\
c_{1 0} & \stackrel{\to}{\to} & c_{1 1} & \to & c_{1 2} \\ 
\downarrow & & \downarrow & & \downarrow \\
c_{2 0} & \stackrel{\to}{\to} & c_{2 1} & \to & c_{2 2} 
}$$ 

in which all rows and columns are reflexive coequalizers (using preservation of reflexive coequalizers in separate variables), and all squares are _serially_ commutative. According to [Toposes, Triples, Theories](#BarrWells), lemma 4.2 page 248, the diagonal is also a (reflexive) coequalizer, as claimed. (See also the lemma on page 1 of Johnstone's [Topos Theory](#Johnstone).) 
=-- 

Proposition \ref{PreservingReflectiveCoequalizersInTwoVariables} is particularly interesting when $F$ is the [[tensor product]] of a cocomplete [[closed monoidal category]] $C$.  In this case it implies that the [[free monoid monad]] on such a category preserves reflexive coequalizers, and thus (by [Linton's theorem](#LintonTheorem)) the category of [[monoid objects]] in $C$ is cocomplete. 

+-- {: .num_prop}
###### Proposition

Reflexive coequalizers in [[Set]] [[limits commuting with colimits|commute]] with [[finite products]]: 

the $n$-fold product functors $Set^n \stackrel{\prod}{\to} Set$ preserve reflexive coequalizers. 

=--

+-- {: .proof}
###### Proof

This follows from prop. \ref{PreservingReflectiveCoequalizersInTwoVariables} as well as from the fact that the [[diagram]] category $\{ 0 \stackrel{\overset{d_0}{\to}}{\stackrel{\overset{s_0}{\leftarrow}}{\underset{d_1}{\to}}} 1\}$ with $d_0 \circ s_0 = d_1 \circ s_0 = id$ is a [[sifted category]].

=--

Of course, the diagonal functor $\Delta: Set \to Set^n$, being [[left adjoint]] to the product functor, preserves reflexive coequalizers; therefore the composite 

$$Set \stackrel{\prod \Delta}{\to} Set: x \mapsto \hom(n, x)$$ 

also preserves reflexive coequalizers. 

This has a further consequence which is technically very convenient: 

+-- {: .num_theorem}
###### Theorem

If $T$ is a [[finitary monad]] on $Set$, then $T$ preserves reflexive coequalizers.

=--

+-- {: .proof}
###### Proof

We have a [[coend]] formula for $T$: 

$$T(-) \cong \int^{n \in Fin} T(n) \times \hom(n, -)$$ 

and since this is a colimit of functors $\hom(n, -)$ which preserve reflexive coequalizers, $T$ must also preserve reflexive coequalizers. 

=--

Since finitary monads $T$ preserve reflexive coequalizers, it follows that the monadic functor $U \colon Set^T \to Set$ reflects reflexive coequalizers, and so since $Set$ has reflexive coequalizers, $Set^T$ must as well. Therefore, by proposition \ref{LintonTheorem}, $Set^T$ is cocomplete. This is actually true for infinitary monads $T$ on $Set$ as well, at least if we assume the axiom of choice (see [here](http://ncatlab.org/nlab/show/colimits+in+categories+of+algebras#reflexive_coequalizers_and_cocompleteness_16) for a proof), but the argument just given is a choice-free proof for the case of finitary monads. 


## Applications

* Reflexive coequalizers figure in the [[crude monadicity theorem]].

## References

* [[Fred Linton]], _Coequalizers in categories of algebras_, Seminar on Triples and Categorical Homology Theory, Lecture Notes in Mathematics Vol. 80 (1969), 75-90. 
{#Linton}

* [[Michael Barr]] and [[Charles Wells]], _Toposes, Theories, and Triples_, Reprints in Theory and Applications of Categories (2005), 1-289. ([online pdf](http://www.tac.mta.ca/tac/reprints/articles/12/tr12.pdf)) 
{#BarrWells}

* [[Peter Johnstone]], Topos Theory, London Mathematical Society Monographs no. 10, Academic Press, 1977. 
{#Johnstone} 

[[!redirects reflexive coequalizer]]
[[!redirects reflexive coequalizers]]
[[!redirects reflexive coequaliser]]
[[!redirects reflexive coequalisers]]
[[!redirects coreflexive equalizer]]
[[!redirects coreflexive equalizers]]
[[!redirects coreflexive equaliser]]
[[!redirects coreflexive equalisers]]
[[!redirects reflexive equalizer]]
[[!redirects reflexive equalizers]]
[[!redirects reflexive equaliser]]
[[!redirects reflexive equalisers]]

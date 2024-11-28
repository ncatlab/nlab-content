
> This page is about plain [[functors]] preserving [[limits]]. For [[internal functors]] in [[Top]], hence between [[topological groupoids]], see there.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Definition

In ordinary ([[Set]]-based) [[category theory]], a [[functor]] $F \colon  C \to D$ is **continuous** if it [[preserved limit|preserves]] all [[small diagram|small]] [[limits]] that exist in its [[domain]] $C$, i.e. given any [[small category]] [[diagram]] $A \colon E \to C$ in $C$ for which $\lim A$ exists, with universal [[cone]] $\lim A \to A$, application of $F$ to that cone results in a universal cone $F(\lim A) \to F \circ A$, thus making $F(\lim A)$ the limit of $F \circ A$. 

Put slightly differently, the limit $\lim (F \circ A)$ exists and the natural [[map]] induced by the [[universal property]] of the limit

$$
  F(\lim A) \longrightarrow \lim (F\circ A)
$$

is an [[isomorphism]]. In many and perhaps most cases, one refers to continuous functors $F \colon C \to D$ in cases where one already knows $C$ and $D$ are [[complete categories]], i.e., where $\lim A$ and $\lim F \circ A$ exist as a matter of course. 

In such cases, all limits can be obtained from (small) [[products]] and binary [[equalizers]] (see [here](limit#ConstructionFromProductsAndEqualizers)), and so it follows that a functor from a [[complete category]] is continuous if and only if it [[preserved limit|preserves]] all products and all binary equalizers. 

## Examples

\begin{example} 
The archetypical example is the [[Set]]-valued [[hom-functor]]: its continuity in both arguments (cf. *[[hom-functors preserve limits]]*) is indeed equivalent to the very definition of [[limit]]: for 
$F \colon D^{op} \to C$ a [[diagram]] and $c \in C$, the [[covariant functor|covariant]] [[hom-functor]] $Hom_C(c,-) : C \to Set$ satisfies by definition of [[limit]]
$$
  Hom_C(c, \lim F)
  \simeq
  \lim Hom(c,F(-))
  \,.
$$ 
Likewise for [[contravariant functor|contravariant]] representable functors on $C$, i.e., functors of the form $C(-, c): C^{op} \to Set$, which take limits in $C^{op}$ to limits in $Set$, or [[colimits]] in $C$ to limits in $Set$. 
\end{example} 

\begin{example}
Every [[right adjoint functor]] is continuous, since [[right adjoints preserve limits]].
\end{example}

## In enriched category theory 

One can also formulate limit preservation in terms of [[representable functors]]. This is especially appropriate in [[enriched category]] theory, where ordinary limits in terms of cones may no longer suffice and one should use [[weighted limits]] instead. Thus, working over a [[base of enrichment]] $V$, assumed to be a [[Bénabou cosmos]] for convenience, suppose given a ([[enriched functor|$V$-enriched]]) functor $F \colon C \to D$, a small weight $W\colon J \to V$, and a diagram $A \colon J \to C$ over that weight. Assume the [[weighted limit]] $\{W, A\}$ exists in $C$, i.e., suppose we have a representing object for the $V$-functor $c \mapsto V^{J}(W, C(c, A(-)))$, giving an isomorphism 

$$C(c, \{W, A\}) \cong V^{J}(W, C(c, A(-)))$$ 

natural in $c$. In this situation, playing the role analogous to a universal cone is a universal $V$-[[natural transformation]] 

$$W \to C(\{W, A\}, A(-))$$ 

and we say $F \colon C \to D$ *preserves* the weighted limit if the composite 

$$W \to C(\{W, A\}, A(-)) \to D(F\{W, A\}, (F \circ A)(-))$$ 

induces, &agrave; la [[Yoneda lemma|Yoneda]], a $V$-natural isomorphism 

$$D(d, F\{W, A\}) \cong V^J(W, D(d, (F \circ A)(-))).$$ 

Then we say that $F \colon C \to D$ is *$V$-continuous* if it preserves all weighted limits that exist in $C$. 


## Relation to other concepts

* The [[adjoint functor theorem]] states that any continuous functor between [[complete category|complete]] categories has a [[adjoint functor|left adjoint]] if it satisfies a certain 'small solution set' criterion.

* If $C$ has [[finite  limits]], then functors commuting 
with these _finite_ limits are precisely what are
called left [[exact functors]], or "finitely continuous" functors. 


## Warnings

1. It is not enough to demand that there exists an abstract isomorphism $F(\lim A) \cong \lim (F\circ A)$.

2. Topologists sometimes use "continuous functor" to mean a [[Top]]-[[enriched functor]], since a functor between topologically [[enriched categories]] is enriched iff its actions on hom-spaces are [[continuous functions]].

3. Sheaf-theorists sometimes say "continuous functor" for a [[cover-preserving functor]] between [[sites]], with the intuition being that it generalizes the [[inverse image]] induced by a [[continuous function]] of topological spaces.

4. H. Bass in his treatment of [[K-theory]] uses the older term 'right continuous functor' for the dual notion of [[cocontinuous functor]] in a version which is [[additive functor|additive]]. If the domain of an additive functor which commutes with direct sums is a [[cocomplete category]], then the functor automatically has [[adjoint functor|right adjoint]]. Following this fact, some people in ring theory and noncommutative geometry use the simple term 'continuous functor' for a functor with a right adjoint (even if the domain [[abelian category]] is not cocomplete). In general, of course, this is just a bit more than *co*continuous in the standard sense.


## Related concepts

* [[cocontinuous functor]]

* [[complete category]]

* [[adjoint functor theorem]]


[[!include properties of functors -- contents]]



## References


* [[Peter Freyd]], [[Max Kelly]], *Categories of continuous functors*, J. Pure. Appl. Algebra **2** (1972) 169-191 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90001-1">doi:10.1016/0022-4049(72)90001-1</a>&rbrack; 

* [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

[[!redirects continuous functors]]



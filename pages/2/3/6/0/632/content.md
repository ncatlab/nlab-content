
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

A [[functor]] $F \colon C\to D$ is **conservative** if it is "isomorphism-[[reflected limit|reflecting]]", i.e. if $g \colon a\to b$ is a [[morphism]] in $C$ such that $F(g)$ is an [[isomorphism]] in $D$, then $g$ is an isomorphism in $C$.

=--

+-- {: .num_remark}
###### Remark

Sometimes (e.g. in the [[Elephant]]) conservative functors are assumed to be [[faithful functor|faithful]] as well.  If $C$ has, and $F$ preserves, [[equalizer]]s, then conservativity implies faithfulness.

=--

See [[conservative morphism]] for a generalization to an arbitrary [[2-category]].

## Examples


\begin{example}\label{FullyFaithfulFunctorIsConservative}
Every [[fully faithful functor]], and more generally any [[pseudomonic functor]], is a conservative functor. 

(Every [[fully faithful functor]] is [[pseudomonic]].)
\end{example}

But further would-be converses of Exp. \ref{FullyFaithfulFunctorIsConservative} fail: not every conservative functor is full or faithful:

\begin{example}
An example of a functor that is conservative but not full is the inclusion of the [[groupoid core]] $Core(\mathcal{C}) \longrightarrow \mathcal{C}$ of a [[category]] $\mathcal{C}$ that is itself not a groupoid, into that category.  
\end{example}

\begin{example}
An example of a functor that is conservative but not faithful is the unique functor from any groupoid with two distinct isomorphisms $f, g : x \to y$ to the [[terminal]] groupoid.
\end{example}

+-- {: .num_example #MonadicFunctorIsConservative}
###### Example

Every [[monadic functor]] is a conservative functor (see also at *[[monadicity theorem]]*): 

For a [[algebra over a monad|$T$-algebra]] [[homomorphism]] given by an [[invertible morphism]] $f \colon A \to B$, the [[inverse]] $f^{-1} \colon B \to A$ is easily seen to also be a $T$-algebra homomorphism.

=--


+-- {: .num_prop #PullbackAlongEpimorphisms}
###### Proposition

Let $C$ be a [[category]] with [[pullbacks]]. Given any [[morphism]] $f \colon X \longrightarrow Y$ in $C$ write

$$
  f^\ast \colon C_{/Y} \longrightarrow C_{/X}
$$

for the [[functor]] of [[pullback]] along $f$ between [[slice categories]] ("[[base change]]"). If [[strong epimorphisms]] in $\mathcal{C}$ are preserved by pullback, then the following are equivalent:

1. $f$ is a [[strong epimorphism]];

1. $f^\ast$ is conservative.

=--

(e.g. [Johnstone, lemma A.1.3.2](#Johnstone))


+-- {: .num_example #ConservativeFunctorsBetweenPretoposesAreInjectiveOnSubobjectLattices}
###### Example

When $C$ and $D$ are [[pretopos|pretoposes]], a pretopos morphism $F \colon C \to D$ is conservative if and only if for every object $c \in C$, the induced map between [[poset of subobjects | subobject lattices]] $F^{(c)} : \operatorname{Sub}(c) \to \operatorname{Sub}(F(c))$ is injective.

=--


## Properties

\begin{proposition}
\label{ConservativeFunctorsReflectLimitsWhichTheyPreserve}
A conservative functor $F \colon C \to D$ [[reflected limit|reflects]] all [[limits]] and [[colimits]] that it [[preserved limit|preserves]] and which exist in the source category.
\end{proposition}

\begin{proof}
We discuss the case of limits (the argument for colimits is [[formally dual]]):

Let $K \colon J \to C$ be a [[diagram]] in $C$ whose limit $\lim K$ exists and such that $\lim (F\circ K) \,\simeq\, F (\lim K)$. Now if $const_c \to K$ is a [[cone]] in $C$ that is sent to a limiting cone $F const_c$ in $D$, then by the [[universal property]] of the limit in $D$ the morphism $F( c \to \lim K)$ is an [[isomorphism]] in $D$, hence must have been an isomorphism in $C$ (by the assumption that $F$ is conservative), hence $const_c$ must have been a limiting cone in $C$.
\end{proof}

\begin{proposition}
Up to [[equivalence]], every functor between small categories can be factored as an [[iterated localization]] followed by a conservative functor.
\end{proposition}


## Related concepts

* [[monadicity theorem]]

* [[conservative (∞,1)-functor]]

* [[iterated localization]]


## Literature


* Geun Bin Im, [[Gregory Maxwell Kelly]], _Some remarks on conservative functors with left adjoints_,  J. Korean Math. Soc. __23__ (1986),  no. 1, 19&#8211;33, [MR87i:18002b](http://www.ams.org/mathscinet-getitem?mr=843247), [pdf](https://koreascience.kr/article/JAKO198621048976714.pdf)
* Geun Bin Im, [[Gregory Maxwell Kelly]], _On classes of morphisms closed under limits_, J. Korean Math. Soc. __23__ (1986), no. 1, 1&#8211;18, [pdf](https://koreascience.kr/article/JAKO198621048976702.pdf)
* Geun Bin Im, [[Gregory Maxwell Kelly]], _Adjoint-triangle theorems for conservative functors_, Bull. Austral. Math. Soc. __36__ (1987),  no. 1, 133&#8211;136, [MR88k:18005](http://www.ams.org/mathscinet-getitem?mr=897429), [doi](http://dx.doi.org/10.1017/S000497270002637X) 

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_

Formalization in [[cubical Agda]]:

* [[1lab]], *[Functors](https://1lab.dev/Cat.Functor.Base.html#functors)*

For an example of a conservative, but not faithful, functor $f: A\to Set$ having a left adjoint:

* [[Reinhard Börger]], [[Walter Tholen]], Example 2.4 in _Strong regular and dense generators_,  [[Cahiers de Topologie et Géométrie Différentielle Catégoriques]] **32** 3 (1991) 257-276 &lbrack;[numdam:CTGDC_1991__32_3_257_0](http://www.numdam.org/item?id=CTGDC_1991__32_3_257_0), [MR1158111](http://www.ams.org/mathscinet-getitem?mr=1158111)&rbrack;



[[!redirects conservative functors]]
[[!redirects conservative]]


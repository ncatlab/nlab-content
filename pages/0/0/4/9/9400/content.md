
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Van Kampen colimits

* table of contents
{: toc}

## Idea

A [[colimit]] in a [[category]] or [[higher category]] is called *van Kampen* &lbrack;[Sobocinski & Heindel 2011](#SobocinskiHeindel11)&rbrack; if it is both [[universal colimit|universal]] (i.e. [[pullback-stability|stable]] under [[pullback]]) and satisfies [[descent]].  Many [[exactness properties]] can be phrased in terms of certain colimits being van Kampen.

## Definition

Let $\mathcal{C}$ be a [[category]] with [[pullbacks]].
Then there is a (pseudo) [[2-functor]]
\[
  \label{SelfIndexingFunctor}
  S 
  \,\colon\,
  C^{op} \to Cat 
\]
defined by $S(x) \,\coloneqq\, C/x$ (the [[slice category]]), called the *[[self-indexing]]* of $C$.  Its [[Grothendieck construction]] is the [[codomain fibration]].

\begin{definition}\label{VanKampenColimit}
A [[colimit]] in $\mathcal{C}$ is **van Kampen** if it is [[preserved limit|preserved]] by the functor $S$ (eq:SelfIndexingFunctor), i.e. it is taken to a (weak) [[2-limit]] in $Cat$.
\end{definition}


### Universality and descent

We need the following notation:

* For $\mathcal{D}$ any [[category]], write $\mathcal{D}^{\triangledown}$ for the result of adjoining to it a [[terminal object]]. This comes with a canonical [[full subcategory]] inclusion $\mathcal{D} \hookrightarrow \mathcal{D}^{\triangledown}$

* For $\mathcal{D}$ a [[small category]], and $G \,\colon\, \mathcal{D} \to \mathcal{C}$ a $\mathcal{D}$-shaped [[diagram]] with [[colimit]] $\underset{\longrightarrow}{\lim} G \,\in\, \mathcal{C}$, write $G^{\triangledown} \,\colon\, \mathcal{D}^{\triangledown} \longrightarrow \mathcal{C}$ the extension of $G$ to $\mathcal{D}^{\triangledown}$ by assigning $\underset{\longrightarrow}{\lim} G$ to the adjoined terminal object.

\begin{theorem}\label{UniversalityAndDescent}
**(equifibrancy characterization of van Kampen colimits)**
\linebreak
If $\mathcal{C}$ has all [[colimits]] of $\mathcal{D}$-shaped diagrams, then the colimit $\underset{\longrightarrow}{\lim}G$ of $G \colon \mathcal{D}\to \mathcal{C}$ is van Kampen (Def. \ref{VanKampenColimit}) if and only if the following condition holds: 

* For any diagram $F^{\triangledown} \,\colon\, \mathcal{D}^{\triangledown} \to \mathcal{C}$ and [[natural transformation]] $\alpha^{\triangledown} \,\colon\, F^{\triangledown} \Rightarrow G^{\triangledown}$ whose [[restriction]] $\alpha \colon F \Rightarrow G$ along $\mathcal{D} \hookrightarrow \mathcal{D}^{\triangledown}$ is [[equifibered natural transformation|equifibered]], the following are equivalent:

  1. $\alpha^{\triangledown}$ is [[equifibered natural transformation|equifibered]].

  1. $F^{\triangledown}$ is a [[colimit|colimiting]] [[cocone]].

\end{theorem}
\begin{proof}
First note that the [[2-limit]] of $S\circ G$ is [[equivalence of categories|equivalent]] to the [[full subcategory]] of the [[slice category]] of the [[functor category]]
$$
  \big([D,C] \Downarrow G\big)
  \hookrightarrow
  [\mathcal{D},\mathcal{C}]/G
$$
consisting of the [[equifibered natural transformation|equifibered transformations]].  Moreover, under this equivalence, the comparison map $S(x) \to \lim (S\circ G)$ is identified with the pullback functor
$$ 
  C/x \longrightarrow ([D,C] \Downarrow G)
  \,.
$$
Now, this functor has a [[left adjoint]] given by taking [[colimits]]. [Therefore](adjoint+functor#FullyFaithfulAndInvertibleAdjoints) it is an [[equivalence of categories|equivalence]] if and only if the [[unit of an adjunction|unit]] and [[counit of an adjunction|counit]] of the adjunction are isomorphisms.

The unit is the map from an equifibered transformation over $G$ into the pullback of its colimit.  The latter underlies an equifibered $\alpha'$ by construction, so the unit is an isomorphism just when $\text{(2)}\Rightarrow \text{(1)}$.  Similarly, the counit is the map into an object over $x$ from the colimit of its pullback.  Thus, it is an isomorphism just when $\text{(1)}\Rightarrow\text{(2)}$.
\end{proof}

\begin{remark}
The condition $\text{(1)}\Rightarrow\text{(2)}$ is precisely the statement that the colimit of $G$ is [[universal colimit|universal]], i.e. preserved by pullback.  The condition $\text{(2)}\Rightarrow\text{(1)}$ is a form of [[descent]].
\end{remark}

### Colimits in Span

+-- {: .num_theorem #ColimitsInSpan}
###### Theorem
A colimit in $C$ is van Kampen if and only if it is preserved by the inclusion $C\to Span(C)$ into the [[bicategory]] of [[spans]] in $C$.
=--
([Sobocinski & Heindel 2011](#SobocinskiHeindel11)).

## Examples

\begin{example}

* A category with [[pullbacks]] is [[lextensive category|lextensive]] just when [[coproducts]] are van Kampen.

* A category with [[pullbacks]] is [[adhesive category|adhesive]] just when [[pushouts]] of [[monomorphisms]] are van Kampen.

* A category with [[pullbacks]] is [[exhaustive category|exhaustive]] just when transfinite [[unions]] of monomorphisms are van Kampen.

\end{example}

\begin{example}\label{RegularCatWithVanKampColimitsIsExact}
A [[regular category]] with van Kampen [[quotients]] of [[congruences]] is [[exact category|exact]]. 
\end{example}
\begin{proof}
Let $p_1, p_2 : R \rightrightarrows A$ be a congruence. We need to show that $R$ is the [[kernel pair]] of the [[quotient map]] $A \to A/R$.

Let the transitivity of the congruence be witnessed by $t \,\colon\, R \times_A R \to R$. Then, in the following [[diagram]]

$$
\array{
  R \times_A R 
    & 
  \underoverset{\pi_2}{t}{\rightrightarrows} 
    & 
  R & \stackrel{p_2}{\to} & A
  \\
  {{}^\mathllap{\pi_1}}\big\downarrow && \big\downarrow{{}^\mathrlap{p_1}} && \big\downarrow 
  \\
  R & \underoverset{p_2}{p_1}{\rightrightarrows} & A & \to & A/R
}
$$

the left squares are [[pullbacks]] and the top diagram is a [[split coequalizer]] (with the splitting maps given by reflexivity), [hence](split+coequalizer#AsCoequalizers) a [[coequalizer]]. Now since the bottom coequalizer is assumed to be van Kampen, Thm. \ref{UniversalityAndDescent} implies that also the right square is a pullback. But this is the desired statement that $R$ is the [[kernel pair]] of $A \to A/R$.
\end{proof}

\begin{example}
In [[Set|$Set$]], the [[pushout]] square
$$
  \array{ 
    2 & \to & 1 
    \\ 
    \big\downarrow && \big\downarrow 
    \\ 
    1 & \to & 1 
  }
$$
is not van Kampen, neither is the [[coequalizer]] diagram $\mathbf 1 \rightrightarrows \mathbf 1 \to \mathbf 1$.

On the other hand, in an [[(∞,1)-topos]] (say [[∞Grpd]]), the descent property of the [[circle]] seen [[circle type#as_a_coequalizer|as a coequalizer]] gives a concise proof that the [[loop space]] of the circle is equivalent to the [[integers]]: in the diagram below, the two squares on the left are pullbacks because both $\mathrm{id}$ and $s$ are isomorphisms, and the top row is a [[homotopy coequalizer]] diagram because the [[line type]] is [[contractible]]. Furthermore, there is a higher coherence relating the two homotopies obtained by composing the top cofork with the back and right squares and by composing the front and right squares with the bottom cofork, ensuring that this diagram is [[homotopy coherent]].

$$
\array{
  \mathbb{Z} 
    & 
  \underoverset{\mathrm{id}}{s}{\rightrightarrows} 
    & 
  \mathbb{Z} & \to & \mathbf{1} 
  \\
  \big\downarrow && \big\downarrow && \big\downarrow 
  \\
  \mathbf{1} & \rightrightarrows & \mathbf{1} & \to & S^1
  \mathrlap{\,.}
}
$$

Then, descent implies that the square on the right is a pullback, which says exactly that the [[path space]] between any two points of the circle is [[homotopy equivalence|homotopy equivalent]] to the [[integers]] $\mathbb{Z}$.
\end{example}

## In higher categories 
 {#InHigherCategories}

There is an evident generalization of the definition to [[higher category theory|higher categories]], and in particular to [[(∞,1)-categories]].  In the latter case, van Kampen colimits exactly characterize descent.  In particular,we have:

* A [[locally presentable (∞,1)-category]] is an [[(∞,1)-topos]] just when *all* colimits are van Kampen.

If we take Theorem \ref{UniversalityAndDescent} as the definition of "van Kampen colimit", this follows from Theorem 6.1.3.9 of [[HTT]], see also around ([[(infinity,2)-Categories and the Goodwillie Calculus|Lurie 2Cats+Goodwillie, example 1.2.3]]).  The $(\infty,1)$-categorical version of Theorem \ref{UniversalityAndDescent} may not exactly be in the literature, however.  The cited theorem of HTT essentially gives Theorem \ref{UniversalityAndDescent} under the additional global hypothesis that all colimits in $C$ are universal.

In this case, being van Kampen is also equivalent to being preserved by the composite of $S$ with the [[core]] functor $Core : (\infty,1)Cat \to \infty Gpd$.  Thus, the [[adjoint functor theorem]] (specifically, the [[representable functor theorem]]) implies that (assuming all colimits to be universal), all colimits are van Kampen just when all small versions of $Core \circ S$ are [[representable functor|representable]], i.e. when [[object classifiers]] exist.


## Related pages

* [[exactness property]]

* [[object classifier in an (∞,1)-topos]]

* [[descent]] / [[universal colimit]]

* [[strict initial object]]

## References

* {#SobocinskiHeindel11} [[Pawel Sobocinski]], [[Tobias Heindel]], *Being Van Kampen is a universal property*, Logical Methods in Computer Science, **7** 1 (2011) &lbrack;[arXiv:1101.4594](https://arxiv.org/abs/1101.4594), <a href="https://doi.org/10.2168/LMCS-7(1:14)2011">doi:10.2168/LMCS-7(1:14)2011</a>&rbrack;


[[!redirects van Kampen colimits]]

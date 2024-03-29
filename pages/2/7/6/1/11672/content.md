
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[homotopy colimits]] of [[filtered diagrams]]

## Characterization

+-- {: .num_prop #CharacterizationOfFilteredHomotopyColimits}
###### Proposition

In a [[combinatorial model category]], for every sufficiently large  [[regular cardinal]] $\kappa$ the following holds:

* $\kappa$-[[filtered colimits]] preserve weak equivalences;

* hence $\kappa$-[[filtered colimits]] are already [[homotopy colimits]].


=--

This appears as ([Dugger 00, prop 7.3](#Dugger00)).

+-- {: .proof}
###### Proof


The point is to choose $\kappa$ such that all domains and codomains of the generating cofibrations are $\kappa$-[[compact object]]. This is possible since by assumption that $C$ is a [[locally presentable category]] all its objects are [[small objects]], hence each a $\lambda$-[[compact object]] for some cardinal $\lambda$. Take $\kappa$ to be the maximum of these.

Let $F, G : J \to C$ be $\kappa$-filtered diagrams in $C$ and $F \to G$ a [[natural transformation]] that is degreewise a weak equivalence. Using the functorial factorization provided by the [[small object argument]] this may be factored as $F \to H \to G$ where the first transformation is objectwise an acyclic cofibration and the second objectwise an acyclic fibration, and by functoriality of the factorization this sits over a factorization

$$
  \lim_\to F \stackrel{\simeq}{\hookrightarrow} \lim_\to H \stackrel{}{\to}\lim_\to G
  \,.
$$

It remains to show that the second morphism is a weak equivalence. But by our factorization and by [[category with weak equivalences|2-out-of-3]] applied to our componentwise weak equivalences, we have that all its components $H(j) \to G(j)$ are acyclic fibrations.

At [[small object]] it is described in detail how $\kappa$-smallness of an object $X$ implies that morphisms from $X$ into a $\kappa$-filtered colimit lift to some component of the colimit

$$
  \array{
    \cdots&\to&H(j-1) &\to& H(j) &\to& H(j+1) &\to& \cdots
    \\
    &&&{}^{\mathllap{\exists \hat f}}\nearrow&\downarrow & \swarrow
    \\
    &&X& \stackrel{\forall f}{\to} &\lim_\to H
  }
  \,.
$$

So given a diagram

$$
  \array{
    X &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow
    \\
    Y &\to& \lim_\to G 
  }
$$

we are guaranteed, by the $\kappa$-[[small object|smallness]] of $X$ and $Y$ that we established above, a lift

$$
  \array{
    X &\to& H(j) &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow^{\in \mathrlap{\in rlp(I)}}
    &&
    \downarrow
    \\
    Y &\to& G(j) &\to& \lim_\to G
  }
$$

into some component at $j \in J$ and hence a lift

$$
  \array{
    X &\to& H(j) &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} &
    \nearrow
    & \downarrow^{\in \mathrlap{\in rlp(I)}}
    &&
    \downarrow
    \\
    Y &\to& G(j) &\to& \lim_\to G
  }
  \,.
$$

Thereby $\lim_\to H \to \lim_\to G$ is in $rlp(I) \subset W$.

=--

+-- {: .num_cor}
###### Corollary

In the situation of prop \ref{CharacterizationOfFilteredHomotopyColimits},
since finite [[homotopy limits]] are given, after [[fibrant resolution]], by [[finite limits]], it follows from the ordinary commutativity of [[filtered colimits]] with finite limits that also filtered homotopy colimits commute with finite homotopy limits.
=--

## Related concepts

* [[filtered (∞,1)-colimit]]

## References

* {#Dugger00} [[Daniel Dugger]], _Combinatorial model categories have presentations_ ([arXiv:math/0007068](http://arxiv.org/abs/math/0007068))

[[!redirects filtered homotopy colimits]]
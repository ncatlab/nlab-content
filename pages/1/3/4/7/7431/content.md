# Relatively compact morphisms

* table of contents
{: toc}

## Definition

+-- {: .num_defn #RelativelyKappaCompact}
###### Definition

For $\kappa$ some [[cardinal]], say a morphism $f : x \to y$ in $C$ is **relatively $\kappa$-compact** if for all [[(∞,1)-pullbacks]] along $h : y' \to y$ to $\kappa$-[[compact object in an (∞,1)-category|compact object]]s, $y'$, the pulled back object $h^* x'$ is itself a $\kappa$-compact object.

=--

## Characterization of $(\infty,1)$-toposes

+-- {: .num_theorem}
###### Theorem

A [[presentable (∞,1)-category]] $C$  is an [[(∞,1)-topos]] precisely if

1. it has [[universal colimits]];

1. for sufficiently large regular [[cardinal]]s $\kappa$, $C$ has a [[(sub)object classifier in an (infinity,1)-topos|classifying object]] for relatively $\kappa$-compact morphisms.

=--

+-- {: .num_lemma #RelativelyCompactInInfinityGroupods}
###### Lemma

In [[∞Grpd]] the relatively $\kappa$-compact morphisms, $X \to Y$, def. \ref{RelativelyKappaCompact} are precisely those all whose [[homotopy fibers]]

$$
  X_{y} := X \times_{Y} \{y\}
$$ 

over all [[objects]] $y \in Y$ are $\kappa$-[[small infinity-groupoids]].

=--

+-- {: .proof}
###### Proof

We may write $Y$ as an [[(∞,1)-colimit]] over itself (see there)

$$
  Y \simeq {\lim_{\to}}_{y \in Y} \{y\} 
$$

and then use the fact that [[∞Grpd]] -- being an [[(∞,1)-topos]] -- has 
[[universal colimits]], to obtain the [[(∞,1)-pullback]] diagram

$$
  \array{
    {\lim_{\to}}_{y \in Y} X_y 
      &\stackrel{\simeq}{\to}
     & X
    \\
    \downarrow && \downarrow
    \\
    {\lim_{\to}}_{y \in Y} \{y\}
    &\stackrel{\simeq}{\to}&
    Y
  }
$$

exhibiting $X$ as an $(\infty,1)$-colimit of $\kappa$-small objects
over $Y$. By stability of $\kappa$-compact objects under
$\kappa$-small colimits (see [here](http://ncatlab.org/nlab/show/compact+object+in+an+%28infinity%2C1%29-category#StabilityUnderColimits))
it follows that $X$ is $\kappa$-compact if $Y$ is. 

=--

This is due to [[Charles Rezk]]. The statement appears as [[Higher Topos Theory|HTT, theorem 6.1.6.8]].

[[!redirects relatively k-compact morphism in an (infinity,1)-topos]]

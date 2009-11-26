<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

An [[object]] $X$ of a [[category]] is **small** if it is $\kappa$-[[compact object|compact]] for some [[regular cardinal]] $\kappa$ (and therefore also for all greater regular cardinals as well). 

Here, $X$ is called $\kappa$-compact if the [[representable functor|corepresentable functor]] $hom(X,\cdot)$ preserves $\kappa$-[[directed colimit]]s.

## Details ##

We unwrap the definition further. Jet $J$ be a $\kappa$-filtered [[poset]], i.e. one in wich every sub-poset $J' \subset J$ of cardinality $|J'| \lt \kappa$ has an upper bound in $J$.

Let $C$ be a category and $F : J \to C$ a diagram, called a $\kappa$-filtered diagram. Let $X \in C$ be any [[object]].

Then the condition that $X$ commutes with the colimit over $F$ means that the map of [[hom-set]]s

$$
  \lim_{\to^j} Hom_C(X, F(j))
  \to 
  Hom_C(X,\lim_{\to^j} F(j))
$$

is not only an [[epimorphism]] (a [[surjection]]), which it is automatically as a coequalizer, but even an [[isomorphism]], i.e. a [[bijection]].

By the general properties of [[colimit]] (recalled at [[limits and colimits by example]]), the colimit

$$
  \lim_{\to^j} Hom_C(X,F(j))
$$

may be expressed as a [[coequalizer]]

$$
  \stackrel{\to}{\to} \coprod_{j \in J} Hom_C(X,F(j)) 
  \to
  \lim_{\to^j} Hom_C(X,F(j))
$$

hence as a [[quotient set]] of the the set of morphism in $C$ from $X$ into one of the objects $F(j)$. Being a quotient set, every element of it is _represented_ by one of the original elements in $\coprod_j Hom_C(X,F(j))$.

This means that we have

**Restatement**

The object $X$ commutes with the colimit over $F$ precisely if every morphism $X \to \lim_\to F$ lifts to a morphism $C \to F(j)$ into one of the $F(j)$, schematically:

$$
  \array{
    \cdots&\to&F(j-1) &\to& F(j) &\to& F(j+1) &\to& \cdots
    \\
    &&&{}^{\mathllap{\exists \hat f}}\nearrow&\downarrow & \swarrow
    \\
    &&X& \stackrel{f}{\to} &\lim_\to F
  }
  \,.
$$

## Properties ##

Let $\lambda \gt \kappa$ be a regular cardinal greater than $\kappa$.  Then any $\lambda$-filtered category $D$ is also $\kappa$-filtered.  For being $\lambda$-filtered means that any diagram in $D$ of size $\lt\lambda$ has a cocone; but any diagram of size $\lt\kappa$ is of course also $\lt\lambda$.  Thus, any $\lambda$-filtered colimit is also a $\kappa$-filtered colimit, so any functor which preserves $\kappa$-filtered colimits must in particular preserve $\lambda$-filtered colimits.  It follows that any $\kappa$-presentable object is also $\lambda$-presentable.

## Examples and applications ##

* By definition, in a [[locally presentable category]] every object is a [[colimit]] over small objects.

* Smallness of objects plays a crucial role in the [[small object argument]].

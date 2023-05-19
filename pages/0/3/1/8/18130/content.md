
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[topological space]] $(X,\tau)$ is called a _Kolmogorov space_ if it satisfies the $T_0$-[[separation axiom]], hence if for $x_1 \neq x_2 \in X$ any two distinct points, then at least one of them has an [[open neighbourhood]] $U_{x_i} \in \tau$ which does not contain the other point.

[[!include main separation axioms -- table]]

## Properties
 {#Properties}


### Alternative Characterizations

Regard [[Sierpinski space]] $\Sigma$ as a [[locale]] object in the category of topological spaces (meaning: the representable functor $Top(-, \Sigma): Top^{op} \to Set$ lifts through the monadic forgetful functor $Loc \to Set$ from the category of locales), hence as a [[dualizing object]] that induces a contravariant adjunction between locales and topological spaces. Thus for a space $X$, the locale $Top(X, \Sigma)$ is the locale of [[open sets]]; for a locale $L$, there is an accompanying topological space of points $Loc(L, \Sigma)$. The unit of the adjunction is called the double dual embedding.  

\begin{proposition}
A [[topological space]] $X$ is $T_0$ precisely when the double dual embedding $X \to Loc(Top(X, \Sigma), \Sigma)$ is a [[monomorphism]].
\end{proposition} 

The proof is trivial: the monomorphism condition translates to saying that for any points $x, y \in X$, if the truth values of $x \in U$ and $y \in U$ agree for every open set $U$, then $x = y$. 


[[!include main separation axioms -- as lifting properties]]


### Reflection

+-- {: .num_prop #KolmogorovQuotient}
###### Proposition
**(Kolmogorov quotient)**

Let $(X,\tau)$ be a [[topological space]]. Consider the [[relation]] on the underlying set by which $x_1 \sim x_1$ precisely if neither $x_i$ has an [[open neighbourhood]] not containing the other. This is an [[equivalence relation]]. The [[quotient topological space]] $X \to X/\sim$ by this
equivalence relation is a $T_0$-space. 

This construction is the reflector exhibiting Kolmogorov spaces as a [[reflective subcategory]] of the [[category]] [[Top]] of all topological spaces.

=--

## Related concepts

* [[Hausdorff topological space]]

* [[nice topological space]]

## References

* Wikipedia, _[Kolmogorov space](https://en.wikipedia.org/wiki/Kolmogorov_space)_


[[!redirects T0]]
[[!redirects T_0]]

[[!redirects Kolmogorov space]]
[[!redirects Kolmogorov spaces]]
[[!redirects T0 space]]
[[!redirects T0 spaces]]
[[!redirects T0-space]]
[[!redirects T0-spaces]]
[[!redirects T_0 space]]
[[!redirects T_0 spaces]]
[[!redirects T_0-space]]
[[!redirects T_0-spaces]]

[[!redirects Kolmogorov topological space]]
[[!redirects Kolmogorov topological spaces]]
[[!redirects T0 topological space]]
[[!redirects T0 topological spaces]]
[[!redirects T_0 topological space]]
[[!redirects T_0 topological spaces]]
[[!redirects T0-topological space]]
[[!redirects T0-topological spaces]]
[[!redirects T_0-topological space]]
[[!redirects T_0-topological spaces]]

[[!redirects Kolmogorov quotient]]
[[!redirects Kolmogorov quotients]]
[[!redirects T0 quotient]]
[[!redirects T0 quotients]]
[[!redirects T0-quotient]]
[[!redirects T0-quotients]]
[[!redirects T_0 quotient]]
[[!redirects T_0 quotients]]
[[!redirects T_0-quotient]]
[[!redirects T_0-quotients]]

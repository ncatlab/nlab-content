
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An ordinary [[category]] is _[[idempotent complete category|idempotent complete]]_, aka _[[Karoubi envelope|Karoubi complete]]_ or _[[Cauchy completion|Cauchy complete]]_ , if every [[idempotent]] splits.  Since the splitting of an idempotent is a limit *or* colimit of that idempotent, any category with [[finitely complete category|all finite limits]] or [[finitely cocomplete category|all finite colimits]] is idempotent complete.

In an [[(∞,1)-category]] the idea is the same, except that the notion of *idempotent* is more complicated.  Instead of just requiring that $e\circ e = e$, we need an [[equivalence]] $e\circ e \simeq e$, together with higher coherence data saying that, for instance, the two derived equivalences $e\circ e\circ e \simeq e$ are equivalent, and so on up.  In particular, *being idempotent* is no longer a [[stuff, structure, property|property]] of a morphism, but *structure* on it.

It is still true that a splitting of an idempotent in an $(\infty,1)$-category is a limit or colimit of that idempotent (now regarded as a diagram with all its higher coherence data), but this limit is no longer a finite limit; thus an $(\infty,1)$-category can have all finite limits without being idempotent-complete.


## Definition

+-- {: .num_defn}
###### Definition

Let for a linearly ordered set $J$ the simplicial set $\Delta^J:=N(J)$ be defined to be the nerve of $J$; i.e. $\Delta^J$ is given in degree $n$ given by nondecreasing maps $\{0,...,n\}\to J$.

The simplicial set $Idem^+$ is defined as follows: for every nonempty, finite, linearly ordered set J, $sSet(\Delta^J,Idem^+)$ can be identified with the set of pairs $(J_0,\sim)$, where $J_0\subseteq J$ and $\sim$ is 
an equivalence relation on $J_0$which satisfies the following condition: 

Let $i \le j \le k$ be elements of $J$ such that $i, k \in J_0$ , and $i \sim k$. Then $j \in J_0$ , and $i \sim j \sim k$.

Let $Idem$ denote the simplicial subset of $Idem^+$, corresponding to those pairs $(J_0 , \sim)$ such that $J = J_0$ . 
Let $Ret \subseteq Idem^+$ denote the simplicial subset corresponding to those pairs $(J_0 , \sim)$ such that the quotient 
$J_0 / \sim$ has at most one element. 

=--

([Lurie, 4.4.5.2 p.249](#Lurie))


+-- {: .num_defn}
###### Definition 

Let C be an $\infty$-category. 

1.  An idempotent in C is a map of simplicial sets $Idem \to C$. We will refer to $Fun(Idem, C)$ as the 
$\infty$-category of idempotents in $C$. 

1. A weak retraction diagram in $C$ is a map of simplicial sets $Ret \to C$. We will refer to $Fun(Ret, C)$ as 
the $\infty$-category of weak retraction diagrams in $C$. 

1. A strong retraction diagram in $C$ is a map of simplicial sets $Idem^+ \to C$. We will refer to $Fun(Idem+, C)$ 
as the $\infty$-category of strong retraction diagrams in $C$.
=--

([Lurie, 4.4.5.4 p.250](#Lurie))

## Properties

The following properties generalize those of idempotent-complete 1-categories.

+-- {: .num_theorem}
###### Theorem

A [[small (∞,1)-category]] is idempotent-complete if and only if it is [[accessible (∞,1)-category|accessible]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, 5.5.3.6]].

=--

+-- {: .num_theorem}
###### Theorem

For $C$ a [[small (∞,1)-category]] and $\kappa$ a [[regular cardinal]], the [[(∞,1)-Yoneda embedding]] $C \to C' \hookrightarrow Ind_\kappa(C)$ with $C'$ the full subcategory on $\kappa$-[[compact object]]s exhibits $C'$ as the idempotent completion of $C$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 5.4.2.4]].

=--

## Related concepts

* [[Karoubi envelope]]

* [[Cauchy completion]]


## References

Section 4.4.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
 {#Lurie}


[[!redirects idempotent complete (∞,1)-category]]
[[!redirects idempotent-complete (infinity,1)-category]]
[[!redirects idempotent-complete (∞,1)-category]]

[[!redirects idempotent-complete quasi-category]]
[[!redirects idempotent-complete quasi-categories]]

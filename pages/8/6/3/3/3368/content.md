
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
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

Let for a [[linear order|linearly ordered]] set $J$ the [[simplicial set]] $\Delta^J:=N(J)$ be defined to be the [[nerve]] of $J$; i.e. $\Delta^J$ is given in degree $n$ given by nondecreasing maps $\{0,...,n\}\to J$.

The [[simplicial set]] $Idem^+$ is defined as follows: for every nonempty, finite, linearly ordered set J, $sSet(\Delta^J,Idem^+)$ is the set of pairs $(J_0,\sim)$, where $J_0\subseteq J$ and $\sim$ is 
an [[equivalence relation]] on $J_0$ which satisfies the following condition: 

* Let $i \le j \le k$ be elements of $J$ such that $i, k \in J_0$ , and $i \sim k$. Then $j \in J_0$ , and $i \sim j \sim k$.

Let $Idem$ denote the simplicial subset of $Idem^+$, corresponding to those pairs $(J_0 , \sim)$ such that $J = J_0$ . 
Let $Ret \subseteq Idem^+$ denote the simplicial subset corresponding to those pairs $(J_0 , \sim)$ such that the quotient 
$J_0 / \sim$ has at most one element. 

=--

([Lurie, 4.4.5.2 p.249](#Lurie))


+-- {: .num_defn}
###### Definition 

Let C be an $\infty$-category, incarnated as a [[quasi-category]].  

1.  An **idempotent morphism** in C is a map of simplicial sets $Idem \to C$. We will refer to $Fun(Idem, C)$ as the 
**$(\infty,1)$-category of idempotents** in $C$. 

1. A **weak retraction diagram** in $C$ is a [[homomorphism]] of [[simplicial sets]] $Ret \to C$. We refer to $Fun(Ret, C)$ as 
the **$(\infty,1)$-category of weak retraction diagrams** in $C$. 

1. A **strong retraction diagram** in $C$ is a map of simplicial sets $Idem^+ \to C$. We will refer to $Fun(Idem+, C)$ 
as the **$(\infty,1)$-category of strong retraction diagrams** in $C$.

=--

([Lurie, 4.4.5.4 p.250](#Lurie))

+-- {: .num_defn}
###### Definition 

An idempotent $F \colon Idem \to C$ is **effective**  if it extends to a map $Idem^+ \to C$. 

=--

([Lurie, above corollary 4.4.5.14](#Lurie))

+-- {: .num_prop}
###### Proposition

An idempotent diagram $F \colon Idem \to C$ is effective precisely if it admits an [[(∞,1)-limit]], equivalently if it admits an [[(∞,1)-colimit]].

=--

By ([Lurie, lemma 4.3.2.13](#Lurie)).


+-- {: .num_defn}
###### Definition 

$C$ is called an **idempotent complete $(\infty,1)$** if every idempotent is effective.

=--

([Lurie, above corollary 4.4.5.14](#Lurie))

## Properties

The following properties generalize those of idempotent-complete 1-categories.

+-- {: .num_theorem}
###### Theorem

A [[small (∞,1)-category]] is idempotent-complete if and only if it is [[accessible (∞,1)-category|accessible]].

=--

This is [[Higher Topos Theory|HTT, 5.4.3.6]].


+-- {: .num_theorem}
###### Theorem

For $C$ a [[small (∞,1)-category]] and $\kappa$ a [[regular cardinal]], the [[(∞,1)-Yoneda embedding]] $C \to C' \hookrightarrow Ind_\kappa(C)$ with $C'$ the full subcategory on $\kappa$-[[compact object]]s exhibits $C'$ as the idempotent completion of $C$.

=--

This is [[Higher Topos Theory|HTT, lemma 5.4.2.4]].


## Coherent vs incoherent idempotents

We may also ask how idempotent-completeness of $C$ is related to that of its [[homotopy category]] $h C$.  An idempotent in $h C$ is an "incoherent idempotent" in $C$, i.e. a map $e:X\to X$ such that $e \sim e^2$, but without any higher coherence conditions.  In this case we have:

+-- {: .num_theorem}
###### Theorem
**([[Higher Algebra|HA]] Lemma 1.2.4.6)**
If $C$ is [[stable (infinity,1)-category|stable]], then $C$ is idempotent-complete (i.e. every coherent idempotent is effective) if and only if $h C$ is (as a 1-category).
=--

However, if $C$ is not stable, this is false.  The following counterexample in [[?Gpd]] is constructed in Warning 1.2.4.8 of [[Higher Algebra|HA]].  Let $\lambda : G \to G$ be an injective but non-bijective group homomorphism such that $\lambda$ and $\lambda^2$ are conjugate.  (One such is obtained by letting $G$ be the group of endpoint-fixing homeomorphisms of $[0,1]$, with $\lambda(g)$ acting as a scaled version of $g$ on $[0,\frac 1 2]$ and the identity on $[\frac 1 2,1]$.  Then $\lambda(g) \circ h = h \circ \lambda^2(g)$ for any $h$ such that $h(t) = 2t$ for $t \in [0,\frac 1 4]$.)

Then $B\lambda : B G \to B G$ is homotopic to $B\lambda^2$, hence idempotent in the homotopy category.  If it could be lifted to a coherent idempotent, then the colimit of the diagram
$$B G \xrightarrow{B \lambda} B G \xrightarrow{B \lambda} BG \to \cdots$$
would be its splitting, and hence the map $B G \to \colim (B G\xrightarrow{B \lambda} B G \to\cdots)$ would have a [[section]].  Passing to fundamental groups, $G \to \colim (G\xrightarrow{\lambda} G \to\cdots)$ would also have a section; but this is impossible as $\lambda$ is injective but not surjective.

However, we do have the following:

+-- {: .num_theorem}
###### Theorem
**([[Higher Algebra|HA]] Lemma 7.3.5.14)**
A morphism $e$ in an $(\infty,1)$-category $C$ is idempotent (i.e. $e:\Delta^1 \to C$ extends to $Idem$) if and only if there is a homotopy $h : e \sim e^2$ such that $h\circ 1 \sim 1\circ h$.
=--

In other words, an incoherent idempotent can be fully coherentified as soon as it admits one additional coherence datum.

## Related concepts

* [[Karoubi envelope]]

* [[Cauchy completion]]

* [noncommutative motives -- as universal additive invariants](noncommutative+motive#AsUniversalAditiveInvariant)


## References

Section 4.4.5 of

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
 

Formalization in [[homotopy type theory]]:

* {#Shulman14} [[Mike Shulman]], _[Splitting idempotents](http://homotopytypetheory.org/2014/12/08/splitting-idempotents/)_ 2014

[[!redirects idempotent complete (∞,1)-category]]
[[!redirects idempotent-complete (infinity,1)-category]]
[[!redirects idempotent-complete (∞,1)-category]]

[[!redirects idempotent-complete quasi-category]]
[[!redirects idempotent-complete quasi-categories]]

[[!redirects idempotent-completion of an (∞,1)-category]]
[[!redirects idempotent-completion of an (infinity,1)-category]]

[[!redirects idempotent complete (infinity,1)-categories]]
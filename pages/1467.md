
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Compact spaces
* table of contents
{: toc}

## Idea
 {#Idea}

A [[topological space]] (or more generally: a [[convergence space]]) is _compact_ if all [[sequences]] and more generally [[nets]] inside it [[convergence|converge]] as much as possible. 

Compactness is a topological notion that was developed to abstract the key property of a [[subspace]] of a [[Euclidean space]] being "[[closed space|closed]] and [[bounded set|bounded]]": *every [[net]] must [[accumulation point|accumulate]] somewhere in the subspace*. (Roughly, the reason is that boundedness implies the net cannot escape the subspace, and the point to which it accumulates lies in the subspace by closure. This is the statement of the _[[Heine-Borel theorem]]_, see there for for more.) 

Compactness provides an intrinsic way of formulating this property in the context of general topological spaces, without the need to view them as subspaces of an ambient space.  Still, it is common to work with _compact [[subsets]]_ of a given space.  These are those subsets which are compact spaces with the [[subspace topology]].

One often wishes to study [[compact Hausdorff spaces]] ("compacta") since these enjoy particularly useful properties. For instance they all arise as [[one-point compactifications]] (of [[locally compact Hausdorff spaces|locally compact]] [[Hausdorff spaces]], see [this remark](one-point+compactification#CompactHausdorffSpaceIsCompactificationOfComplementOfAnyPoint)).

As for most concepts related to [[topological spaces]], there is also a concept of compactness for _[[locales]]_. Observe that (using [[classical logic]]) every [[locally compact locale]] is aready [[spatial locale|spatial]] ([this prop.](locally+compact+locale#UsingClassicalLogicLocallyCompactLocaleIsSpatial)).
Instead of compact Hausdorff locales one usually considers compact [[regular space|regular]] locales, since regularity is easier to formulate and handle than Hausdorffness in locale theory (these are equivalent, since every locale is $T_0$ [[separation axiom|separated]] and hence $T_3$ if regular, while every Hausdorff space is $T_3$ if compact).



## Definitions/characterizations 

There are many ways to say that a space $X$ is compact. The first is perhaps the most common: 

+-- {: .num_defn #OpenCover}
###### Definition
**([[open cover]])**

Let $(X,\tau)$ be a [[topological space]]. Then an [[open cover]] is a [[set]] $\{U_i \subset X\}_{i \in I}$ of [[open subsets]] (i.e. $(U_i \subset X) \in \tau \subset P(X)$) such that their [[union]] is all of $X$

$$
  \underset{i \in I}{\cup} U_i = X
  \,.
$$

This is called a _[[finite open cover]]_ if $I$ is a (Kuratowski-)[[finite set]].

A _subcover_ of an open cover as above is a [[subset]] $J\subset I$ of the given open subsets, such that their union still exhausts $X$, i.e. $\underset{i \in J \subset I}{\cup} U_i = X$.

=--

+-- {: .num_defn #hb}
###### Definition
**(compact space)**

A [[topological space]] is called _compact_ if every [[open cover]] has a finite subcover (def. \ref{OpenCover}).

=-- 

For the purposes of exposition, this definition will be taken as the baseline definition. Throughout the remainder of this section we state a number of propositions of type "A space is compact (in the sense of Definition \ref{hb}) iff it satisfies property P", which can be read as saying that property P can be taken as an alternative definition of compactness (and may in fact be considered a more convenient or preferable definition over \ref{hb}, depending on author and context). 

+-- {: .num_remark #DifferingTerminology}
###### Remark
**(differing terminology)**

Some authors use "compact" to mean "compact and [[Hausdorff topological space|Hausdorff]]" (a much [[nice topological space|nicer sort of space]], and forming a much [[nice category of spaces|nicer category of spaces]], see at _[[compact Hausdorff space]]_), and use the word "[[quasicompact]]" to refer to just "compact" as we are using it here. This custom seems to be prevalent among [[algebraic geometry|algebraic geometers]], for example, and particularly so within Francophone schools.

> But it is far from clear to me ([[Todd Trimble]]) that "quasicompact" is very well-established outside such circles (despite some arguments in favor of it), and using simply "compact" for the nicer concept therefore carries some risk of creating misunderstanding among mathematicians at large. My own habit at any rate is to say "compact Hausdorff" for the nicer concept, and I will continue using this on the $n$Lab until consensus is reached (if that happens).

Another term in usage is 'compactum' to mean a [[compact Hausdorff space]] (even when 'compact' is not used to imply Hausdorffness).

=-- 

The various reformulations of compactness fall into several families. Some are more or less tautological reformulations based on direct logical or set-theoretic manipulations of the open covering definition; we give these first. Others express compactness in terms of notions of convergence (nets, filters, ultrafilters). A third family expresses compactness of a space in terms of "stable" properties of maps sourced is that space; this is perhaps the most intrinsically categorical of the three families. 

### Elementary reformulations 

If [[excluded middle]] is assumed, then def. \ref{hb} has the following reformulations in terms of [[closed subsets]]:

+-- {: .num_prop #fip}
###### Proposition
**(compactness in terms of closed subsets)**

Let $(X,\tau)$ be a [[topological space]]. 
Assuming [[excluded middle]], then the following are equivalent:

1. $(X,\tau)$ is compact in the sense of def. \ref{hb}.

1. Let $\{C_i \subset X\}_{i \in I}$ be a set of [[closed subsets]] such that their [[intersection]] is [[empty set|empty]] $\underset{i \in I}{\cap} C_i = \emptyset$, then there is a [[finite set|finite]] [[subset]] $J \subset I$ such that the corresponding finite intersection is still empty: $\underset{i \in  J \subset i}{\cap} C_i = \emptyset$.
   
1. Let $\{C_i \subset X\}_{i \in I}$ be a set of [[closed subsets]] such that it enjoys the  _[[finite intersection property]]_, meaning that for every [[finite set|finite]] [[subset]] $J \subset I$ then the corresponding finite intersection is [[inhabited set|non-empty]] $\underset{i \in J \subset I}{\cap} C_i \neq \emptyset$. Then also the total intersection is [[inhabited set|inhabited]], $\underset{i \in I}{\cap} C_i \neq \emptyset$.


=--

+-- {: .proof}
###### Proof

The equivalence of the first two statements follows by [[de Morgan's law]] ([[complements]] interchange [[unions]] with [[intersections]]), the definition of [[closed subsets]] as the complements of [[open sets]], and (using [[excluded middle]]) that dually the complements of closed subsets are the open subsets:

Let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]]. Write $C_i \coloneqq X \backslash U_i$ for the corresponding closed complements. By [[de Morgan's law]] the condition that $\underset{i \in I}{\cup} U_i = X$ is equivalent to $\underset{i \in I}{\cap} C_i = \emptyset$. The second statement is that there is then a finite subset $J \subset I$ such that also $\underset{i \in J \subset I}{\cap} C_i = \emptyset$, and under forming complements again this is equivalently the first statement.

Then statement 3 is the [[contraposition]] of the second, and contrapositives are equivalent under [[excluded middle]].

=-- 

The closed-subset formulations of compactness appear frequently and are often more convenient. For example, [[compactness theorems]] in [[model theory]] draw on a connection between the finite intersection property and finite satisfiability of sets of axioms. 

### Compactness for locales 

In another direction, the definition (\ref{hb}) also works for [[locales]], since it refers only to the [[frame]] of open sets.  Here is an equivalent way to phrase it that is often convenient for locale theory. 

+-- {: .num_prop #directed}
###### Proposition

$X$ is compact iff given any [[direction|directed]] collection of opens whose union is $X$ (a directed open cover), $X$ belongs to the collection.

=-- 

+-- {: .proof} 
###### Proof 
For the "only if" direction: if $\mathcal{U}= \{U_i\}_{i \in I}$ is a directed open cover, then by the open-cover definition of compactness, $X$ is the union of finitely many $U_i$. But by definition of directedness, any finite subfamily of $\mathcal{U}$ has an upper bound in $\mathcal{U}$; since the only upper bound of $X$ is $X$, it follows that $X$ belongs to $\mathcal{U}$. 

For the "if" direction: given an open cover $\mathcal{U}$ of $X$, let $\mathcal{U}'$ be the family of open sets that are unions of finite subfamilies of $\mathcal{U}$. This $\mathcal{U}'$ is clearly directed, and an open cover of $X$ since $\mathcal{U}$ is. By hypothesis, $X$ belongs to $\mathcal{U}'$, so $X$ is a union of finitely many elements of $\mathcal{U}$. This shows $X$ is compact according to Definition \ref{hb}. 
=-- 

As the union is a [[colimit]] in the [[category of open subsets]] $Op(X)$, we can also say

+-- {: .num_prop #object}
###### Proposition

$X$ is compact iff it is a [[compact object]] in $Op(X)$.

=-- 

+-- {: .proof} 
###### Proof 
To say $X$ is a compact object means that $\hom(X, -): Op(X) \to Set$ preserves [[filtered colimits]], or colimits of filtered diagrams. Here we may as well replace $Set$ by the full subcategory consisting of $0, 1$ (a $0$-element set or a $1$-element set) since the hom-sets for posets are of size $0$ or $1$. Further, 
in a [[poset]] like $Op(X)$, a filtered diagram is the same as a nonempty directed diagram $D$, and $\hom(X, \bigcup_{d \in D} d)$ has size $1$ iff $X = \bigcup_{d \in D} d$. On the other hand, $\bigcup_{d \in D} \hom(X, d)$ has size $1$ iff $X = d$ for some $d$ in $D$. Thus that $\hom(X, -)$ preserves filtered colimits amounts to the same thing as saying $X$ belongs to any directed open cover $D$, which is the same as compactness by Proposition \ref{directed}. 
=-- 


### Compactness via convergence 

If the [[ultrafilter theorem]] (a weak form of the [[axiom of choice]]) is assumed, compactness may be characterized in terms of [[ultrafilter]] (or ultranet) [[convergence]]: 

+-- {: .num_prop #ultrafilter}
###### Proposition

$X$ is compact iff every [[ultrafilter]] $\mathcal{U}$ (or ultranet $\nu$) on $X$ [[converges|converges]] to some point $x \in X$, meaning that $\mathcal{U}$ contains the filter of [[neighborhoods]] of $x$ (or that $\nu$ is eventually in any neighbourhood of $x$).

=--

In any case, compactness can be characterized in terms of [[proper filter]] or equivalently (see at _[[eventuality filter]]_) of [[net]] [[convergence]] . 

+-- {: .num_prop #refinement}
###### Proposition

$X$ is compact iff every [[proper filter]]/[[net]] on $X$ has a [[convergence|convergent]] proper [[refinement]]/[[subnet]].

=--

This is equivalent to the characterization given in the [Idea-section](#Idea) above:
 
+-- {: .num_prop #clustering}
###### Proposition

$X$ is compact iff every proper filter $\mathcal{U}$ (or net $\nu$) on $X$ has a cluster point $x$, meaning that every element of $\mathcal{U}$ meets (has [[inhabited set|inhabited]] intersection with) every neighbourhood of $x$ (or $\nu$ is frequently in every neighbourhood of $x$).

=-- 

While the usual definitions (\ref{hb}&\ref{fip}) are for [[topological spaces]], the convergence definitions (\ref{ultrafilter}--\ref{clustering}) make sense in any [[convergence space]]. 

### Compactness via completeness

+-- {: num_prop #completeness}
A [[uniform space]] $X$ is compact if and only if it is [[complete space|complete]] and [[totally bounded space|totally bounded]].  Moreover, a compact Hausdorff topological space has a unique compatible uniformity, which is complete and totally bounded.
=--

In [[constructive mathematics]], "complete and totally bounded" is sometimes taken as a substitute for open-cover compactness (to which it is no longer equivalent); see [[Bishop-compact space]].

### Compactness via stability properties 

Frequently in [[category theory]], for example when we discuss [[internal logic]] in [[toposes]], we are interested in properties of maps that are stable under [[pullback]], and it turns out that compactness can be reformulated in terms of stability properties. 

A first example concerns the property of a topological space $X$ that the unique map $!: X \to 1$ to the [[point space]] (the [[terminal object]] in [[Top]]) is a [[closed map]]. As a statement in ordinary [[point-set topology]], this is plainly a [[tautology]], trivially true for any space $X$. (Side remark: it is not at all a tautology in the more general setting of [[internal locales]] in [[toposes]]; the word "closed" is reserved for locales $X$ having that property. See also _[[closed morphism]]_.) However, even in ordinary point-set topology, $!: X \to 1$ is usually not *stably closed*. In more detail: the pullback of $!: X \to 1$ along a (or the) map $Y \to 1$ is the [[projection]] map 

$$X \times Y \to Y$$ 

out of the [[product topological space]] and the issue is whether this map is closed. This leads us to the following proposition. 

+-- {: .num_defn #projection}
###### Proposition
**([[closed-projection characterization of compactness]])**

A topological space $X$ is compact (def. \ref{hb}) precisely if for any topological space $Y$, the [[projection map]] $X \times Y \to Y$ out of their [[product topological space]] is [[closed map|closed]]. 

=-- 

Thus, compactness of $X$ is equivalent to $!: X \to 1$ being stably closed. 
For a **proof**, see *[[closed-projection characterization of compactness]]*. 

+-- {: .num_remark}
###### Remark

Contrary to possible appearance, the equivalence in prop. \ref{projection} does not require the [[axiom of choice]]; see [this MO question](http://mathoverflow.net/questions/42186/does-compact-iff-projections-are-closed-require-some-form-of-choice/42196) and answers, as well as [this page](/toddtrimble/published/Characterizations+of+compactness). See also the page [[compactness and stable closure]] (under construction).  This equivalence is also true for [[locales]], by way of proper maps; see below. 

Moreover, the characterization of compact spaces via prop. \ref{projection} may be used to give an attractive proof of the [[Tychonoff theorem]], due to Clementino and Tholen. See [here](https://ncatlab.org/nlab/show/closed-projection%20characterization%20of%20compactness) for details. 

=--

Of course, the notion of being stably closed applies to maps $p: X \to Y$ besides $!: X \to 1$. An analysis of this notion (that the pullback $f^\ast p: X \times_Y Z \to Z$ is a closed map for every map $f: Z \to Y$) leads to the correct notion of [[proper map]] in [[algebraic geometry]] and elsewhere. 

Closely related to [[closed-projection characterization of compactness]], a characterisation of compactness in terms of logical [[quantification]] is featured in [[Paul Taylor]]'s [[Abstract Stone Duality]]:

+-- {: .num_prop #quantification}
###### Proposition

$X$ is compact iff for any space $Y$ and any open subset $U$ of $X \times Y$, the subset
$$ \forall_X U = \{ b : Y \;|\; \forall\; a: X,\; (a, b) \in U \} $$
is open in $Y$.

=--

To remove it from dependence on points, we can also write the definition like this:

+-- {: .num_defn #pointless}
###### Definition
$X$ is compact iff given any space $Y$ and any open $U$ in $X \times Y$, there exists an open $\forall_X U$ in $Y$ that satisfies the [[universal property]] of universal [[quantification]]:
$$ V \subseteq \forall_X U \;\Leftrightarrow\; X \times V \subseteq U $$
for every open $V$ in $Y$.
=--

A [[de Morgan duality|dual]] condition is satisfied by an [[overt space]].

## Properties

### Various

+-- {: .num_prop #UnionsAndIntersectionOfCompactSubspaces}
###### Proposition
**(unions and intersection of compact spaces)**

Let $(X,\tau)$ be a [[topological space]] and let 

$$
  \{K_i \subset X\}_{i \in I}
$$ 

be a [[set]] of [[compact topological space|compact]] [[subspaces]]. 

1. If $I$ is a [[finite set]], then the [[union]] $\underset{i \in I}{\cup} K_i \subset X$ is itself a compact subspace;

1. If all $K_i \subset X$ are also [[closed subsets]] then their [[intersection]] $\underset{i \in I}{\cap} K_i \subset X$ is itself a compact subspace. 

=--

+-- {: .proof}
###### Proof

Regarding the first statement:

Let $\{U_j \subset X\}_{j \in J}$ be an [[open cover]] of the union. Then this is also an open cover of each of the $K_i$, hence by their compactness there are finite subsets $J_i \subset J$ such that $\{U_{j_i} \subset X\}_{j_i \in J_i}$ is a finite cover of $K_i$. Accordingly then $\underset{i \in I}{\cup} \{ U_{j_i} \subset X \}_{j_i \in J_i}$ is a finite open cover of the union.

Regarding the second statement:

By the axioms on a [[topological space|topology]], the intersection of an arbitrary set of [[closed subsets]] is again closed. Hence the intersection of the closed compact subspaces is closed. But since [[subsets are closed in a closed subspace precisely if they are closed in the ambient space]] then for each $i \in I$ the intersection is a closed subspace of the compact space $K_i$. Since [[closed subspaces of compact spaces are compact]] it follows that the intersection is actually compact, too.

=--

+-- {: .num_prop #IntersectionCompactWithOpen}
###### Proposition
**(complements of compact with open subspaces is compact)**

Let $X$ be a [[topological space]]. Let

1. $K\subset X$ be a [[compact topological space|compact]] [[subspace]];

1. $U \subset X$ be an [[open subset]].

Then the [[complement]]

$$
  K \setminus U \subset Xcov
$$

is itself a compact subspace.

=--

+-- {: .proof #ProofIntersectionCompactWithOpen}
###### Proof

Let $\{V_i \subset K \setminus U\}$ be an [[open cover]] of the complement subspace. We need to show that this admits a finite subcover.

Observe that by definition of the [[subspace topologies]] on $K \setminus U$  and on $K$:

1. the $V_i \subset K \setminus U$ are still open when regarded as subsets $V_i \subset K$ of $K$;

1. also the intersection $K \cap U \subset K$ is an open subset of the compact subspace $K$. 

This means that

$$
  \{ 
    V_i \subset K
  \}_{i \in I}
  \sqcup 
   (U \cap K)
$$

is an [[open cover]] of $K$. Hence by the compactness of $K$, this has a finite subcover. If $U \cap K$ is retained in this subcover then it is of the form

$$
  \{ V_j \subset K\}_{j \subset J} \sqcup (U \cap K)
$$

otherwise it is of the form

$$
  \{ V_j \subset K\}_{j \subset J} 
$$


with $J \subset I$ a [[finite set|finite]] [[subset]]. 

Since either of these is still a cover, also their restriction from $K$ to $K \setminus U$ is a cover of $K \setminus U$. But by assumption the $V_j$ are already restricted to $K \setminus U$, while the restriction of $(U \cap K)$ to $K \setminus U$ is empty. Therefore in either of the above cases we find that 

$$
  \{ V_j \subset K \setminus U\}_{j \subset J} 
$$

is a finite subcover of the original open cover of $K \setminus U$. Therefore $K \setminus U$ is compact.


=--

+-- {: .num_prop #ProductOfCompactSpacesIsCompact}
###### Proposition

Assuming the [[axiom of choice]], the category of compact spaces admits all small [[products]]. And, even without the axiom of choice, the category of compact locales admits all small products. 

=-- 

\begin{proof}
The first statement follows from the [[Tychonoff theorem]]: every [[product topological space]] of compact spaces is itself again compact.
\end{proof}

+-- {: .num_remark} 
###### Remark 
However, the category of compact spaces does not admit [[equalizers]]. An explicit example is where one takes two maps $[0, 1] \to \{0, 1\}$ where the codomain is [[Sierpinski space]], where one of the maps $f$ has $f^{-1}(1) = [0, 1/2)$, and the other is the constant map at $1$. If an equalizer in $Comp$ existed, then $\hom(1, -): Comp \to Set$ would have to preserve it, so set-theoretically it would have to be $[0, 1/2)$. The topology on $[0, 1/2)$ would then have to be the same as or finer than the subspace topology in order for the equalizer map to be continuous. But if the subspace topology isn't compact, then no finer topology would make it compact either. (Here we are invoking the contrapositive of the proposition that if $(X, \tau)$ is compact and $\tau' \subseteq \tau$ is a coarser topology, then $(X, \tau')$ is also compact.) 

On the other hand, the category of [[compactum|compact Hausdorff spaces]] does admit all [[limits]], and this fact does not require the full strength of the axiom of choice, but only a weaker choice principle called the [[ultrafilter principle]]. 
=-- 


+-- {: .num_prop }
###### Proposition

The direct [[image]] of a compact subspace under a [[continuous map]] is compact. A topological space becomes a [[bornological set]] by taking the bounded sets to be subsets contained in some compact subspace, and under this bornology, every continuous function is a bounded map.

If the spaces in question are $T_1$, then the sets with compact closure also constitute a bornology and continuous maps become bounded. In a non-Hausdorff situation these bornologies might differ because the closure of a compact set need not be compact.

=--


+-- {: .num_prop }
###### Proposition

A compact [[Hausdorff space]] must be [[normal space|normal]].  That is, the [[separation axioms]] $T_2$ through $T_4$ (when interpreted as an increasing sequence) are equivalent in the presence of compactness.

=--


+-- {: .num_prop }
###### Proposition

The [[Heine-Borel theorem]] asserts that a subspace $S \subset \mathbb{R}^n$ of a [[Cartesian space]] is compact precisely if it is [[closed subset|closed]] and [[bounded subset|bounded]].

=--

+-- {: .num_prop }
###### Proposition

We have:

1. [[compact subspaces of Hausdorff spaces are closed]].

1. [[closed subsets of compact spaces are compact]]

Hence:

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

=--

+-- {: .num_prop}
###### Proposition

[[sequentially compact metric spaces are equivalently compact metric spaces]]

[[countably compact metric spaces are equivalently compact metric spaces]]

[[compact spaces equivalently have converging subnet of every net]]

=--

+-- {: .num_prop}
###### Proposition

[[continuous images of compact spaces are compact]]

=--

+-- {: .num_prop}
###### Proposition

[[maps from compact spaces to Hausdorff spaces are closed and proper]]

=--

+-- {: .num_prop}
###### Proposition

[[continuous metric space valued function on compact metric space is uniformly continuous]]

=--



### Relation to compact objects in $Top$

One might expect that compact topological spaces are precisely the [[compact objects]] in [[Top]] in the abstract sense of [[category theory]], but this identification requires care, the naive version fails. See at _[compact object -- Compact objects in Top](compact+object#CompactObjectsInTop)_


## Examples

### General
 {#ExamplesGeneral}

+-- {: .num_prop }
###### Proposition

A [[discrete space]] is compact iff its underlying set is [[finite set|finite]].  

In [[constructive mathematics]], a discrete space is compact iff its underlying set is [[Kuratowski-finite]].

=--



+-- {: .num_example #CompactClosedInterval}
###### Example
**([[closed intervals]] are [[compact topological space|compact]])**

For any $a \lt b \in \mathbb{R}$ the [[closed interval]]

$$
  [a,b] \subset \mathbb{R}
$$

regarded with its [[topological subspace|subspace topology]]
of [[Euclidean space]] with its [[metric topology]] is
a compact topological space.

=--

(See [[closed intervals are compact topological spaces]].)  



In contrast:

+-- {: .num_example}
###### Nonexample

For all $n \in \mathbb{N}$, $n \gt 0$, the [[Euclidean space]] $\mathbb{R}^n$, regarded with its [[metric topology]], is _not_ compact.

=--

This is a special case of the [[Heine-Borel theorem]] (example \ref{HeineBorelTheorem} below), but for illustration it is instructive to consider the direct proof:

+-- {: .proof}
###### Proof

Pick any $\epsilon \in (0,1/2)$. Consider the open cover of $\mathbb{R}^n$ given by

$$
  \left\{
      U_n \coloneqq
     (n-\epsilon, n+1+\epsilon)
     \times
     \mathbb{R}^{n-1}
     \;\subset\;
     \mathbb{R}^{n+1}
  \right\}_{n \in \mathbb{Z}}
  \,.
$$

This is not a finite cover, and removing any one of its patches $U_n$, it ceases to be a cover, since the points of the form $(n + \epsilon, x_2, x_3, \cdots, x_n)$ are contained only in $U_n$ and in no other patch.

=--


+-- {: .num_example}
###### Example

By the [[Tychonoff theorem]], every [[product topological spaces]] of compact spaces is again compact. 

=--

This implies the [[Heine-Borel theorem]], saying that:

+-- {: .num_example #HeineBorelTheorem}
###### Example
**([[Heine-Borel theorem]])**

Every [[bounded subset|bounded]] and [[closed subspace]] of a [[Euclidean space]] is compact.

=--

In particular:

+-- {: .num_example}
###### Nonexample

The [[open intervals]] $(a,b) \subset \mathbb{R}$ and the [[half-open intervals]] $[a,b)  \subset \mathbb{R}$ and $(a,b] \subset \mathbb{R}$ are not compact.

=--

+-- {: .num_example }
###### Example

The [[Mandelbrot set]], regarded as a [[subspace]] of the [[plane]], is a compact space (see [this prop.](/nlab/show/Mandelbrot+set#MndlbrtIsCompact)). 

=--

+-- {: .num_example} 
###### Example 
Any set when equipped with the [[cofinite topology]] forms a compact space. This space is also $T_1$ (i.e., [[singletons]] are closed), but is not Hausdorff if the underlying set is [[infinite set|infinite]]. 
=-- 



### Compact spaces which are not sequentially compact
 {#CompactSpacesWhichAreNotSequentiallyCompact}

A famous example of a space that is compact, but not [[sequentially compact space|sequentially compact]] is the product space
$$
    \{0,1\}^{I} \coloneqq \{0, 1\}^{[0, 1]}
  \coloneqq \underset{[0,1]}{\prod} \{0,1\}
$$
with the [[product topology]]. 

This space is compact by the [[Tychonoff theorem]].

But it is not [[sequentially compact topological space|sequentially compact]]. We now discuss why. (We essentially follow [Steen-Seebach 70, item 105](#SteenSeebach70)).
 
Points of $\{0,1\}^{I}$ are functions $I \to \{0,1\}$, and the product topology is the topology of pointwise convergence.

Define a sequence $(a_n)$ in $I^{I}$ with $a_n(x)$ being the nth digit in the binary expansion of $x$ (we make the convention that binary expansions do not end in sequences of $1$s).  Let $a \coloneqq (a_{n_k})$ be a subsequence and define $p_a \in I$ by the binary expansion that has a $0$ in the $n_k$th position if $k$ is even and a $1$ if $k$ is odd (and, for definiteness and to ensure that this fits with our convention, define it to be $0$ elsewhere).  Then the projection of $(a_{n_k})$ at the $p_a$th coordinate is $1, 0, 1,0,...$ which is not convergent.  Hence $(a_{n_k})$ is not convergent.

(Basically that's the diagonal trick of [[Cantor's theorem]]).

However, as $\{0,1\}^I$ is compact, $a$ has a [[convergence|convergent]] [[subnet]].  An explicit construction of a convergent subset, given a [[cluster point]] $a$, is as follows.  A function $a \colon I \to \{0,1\}$ is a [[cluster point]] of $(a_n)$ if, for any $p_1, \dots, p_n \in I$ the set

$$
A(p_1,\dots,p_n) \coloneqq \{k \in \mathbb{R} : a_k(p_i) = a(p_i) \forall i\}
$$

is infinite.  We index our subnet by the family of finite subsets of $I$ and define the subnet function $\mathcal{F}(I) \to \mathbb{N}$ to be

$$
\{p_1,\dots,p_n\} \mapsto \min A(p_1,\dots,p_n)
$$

This is a convergent sub-[[net]].




## In synthetic topology

In [[synthetic topology]], where 'space' means simply 'set' (or [[type]], i.e. the basic objects of our foundational system), one natural notion of "compact space" is a [[covert set]], i.e. a set whose discrete topology is covert.  This includes the expected examples in various [[gros toposes]].


## Compact spaces and proper maps

A space $X$ is compact if and only if the unique map $X\to 1$ is [[proper map|proper]].  Thus, properness is a "relativized" version of compactness.

For topological spaces, this is either a definition of "proper map" (closed with compact fibers) or follows from the above characterization of compactness in terms of projections being closed maps (if proper maps are defined to be those that are universally closed).  For locales, it follows from the definition of proper map (a closed map such that $f_*$ preserves directed joins) and the fact that compact locales are automatically [[covert space|covert]] (see [[covert space]] for a proof).


## Related concepts

* [[Lebesgue number lemma]]

* [[sequentially compact topological space]], [[countably compact topological space]], [[paracompact topological space]], [[locally compact topological space]], [[strongly compact topological space]], [[compactly generated topological space]]

* [[compactification]]

  * [[one-point compactification]]

  * [[Stone-Cech compactification]]

* [[compact-open topology]]

* [[closed manifold]]

* [[compact topos]]

* [[compactly supported cohomology]]

* [[complete algebraic variety]]


## References

Examples of compact spaces that are not sequentially compact are in

* {#SteenSeebach70} Lynn Steen, J. Arthur Seebach, _Counterexamples in Topology_, Springer-Verlag, New York (1970) 2nd edition,  (1978), Reprinted by Dover Publications, New York, 1995

On compact [[metric spaces]]:

* Roland Speicher, _Compact metric spaces_ ([pdf](http://www.mast.queensu.ca/~speicher/Chapter10.pdf))

* Alan Sokal, _Compactness of metric spaces_ ([pdf](http://www.ucl.ac.uk/~ucahad0/3103_handout_2.pdf))

For [[proper base change theorem]] e.g.

* {#Milne} [[James Milne]], section 17 of _[[Lectures on Étale Cohomology]]_
 


[[!redirects compact space]]
[[!redirects compact spaces]]
[[!redirects compact topological space]]
[[!redirects compact topological spaces]]
[[!redirects compact convergence space]]
[[!redirects compact convergence spaces]]
[[!redirects compact locale]]
[[!redirects compact locales]]

[[!redirects compact manifold]]
[[!redirects compact manifolds]]

[[!redirects compact subspace]]
[[!redirects compact subspaces]]
[[!redirects compact subset]]
[[!redirects compact subsets]]
[[!redirects compact set]]
[[!redirects compact sets]]

[[!redirects compact]]

[[!redirects compactness]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# The separation axioms
* table of contents
{: toc}

## Idea
 {#Idea}

The plain definition of _[[topological space]]_ happens to allow examples where distinct points or distinct subsets of the underlying set of a topological space appear as as more-or-less unseparable as seen by the topology on that set. In many applications one wants to exclude at least some of such degenerate examples from the discussion. The relevant conditions to be imposed on top of the plain [[axioms]] of a [[topological space]] are hence known as _separation axioms_.

These axioms are all of the form of saying that two subsets (of certain forms) in the topological space are 'separated' from each other in one sense if they are 'separated' in a (generally) weaker sense. For example the weakest axiom (called $T_0$) demands that if two points are distinct as elements of the underlying set of points, then there exists at least one [[open subset]] that contains one but not the other.

In this fashion one may impose a hierarchy of stronger axioms. For example demanding that given two distinct points, then each of them is contained in some open subset not containing the other ($T_1$) or that such a pair of open subsets around two distinct points may in addition be chosen to be disjoint ($T_2$). This last condition, $T_2$, also called the _[[Hausdorff topological space|Hausdorff condition]]_ is the most common among all separation axioms. Often (but by far not always) this is considered by default.

Originally there were four separation axioms $T_1, T_2, T_3, T_4$; nowadays one considers various more. Besides the extrapolation of the original sequence from $T_0$ through $T_6$ (with $T_{2\frac{1}{2}}$ and $T_{3\frac{1}{2}}$ interpolated), there is a similar sequence of axioms called $R_0, R_1, R_2, R_3$ (with their extrapolations and interpolations) of the same form, except that they do not start with mentioning two set-theoretically distinct points, but two points satisfying the conclusion of $T_0$. This and more is spelled out [below](#TheClassicalTheory).

There are also axioms that do not follow the pattern of "if certain two subsets are separated in some weak sense, then they are also separated in some stronger sense", but that still axiomatize some kind of separatedness. For example the condition on a [[topological space]] being [[sober topological space|sober]] is of a different nature, but is implied by $T_2$ and implies $T_0$. Notice that via their [[full subcategory|full embdding]] into [[locales]], [[sober topological spaces]] may be understood without reference to their underlying set pf points at all.

All separation axioms are satisfied by [[metric spaces]], from whom the concept of topological space was originally abstracted. Hence imposing some of them may also be understood as gauging just how far one allows topological spaces to generalize away from metric spaces

Several separation axioms may also be interpreted in broader contexts that plain topological spaces, for instance for [[convergence space]] or for [[locales]]; or the may be considered under weaker assumptions, such as those of [[constructive mathematics]] and [[predicative mathematics]].



## The classical theory
 {#TheClassicalTheory}

First, we will consider how, for topological spaces in [[classical mathematics]], the separation axioms are about sets\' being 'separated' as stated above.  Throughout, fix a [[topological space]] $S$.


### Separation conditions

Fix two sets ([[subsets]]) $F$ and $G$ of $S$.

*  The sets $F$ and $G$ are __[[disjoint sets|disjoint]]__ if their [[intersection]] is [[empty set|empty]]:
   $$ F \cap G = \empty .$$
*  They are __topologically disjoint__ if there exists a [[neighbourhood]] of one set that is disjoint from the other set:
   $$ (\exists\; U \stackrel{\circ}\supseteq F,\; U \cap G = \empty) \;\vee\; (\exists\; V \stackrel{\circ}\supseteq G,\; F \cap V = \empty) .$$
   Notice that topologically disjoint sets must be disjoint.
*  They are __separated__ if each set has a neighbourhood that is disjoint from the other set:
   $$ (\exists\; U \stackrel{\circ}\supseteq F,\; U \cap G = \empty) \;\wedge\; (\exists\; V \stackrel{\circ}\supseteq G,\; F \cap V = \empty)
   \;\;\equiv\;\;
   \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap G = \empty \;\wedge\; F \cap V = \empty .$$
   Notice that separated sets must be topologically disjoint.

*  {#SeparatedByNeighbourhoods} They are __separated by neighbourhoods__ if they have disjoint neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; U \cap V = \empty .$$
   Notice that sets separated by neighbourhoods must be separated.

*  They are __separated by closed neighbourhoods__ if they have disjoint closed neighbourhoods:
   $$ \exists\; U \stackrel{\circ}\supseteq F,\; \exists\; V \stackrel{\circ}\supseteq G,\; Cl(U) \cap Cl(V) = \empty .$$
   Notice that sets separated by closed neighbourhoods must be separated by neighbourhoods.
*  They are __separated by a function__ if there exists a continuous [[real number|real]]-valued [[function]] on the space that maps $F$ to $0$ and $G$ to $1$:
   $$ \exists\; f: S \to \mathbf{R},\; F \subseteq f^*(\{0\}) \;\wedge\; G \subseteq f^*(\{1\}) .$$
   Notice that sets separated by a function must be separated by closed neighbourhoods (the preimages of $[-\epsilon, \epsilon]$ and $[1-\epsilon, 1+\epsilon]$).
*  Finally, they are __precisely separated by a function__ if there exists a continuous real-valued function on the space that maps precisely $F$ to $0$ and $G$ to $1$:
   $$ \exists\; f: S \to \mathbf{R},\; F = f^*(\{0\}) \;\wedge\; G = f^*(\{1\}) .$$
   Notice that sets precisely separated by a function must be separated by a function.

Often $F$ and $G$ will be points (identified with their [[singleton]] subsets); in that case, one usually says _distinct_ in place of _disjoint_.

Often $F$ or $G$ will be closed sets; notice that disjoint closed sets are automatically separated, while a closed set and a point, if disjoint, are automatically topologically disjoint.


### Separation axioms

The classical separation axioms are all statements of the form

*  When $F$ is a (point/closed) set and $G$ is a (point/closed) set, if $F$ and $G$ are (separated in some weak sense), then they are (separated in some strong sense).

The axioms with names (at least with known to the authors so far of this article) are summarised in the tables below.  When a row or column is missing from a table, either no name is known or the implication follows from the converses mentioned after the separation conditions above in the context of that table; there are two potential tables that are completely blank for the latter reason.  When an entry in a table is repeated, that corresponds to a theorem that one separation axiom implies another.

When both sets are points:
<table><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Distinct</th> <th>Topologically distinct</th></tr>
<tr><th>Topologically distinct</th> <td markdown="1">$T_0$</td></tr>
<tr><th>Separated</th> <td markdown="1">$T_1$</td> <td markdown="1">$R_0$</td></tr>
<tr><th>Separated by neighbourhoods</th> <td markdown="1">$T_2$</td> <td markdown="1">$R_1$</td></tr>
<tr><th>Separated by closed neighbourhoods</th> <td markdown="1">$T_{2\frac{1}{2}}$</td> <td markdown="1">$R_{1\frac{1}{2}}$</td></tr>
<tr><th>Separated by a function</th> <td markdown="1">Completely $T_2$</td> <td markdown="1">Completely $R_1$</td></tr></table>

When one set is a point and the other is closed:
<table markdown="1"><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Disjoint</th></tr>
<tr><th>Separated by neighbourhoods</th> <td>Regular</td></tr>
<tr><th>Separated by closed neighbourhoods</th> <td>Regular</td></tr>
<tr><th>Separated by a function</th> <td>Completely regular</td></tr></table>

When both sets are closed:
<table markdown="1"><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Disjoint</th></tr>
<tr><th>Separated by neighbourhoods</th> <td>Normal</td></tr>
<tr><th>Separated by closed neighbourhoods</th> <td>Normal</td></tr>
<tr><th>Separated by a function</th> <td>Normal</td></tr>
<tr><th>Precisely separated by a function</th> <td>Perfectly normal</td></tr></table>

When the sets are arbitrary:
<table markdown="1"><tr><th>Stronger condition &#8595;\Weaker condition &#8594;</th> <th>Separated</th></tr>
<tr><th>Separated by neighbourhoods</th> <td>Completely normal</td></tr></table>

### Equivalent incarnations of the axioms
 {#EquivalentIncarnationsOfTheAxioms}

The conditions $T_0$ and $T_1$ have the following equivalent form in terms of [[topological closures]]
of points:

+-- {: .num_prop #T0InTermsOfClosureOfPoints}
###### Proposition
**(T0 in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is $T_0$ 
precisely if the function $Cl(\{-\})$
from the underlying set of $X$ to the set of [[irreducible closed subsets]] of $X$, is [[injective function|injective]]:

$$
  Cl(\{-\}) \;\colon\; X \hookrightarrow IrrClSub(X)
$$


=--

(This statement also motivates the definition of [[sober topological spaces]], for which $Cl(\{-\})$ is required to be a [[bijection]]).

+-- {: .proof}
###### Proof

Assume first that $X$ is $T_0$. Then we need to show that if $x,y \in X$ are such that
$Cl(\{x\}) = Cl(\{y\})$ then $x = y$. Hence assume that $Cl(\{x\}) = Cl(\{y\})$.
Since the closure of a point is the [[complements]] of the union of the open subsets not containing the point,
this means that the union of open subsets that do not contain $x$
is the same as the union of open subsets that do not contain $y$. Hence every
open subset that does not contain $x$ also does not contain $y$, and vice versa.
By $T_0$ this is not the case when $x \neq y$, hence it follows that $x = y$.

Conversely, assume that if $x,y \in X$ are such that $Cl\{x\} = Cl\{y\}$ then $x = y$.
We need to show that if $x \neq y$ then there exists an open neighbourhood around one of the
two points not containing the other. Hence assume that $x \neq y$.
By assumption it follows that $Cl(\{x\} \neq Cl(\{y\})$.
Since the closure of a point is the [[complements]] of the union of the open subsets not containing the point, this
means that there must be at least one open subset which contains $x$ but not $y$, or vice versa.
By definition this means that $(X,\tau)$ is $T_0$.


=--

+-- {: .num_prop #T1InTermsOfClosureOfPoints}
###### Proposition
**(T1 in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is $T_1$ precisely if
all its points are [[closed points]].

=--

+-- {: .proof}
###### Proof

Assume first that $(X,\tau)$ is $T_1$. We need to show that for every point $x \in X$ we have
$Cl(\{x\}) = \{x\}$. Since the closure of a point is the [[complement]] of the union of all open subsets not containing this point,
this is the case precisely if the union of all open subsets not containing $x$ is $X \backslash \{x\}$, hence
if every point $y \neq x$ is member of at least one open subset not containing $x$. This is true by $T_1$.

Conversely, assume that for all $x \in X$ then $Cl(\{x\}) = \{x\}$. Then for $x \neq y \in X$ two
distinct points we need to produce an open subset of $y$ that does not contain $x$. But as before,
since $Cl(\{x\})$ is the complement of the union of all open subsets that do not contain $x$, and
the assumption $Cl\{x\} = \{x\}$ means that $y$ is member of one of these open subsets that do not
contain $x$.

=--



### Relations between the axioms

First of all, notice that the $T_1$ condition, that distinct points are separated, is equivalent to the condition that every point is closed.  Thus, $T_1$ serves as a linchpin between conditions on points and conditions on closed sets.

Many implications between separation axioms can be seen in the following Hasse diagram:

<img src="http://ncatlab.org/nlab/files/separation.png" width="472" alt="" />

Here, there are two entries at each node; the one on the right includes the $T_0$ axiom, while the one on the left does not.  This diagram shows the separation axioms as a meet sub-[[semilattice]] of the lattice of all conditions on topological spaces; for example, you can see, by following the diagram upwards, that any space that is both **n**ormal and **r**egular must be $R_3$.  And since $R_3$ never appears in the tables above, you can take this as a *definition* of $R_3$.

In general, the names in this diagram are:

*  'P' for 'perfectly',
*  'C' for 'complete',
*  'N' for '[[normal space|normal]]',
*  'R' (without a subscript) for '[[regular space|regular]]'
*  'T' or 'R' with a subscript are written and pronounced that way.

Warning: $T_i$ for $i \geq 3$ has been used in different ways in the past, and perhaps by some schools still.  Also, all of the $R_i$ terms are rare.  It is safest to say, for example, 'normal Hausdorff' for $T_4$ and clearer to say, for example, 'normal regular' for $R_3$.  If you want to avoid the subscript terms entirely, then you can, by doing the above and the following:

*  $T_2$ = [[Hausdorff space|Hausdorff]],
*  $T_1$ = accessible,
*  $T_0$ = Kolmogorov,
*  $R_1$ = reciprocal,
*  $R_0$ = symmetric.

On the other hand, if you want to use *more* symbols, then you can:

*  $R_2$ = regular,
*  $R_{2\frac{1}{2}}$ = completely regular.

It would be easy to invent an $N_i$ series for the various kinds of normal spaces, but nobody seems to have done so yet.

Other terms are also in use, principally 'Tychonoff' for [[Tychonoff space|completely regular Hausdorff]] ($T_{3\frac{1}{2}}$).


### Other axioms

There are other axioms sometimes included among the separation axioms that don\'t fit the preceding pattern; but like the others, they all hold of a metric space:

*  [[sober space|sober]] and having enough points,
*  [[semiregular space|semiregular]],
*  fully normal and fully $T_4$, which are related to [[paracompact space|paracompactness]].


## Beyond the classical theory

The axioms $T_1$ and below can be phrased entirely in terms of the [[specialisation order]], as follows:

*  In general, the specialisation order is a [[preorder]].
*  The space is $T_0$ if and only if the specialisation order is a [[partial order]].
*  The space is $R_0$ if and only if the specialisation order is an [[equivalence relation]].
*  The space is $T_1$ if and only if the sepcification order is the [[equality relation]].

Note that *any* preorder is the specialisation order for its own [[specialisation topology]].


The separation conditions that appear in $T_2$ and below, or rather their [[negation]]s, can be easily phrased in terms of the [[convergence space|convergence structure]], as follows:

*  Two points are not distinct if and only if they are equal (of course).
*  They are __topologically indistinguishable__ (that is, not topologically distinct) if and only if every [[net]] (or [[filter]]) that [[convergnce|converges]] to one must also converge to the other; it\'s enough to check the [[ultrafilters]] generated by the two points.
*  They are not separated if and only there exists a net (or proper filter) that converges to both.

So by taking contrapositives, it\'s easy to generalise $T_2$ and below to [[convergence spaces]].  (All of the axioms *can* be generalised to convergence spaces, since the convergence structure determines the topology, but there are several ways to do so, and it\'s not clear in general which is best.)


For [[locales]], the axioms at the other end are clearest.  Here we want to put everything in terms of open sets, so we simply work with the [[complements]] of the closed sets that appear in those axioms.  Rather than talk about a closed set $F$ and a neighbourhood $U$ of $F$, we talk about an open set $G$ and an open set $U$ such that $G \cup U$ is the entire space.  Now the axioms at the low end are tricky, although there is a standard answer as far down as $T_2$.  (Note that every locale is $T_0$, indeed sober.)


In [[constructive mathematics]], while the classical definitions all make sense, they are never quite what is wanted.  For the low axioms, one may use, as with convergence spaces, conditions that are classically the negations of the separation conditions; for the high axioms, one may use the open sets that are classically the complements of the closed sets in the axioms.  In the middle axioms, these work together; for example, the condition that a point $x$ is disjoint from a closed set $F$ becomes the condition that $x$ belongs to an open set $G$.


Specific examples should be found on the pages for specific separation axioms.


## References

The English Wikipedia has [a decent article](http://secure.wikimedia.org/wikipedia/en/wiki/Separation_axiom), but since I ([[Toby Bartels]]) wrote that too, it\'s not really an independent source.  But you can check the references there!

Lecture notes include

* {#Naik} [[Vipul Naik]], _Topology: The journey into separation axioms_ ([pdf](http://www.cmi.ac.in/~vipul/mathjourneys/contytopologysep.pdf))

[[!redirects topologically distinct points]]
[[!redirects topologically disjoint sets]]
[[!redirects separated sets]]
[[!redirects separation axiom]]
[[!redirects separation axioms]]

[[!redirects separation property]]
[[!redirects separation properties]]


[[!redirects T0]]
[[!redirects T1]]

[[!redirects T0-space]]
[[!redirects T0-spaces]]
[[!redirects T0-topological space]]
[[!redirects T0-topological spaces]]

[[!redirects T1-space]]
[[!redirects T1-spaces]]
[[!redirects T1-topological space]]
[[!redirects T1-topological spaces]]


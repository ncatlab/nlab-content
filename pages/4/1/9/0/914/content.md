
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 
 {#Idea}

A _net_ in a [[set]] $X$ is simply a [[function]] from a [[directed set]] $D$ to $X$. Special cases of nets are [[sequences]], for which $D = \mathbb{N}_{\leq}$ is the [[natural numbers]]. Regarded as a generalization of sequences, nets are used in [[topology]] for formalization of the concept of [[convergence]].

Nets are also called _Moore--Smith sequences_ and are equivalent (in a certain sense) to [[proper filters]], their _[[eventuality filters]]_.

The concept of nets is motivated from the fact that where plain [[sequences]] detect [[topology|topological]] properties in [[metric spaces]], in generally they fail to do so in more general [[topological spaces]]. 
For example [[sequentially compact metric spaces are equivalently compact metric spaces]], but for general [[topological spaces]] being [[sequentially compact space|sequentially compact]] neither implies nor is implied by being [[compact space|compact]] (see at _[[sequentially compact space]]_ [Examples and counter-examples](sequentially+compact+topological+space#Examples)). 

Inspection of these counter-examples reveals that the problem is that sequences indexed by the [[natural numbers]] may be "too short" in that they cannot go deep enough into incountable territory, and they are "too slim" in that they proceed to their potential limiting point only from one direction, instead of from many at once. The use of general [[directed sets]] in place of just the [[natural numbers]] fixed these two issues. 


## Definitions

### Directed sets

+-- {: .num_defn #DirectedSet}
###### Definition
**([[directed set]])**

A _[[directed set]]_ is

* a [[preordered set]] $(D, \leq)$, hence a set $D$ equipped with a [[reflexive]] and [[transitive]] [[relation]] $\leq$

such that

* every [[finite set|finite]] [[subset]] has an [[upper bound]], hence for any $a,b \in D$ there exists $c \in D$ with $a \leq c$ and $b \leq c$.

=--

+-- {: .num_example #DirectedSetOfNaturalNumbers}
###### Example
**([[directed set]] of [[natural numbers]])**

The [[natural numbers]] $\mathbb{N}$ with their canonical
lower-or-equal relation $\leq$ form a [[directed set]] (def. \ref{DirectedSet}).

=--



### Nets
 {#Nets}


+-- {: .num_defn #Net}
###### Definition

For $X$ a [[set]], then a _net_ in $X$ is 

1. a [[directed set]] $A$ (def. \ref{DirectedSet}), called the _index set_,

1. a [[function]] $\nu \colon A \to X$ from (the underlying set of) $A$ to $X$.

We say that $A$ _indexes_ the net.  

=--

+-- {: .num_example #SequencesAreNets}
###### Example
**([[sequences]] are [[nets]])**

A [[sequence]] is a net (def. \ref{Net}) whose directed set of indices is the [[natural numbers]] $(\mathbb{N}, \leq)$ (example \ref{DirectedSetOfNaturalNumbers}).

=--

+-- {: .num_remark}
###### Remark

Although the index set $A$ in def. \ref{Net}, being a [[directed set]], is equipped with a [[preorder]], the function $\nu \colon A \to X$ is not required to preserve this in any way.  This forms an exception to the rule of thumb that a preordered set may be replaced by its quotient [[partial order|poset]].  

You can get around this if you instead define a net in $X$ as a [[multi-valued function]] from a partially ordered directed set $A$ to $X$.  Although there is not much point to doing this in general, it can make a difference if you put restrictions on the possibilities for $A$, in particular if you consider the definition of [[sequence]].  In some [[type theory|type-theoretic]] [[foundations]] of mathematics, you can get the same effect by defining a net to be an 'operation' (a [[prefunction]], like a function but not required to preserve [[equality]]).

=--

### Subnets

There are several different definitions of 'subnet' in the literature, all of which intend to generalise the concept of subsequences.  We give them in order of increasing generality.  Note that it is Definition \ref{AA} which is correct in that it corresponds precisely to refinement of filters.  However, the other two definitions are sufficient (in a sense made precise by theorem \ref{EquivalenceOfDefinitionsOfSubnets} below) and may be easier to work with.


+-- {.num_defn #Willard}
###### Definition
(Willard, 1970).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

We have a [[function]] $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is monotone (that is, for every $\beta_1 \geq \beta_2 \in B$, $f(\beta_1) \geq f(\beta_2)$);
*  $f$ is cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that $f(\beta) \geq \alpha$).
=--

+-- {.num_defn #Kelley}
###### Definition
(Kelley, 1955).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

We have a [[function]] $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is strongly cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$, $f(\beta_1) \geq \alpha$).

=--

+-- {: .num_remark}
###### Remark

Notice that the function $f$ in definitions \ref{Willard} and \ref{Kelley} is _not_ required to be an [[injection]], and it need not be. As a result, a [[sequence]] regarded as a [[net]] in general has more sub-nets than it has sub-sequences.

=--


+-- {.num_defn #AA}
###### Definition
(Smiley, 1957; &#197;rnes & Anden&#230;s, 1972).

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

The [[eventuality filter]] of $y$ (def. \ref{EventualityFilter}) refines the eeventuality filter of $x$.  (Explicitly, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$ there is an $\alpha_1 \geq \alpha \in A$ such that $y_{\beta_1} = x_{\alpha_1}$.)
=--


The equivalence between these definitionsis as follows:

+-- {.num_theorem #EquivalenceOfDefinitionsOfSubnets}
###### Theorem
([Schechter, 1996](#Schechter96)).

1.  If $y$ is a (\ref{Willard})-subnet of $x$, then $y$ is also a (\ref{Kelley})-subnet of $x$, using the same function $f$.
2.  If $y$ is a (\ref{Kelley})-subnet of $x$, then $y$ is also a (\ref{AA})-subnet of $x$.
3.  If $y$ is a (\ref{AA})-subnet of $x$, then there is some net $z$ such that
    *  $z$ is equivalent to $y$ in the sense that $y$ and $z$ are (\ref{AA})-subnets of each other, and
    *  $z$ is a (\ref{Willard})-subnet of $x$, using some function.
=--

So from the perspective of definition (\ref{AA}), there are enough (\ref{Willard})-subnets and (\ref{Kelley})-subnets, up to equivalence.


### Logic of nets 

A [[property]] of [[elements]] of a [[set]] $X$ (given by the [[subset]] $S \subset X$ of those elements of $X$ satisfying this property) may be applied to nets in $X$.  

+-- {.num_defn #EventuallyAndFrequently}
###### Definition

We say that $\nu$ is __[[eventually]]__ in $S$ if for some index $i$, $\nu_j \in S$ for every $j \ge i$.  Dually, we say that $\nu$ is __frequently__ in $S$ if for every index $i$, $\nu_j \in S$ for some $j \ge i$.  

=--

+-- {.num_remark}
###### Remark

Sometimes one says 'infinitely often' in place of 'frequently' and even 'cofinitely often' in place of 'eventually'; these derive from the special case of sequences, where they may be taken literally.
=--

Being eventually in $S$, def. \ref{EventuallyAndFrequently}, is a weakening of being always in $S$ (given by Lawvere\'s [[universal quantifier]] $\forall_\nu$), while being frequently in $S$ is a strengthening of being sometime in $S$ (given by the [[particular quantifier]] $\exists_\nu$).  Indeed we can build a [[formal logic]] out of these.  Use $\ess\forall i, p[\nu_i]$ or $\ess\forall_\nu p$ to mean that a predicate $p$ in $X$ is eventually true, and use $\ess\exists i, p[\nu_i]$ or $\ess\exists_\nu p$ to mean that $p$ is frequently true.  Then we have:
$$\forall_\nu p \;\Rightarrow\; \ess\forall_\nu p \;\Rightarrow\; \ess\exists_\nu p \;\Rightarrow\; \exists_\nu p$$
$$\ess\forall_\nu (p \wedge q) \;\Leftrightarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \wedge q) \;\Rightarrow\; \ess\exists_\nu p \wedge \ess\exists_\nu q$$
$$\ess\forall_\nu (p \vee q) \;\Leftarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \vee q) \;\Leftrightarrow\; \ess\exists_\nu p \vee \ess\exists_\nu q$$
$$\ess\forall_\nu \neg{p} \;\Leftrightarrow\; \neg\ess\exists_\nu p$$
and other analogues of theorems from [[predicate logic]].  Note that the last item listed requires [[excluded middle]] even though its analogue from ordinary predicate logic does not.

A similar logic is satisfied by '[[almost everywhere]]' and its dual ('not almost nowhere' or 'somewhere significant') in [[measure spaces]].


### Nets and filters
 {#NetsAnd} 

Recall that: 

+-- {: .num_defn #Filter}
###### Definition

Given a [[set]] $X$ then a [[set]] of [[subsets]] of $X$, hence a subset of the [[power set]]

$$
  F \subset P(X)
$$


is called a _filter_ of subsets if it is closed under [[intersections]] and taking supersets.

The filter $F$ is called _proper_ if each set in it is [[inhabited subset|inhabited]].

=--

+-- {: .num_defn #EventualityFilter}
###### Definition
**([[eventuality filter]])**

Let $X$ be a [[set]] and let $\nu \colon D \to X$ be a net in $X$ (def. \ref{Net}).

The _[[eventuality filter]]_ $F_\nu$ of the net $\nu$ is the [[filter]] (def. \ref{Filter}) onsisting of the subsets that $\nu$ is _eventually in_, according to def. \ref{EventuallyAndFrequently}.

$$
  \left(
    (U \subset X) \in F_\nu
  \right)
   \,\Leftrightarrow\,
  \left(
    \nu \, \text{is eventually in}\, U
  \right)
  \,.
$$



=--

Conversely, any [[filter]] $\mathcal{F}$ defines a net whose eventuality filter is $\mathcal{F}$.  Let $A$ be the [[disjoint union]] of $\mathcal{F}$; that is, an element of $A$ is of the form $(U,x)$, where $x \in U \in \mathcal{F}$.  Define $(U,x) \geq (V,y)$ iff $U \subseteq V$ (regardless of $x$ and $y$).  Since $\mathcal{F}$ is a filter, one can show that $A$ is a [[directed set]] (one needs here that $\mathcal{F}$ is proper).  Define $\nu(U,x)$ to be $x$; then $\nu$ is a net in $X$ whose eventuality filter is $\mathcal{F}$ again.  (It is actually enough to use only a base of the filter when defining $A$.)

Nets are considered __equivalent__ if they have the same eventuality filter; in other words, they are both subnets of each other.  In particular, they define the same logical quantifiers and are therefore equivalent for the application to topology below.  (Of course, it is possible to distinguish them by using the standard logical quantifiers instead.)


## Nets in topological spaces 

A net $\nu$ in a [[topological space]] __[[convergence|converges]]__ to a point $x$ in the space if, given any [[neighbourhood]] $U$ of $x$, $\nu$ is eventually in $U$ (def. \ref{EventuallyAndFrequently}); $\nu$ __clusters__ at $x$ if, for every neighbourhood $U$ of $x$, $\nu$ is frequently in $U$ (also def. \ref{EventuallyAndFrequently}).  One can in fact recover the topology on the set $X$ simply by knowing which nets converge to which points.  It is possible to define elementary conditions on this [[convergence]] relation that characterise whether it is topological (that is whether it comes from a topology on $X$), although these are a bit complicated.

By keeping only the simple conditions, one gets the definition of a [[convergence space]]; this is a more general concept than a topological space and includes many non-topological situations where we want to say that a sequence converges to some value (such as convergence in measure).  It is also very nice to describe [[compact space|compact]] and [[Hausdorff space|Hausdorff]] spaces in terms of the convergence relation.

Although nets are perhaps more familiar, due to their similarity to sequences, one gets a cleaner theory by talking about filters, since equivalent filters are equal and (as long as one is not a [[predicative mathematics|predicativist]]) the set of filters on a set $X$ is small (not a proper class).


## Related concepts

* [[limit of a net]]


## References

A textbook account is in 

* {#Schechter96} [[Eric Schechter]], sections 7.14--7.21 of _[[Handbook of Analysis and its Foundations]]_, Academic Press (1996)

Lecture notes include

* {#Vermeeren10} [[Stijn Vermeeren]], _Sequences and nets in topology_, 2010 ([pdf](http://stijnvermeeren.be/download/mathematics/nets.pdf))


[[!redirects net]]
[[!redirects nets]]

[[!redirects subnet]]
[[!redirects subnets]]

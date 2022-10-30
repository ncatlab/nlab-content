# Contents
* the following line creates the automatic table of contents
{:toc}

## Idea 

_Nets_ are generalisations of [[sequences]] that are used especially in topology.  They are also called _Moore--Smith sequences_ and are equivalent (in a certain sense) to [[proper filters]].


## Definitions

A __net__ $\nu$ in a [[set]] $X$ is a [[direction|directed set]] $A$ and a [[function]] $\nu: A \to X$; we say that $A$ _indexes_ the net.  The notation used is based on the special case of an infinite [[sequence]]; the value of the function $\nu$ at the index $i$ is written $\nu_i$.  Indeed, an infinite sequence in $X$ is a net indexed by the [[natural numbers]].

Although $A$, being a directed set, is equipped with a [[preorder]], the net is not required to preserve this in any way.  This forms an exception to the rule of thumb that a preordered set may be replaced by its quotient [[partial order|poset]].  You can get around this if you instead define a net in $X$ as a [[multi-valued function]] from a partially ordered directed set $A$ to $X$.  Although there is not much point to doing this in general, it can make a difference if you put restrictions on the possibilities for $A$, in particular if you consider the definition of [[sequence]].  In some type-theoretic [[foundations]] of mathematics, you can get the same effect by defining a net to be an 'operation' (a [[prefunction]], like a function but not required to preserve [[equality]]).


## Subnets

There are several different definitions of 'subnet' in the literature, all of which intend to generalise subsequences.  We give them in order of increasing generality.  Note that it is Definition \ref{AA} which is correct in that it corresponds precisely to refinement of filters.  However, the other two definitions are sufficient (in a sense to be made precise at the end of this section) and may be easier to work with.

Given a net $(x_{\alpha})$ with index set $A$, and a net $(y_{\beta})$ with an index set $B$, we say that $y$ is a __subnet__ of $x$ if:

+-- {.num_defn #Willard}
###### Definition
(Willard, 1970).

We have a function $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is monotone (that is, for every $\beta_1 \geq \beta_2 \in B$, $f(\beta_1) \geq f(\beta_2)$);
*  $f$ is cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that $f(\beta) \geq \alpha$).
=--

+-- {.num_defn #Kelley}
###### Definition
(Kelley, 1955).

We have a function $f\colon B \to A$ such that

*  $f$ maps $x$ to $y$ (that is, for every $\beta \in B$, $y_{\beta} = x_{f(\beta)}$);
*  $f$ is strongly cofinal (that is, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$, $f(\beta_1) \geq \alpha$).
=--

+-- {.num_defn #AA}
###### Definition
(Smiley, 1957; &#197;rnes & Anden&#230;s, 1972).

The eventuality filter of $y$ (see below) refines the eventuality filter of $x$.  (Explicitly, for every $\alpha \in A$ there is a $\beta \in B$ such that, for every $\beta_1 \geq \beta \in B$ there is an $\alpha_1 \geq \alpha \in A$ such that $y_{\beta_1} = x_{\alpha_1}$.)
=--

The equivalence between these is as follows:

+-- {.un_thm}
###### Theorem
(Schechter, 1996).

1.  If $y$ is a (\ref{Willard})-subnet of $x$, then $y$ is also a (\ref{Kelley})-subnet of $x$, using the same function $f$.
2.  If $y$ is a (\ref{Kelley})-subnet of $x$, then $y$ is also a (\ref{AA})-subnet of $x$.
3.  If $y$ is a (\ref{AA})-subnet of $x$, then there is some net $z$ such that
    *  $z$ is equivalent to $y$ in the sense that $y$ and $z$ are (\ref{AA})-subnets of each other, and
    *  $z$ is a (\ref{Willard})-subnet of $x$, using some function.
=--

So from the perspective of definition (\ref{AA}), there are enough (\ref{Willard})-subnets and (\ref{Kelley})-subnets, up to equivalence.


## Logic of nets 

A property of elements of $X$ (given by a [[subset]] $S$ of $X$) can be applied to nets in $X$.  We say that $\nu$ is __eventually__ in $S$ if for some index $i$, $\nu_j \in S$ for every $j \ge i$.  Dually, we say that $\nu$ is __frequently__ in $S$ if for every index $i$, $\nu_j \in S$ for some $j \ge i$.  Sometimes one says 'infinitely often' in place of 'frequently' and even 'cofinitely often' in place of 'eventually'; these derive from the special case of sequences, where they may be taken literally.

Note that being eventually in $S$ is a weakening of being always in $S$ (given by Lawvere\'s [[universal quantifier]] $\forall_\nu$), while being frequently in $S$ is a strenghtening of being sometime in $S$ (given by the [[particular quantifier]] $\exists_\nu$).  Indeed we can build a logic out of these.  Use $\ess\forall i, p[\nu_i]$ or $\ess\forall_\nu p$ to mean that a predicate $p$ in $X$ is eventually true, and use $\ess\exists i, p[\nu_i]$ or $\ess\exists_\nu p$ to mean that $p$ is frequently true.  Then we have:
$$\forall_\nu p \;\Rightarrow\; \ess\forall_\nu p \;\Rightarrow\; \ess\exists_\nu p \;\Rightarrow\; \exists_\nu p$$
$$\ess\forall_\nu (p \wedge q) \;\Leftrightarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \wedge q) \;\Rightarrow\; \ess\exists_\nu p \wedge \ess\exists_\nu q$$
$$\ess\forall_\nu (p \vee q) \;\Leftarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \vee q) \;\Leftrightarrow\; \ess\exists_\nu p \vee \ess\exists_\nu q$$
$$\ess\forall_\nu \neg{p} \;\Leftrightarrow\; \neg\ess\exists_\nu p$$
and other analogues of theorems from [[predicate logic]].  Note that the last item listed requires [[excluded middle]] even though its analogue from ordinary predicate logic does not.

A similar logic is satisfied by 'almost everywhere' and its dual in [[measure spaces]].


## Nets and filters 

A net $\nu$ in a set $X$ defines a proper [[filter]] of subsets of $X$, called the __eventuality filter__ of the net.  It consists simply of those subsets of $X$ that $\nu$ is eventually in.  (Recall that a _filter_ of subsets is a collection of subsets that is closed under intersection and taking supersets; the filter is _proper_ if each set in it is inhabited.)

Conversely, any filter $\mathcal{F}$ defines a net whose eventuality filter is $\mathcal{F}$.  Let $A$ be the [[disjoint union]] of $\mathcal{F}$; that is, an element of $A$ is of the form $(U,x)$, where $x \in U \in \mathcal{F}$.  Define $(U,x) \geq (V,y)$ iff $U \subseteq V$ (regardless of $x$ and $y$).  Since $\mathcal{F}$ is a filter, one can show that $A$ is a directed set (one needs here that $\mathcal{F}$ is proper).  Define $\nu(U,x)$ to be $x$; then $\nu$ is a net in $X$ whose eventuality filter is $\mathcal{F}$ again.  (It is actually enough to use only a base of the filter when defining $A$.)

Nets are considered __equivalent__ if they have the same eventuality filter; in other words, they are both subnets of each other.  In particular, they define the same logical quantifiers and are therefore equivalent for the application to topology below.  (Of course, it is possible to distinguish them by using the standard logical quantifiers instead.)


## Nets in topological spaces 

A net $\nu$ in a [[topological space]] __converges__ to a point $x$ in the space if, given any neighbourhood $U$ of $x$, $\nu$ is eventually in $U$; $\nu$ __clusters__ at $x$ if, for every neighbourhood $U$ of $x$, $\nu$ is frequently in $U$.  One can in fact recover the topology on the set $X$ simply by knowing which nets converge to which points.  It is possible to define elementary conditions on this convergence relation that characterise whether it is topological (that is whether it comes from a topology on $X$), although these are a bit complicated.

By keeping only the simple conditions, one gets the definition of a [[convergence space]]; this is a more general concept than a topological space and includes many non-topological situations where we want to say that a sequence converges to some value (such as convergence in measure).  It is also very nice to describe [[compact space|compact]] and [[Hausdorff space|Hausdorff]] spaces in terms of the convergence relation.

Although nets are perhaps more familiar, due to their similarity to sequences, one gets a cleaner theory by talking about filters, since equivalent filters are equal and (as long as one is not a [[predicative mathematics|predicativist]]) the set of filters on a set $X$ is small (not a proper class).


## References

*  _[[HAF]]_, Sections 7.14--7.21


[[!redirects net]]
[[!redirects nets]]

[[!redirects subnet]]
[[!redirects subnets]]

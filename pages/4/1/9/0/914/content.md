# Idea #

_Nets_ are generalisations of [[sequences]] that are used especially in topology.  They are also called _Moore--Smith sequences_ and are equivalent (in a certain sense) to proper [[filters]].

# Definition #

A __net__ $\nu$ in a [[set]] $X$ is a [[direction|directed set]] $A$ and a [[function]] $\nu: A \to X$; we say that $A$ _indexes_ the net.  The notation used in based on the special case of an infinite [[sequence]]; the value of the function $\nu$ at the index $i$ is written $\nu_i$.  Indeed, an infinite sequence in $X$ is a net indexed by the [[natural numbers]].

Although $A$, being a directed set, is equipped with a [[preorder]], the net is not required to preserve this in any way.  This forms an exception to the rule of thumb that a preordered set may be replaced by its quotient [[partial order|poset]].  You can get around this if you instead define a net in $X$ as a [[multi-valued function]] from a partially ordered directed set $A$ to $X$.  Although there is not much point to doing this in general, it can make a difference if you put restrictions on the possibilities for $A$, in particular if you consider the definition of [[sequence]].  In some type-theoretic [[foundations]] of mathematics, you can get the same effect by defining a net to be an 'operation' (a [[prefunction]], like a function but not required to preserve [[equality]]).

# Logic of nets #

A property of elements of $X$ (given by a [[subset]] $S$ of $X$) can be applied to nets in $X$.  We say that $\nu$ is __eventually__ in $S$ if for some index $i$, $\nu_j \in S$ for every $j \ge i$.  Dually, we say that $\nu$ is __frequently__ in $S$ if for every index $i$, $\nu_j \in S$ for some $j \ge i$.  Sometimes one says 'infinitely often' in place of 'frequently' and even 'cofinitely often' in place of 'eventually'; these derive from the special case of sequences, where they may be taken literally.

Note that being eventually in $S$ is a weakening of being always in $S$ (given by Lawvere\'s universal quantifier $\forall_\nu$), while being frequently in $S$ is a strenghtening of being sometime in $S$ (given by the particular quantifier $\exists_\nu$).  Indeed we can build a logic out of these.  Use $\ess\forall i, p[\nu_i]$ or $\ess\forall_\nu p$ to mean that a predicate $p$ in $X$ is eventually true, and use $\ess\exists i, p[\nu_i]$ or $\ess\exists_\nu p$ to mean that $p$ is frequently true.  Then we have:
$$\forall_\nu p \;\Rightarrow\; \ess\forall_\nu p \;\Rightarrow\; \ess\exists_\nu p \;\Rightarrow\; \exists_\nu p$$
$$\ess\forall_\nu (p \wedge q) \;\Leftrightarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \wedge q) \;\Rightarrow\; \ess\exists_\nu p \wedge \ess\exists_\nu q$$
$$\ess\forall_\nu (p \vee q) \;\Leftarrow\; \ess\forall_\nu p \wedge \ess\forall_\nu q$$
$$\ess\exists_\nu (p \vee q) \;\Leftrightarrow\; \ess\exists_\nu p \vee \ess\exists_\nu q$$
$$\ess\forall_\nu \neg{p} \;\Leftrightarrow\; \neg\ess\exists_\nu p$$
and other analogues of theorems from [[predicate logic]].  Note that the last item listed requires [[excluded middle]] even though its analogue from ordinary predicate logic does not.

A similar logic is satisfied by 'almost everywhere' and its dual in [[measure spaces]].

# Nets and filters #

A net $\nu$ in a set $X$ defines a proper [[filter]] of subsets of $X$, called the __eventuality filter__ of the net.  It consists simply of those subsets of $X$ that $\nu$ is eventually in.  (Recall that a _filter_ of subsets is a family of subsets that is closed under intersection and taking supersets; the filter is _proper_ if each set in it is inhabited.)

Conversely, any filter $\mathcal{F}$ defines a net whose eventuality filter is $\mathcal{F}$.  Let $A$ be the [[disjoint union]] of $\mathcal{F}$; that is, an element of $A$ is of the form $(U,x)$, where $x \in U \in \mathcal{F}$.  Define $(U,x) \geq (V,y)$ iff $U \subseteq V$ (regardless of $x$ and $y$).  Since $\mathcal{F}$ is a filter, one can show that $A$ is a directed set (one needs here that $\mathcal{F}$ is proper).  Define $\nu(U,x)$ to be $x$; then $\nu$ is a net in $X$ whose eventuality filter is $\mathcal{F}$ again.  (It is actually enough to use only a base of the filter when defining $A$.)

Nets are considered __equivalent__ if they have the same eventuality filter; in particular, they define the same logical quantifiers and are therefore equivalent for the application to topology below.  Of course, it is possible to distinguish them by using the standard logical quantifiers instead.

# Nets in topological spaces #

A net $\nu$ in a [[topological space]] __converges__ to a point $x$ in the space if, given any neighbourhood $U$ of $x$, $\nu$ is eventually in $U$; $\nu$ __clusters__ at $x$ if, for every neighbourhood $U$ of $x$, $\nu$ is frequently in $U$.  One can in fact recover the topology on the set $X$ simply by knowing which nets converge to which points.  It is possible to define elementary conditions on this convergence relation that characterise whether it is topological (that is whether it comes from a topology on $X$), although these are a bit complicated.

By keeping only the simple conditions, one gets the definition of a [[convergence space]]; this is a more general concept than a topological space and includes many non-topological situations where we want to say that a sequence converges to some value (such as convergence in measure).  It is also very nice to describe [[compact space|compact]] and [[Hausdorff space|Hausdorff]] spaces in terms of the convergence relation.

Although nets are perhaps more familiar, due to their similarity to sequences, one gets a cleaner theory by talking about filters, since equivalent filters are equal and (as long as one is not a [[predicative mathematics|predicativist]]) the set of filters on a set $X$ is small (not a proper class).

[[!redirects nets]]
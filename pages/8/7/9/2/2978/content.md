# Totally bounded spaces
* tic
{: toc}


## Idea

A space is _totally bounded_ if it may be covered by finitely many sets of arbitrarily small size.

The [[Heine-Borel theorem]], which states that a closed and bounded subset of the [[real line]] is [[compact space|compact]] (in the finite open subcover sense), applies to all [[cartesian spaces]] but not to general [[metric spaces]].  However, if we use two facts about the real line (which hold for all cartesian spaces) ---that a subset is [[closed subspace|closed]] if and only if it is [[complete space|complete]] and that a subset is [[bounded space|bounded]] if and only if it is _totally bounded_---, then we get a theorem that *does* apply to all metric spaces (at least assuming the [[axiom of choice]]): that a complete and totally bounded space is compact.

The concept (and the Heine--Borel theorem, in this sense) apply not only to metric spaces but to [[uniform spaces]]; like completeness, total boundedness is a uniform property.


## Definition

In the following definitions, '[[finite set|finite]]' means Kuratowski-finite, or finitely indexed, for the purposes of [[constructive mathematics]].  All of these definitions are constructively equivalent.

The slickest definition for [[uniform spaces]] is probably this one:

+-- {: .un_defn #slick}
###### Definition

A uniform space $X$ is __totally bounded__ if every [[uniform cover]] of $X$ has a finite subcover.
=--

Since uniform covers are not a common approach to uniform spaces, we unwrap the definition of uniform covers in terms of entouranges to get this definition:

+-- {: .un_defn #uniform}
###### Definition

A uniform space $X$ is __totally bounded__ if, for every entourage $U$ of $X$, there is a finite [[open cover]] $\mathcal{C}$ of $X$ such that every set $G$ in $\mathcal{C}$ satisfies $G \times G \subseteq U$.
=--

In fact, it is enough to consider only basic entourages for some base of the uniformity.  Thus, we may specialise to [[gauge spaces]]:

+-- {: .un_defn #gauge}
###### Definition

A gauge space $X$ is __totally bounded__ if, for every gauging distance $d$ of $X$, there is a finite open cover $\mathcal{C}$ of $X$ such that every set in $\mathcal{C}$ has $d$-diameter less than $1$.
=--

In fact, it is enough to consider only basic gauging distances for some base of the gauge, or even for some subbase of the gauge if we make the requirement for arbitrarily small diameters (rather than the fixed diameter $1$ as above).  Thus, we may specialise to [[metric spaces]]:

+-- {: .un_defn #metric}
###### Definition

A metric space $X$ is __totally bounded__ if, for every positive number $\epsilon$, there is a finite open cover $\mathcal{C}$ of $X$ such that every set in $\mathcal{C}$ has diameter less than $\epsilon$.
=--


## Properties

All of these results hold constructively unless otherwise noted.

Every [[compact space]] is totally bounded; this is immediate from Definition \ref{slick}, since every uniform cover is an open cover.  Conversely, if one assumes the [[ultrafilter principle]], then every [[complete space]] and totally bounded space is compact.

Any [[product]] of totally bounded spaces is totally bounded.  The totally bounded subspaces of a given space $X$ form an [[ideal]] in the [[power set]] of $X$.

A [[subspace]] of a [[Cartesian space]] is totally bounded if and only if it is [[bounded space|bounded]].  Every totally bounded metric space is [[separable space|separable]].


## Precompact spaces

Here is another definition of total boundedness, different in style from the others.  It makes sense even more generally, for any [[Cauchy space]]:

+-- {: .un_defn #precompact}
###### Definition

A Cauchy space $X$ is __precompact__ if its [[complete space|completion]] $\overline{X}$ is compact.
=--

It is immediate that a Cauchy space is compact if and only if it is both complete and precompact.

Every precompact uniform space is totally bounded; using Definition \ref{slick}, this may be proved by checking that any uniform cover of $X$ generates a uniform cover of $\overline{X}$.  The converse, that every totally bounded space is precompact, is equivalent to the [[ultrafilter principle]].  Of course, many totally bounded spaces may be proved precompact on weaker assumptions; in particular, that a bounded subset of a cartesian space is precompact is equivalent to the [[fan theorem]] (and so also follows from the principle of [[excluded middle]]).


## References

*  _[[HAF]]_, Sections 19.14--20

# Simple functions
* table of contents
{: toc}

## Idea

Simple functions are (almost) the most basic notion of [[measurable function]] in [[measure theory]].  Given a [[measure]], it\'s easy to define the [[integral]] of a simple function, and we extend this to more general functions by continuity.


## Definitions

Let $X$ be a [[measurable space]].  We may want $X$ to be equipped with some more data; if $X$ is a [[measure space]], then this is plenty of data.  However, for the most basic definitions, it\'s enough if $X$ is simply a measurable space in the usual sense.

Let $K$ be a [[local field]], usually the field of [[real numbers]] or the field of [[complex numbers]].  We take $K$ to be a measurable space using its [[Borel sets]].  (We really could use something more general for $K$.)

+-- {: .num_defn #trad}
###### Definition

Traditionally, a __simple function__ on $X$ valued in $K$ is a [[measurable function]] from $X$ to $K$ whose [[range]] is [[finite set|finite]].
=--

Since a simple function $f$ is measurable and a [[singleton subset|singleton]] is Borel, each [[fibre]] of $f$ is a [[measurable set]] in $X$; the function $f$ is given by the (finitely many) nonempty fibres and their (singleton) images.  This suggests another way to look at simple functions:

+-- {: .num_defn #lincomb}
###### Definition

A __simple function__ on $X$ valued in $K$ is a formal $K$-[[linear combination]] of [[measurable subsets]] of $X$.
=--

Here we identify a measurable set $A$ with its [[characteristic function]] $\chi_A$, so the formal linear combination $\sum_i c_i A_i$ is identified with the function $\sum_i c_i \chi_{A_i}$, which is measurable and whose range is contained in the finite set of sums of the $c_i$.  (If there are $n$ terms in the linear combination, then there are at most $2^n$ such sums.)

However, the na&#239;ve notion of equality of linear combinations is finer than equality of the corresponding functions, so we must combine Definition \ref{lincomb} with a definition of equality:

+-- {: .num_defn #equal}
###### Definition

Two simple functions on $X$ valued in $K$, in the sense of Definition \ref{lincomb}, are __equal__ if their corresponding [[functions]] from $X$ to $K$ are equal as functions.
=--

Then we have a [[canonical transformation|canonical]] [[bijection]] between the set of simple functions as in Definition \ref{trad} and the set of [[equivalence classes]] of simple functions as in Definition \ref{lincomb}.

Arguably, even this is not really the correct notion of equality, since functions may be equal for the purpose of integration without being literally equal.  If $X$ is equipped with a $\sigma$-[[sigma-ideal|ideal]] of [[null sets]] (or a $\delta$-[[delta-filter|filter]] of [[full sets]]), then we may consider a yet coarser notion of equality:

+-- {: .num_defn #almostequal}
###### Definition

Two simple functions, in the sense of either Definition \ref{trad} or Definition \ref{lincomb}, are __almost equal__ if they (or their corresponding functions) are [[almost equality|equal almost everywhere]].
=--

Sometimes, we wish to restrict attention to those simple functions which we expect to have a finite integral.  If $X$ is equipped with an [[ideal]] of [[bounded sets]] (which in a measure space are sets with finite measure), then we may do this:

+-- {: .num_defn #bounded}
###### Definition

A __bounded simple function__ is a simple function in the sense of Definition \ref{trad} such that the fibre over every non-zero number is bounded, or equivalently (in the sense of Definition \ref{lincomb}) a formal linear combination of bounded measurable sets.
=--

In some approaches to [[measure theory]], one *starts* with a $\delta$-[[delta-ring|ring]] of measurable sets, which may be reinterpreted as the bounded sets in the generated $\sigma$-[[sigma-algebra|algebra]] of [[relatively measurable sets]], and then the simple functions will automatically be bounded.

+-- {: .query}
I'm not sure of the right terminology here; this conflicts with the usual meaning of [[bounded function]].
=--

Finally, there is one more useful restriction on simple functions:

+-- {: .num_defn #positive}
###### Definition

A __positive simple function__ is a simple function in the sense of Definition \ref{trad} whose range consists entirely of nonnegative [[real numbers]], or equivalently (in the sense of Definition \ref{lincomb}) a formal ${[0,\infty[}$-linear combination of measurable sets.
=--

Sometimes one allows a positive simple function to take the value $\infty$ (so to be a $[0,\infty]$-linear combination).  We will call this an __extended positive simple function__.


## Integration

Let $X$ be equipped with a [[measure]] $\mu$, so $(X,\mu)$ is a [[measure space]].  (In particular, $X$ has the structure necessary for all of the definitions above, including both Definitions \ref{almostequal} and \ref{bounded}.)

If $f$ is a simple function from $X$ to $K$, then we wish to define the [[integral]] of $f$.  In general, this is a little tricky, but it\'s easy if $f$ is either [bounded](#bounded) or [positive](#positive).  It is easiest to write down the definition if we think of simple functions using Definition \ref{lincomb}.  Then we have:

+-- {: .num_defn #integral}
###### Definition

The __integral__ of the simple function $f$, represented by the linear combination $\sum_i c_i A_i$, is $\sum_i c_i \mu(A_i)$.
=--

+-- {: .num_prop #extended}
###### Proposition

The integral of a positive simple function always exists.  It is finite if $\mu$ is a [[finite measure]], and it is positive (possibly $0$ or $\infty$) if $\mu$ is a [[positive measure]].
=--

If $\mu$ is a positive measure, then the definition and proposition above generalise to extended positive simple functions.  (But the integral of an extended positive simple function with respect to a finite positive measure need not be finite.)

+-- {: .num_prop #finite}
###### Proposition

The integral of a bounded simple function always exists and is finite (being a finite linear combination of finite numbers).
=--

+-- {: .num_prop #separation}
###### Proposition

Two (bounded or positive) simple functions $f$ and $g$ are almost equal (with respect to $\mu$) if and only if the integral of $f - g$ is zero.
=--

+-- {: .num_defn #norm}
###### Definition

The __$L^1$-norm__ of a simple function is the integral of its [[absolute value]] (which is positive) with respect to the absolute value of the measure $\mu$ (which is a positive measure):
$$ {\|f\|}_1 \coloneqq \int {|f|} {|\mu|} .$$
=--

In this context, we usually start with a positive measure $\mu$; in that case, of course, there is no need to bother taking the absolute value of $\mu$.

+-- {: .num_prop #NVS}
###### Proposition

The bounded simple functions form a [[normed vector space]] $BSF$ under the $L^1$-norm, if we consider them up to [almost equality](#almostequal).
=--

If we don\'t use almost equality, then we get in general only a [[seminorm]], but if we pass to a [[quotient space]] with a norm, then Proposition \ref{separation} tells us that we are now using almost equality.

+-- {: .num_defn #L1}
###### Definition

The [[complete space|completion]] of the normed vector space $BSF$ is the [[Banach space]] $L^1$ of __[[absolutely integrable functions]]__.
=--

+-- {: .num_prop #integration}
###### Proposition

Taking the integral of a bounded simple function is a [[continuous linear functional]] on $BSF$, so it extends to all of $L^1$.
=--

In this way, we may define the integral of any absolutely integrable function.

+-- {: .query}
There might be some technical requirements for this to be true.  I\'ll try to check on that.
=--


[[!redirects simple function]]
[[!redirects simple functions]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Measure spaces
* table of contents
{: toc}

## Idea

Measure spaces are used in the general theory of measure and [[integration]], somewhat analogous to the role played by [[topological spaces]] in the study of continuity.

For the general theory of measure spaces, we first need a _[[measurable space]]_ $(X, \Sigma)$, that is a [[set]] equipped with a collection $\Sigma$ of __measurable sets__ complete under certain operations.  Then this becomes a measure space $(X, \Sigma, \mu)$ by throwing in a [[function]] $\mu$ from $\Sigma$ to a space of values (such as the [[real line]]) that gets along with the set-theoretic operations that $\Sigma$ has.  If $E$ is a measurable set, then $\mu(E)$ is called the __measure__ of $E$ with respect to $\mu$.


## Notation

The original notation for an integral (going back to [[Gottfried Leibniz]]) was
\[ \label{Leibniz} \int_a^b f(x) \,\mathrm{d}x \]
(where $f(x)$ would be replaced by some formula in the variable $x$).  In modern measure theory, we can now understand this as the integral of the [[measurable function]] $f$ on the [[interval]] $[a,b]$ relative to [[Lebesgue measure]].  If we wish to generalise from Lebesgue measure to an arbitrary measure $\mu$ and generalise from $[a,b]$ to an arbitrary measurable set $S$, then we can write
\[ \label{full} \int_S f(x) \,\mu(\mathrm{d}x) \]
instead.  Now, if $f$ is not given by a formula, then there is no need for the dummy variable $x$, which gives
\[ \label{simple} \int_S f \,\mu .\]
However, it has been more common to keep the symbol '$\mathrm{d}$' and write
\[ \label{excessive} \int_S f \,\mathrm{d}\mu .\]
(Note that '$\mathrm{d}$' can be read as 'with respect to' in both (eq:Leibniz) and (eq:excessive), although meaning different things; in the former case, it indicates the dummy variable, while in the latter case, it indicates the measure.)  This notation then leads to replacing (eq:full) with
\[ \label{switched} \int_S f(x) \,\mathrm{d}\mu(x) .\]
This last notation, however, hides the fact that integrating a function with respect to a measure is a way of multiplying a function by a measure to get a new measure; the integral of $f$ on $S$ with respect to $\mu$ is simply the measure of $S$ with respect to $f \mu$, as can be seen in (eq:simple).  Compare also notation for [[Radon?Nikodym derivatives]].

It is also possible to take the entire expression '$\mathrm{d}\mu$' as the name of the measure, writing $\mathrm{d}\mu(A)$ even where the common notation is $\mu(A)$.  In that case, the common expression (eq:excessive) is literally the same as (what would otherwise be) (eq:simple), although (eq:switched) is not quite the same as (what would otherwise be) (eq:full).

We will use (eq:simple) below (although other forms may well be found on other pages).

See [Usenet discussion](http://groups.google.com/group/sci.math.research/browse_thread/thread/e28593bfd6b83aac/67a61d19e8f4d57f), and contrast (eq:switched) with the [Stieltjes integral](http://secure.wikimedia.org/wikipedia/en/wiki/Stieltjes_integral).  The notation (eq:simple) has also been used in an introductory graduate-level course by [[John Baez]].

There is also some variation in notation as to whether to use a roman '$\mathrm{d}$' or an italic '$\mathit{d}$'; roman is more common in England and italic in America.  But of course, that variation should not cause any difficulties!


## Definitions

A __measure space__ is a [[measurable space]] equipped with a measure.  There are many different kinds of measures; we start with the most specific and then consider generalisations.  The motivating example is [[Lebesgue measure]] on the [[unit interval]].


### Probability measures

Let $(X, \Sigma)$ be a measurable space.  A __[[probability measure]]__ on $X$ (due to Kolmogorov) is a [[function]] $\mu$ from the collection $\Sigma$ of measurable sets to the [[unit interval]] $[0,1]$ such that:

1.  The measure of the [[empty set]] is [[zero]]:  $\mu(\emptyset) = 0$;
2.  The measure of the entire space is [[one]]:  $\mu(X) = 1$;
3.  Countable additivity:  $\mu(\bigcup_{i = 1}^{\infty} S_i) = \sum_{i=1}^{\infty} \mu(S_i)$ whenever the $S_i$ are mutually [[disjoint sets|disjoint]].

(Part of the latter condition is the requirement that the sum on the right-hand side must converge.)

It is sometimes stated (but in fact follows from the above) that:

*  Finitary additivity:  $\mu(S \cup T) = \mu(S) + \mu(T)$ whenever $S$ and $T$ are disjoint.
*  $\mu$ is increasing:  $\mu(A) \leq \mu(B)$ if $A \subseteq B$.

The first of these conditions will follow for all of the generalised notions of measure below, but the others usually will not. Related query discussion is archived [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2829&Focus=28141#Comment_28141).

### Generalisations

From now on, we drop (2); the next step is to generalise the [[target]] of $\mu$, as follows:
*  Use $\mathbf{R} = ]-\infty,\infty[$ for a __finite measure__.
*  Use $[0,\infty]$ (instead of $[0,1]$) for a __positive measure__.
*  Use $]-\infty,\infty]$ for a __signed measure__.
*  Use $\mathbf{C}$ for a __complex-valued measure__.
*  Use an arbitrary [[topological vector space]] $V$ for a __$V$-valued measure__.
*  In principle, one could go further yet; $V$ just needs an analogue of addition with a notion of countable sum (such as a [[topological abelian group]] has).  But until someone suggests a useful example, we will leave this to the [[centipede mathematics|centipedes]].

Some futher terms:
*  We can combine conditions; for example a __finite positive measure__ takes values in $[0,\infty[$.
*  A measure is __bounded__ if, for some (finite) real number $M$, $-M \leq \mu(S) \leq M$ for every measurable set $S$.
*  A measure is __$\sigma$-finite__ if every measurable set is a union of countably many sets with finite measure.

Remarks:
*  The property that $\mu$ is increasing holds for all positive measures in the name but may fail for others.
*  A positive measure that satisfies (2) must be a probability measure as defined earlier; that is, it satisfies $\mu(S) \leq 1$ for all $S$.
*  When $\infty$ is allowed as a value of $\mu$, then the requirement in (3) that the sum converges should be interpreted in this light; that is, the sum may diverge to infinity.  (For a positive measure, therefore, the convergence criterion is vacuous in [[classical mathematics]].)
*  Notice that $-\infty$ is not allowed as a value for a signed measure.  It works just as well to allow $-\infty$ and forbid $\infty$.  It is even possible to allow both, but this is a little trickier, so we deal with it later.

Another possibility is to generalise the [[source]] of $\mu$; instead of using a $\sigma$-algebra on $X$, we could use a $\sigma$-ring or even a $\delta$-ring.  These versions are mostly more about changing the definition of [[measurable space]], so refer there for details of the definition; however, we note that (3), when $\Sigma$ is a $\delta$-ring, should state that the left-hand side exists (that is, the union is measurable) if the right-hand side converges.  Generalising $\Sigma$ in this way is complementary to generalising the target above; in particular it may allow one to avoid dealing with $\infty$.  For example, while Lebesgue measure is only a positive measure on a $\sigma$-algebra, it is a *finite* positive measure on the $\delta$-ring of bounded measurable sets.  Indeed, every signed measure gives rise to finite measure on its $\delta$-ring of finitely measurable sets (defined below); conversely, every $\sigma$-finite measure can be recovered from this by imposing (3) in all cases.

Yet another possibility is to drop countable additivity, replacing it with finite additivity.  The result is a __finitely-additive measure__, sometimes called a __charge__ to avoid the [[red herring principle]].  For a charge, one could replace $\Sigma$ with an algebra (or even a ring) of sets; again see [[measurable space]] for these definitions.

Finally, an __extended measure__ takes values in the set $[-\infty,\infty]$ of extended real numbers.  Here we have the problem that, even when considering finite additivity, we might have to add $\infty$ and $-\infty$.  While we might simply require that this never happens (so that at least one of $\mu(S)$ and $\mu(T)$ must be finite if they have opposite signs and $S \cap T = \empty$), this does not include some examples that we want.  To deal with this, we define an extended measure to be a formal difference $\mu^+ - \mu^-$ of positive measures; $\mu(S) = \mu^+(S) - \mu^-(S)$ whenever this is not of the form $\infty - \infty$ and is otherwise undefined.  Note that the set of extended measures on $X$ is a [[quotient set]] of the set of pairs of positive measures; we say that $\mu = \nu$ if $\mu(S) = \nu(S)$ whenever either side is defined, that is if they are the same as [[partial functions]] from $S$ to $[-\infty,\infty]$.


### Constructive theory

In Henry Cheng\'s [[constructive mathematics|constructive]] theory of measure, the definition of [[measurable space]] becomes more complicated; the main point is that a single measurable set $S$ is replaced by a _complemented pair_ $(S,T)$.  Once that is understood, very little needs to be changed to define a measure space.

In the requirements (1--3), the constants $\empty$ and $X$ and the operation $\union$ are interpreted by formal [[de Morgan duality]], as explained at [[Cheng measurable space]].  The convergence requirement in (3) should be interpreted in the strong sense of located convergence and is no longer trivial for positive measures.  We must add a further requirement to enforce the idea that $\mu(S,T)$ is the measure of $S$ alone, as follows:

*  $\mu(S,T) = \mu(S,U)$ whenever $(S,T)$ and $(S,U)$ are both complemented pairs.

In general, a _measurable set_ is any set $S$ such that $(S,T)$ is a complemented pair for some set $T$; the term 'measurable set' in the classical theory should be interpreted as either 'mesurable set' or 'complemented pair' in the constructive theory, depending on context.  Usually both interpretations will actually work, but often only the first set of the pair will matter, thanks to the axiom above.

We will mention other occasional fine points in the constructive theory when they occur; the main outline does not change.

+-- {: .query}
I need to check Bishop & Bridges to see if there are any other changes, but I don\'t think so; that is, I went through the following, and it all seems correct as it is.  ---Toby
=--


### Subsidiary definitions

Given a measure space $(X,\Sigma,\mu)$, a __$\mu$-null $\Sigma$-measurable set__ is a measurable set $N$ such that $\mu(S) = 0$ whenever $S \subseteq N$ is measurable; a __$\mu$-null set__ is any subset of a null measurable set.  In a positive measure space, we don\'t have to bother with $S$; $N$ will be a null measurable set as long as $\mu(N) = 0$.

A __$\mu$-full $\Sigma$-measurable set__ is a measurable set $F$ such that $\mu(S) = \mu(S \cap F)$ for every measurable set $S$; a __$\mu$-full set__ is any superset of a full measurable set.  In a probability measure space, we don\'t have to bother with $S$; $F$ will be a full set as long as $\mu(F) = 1$.  Classically, a full set is precisely the [[complement]] of a null set, but this doesn\'t hold in the constructive theory.

A property of elements of $X$ holds __$\mu$-almost everywhere__ if the set of values where it holds is a full set.

A measure is __complete__ if every full set is measurable.  We may form the __completion__ of a measure space by accepting as a measurable set the intersection of any set and a full set; these __$\mu$-measurable sets__ will automatically form a $\sigma$-algebra (or whatever $\Sigma$ originally was).  Classically, a measure is complete if and only if every null set is measurable and a set is $\mu$-measurable if and only if it is the [[symmetric difference]] between a measurable set and a null set.

A __$\mu$-finitely measurable set__ is a measurable set $M$ such that $\mu(S)$ is finite whenever $S \subseteq M$ is measurable; a __$\sigma$-finitely measurable set__ is any union of countably many finitely measurable sets.  Again, we don\'t have to bother with $S$ in a positive measure space.  Note that a measure space is ($\sigma$)-finite if and only if every measurable set is ($\sigma$)-finitely measurable.  The finitely measurable sets form a $\delta$-ring, and the $\sigma$-finitely measurable sets form a $\sigma$-ring.

Recall that a $\Sigma$-[[measurable function]] from $(X,\Sigma)$ to some other measurable space is any function $f$ such that the [[preimage]] under $f$ of a measurable set is always measurable (or something more complicated in the constructive theory).  Now that we have a measure space, let a __$\mu$-measurable function__ be a [[partial function]] $f$ from $X$ to some other measurable space such that the domain of $f$ is full and the preimage under $f$ of a measurable set is always $\mu$-measurable (that is measurable in the completion of $\mu$), and let two such functions be __$\mu$-equivalent__ if their [[equaliser]] is a full set.  We are really interested in the [[quotient set]] under this equivalence and so identify equivalent $\mu$-measurable functions.  Classically, every $\mu$-measurable function is equivalent to some (total) $\Sigma$-measurable function, so the definition is simpler in that case; however, partial functions still come up naturally in the classical theory, so it can be convenient to allow them rather than (as is usually done in a rigorous treatment) systematically replacing them with total functions.

A __$\mu$-integrable function__ is a $\mu$-measurable function $f$ such that the integral $\int_S f \,\mu$ (as defined below) exists for every measurable set $S$; it is enough to check $S = X$.  Equivalently, we may say that it is a $\mu$-measurable function $f$ such that the extended measure $f \mu$ (also defined below) is actually a finite measure.  (In any case, we get a finite measure $f \mu$ if $f$ is integrable.)


### Integration

In the following, 'measurable' will mean $\mu$-measurable.  That is, we assume that $\mu$ is complete and identify $\mu$-equivalent functions.  We will also assume that $\mu$ is a positive measure until I make sure of what must be done to generalise.

Given a measure $\mu$, a measurable set $S$, and a measurable function $f$, we will define the integral
$$ \int_S f \,\mu $$
(see above for variations in notation) in stages, from the simplest form of $f$ to the most arbitrary.

Each measurable subset $S \subseteq X$ induces a measurable [[characteristic function]] $\chi_S\colon X \to \mathbb{R}_+$ where $\chi_S(x) = 1$ if $x \in S$, $\chi_S(x) = 0$ if $x \in \neg{S}$.  In general, we have
$$ \int_S f \,\mu = \int_X \chi_S f \,\mu ,$$
so from now on we will assume that we are integrating over all of $X$ (and drop the subscript).

A __simple function__ is a finite $\mathbb{R}_+$-linear combination of measurable characteristic functions; the first form of integral that we define is
$$ \int \sum_{1 \leq i \leq n} a_i \chi_{S_i} \,\mu = \sum_{1 \leq i \leq n} a_i \mu(S_i) .$$ 

The integral is extended to all measurable functions $f\colon X \to [0, \infty]$ by the rule 
$$ \int f \,\mu = \sup \{ \int s \,\mu \;|\; 0 \leq s \leq f, s simple \} $$
if this [[supremum]] converges.  Classically, the integral either converges or diverges to infinity, so $\int f \,\mu$ exists in some sense in any case; the possibilities are more complicated constructively.

For any measurable function $f\colon X \to [-\infty, \infty]$, define $f_+$ and $f_{-}$ by 
$$ f_+(x) = \max\{f(x), 0\}, \qquad f_{-}(x) = \max\{-f(x), 0\} $$ 
so that $f = f_+ - f_{-}$, ${|f|} = f_+ + f_{-}$.  Then the final definition is
$$ \int f \,\mu = \int f_{+} \,\mu - \int f_{-} \,\mu $$
if both integrals on the right converge.  Classically, the other possibilities are $\infty$, $-\infty$, and $\infty - \infty$; not much can be done with the latter.

A measurable function $f$ is **integrable** with respect to $\mu$ if this integral converges.  It can be proved that all of the definitions above are consistent; that is, if the final definition is applied to a simple function, then it agrees with the original definition.


If $f$ takes values in the field $\mathbb{C}$ of [[complex numbers]] or in some more general [[Banach space]] $V$, then we can still ask whether ${|f|}$ is integrable.  If it is, then we say that $f$ is __absolutely integrable__.  We can then define the integral of $f$; we always have
$$ {\|\int f \,\mu\|} \leq \int {\|f\|} \,\mu .$$
This integral is easy to define if $V$ has a basis; for example, a measurable complex-valued function $f\colon X \to \mathbb{C}$ is integrable iff both its real and imaginary parts are integrable, and we have
$$ \int f \,\mu = \int \Re{f} \,\mu + \mathrm{i} \int \Im{f} \,\mu .$$

+-- {: .query}
I need to check [[HAF]] for more details here in the general case.  In particular, something can be integrable without being absolutely integrable (although not if it\'s complex-valued, of course) or indeed even without being valued in a (pseudo)normed space.
=--

The vector space of $V$-valued integrable functions is itself a Banach space, using the norm
$$ {\|f\|_1} \coloneqq \int {\|f\|} \,\mu .$$
Note that we must use the notion of measurable function as an equivalence class of functions to get a Banach space here; otherwise we have only a pre-Banach space (that is, a complete pseudonormed vector space).

This Banach space is called a __[[Lebesgue space]]__ and is denoted $L^1(\mu,V)$, $L^1(X,V)$, or just $L^1$, depending on context.  The default value of $V$ is usually either $\mathbb{R}$ or $\mathbb{C}$, depending on the author.  More general Lebesgue spaces of the form $L^p$ also exist; $f$ is in $L^p$ precisely when ${|f|^p}$ is integrable, and we use
$$ {\|f\|_p} \coloneqq \root p {\int {\|f\|^p} \,\mu} $$
as the norm.


## The algebra of measures

Note that
$$ (f \mu) (S) = \int \chi_S f \,\mu $$
makes $f \mu$ into a $V$-valued measure whenever $f$ is an integrable $V$-valued function.  When $f$ is $[-\infty,\infty]$-valued and $\mu$ is a signed measure, then $f$ is an extended measure which is finite iff $f$ is integrable.  We have
$$ (f g) \mu = f (g \mu) .$$
Thus integration can be seen as a way of multiplying a function by a measure to get another measure.

The [[Radon-Nikodym derivative]] is about reversing this.

Other topics: absolute continuity, etc.


## Noncommutative measure theory

Every commutative [[von Neumann algebra]] is isomorphic to the [[Lebesgue space]] $L^\infty(X,\mu)$ where $\mu$ is some measure (which is irrelevant) on a [[localisable measurable space]], and this extends to a [[dual category|duality]] between localisable measurable spaces and commutative von Neumann algebras.  This is similar to the correspondence between commutative $C^*$-[[C-star algebra|algebras]] and [[locally compact Hausdorff space]]s, which is the central approach to [[noncommutative geometry]].  It is useful to exploit the intuition that the theory of (noncommutative) von Neumann algebras is a noncommutative analogue of classical measure theory.


## Examples

* [[Haar measure]], [[Borel measure]], [[Radon measure]], [[spectral measure]]


## Related concepts

* [[measurable locale]]



[[!redirects measure space]]
[[!redirects measure spaces]]
[[!redirects measure]]
[[!redirects measures]]

[[!redirects finite measure]]
[[!redirects finite measures]]
[[!redirects positive measure]]
[[!redirects positive measures]]
[[!redirects signed measure]]
[[!redirects signed measures]]
[[!redirects complex-valued measure]]
[[!redirects complex-valued measures]]
[[!redirects valued measure]]
[[!redirects valued measures]]
[[!redirects V-valued measure]]
[[!redirects V-valued measures]]

[[!redirects finitely additive measure]]
[[!redirects finitely additive measures]]
[[!redirects extended measure]]
[[!redirects extended measures]]
[[!redirects sigma-finite measure]]
[[!redirects sigma-finite measures]]
[[!redirects ∞-finite measure]]
[[!redirects ∞-finite measures]]

[[!redirects null set]]
[[!redirects null sets]]
[[!redirects null subset]]
[[!redirects null subsets]]
[[!redirects full set]]
[[!redirects full sets]]
[[!redirects full subset]]
[[!redirects full subsets]]
[[!redirects complete measure]]
[[!redirects complete measures]]
[[!redirects complete measure space]]
[[!redirects complete measure spaces]]

[[!redirects finitely measurable set]]
[[!redirects finitely measurable sets]]
[[!redirects sigma-finitely measurable set]]
[[!redirects sigma-finitely measurable sets]]
[[!redirects ∞-finitely measurable set]]
[[!redirects ∞-finitely measurable sets]]

[[!redirects integral of a measure]]
[[!redirects integrals of a measure]]
[[!redirects integrals of measures]]
[[!redirects integral with respect to a measure]]
[[!redirects integrals with respect to a measure]]
[[!redirects integrals with respect to measures]]
[[!redirects simple function]]
[[!redirects simple functions]]
[[!redirects integrable function]]
[[!redirects integrable functions]]
[[!redirects absolutely integrable function]]
[[!redirects absolutely integrable functions]]

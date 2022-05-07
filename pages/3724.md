
# Dedekind cuts
* table of contents
{: toc}

## Idea

Dedekind cuts are a way to make precise the idea that a [[real number]] is that which can be approximated (in the [[absolute value]] metric) by [[rational numbers]].

In 1872, [[Richard Dedekind]] published _Stetigkeit und irrationale Zahlen_ (Continuity and irrational numbers), in which he pointed out that a real number may be uniquely determined its order relationships with rational numbers.  That is, the real number $x$ is determined by its __lower set__ $L_x$ and its __upper set__ $U_x$:
\[ \label{cuts} \begin {split}
   L_x \coloneqq \{ a\colon \mathbb{Q} \;|\; a \lt x \} ,\\
   U_x \coloneqq \{ b\colon \mathbb{Q} \;|\; x \lt b \}
.\end {split} \]
Dedekind had found great success understanding the 'ideal numbers' of [[ring theory]] as certain sets, which are what we now understand as [[ideal of a ring|ideals]].  So he defined a 'real number' as a pair of sets of rational numbers, the lower and upper sets shown above (actually a slight variation).  Such a pair of sets of rational numbers he called a 'Schnitt' (English 'cut'), nowadays called a 'Dedekind cut'.


## Definitions {#Definitions}

Exactly which pairs of sets of rational numbers can appear this way?  We will define a __Dedekind cut__ to be any pair $(L,U)$ of sets of rational numbers satisfying these conditions:

1.  $L$ is [[inhabited set|inhabited]]; that is, some rational number belongs to $L$.
2.  Similarly, $U$ is inhabited.
3.  $L$ is downward-closed; that is, if $a \lt b$ are rational numbers with $b \in L$, then $a \in L$.
4.  Similarly, $U$ is upward-closed: if $a \lt b$ are rational numbers with $a \in U$, then $b \in U$.
5.  $L$ is upward-open; that is, if $a \in L$, then $a \lt b$ for some $b \in L$.
6.  Similarly, $U$ is downward-open: if $b \in U$, then $a \lt b$ for some $a \in U$.
7.  If $a \lt b$ are rational numbers, then $a \in L$ or $b \in U$.
8.  If $a \in L$ and $b \in U$, then $a \lt b$.

Actually, this definition is redundant; any pair $(L,U)$ that satisfies (7&8) must also satisfy (3&4).  However, we state (3&4) explicitly to simplify the description of the variations below.

If $x \coloneqq (L,U)$ is a Dedekind cut, then we define $a \lt x$ to mean that $a \in L$ and define $x \lt b$ to mean that $b \in U$.


## Motivation

The point of condition (7) is that we can estimate $x$ as closely as we like by choosing appropriate rational numbers.

This is entirely [[constructive mathematics|constructive]].  We have $a_0 \lt x$ for some $a_0$ (by 1) and $x \lt b_0$ for some $b_0$ (by 2), so if we wish to estimate $x$ to within a positive rational number $\epsilon$, then we simply let $n$ be $\lceil{2/\epsilon}\rceil$ and apply (7) to each of the finitely many ($\lceil{n(b_0-a_0)}\rceil$) rational numbers with denominator $n$ that lie between $a_0$ and $b_0$.  This will eventually give us a numerator $i$ such that $(i-1)/n \lt x \lt (i+1)/n$, so we have estimated $x$ within $2/n \leq \epsilon$.  Alternatively, to estimate $x$ to $n$ digits after a decimal point (with an uncertainty of $1$ in the last digit), apply (7) to each of the $\lceil{(b_0-a_0) \times 10^n}\rceil$ numbers between $a_0$ and $b_0$ that have $n$ digits after the decimal point.  (We can never constructively determine the final digit with perfect certainty; for example, if we successively estimate $x$ as $0.5, 0.50, 0.500, \ldots$, no finite number of such estimates can ever ensure that $x$ won\'t come out to $0.4999\cdots9998$ when we go one digit farther.)

Besides giving us a place to begin our estimation, (1&2) ensure that $x$ is finite.  Condition (8) enforces the [[transitive relation|transitivity]] law $a \lt x \lt b \implies a \lt b$; (3&4) are likewise forms of transitivity.  (5&6) ensure that, even if $x$ happens to be a rational number, we are using the sets $L_x$ and $U_x$ given in (eq:cuts) instead of their closures (defined with $\leq$ instead of $\lt$).


## Properties

We define $x \lt y$ to mean that there exists a rational number $a$ such that $x \lt a \lt y$; that is, some rational number belongs to both the upper set of $x$ and the lower set of $y$.  It is then straightforward to prove that $\lt$ is a [[linear order]]:

*  [[asymmetric relation|Asymmetry]]:  If $x \lt y$ and $y \lt x$, pick $a$ such that $x \lt a \lt y$ and $b$ such that $y \lt b \lt x$.  Applying (8) in two ways, $a \lt b$ and $b \lt a$, which is impossible.
*  [[comparison relation|Comparison]]:  If $x \lt z$ and $y$ is a Dedekind cut, then pick $a$ such that $x \lt a \lt z$.  Using (5) or (6), we can generalise this to two rational numbers $a$ and $b$ such that $x \lt a \lt b \lt z$.  Applying (7) to $a \lt b$, we get $x \lt y$ (if $a \lt y$) or $y \lt z$ (if $y \lt b$).
*  [[connected relation|Connectedness]]:  Suppose that $x \lt y$ and $y \lt x$ both fail, and suppose that $a \lt y$.  By (5), we have $a \lt b \lt y$ for some $b$.  Applying (7), we have $a \lt x$ or $x \lt b$.  Since $x \lt b \lt y$ contradicts our assumptions, we have $a \lt x$.  In summary, $a \lt y \implies a \lt x$.  We can prove $a \lt x \implies a \lt y$, $b \lt x \implies b \lt y$, and $b \lt y \implies b \lt x$ similarly.  Therefore, $x$ and $y$ are equal (as pairs of subsets).

As usual with a linear order, we define $x \leq y$ to mean that $y \lt x$ is false.  In particular, connectedness of $\lt$ corresponds to [[antisymmetric relation|antisymmetry]] of $\leq$.

We can also derive a Dedekind cut from any rational number $x$ by taking (eq:cuts) to be the definition of $x$ as a Dedekind cut.  Thus every rational number is interpreted as a real number.  This is a strict inclusion of linear orders:

*  If $x \lt y$ as rational numbers, then let $a$ be the rational number $(x+y)/2$; we have $x \lt a \lt y$, so $x \lt y$ as real numbers.

In this way, the Dedekind cuts form an extension of the linearly ordered set of rational numbers.  More than that, this extension is [[Dedekind completion|Dedekind-complete]], which basically means that you cannot extend further by taking Dedekind cuts of Dedekind cuts.

To be explicit, suppose that $(L,U)$ is a pair of sets of Dedekind cuts (rather than of rational numbers) that satisfies (1--8), using Dedekind cuts in place of rational numbers.  Let $\sup L$ be the union of the left halves of the cuts that appear in $L$, and let $\inf U$ be the union of the right halves of the cuts that appear in $U$.  Then one can prove that $x \coloneqq (\sup L, \inf U)$ is a Dedekind cut (of rational numbers), and furthermore that $L$ and $U$ may be recovered from $x$ as in (eq:cuts), again using Dedekind cuts in place of rational numbers.

We say that the Dedekind cuts form the [[Dedekind completion]] of the linear order $\mathbb{Q}$.


+-- {: .num_remark}
###### Remark

Being a member of the lower (resp. the upper) set of a Dedekind cut is almost [[stable proposition|stable]] (under [[double negation]]): For any rational number $a$ it holds that $a \in L$ iff there exists a rational number $b \gt a$ such that $\neg\neg(b \in L)$. "Only if" is by condition (5). "If" is by condition (7): We have $a \in L$ or $b \in U$. In the first case we're done; in the second case it follows that $\neg(b \in L)$ by (8), which is a contradiction to $\neg\neg(b \in L)$.
=--

+-- {: .num_remark}
###### Remark

Equality of Dedekind cuts is [[stable proposition|stable]] (under [[double negation]]).
=--


## Variations

A Dedekind cut is, in full clarity, a __bounded, open, rounded, located, two-sided Dedekind cut of rational numbers__.  But there are several simple variations on the definition above, many of which may be found in the literature.


### Overdetermined cuts

The conditions (5&6) are not really necessary.  If you leave them out, then the result that $\lt$ is a [[connected relation]] on Dedekind cuts fails; but instead we identify cuts $x$ and $y$ whenever $x \leq y \leq x$.  Then the linearly ordered set of real numbers becomes a [[quotient set]] of the set of cuts.  In a similar vein, we can weaken (3,4,7) as follows:

* 3&#8242;:  If $a \lt b$ are rational numbers with $b \in L$, then $a' \in L$ for some $a' \lt a$.
* 4&#8242;:  If $a \lt b$ are rational numbers with $a \in U$, then $b' \in U$ for some $b' \gt b$.
* 7&#8242;:  If $a \lt b$ are rational numbers, then $a' \in L$ for some $a' \lt a$ or $b' \in U$ for some $b' \gt b$.

Just as (3,4) follow from (7,8), so (3&#8242;,4&#8242;) follow from (7&#8242;,8).  Again, $\lt$ is no longer connected, but we still get a linear order on a quotient set.  The weakest axiom system that will give the correct linear order on the quotient is (1,2,7&#8242;,8).  Incidentally, you can also recover the original definition using (3,4,7&#8242;) in place of (7).

To emphasise that one does require (5,6), one may speak of an __open cut__.  To emphasise that one does require (3,4), one may speak of a __rounded cut__.

Note that we may elegantly (although requiring a fancier [[logic]]) combine (3,4,5,6) into two conditions as follows:

* (3&5):  A rational number $a$ belongs to $L$ if and only if there exists a rational number $b \in L$ such that $a \lt b$.
* (4&6):  A rational number $b$ belongs to $U$ if and only if there exists a rational number $a \in U$ such that $a \lt b$.


### Covering cuts

Another approach is to *strengthen* (7):

* 7&#8243;:  Every rational number belongs to $L$ or $U$.

While (7&#8243;) alone does not imply (7), it does together with (8).  Also note that, using (8), we can even change 'or' to '[[xor]]' in (7&#8243;).

The cuts that satisfy (1--6, 7&#8243;, 8) are precisely the cuts that define [[irrational number]]s.  If we remove either (5) or (6), then the resulting axioms define one cut for each rational number as well.  If we remove *both* (5) and (6), then we get two cuts for each rational number and must (as in the previous section) pass to a quotient; this was actually Dedekind\'s original 1872 system.  These versions are not acceptable [[constructive mathematics|constructively]] (and we cannot even prove that they are closed under addition), but they work fine if you use [[excluded middle]].  (Actually, the somewhat weaker [[limited principle of omniscience]] seems to suffice.)


### One-sided cuts

Suppose that we consider only $L$ and demand (1,3,5), the axioms that refer only to $L$.  Any such set $L$ of rational numbers is a __lower cut__.  Similarly, a set $U$ that satisfies (2,4,6) is an __upper cut__.  If we demand that the set $L$ or $U$ is a [[proper subset]], then we have a __bounded__ lower/upper cut.  If we wish to emphasise that we are discussing a cut as defined above, with both $L$ and $U$, we speak of a __two-sided cut__.

Assuming [[excluded middle]], every bounded lower or upper cut generates a two-sided cut, by whichever of these rules is needed:
\[ \label{twosiding} \begin {split}
   U \coloneqq \{ b\colon \mathbb{Q} \;|\; \forall a \in L,\; a \lt b \} ,\\
   L \coloneqq \{ a\colon \mathbb{Q} \;|\; \forall b \in U,\; a \lt b \}
.\end {split} \]
In addition, the unbounded lower cut $L \coloneqq \mathbb{Q}$ represents $\infty$, while the unbounded upper cut $U \coloneqq \mathbb{Q}$ represents $-\infty$.

In [[constructive mathematics]], one-sided cuts define a potentially more general notion of real number, called a [[lower real]] or [[upper real]] (with the same direction as the cut).  Unlike the covering cuts in the previous section, these are actually of interest constructively.  If we wish to emphasise or clarify that we are discussing a two-sided cut as in our original definition, rather than a one-sided cut which has been made two-sided through (eq:twosiding) (which may not satisfy (7) constructively), then we may speak of a __located cut__.


### Unbounded cuts

If we drop conditions (1&2), then the result is an __extended cut__; these represent [[extended real number]]s.  If we wish to emphasise or clarify that we are discussing a cut that satisfies (1,2), then we may speak of a __bounded cut__.

By [[excluded middle]], every extended cut is either a Dedekind cut, $(\mathbb{Q},\empty)$, or $(\empty,\mathbb{Q})$.  While the bounded cuts represent real numbers, the other two extended cuts represent $\pm\infty$.


### Interval cuts
{#intervals}

If we drop (7) (but keep 3&4), then the result is an __interval cut__; these represent intervals of the form $[x,y]$ for $x \leq y$, where $x$ is a lower real and $y$ is an upper real.  If we use only (1--6), then we allow for __back-to-front intervals__ $[x,y]$ where $x \leq y$ is no longer required.  Even classically, we cannot represent back-to-front intervals as subsets of the real line, but it is still possible to compute with them.

Whereas a located Dedekind cut can be approximated as closely as we wish, an interval cut represents a number as we measure it in the real world, where we may not be technically able (or even theoretically able, as in [[quantum physics]]) to make a more precise measurement.  A back-to-front interval indicates that we have made contradictory measurements, perhaps as a result of experimental error.

An article on [[interval arithmetic]] is probably the right place to talk about these systems (although there are many varieties of interval arithmetic).


### Cuts of other numbers

Instead of starting with rational numbers, we could use any [[dense suborder|dense]] subset of $\mathbb{Q}$; the result would be equivalent.  For example, we could start with the [[dyadic number]]s to show more explicitly how real numbers are represented by rational numbers written in binary notation.  Alternatively, we could start with something larger than (or incomparable with) $\mathbb{Q}$ that is still a dense subset of $\mathbb{R}$ (although you have to know what $\mathbb{R}$ is to state this).  For example, we could start with the real [[algebraic number]]s or the [[computable number]]s.

The basic theory also generalises immediately to any unbounded, [[dense linear order]] $S$; again, the result is equivalent as long as $S$ is a [[countably infinite set]].  The theory may be generalised further even to orders which may not be unbounded, dense, or even linear, but this requires modifications; see [[Dedekind completion]] for unbounded dense [[quasiorders]] or unbounded dense [[irreflexive comparisons]] or Sections 4.31--39 of _[[HAF]]_ for even more generality.


## References

* [[Richard Dedekind]]; 1872; _Stetigkeit und irrationale Zahlen_:
   *  [Google Books](http://books.google.com/books?id=AO4GAAAAYAAJ) (in Fraktur font),
   *  [retyped](http://www.math.ru.nl/werkgroepen/gmfw/bronnen/dedekind2.html) 
* [[Richard Dedekind]], _Continuity and irrational numbers_, in Essays on the Theory of Numbers (trans. W. Beman), 1901 ([Project Gutenberg](http://www.gutenberg.org/ebooks/21016))

*  [[Paul Taylor]]; 2007--2009(?); [Dedekind cuts](http://www.paultaylor.eu/ASD/dedras/classical)
*  _[[HAF]]_, 4.31--4.39


[[!redirects Dedekind cut]]
[[!redirects Dedekind cuts]]
[[!redirects Dedekind real]]
[[!redirects Dedekind reals]]
[[!redirects Dedekind real number]]
[[!redirects Dedekind real numbers]]

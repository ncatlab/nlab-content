
# Extended real numbers
* table of contents
{: toc}

## Idea

An extended real number is usually a [[real number]], but it might be $\pm\infty$.  We can also think of an extended real number as a number of the form $\log(1/t - 1)$ for $t \in [0,1]$ (including $t = 0,1$) or a number of the form $\tan t$ for $t$ a real number (including an odd multiple of $\pi/2$).

There are actually two slightly different notions that both go by the name 'extended real number': one in which $\infty$ and $-\infty$ are distinct (the [[logarithm]]), and one in which they are identified (the [[tangent]]).  The latter kind forms a [[quotient set|quotient space]] of the former.


## Definitions

Classically, one simply defines an extended real number to be either a real number, $\infty$, or (for the version in which these are distinguished) $-\infty$.  However, one has to take more care for a definition that works in [[constructive mathematics]].  Such a definition may also be interesting to a classical mathematician for its own sake, of course.


### As extended Dedekind cuts

One way to define extended real numbers is to adjust the notion of [[Dedekind cut]].  This naturally defines the sort of extended real number in which $\infty \ne -\infty$.

So let an __extended Dedekind cut__ be a pair $(L,U)$ of sets of [[rational numbers]] such that:

*  For each $a \in L$, there is some $b \in L$ such that $a \lt b$.
*  For each $b \in U$, there is some $a \in U$ such that $a \lt b$.
*  Whenever $a \lt b$ are rational numbers, either $a \in L$ or $b \in U$ (non-exclusively).
*  If $a \in L$ and $b \in U$, then $a \lt b$.

(The usual slight variations available in the notion of Dedekind cut apply here as well, in the same ways.)

If $L$ is empty, then $U$ must be the set of all rational numbers; this extended cut represents $-\infty$.  If $U$ is empty, then $L$ must be the set of all rational numbers; this extended cut represents $\infty$.  An extended Dedekind cut is __bounded__ if instead $L$ and $U$ are both [[inhabited set|inhabited]].  The bounded cuts are the usual Dedekind cuts that represent real numbers.  So the only change is that we no longer require this boundedness condition.

The space of extended real numbers in this sense is often denoted $\overline{\mathbb{R}}$.  As a [[topological space]] (or [[locale]], constructively), it is the [[end compactification]] of the [[locally compact space]] $\mathbb{R}$.  Geometrically, this is a [[line segment]], the __extended real number line segment__.


### As ratios of real numbers

Another way to define extended real numbers is to represent them as ratios of real numbers.  This naturally defines the sort of extended real number in which $\infty = -\infty$.

So let a __nontrivial ratio__ of real numbers be a pair $(a,b)$ of real numbers such that either $a \ne 0$ or $b \ne 0$.  (By $\ne$ we mean the usual [[apartness relation]] on real numbers.)  We write the ratio as $a &#8758; b$, and we consider $a &#8758; b$ and $c &#8758; d$ to be __equivalent__, written $a &#8758; b &#8759; c &#8758; d$, if $a d = b c$.  This is an [[equivalence relation]] on nontrivial ratios; modulo this equivalence relation, the nontrivial ratios represent extended real numbers.

If $b \ne 0$, then the nontrivial ratio $a &#8758; b$ is equivalent to $a/b &#8758; 1$ and represents the real number $a/b$.  The nontrivial ratios $a &#8758; 0$ for $a \ne 0$ are all equivalent and represent $\infty$.  (The ratio $0 &#8758; 0$ is considered trivial and does not represent any extended real number.  If we want to include it, then we get a [[wheel]].)

This is a special case of forming the [[projective line]] of a [[field]], in this case the field of real numbers.  Accordingly, the space of extended real numbers in this sense is often denoted $\mathbb{P}\mathbb{R}^1$.  As a [[topological space]] (or [[locale]], constructively), it is the [[one-point compactification]] of the [[locally compact space]] $\mathbb{R}$.  Geometrically, this is a [[circle]], the __extended real number circle__.


## Orders

We can put a [[linear order]] on $\overline{\mathbb{R}}$ by setting $-\infty \lt x \lt \infty$ for any real number $x$.  In terms of Dedekind cuts, this is the straightforward extension of the usual definition of $\lt$ on such cuts.

We can put a [[cyclic order]] $R$ on $\mathbb{P}\mathbb{R}^1$ by setting $R(x,y,z)$ true if any of the following hold:

*  $x \lt y \lt z$ are all real numbers,
*  $y \lt z \lt x$ are all real numbers,
*  $z \lt x \lt y$ are all real numbers,
*  $y \lt z$ are real numbers and $x = \infty$,
*  $z \lt x$ are real numbers and $y = \infty$,
*  $x \lt y$ are real numbers and $z = \infty$.

(These orders can be defined constructively too, with a little more work.)


## Arithmetic

In $\overline{\mathbb{R}}$, we take $x + \infty$, $\infty + x$, and $\infty + \infty$ to be $\infty$ (for $x$ a real number) and similarly $x - \infty$, $-\infty + x$, and $-\infty - \infty$ to be $-\infty$.  Of course, $\infty$ and $-\infty$ are opposites (additive inverses).  These are all straightforward extensions of the usual definition of addition for Dedekind cuts.  However, when we try $\infty - \infty$ or $-\infty + \infty$, the Dedekind cut calculation gives us $(\empty,\empty)$, which is not a cut, even extended.  (Although some sources define these sums, it is most common to leave them undefined, I think.)

In $\mathbb{P}\mathbb{R}^1$, we similarly take $x + \infty$ and $\infty + x$ to be $\infty$ (for $x$ a real number).  Now $\infty$ is its own opposite.  These all agree with the additive rule $(a &#8758; b) + (c &#8758; d) = (a d + b c &#8758; b d)$.  If we apply this to $\infty + \infty$, however, the result is $0 &#8758; 0$, so again we take that to be undefined.  (However, in this case, the definition $\infty + \infty = \infty$ is also widely seen, I think.)

Note that although we have blithely referred to 'additive inverses', addition does not form a [[group]] in either case.  The reason is that the opposites of $\pm\infty$ are not really additive inverses, since the result of the relevant addition is undefined rather than zero.  (If you define the sum to be zero so that they become inverses, then you lose associativity; ultimately, there is no way to make a group, since $0 + \infty = 1 + \infty$ shows that the operation is not cancellative.)

In $\overline{\mathbb{R}}$, we take $x \cdot {\pm \infty}$ to be $\pm \infty$ when $x \gt 0$ but $x \cdot {\pm \infty} = \mp \infty$ for $x \lt 0$.  (This continues to work even if $x$ is infinite too.)  But now $0 \cdot {\pm \infty}$ is undefined.  (Many sources define this to be zero, although I think this is really because they are using $0 \cdot \infty = 0$ in the nonnegative [[lower reals]], at least in applications to [[measure theory]].)

In $\mathbb{P}\mathbb{R}^1$, we take $x \cdot \infty$ to be $\infty$ as long as $x \ne 0$; but $0 \cdot \infty$ is undefined (although it is defined in the [[wheel]] over $\mathbb{R}$).  We may write $1/\infty = 0$ and $1/0 = \infty$ to define division, but again these are not really multiplicative inverses.  (With $0 \cdot 1 = 0 \cdot 2$ and $\infty \cdot 1 = \infty \cdot 2$, multiplication is not cancellative either.)


## Constructive aspects

The definitions as phrased above give us *[[located real number|located]]* extended real numbers.  We can of course consider unlocated extended real numbers, either [[one-sided real number|one-sided]] or [[MacNeille real number|MacNeille]].  The natural definitions of these are at least somewhat extended; the lower one-sided reals include $\infty$, the upper one-sided reals include $-\infty$, and the MacNeille reals include both (with $\infty \ne -\infty$).  However, one can always restrict to bounded numbers or alternatively fully extend the one-sided numbers, so being extended and being located are technically independent.  Still, whenever $\pm\infty$ shows up constructively (especially if only one of them appears), then this is a sign that one may want to generalise to one-sided (or even MacNeille) reals.

This has implications for arithmetic; for example, while $0 \cdot \infty$ is undefined in the extended located real numbers (and in the MacNeille real numbers), it is $0$ in the nonnegative lower real numbers (and $\infty$ in the extended nonnegative upper real numbers).


[[!redirects extended real]]
[[!redirects extended reals]]
[[!redirects extended real number]]
[[!redirects extended real numbers]]

[[!redirects extended real line]]
[[!redirects extended real number line]]
[[!redirects extended real line segment]]
[[!redirects extended real number line segment]]
[[!redirects extended real circle]]
[[!redirects extended real number circle]]

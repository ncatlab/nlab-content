
# Direct sums of Banach spaces
* table of contents
{: toc}

## Idea

The concept of [[direct sum]] extends easily from [[vector spaces]] to [[topological vector spaces]]; we wish to extend it to [[Banach spaces]].

When taking the direct sum of two (or any [[finite set|finite number]]) of Banach spaces, the only question is which [[norm]] to use; and we have a choice, entirely analogous to the choice of norms to put on the [[Cartesian space]] $\mathbb{R}^2$ (and its [[complexification|complexified]] variant $\mathbb{C}^2$): one for each [[extended real number]] $p \in [1, \infty]$ (and actually more choices than that).  In fact, this is a special case, the direct sum of two copies of the [[line]] $\mathbb{R}$ or $\mathbb{C}$.

For infinitely many summands, the na&#239;ve direct sum is not [[complete space|complete]] under any of these norms, so we must complete it, getting different results for each $p$; this is analogous to the different [[sequence space]]s $l^p$.  Again, this is a special case, a direct sum of infinitely many copies of the line.

In accordance with the last analogy, we speak of $l^p$-direct sums.  In fact, even more variety is possible, corresponding to other possible norms on standard Banach spaces.


## Definitions

Let $V$ be a [[Banach space]] equipped with a [[Schauder basis]] $B$, so that every element of $V$ may be written uniquely as an infinitary [[linear combination]] of elements of $B$.  Suppose also that that the basis is normal: the norm of any element of $B$ is $1$; and absolute:
$$ {\Big\| \sum_i a_i i \Big\|} = {\Big\| \sum_i {|a_i|} i \Big\|} $$
(where the $i$ are the elements of the basis and the $a_i$ are scalars).  The typical example is the [[sequence space]] $l^p$ (or a finitary or uncountablary version) with its usual basis.

Then given a [[family]] $W$ of Banach spaces indexed by the [[set]] $B$, the __$V$-direct sum__ of this family is a [[subspace]] of the [[direct product]] of the family, consisting of those $w$ such that this sum converges:
$$ \sum_i {\|w_i\|} i $$
(where again the $i$ are the basis vectors and $w_i$ is in the space $W_i$, with the norm of $w_i$ taken in $W_i$ and the sum taken in $V$).  Then the norm of $w$ is the norm of this sum:
$$ {\|w\|} \coloneqq {\Big\| \sum_i {\|w_i\|} i \Big\|} .$$

We may succinctly write the $V$-direct sum as follows:
$$ \oplus^V_i W_i \coloneqq \Big\{ (w_i)_i \;\Big|\; {\Big\| \sum_i {\|w_i\|} i \Big\|} \lt \infty \Big\} .$$
Strictly speaking, the only condition on the right-hand side is that the sum exists in $V$; then of course its norm will be positive.  However, often some sense can be established for the sum outside of $V$ but then it will have no (finite) norm.

In particular, if $V = l^p$ (or a finitary or uncountablary version of such) for $1 \leq p \lt \infty$, then
$$ \oplus^p_i W_i \coloneqq \Big\{ (w_i)_i \;\Big|\; \sqrt[p] {\sum_i {\|w_i\|^p}} \lt \infty \Big\} ;$$
and if $V = l^\infty$, then
$$ \oplus^\infty_i W_i \coloneqq \Big\{ (w_i)_i \;\Big|\; \sup_i {\|w_i\|} \lt \infty \Big\} .$$
These are the __$l^p$-direct sum__ and __$l^\infty$-direct sum__ (which is really a special case).  In particular, we have the __$l^1$-direct sum__:
$$ \oplus^1_i W_i \coloneqq \Big\{ (w_i)_i \;\Big|\; \sum_i {\|w_i\|} \lt \infty \Big\} .$$


## Properties

If [[short map|short]] [[linear maps]] are taken as the [[morphisms]] in the category of Banach spaces, then the $l^1$-direct sum is the [[coproduct]], and the $l^\infty$-direct sum is the [[product]].

We can also consider the abstract concepts of [[direct sum]] and [[weak direct product]]; here again the $l^1$-direct sum is the direct sum, and the $l^\infty$-direct sum is the weak direct product.  (It is quite common for coproduct and direct sum to be the same, but weak direct product usually diverges from the product for infinitely many object.  That they match up here cruicially depends on [[complete space|completeness]].)

If every Banach space in a direct sum is a [[Hilbert space]], then their $l^2$-direct sum is also a Hilbert space.  This is the standard notion of __direct sum of Hilbert spaces__.  In [[Hilb]], this the abstract [[direct sum]], the [[weak direct product]], and the [[coproduct]].  Thus for finitely many objects, it is a [[biproduct]] (so $Hilb$ behaves rather like [[Vect]]).

Any Banach space $V$ with basis $B$ is the $V$-direct sum of ${|B|}$ copies of the line ($\mathbb{R}$ or $\mathbb{C}$).


## Direct integrals

As $l^p$ is the [[Lebesgue space]] $L^p$ for a [[measure space]] with [[counting measure]], and infinitary sums are simply the [[integrals]] on such a measure space, we may generalise from direct sums of Banach spaces to their [[direct integral]]s.  This is particularly common (using $p = 2$) for [[Hilbert spaces]].


## References

Here\'s something about direct sums of finitely many Banach spaces using norms (on $\mathbb{C}^n$) *other* than the usual $l^p$-norms:

*  Kato, Saito, Timura (2003); On $\psi$-direct sums of Banach spaces and convexity; Journal of the Australian Mathematical Society 75, 413--422; [web](http://www.austms.org.au/Publ/Jamsa/V75P3/n57.html)

Here, $\psi$ is the norm, viewed as a [[convex function]] of multiple arguments.


[[!redirects direct sum of a Banach space]]
[[!redirects direct sums of a Banach space]]
[[!redirects direct sum of Banach spaces]]
[[!redirects direct sums of Banach spaces]]

[[!redirects direct sum of a Hilbert space]]
[[!redirects direct sums of a Hilbert space]]
[[!redirects direct sum of Hilbert spaces]]
[[!redirects direct sums of Hilbert spaces]]

[[!redirects l1-direct sum]]
[[!redirects l1-direct sums]]
[[!redirects l-1-direct sum]]
[[!redirects l-1-direct sums]]
[[!redirects l^1-direct sum]]
[[!redirects l^1-direct sums]]
[[!redirects l_1-direct sum]]
[[!redirects l_1-direct sums]]
[[!redirects l1 direct sum]]
[[!redirects l1 direct sums]]
[[!redirects l-1 direct sum]]
[[!redirects l-1 direct sums]]
[[!redirects l^1 direct sum]]
[[!redirects l^1 direct sums]]
[[!redirects l_1 direct sum]]
[[!redirects l_1 direct sums]]

[[!redirects lp-direct sum]]
[[!redirects lp-direct sums]]
[[!redirects l-p-direct sum]]
[[!redirects l-p-direct sums]]
[[!redirects l^p-direct sum]]
[[!redirects l^p-direct sums]]
[[!redirects l_p-direct sum]]
[[!redirects l_p-direct sums]]
[[!redirects lp direct sum]]
[[!redirects lp direct sums]]
[[!redirects l-p direct sum]]
[[!redirects l-p direct sums]]
[[!redirects l^p direct sum]]
[[!redirects l^p direct sums]]
[[!redirects l_p direct sum]]
[[!redirects l_p direct sums]]

[[!redirects linfty-direct sum]]
[[!redirects linfty-direct sums]]
[[!redirects l-infty-direct sum]]
[[!redirects l-infty-direct sums]]
[[!redirects l^infty-direct sum]]
[[!redirects l^infty-direct sums]]
[[!redirects l_infty-direct sum]]
[[!redirects l_infty-direct sums]]
[[!redirects linfty direct sum]]
[[!redirects linfty direct sums]]
[[!redirects l-infty direct sum]]
[[!redirects l-infty direct sums]]
[[!redirects l^infty direct sum]]
[[!redirects l^infty direct sums]]
[[!redirects l_infty direct sum]]
[[!redirects l_infty direct sums]]
[[!redirects linfin-direct sum]]
[[!redirects linfin-direct sums]]
[[!redirects l-infin-direct sum]]
[[!redirects l-infin-direct sums]]
[[!redirects l^infin-direct sum]]
[[!redirects l^infin-direct sums]]
[[!redirects l_infin-direct sum]]
[[!redirects l_infin-direct sums]]
[[!redirects linfin direct sum]]
[[!redirects linfin direct sums]]
[[!redirects l-infin direct sum]]
[[!redirects l-infin direct sums]]
[[!redirects l^infin direct sum]]
[[!redirects l^infin direct sums]]
[[!redirects l_infin direct sum]]
[[!redirects l_infin direct sums]]
[[!redirects linfinity-direct sum]]
[[!redirects linfinity-direct sums]]
[[!redirects l-infinity-direct sum]]
[[!redirects l-infinity-direct sums]]
[[!redirects l^infinity-direct sum]]
[[!redirects l^infinity-direct sums]]
[[!redirects l_infinity-direct sum]]
[[!redirects l_infinity-direct sums]]
[[!redirects linfinity direct sum]]
[[!redirects linfinity direct sums]]
[[!redirects l-infinity direct sum]]
[[!redirects l-infinity direct sums]]
[[!redirects l^infinity direct sum]]
[[!redirects l^infinity direct sums]]
[[!redirects l_infinity direct sum]]
[[!redirects l_infinity direct sums]]
[[!redirects l∞-direct sum]]
[[!redirects l∞-direct sums]]
[[!redirects l-∞-direct sum]]
[[!redirects l-∞-direct sums]]
[[!redirects l^∞-direct sum]]
[[!redirects l^∞-direct sums]]
[[!redirects l_∞-direct sum]]
[[!redirects l_∞-direct sums]]
[[!redirects l? direct sum]]
[[!redirects l? direct sums]]
[[!redirects l-∞ direct sum]]
[[!redirects l-∞ direct sums]]
[[!redirects l^? direct sum]]
[[!redirects l^? direct sums]]
[[!redirects l_? direct sum]]
[[!redirects l_? direct sums]]

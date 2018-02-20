
# Absolutely continuous functions
* table of contents
{: toc}

## Idea

The basic idea behind a [[continuous function]] is that the output of the function can be made to change by only a small amount so long as the input is allowed to change by only a small amount.  There are, of course, different ways to make this precise, including [[uniformly continuous functions]] and [[Lipschitz continuous functions]].  With an absolutely continuous function, you allow multiple changes to multiple inputs to combined into a single total change (and one considers the [[absolute values]] of the changes, so that they won\'t cancel).

The result is a notion of function that gets along well with the [[fundamental theorem of calculus]] in the context of the [[Lebesgue integral]] on the [[real line]].  Absolute continuity is weaker than Lipschitz continuity but stronger than mere (pointwise) continuity.


## Definitions

The first definition below is the most elementary; that the others are equivalent are important theorems.

Let $a$ and $b$ be [[real numbers]], and let $f$ be a real-valued [[function]] on the [[interval]] $[a,b]$.  Then $f$ is __absolutely continuous__ on $[a,b]$ iff:

+-- {: .num_defn #elementary}
###### Definition

Given any [[positive number]] $\epsilon$, for some positive number $\delta$, given any [[natural number]] $n$ and any $2n$-tuple of elements of $[a,b]$, interpreted as an $n$-tuple of nonoverlapping subintervals of $[a,b]$, if the total length of the intervals is less than $\delta$, then the total variation of $f$ on the intervals is less than $\epsilon$.  That is (after $\epsilon$ and $\delta$), given $a \leq a_1 \leq b_1 \leq a_2 \leq b_2 \leq \cdots \leq a_n \leq b_n \leq b$, if
$$ \sum_{i = 1}^n (b_i - a_i) \lt \delta ,$$
then
$$ \sum_{i = 1}^n {|{f(b_i) - f(a_i)}|} \lt \epsilon .$$
=--

Various trivial variations of this may be met with: the comparison with $\delta$ and/or $\epsilon$ may be weak instead of strict; the number of subintervals may be infinite (so long as they are still nonoverlapping), since an infinite sum (of nonnegative numbers, as we have here) is simply a [[supremum]] of finite sums; and of course we may start by specifying that the $2n$ numbers come in order as the endpoints of the $n$ subintervals, rather than starting with any $2n$ numbers and then putting them in order and forming the subintervals from those.  (Note that putting them in order is fine even in [[constructive analysis]], since choosing the $i$th element in order from an unordered list of [[rational numbers]] is continuous, so may be extended constructively to real numbers, although we can\'t assume that the ordered list is a permutation of the original unordered list.)

For the next definition, fix a model of [[nonstandard analysis]].

+-- {: .num_defn #nonstandard}
###### Definition

Given any [[hypernatural number]] $n$ in the model and any $2n$-tuple of elements of the nonstandard extension of $[a,b]$, interpreted as an $n$-tuple of nonoverlapping subintervals of $[a,b]$, if the total length of the intervals is [[infinitesimal number|infinitesimal]], then the total variation of $f$ on the intervals is infinitesimal.  That is, given [[hyperreal numbers]] $a \leq a_1 \leq b_1 \leq a_2 \leq b_2 \leq \cdots \leq a_n \leq b_n \leq b$, if
$$ \sum_{i = 1}^n (b_i - a_i) \approx 0 ,$$
then
$$ \sum_{i = 1}^n {|{f^*(b_i) - f^*(a_i)}|} \approx 0 .$$
=--

See [Tuckey 1993](#Tuckey1993), pages 34--36.

That the next definition is equivalent is the [[fundamental theorem of calculus]] for the [[Lebesgue integral]] on the [[real line]].

+-- {: .num_defn #Lebesgue}
###### Definition

There exists a Lebesgue-integrable function $g$ on $[a,b]$ such that $f(x) = f(a) + \int_{a}^{x} g(x) \,\mathrm{d}x$ for $x \in [a,b]$.  (This is a [[semidefinite integral]].)
=--

In this case, $g$ must equal the [[derivative]] $f'$ [[almost everywhere]] on $[a,b]$.  (So in particular, $f$ is differentiable almost everywhere with a Lebesgue-integrable derivative, although this is not enough without requiring that $f$ be an indefinite integral of its derivative.)

+-- {: .num_defn #Luzin}
###### Definition

The function $f$ is [[uniformly continuous]] on $[a,b]$, $f$ is of [[bounded variation]] on $[a,b]$, and the [[direct image]] under $f$ of any [[null subset]] of $[a,b]$ is null.
=--

+-- {: .num_defn #Stieltjes}
###### Definition

The [[Stieltjes measure]] $\mathrm{d}f$ is [[absolutely continuous measure|absolutely continuous]] with respect to [[Lebesgue measure]] on $[a,b]$.
=--

The last of these is the source of the term 'absolutely continuous' as applied to measures.


## Generalizations

One may easily generalize the [[codomain]] of the elmeentary definition of absolutely continuous functions to any [[metric space]].


## Examples

The cube-root function is absolutely continuous (on any bounded interval) but not Lipschitz continuous (on any interval containing $0$).

The [[Cantor function]] is *not* absolutely continuous, even though it is differentiable almost everywhere (with Lebesgue-integrable derivative).


## References

* Curtis Tuckey. 1993. Nonstandard Methods in the Calculus of Variations. CRC Press. [Google books snippet](https://books.google.com/books?id=RvrC1mw9tIEC&q=%22absolutely+continuous%22#v=snippet&q=%22absolutely%20continuous%22&f=false).
  {#Tuckey1993}


[[!redirects absolutely continuous function]]
[[!redirects absolutely continuous functions]]
[[!redirects absolutely continuous mapping]]
[[!redirects absolutely continuous mappings]]
[[!redirects absolutely continuous map]]
[[!redirects absolutely continuous maps]]

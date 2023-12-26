
\tableofcontents

## Definition

### Total preorders

A **total preorder** or **linear preorder** or **preference relation** or **(non-strict) weak order** is a [[preorder]] whose [[posetal reflection]] is a [[total order]], or equivalently it is a [[preorder]] which is also a [[total relation]]: 

* for all elements $x$ and $y$, $x \leq y$ or $y \leq x$

In [[category theory]], a total preorder is a [[thin category]] $C$ for which given two [[objects]] $x \in C$ and $y \in C$, there exists a [[morphism]] in either $\mathrm{hom}(x, y)$ or $\mathrm{hom}(y, x)$. In fact, every total preorder is an unbounded [[prelattice]], a thin [[locally cartesian category]] whose [[opposite category]] is also locally cartesian.

### Cotransitive preorders

A **cotransitive preorder** on a set $S$ is a preorder $\leq$ which satisfies [[cotransitivity]]/[[weak linearity]]: 

* for all $x \in S$, $y \in S$, and $z \in S$, $x \leq z$ implies that $x \leq y$ or $y \leq z$. 

### Relation between the two definitions

\begin{theorem}
Cotransitive preorders are total preorders.
\end{theorem}

\begin{proof}
Cotransitivity of $\leq$ says that for all $x \in S$ and $y \in S$, $x \leq x$ implies that $x \leq y$ or $y \leq x$, and reflexivity says that for all $x$, $x \leq x$ is always true. This implies that for all $x$ and $y$, $x \leq y$ or $y \leq x$ is always true, which is precisely the condition of totality. Since cotransitive preorders are preorders, this implies that cotransitive preorders are total preorders.
\end{proof}

\begin{lemma}
Cotransitive [[partial orders]] are [[total orders]].
\end{lemma}

[TBD: figure out if total preorders are cotransitive preorders.]

\begin{theorem}
[[total order|Total orders]] are cotransitive [[partial orders]]. 
\end{theorem}

## Strict total preorders

Similar to [[total orders]], one could make a distinction between the usual notion of total preorder, and [[strict total preorders]], which are the irreflexive version of total preorders, and are defined as a [[strict preorder]] which is [[weakly linear]] and [[asymmetric]]. 

Using [[excluded middle]], one can move between total preorders and strict total preorders using negation; that is, the negation of a total preorder is a strict total preorder and vice versa. Actually one usually swaps the order too, as follows:

* $x \leq y$ iff $y \nless x$;
* $x \lt y$ iff $y \nleq x$.

To prove this, it\'s enough to see that the properties of a strict total preorder are [[de Morgan duality|dual]] to the properties of a total preorder, as follows:

| strict total preorder |   | total preorder |
| --------------------- | - | -------------- |
| irreflexivity         |   | reflexivity    |
| asymmetry             |   | totality       |
| transitivity          |   | weak linearity |
| weak linearity        |   | transitivity   |

In [[classical mathematics]], the distinction between total preorders and strict total preorders is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total preorders on a given set $S$ and the set of strict total preorders on $S$, and one distinguishes them by their notation. 

In [[constructive mathematics]], however, they are irreducibly different. To be specific, if one starts with a total preorder $\leq$ and defines $\lt$ as above, then weak linearity does not follow; and if one starts with a strict total preorder $\lt$ and defines $\leq$ as above, then totality does not follow. Nevertheless, at least $\leq$ will be a [[preorder]], and least $\lt$ will be a [[strict preorder]]. 

## Examples

An example of a set with a total preorder are the [[dual number|dual]] [[rational numbers]] $\mathbb{Q}[\epsilon]/\epsilon^2$. The dual rational numbers have a strict weak order $\lt$ given by 
$$(a + b \epsilon \lt c + d \epsilon) \iff (a \lt c)$$
for rational numbers $a$, $b$, $c$, and $d$. This strict weak order is not [[connected relation|connected]] because $0 \neq \epsilon$, and thus the negation of the strict weak order, $a \leq b \coloneqq \neg(b \lt a)$, is not [[antisymmetric]]. However, $\leq$ is a total preorder, because the strict weak order $\lt$ is irreflexive, weakly linear, transitive, and asymmetric, which implies that $\leq$ is reflexive, transitive, and total. 

More generally, any [[ordered local ring]] with strict weak order $\lt$ has a total preorder $\leq$ defined by negation of $\lt$. The quotient [[ordered field]] by the [[ideal]] of non-invertible elements results in a total preorder $\leq$ which is also a [[total order]]. In [[constructive mathematics]] one has to make sure that $\lt$ is also decidable. 

## Related concepts

* [[preorder]]

* [[prelattice]]

* [[total relation]]

* [[total order]]

## References

* Wikipedia, *[Total preorder](https://en.wikipedia.org/wiki/Total_preorder)*

* Wikipedia, [Weak order](https://en.wikipedia.org/wiki/Weak_order)

[[!redirects preference relation]]
[[!redirects preference relations]]

[[!redirects total preorder]]
[[!redirects total preorders]]
[[!redirects total preordering]]
[[!redirects total preorderings]]

[[!redirects totally preordered]]
[[!redirects totally preordered set]]
[[!redirects totally preordered sets]]

[[!redirects non-strict weak order]]
[[!redirects non-strict weak orders]]
[[!redirects non-strict weak ordering]]
[[!redirects non-strict weak orderings]]

[[!redirects non-strict weakly ordered]]
[[!redirects non-strict weakly ordered set]]
[[!redirects non-strict weakly ordered sets]]

[[!redirects non-strictly weakly ordered]]
[[!redirects non-strictly weakly ordered set]]
[[!redirects non-strictly weakly ordered sets]]

[[!redirects cotransitive preorder]]
[[!redirects cotransitive preorders]]
[[!redirects cotransitive preordering]]
[[!redirects cotransitive preorderings]]

[[!redirects cotransitively preordered]]
[[!redirects cotransitively preordered set]]
[[!redirects cotransitively preordered sets]]

[[!redirects linear preorder]]
[[!redirects linear preorders]]
[[!redirects linear preordering]]
[[!redirects linear preorderings]]

[[!redirects linearly preordered]]
[[!redirects linearly preordered set]]
[[!redirects linearly preordered sets]]
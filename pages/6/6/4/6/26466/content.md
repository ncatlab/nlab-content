
\tableofcontents

## Idea

A **total preorder** is a [[preorder]] whose [[posetal reflection]] is a [[total order]], or equivalently it is a [[preorder]] which is also a [[total relation]]: 

* for all elements $x$ and $y$, $x \leq y$ or $y \leq x$

In [[category theory]], a total preorder is a [[thin category]] $C$ for which given two [[objects]] $x \in C$ and $y \in C$, there either exists a [[morphism]] in $\mathrm{hom}(x, y)$ or in $\mathrm{hom}(y, x)$. In fact, every total preorder is an unbounded [[prelattice]], a thin [[locally cartesian category]] whose [[opposite category]] is also locally cartesian. 

## Strict total preorders

Similar to [[total orders]], one could make a distinction between the usual notion of total preorder, and [[strict total preorders]], which are the irreflexive version of total preorders, and are defined as a [[comparison]] which is [[irreflexive]], [[asymmetric]], and [[transitive]]. 

Using [[excluded middle]], one can move between total preorders and strict total preorders using negation; that is, the negation of a total preorder is a strict total preorder and vice versa. Actually one usually swaps the order too, as follows:

* $x \leq y$ iff $y \nless x$;
* $x \lt y$ iff $y \nleq x$.

To prove this, it\'s enough to see that the properties of a strict total preorder are [[de Morgan duality|dual]] to the properties of a total preorder, as follows:

| strict total preorder |   | total preorder |
| --------------------- | - | -------------- |
| irreflexivity         |   | reflexivity    |
| asymmetry             |   | totality       |
| transitivity          |   | comparison     |
| comparison            |   | transitivity   |

In [[classical mathematics]], the distinction between total preorders and strict total preorders is merely a terminological technicality, which is not always observed; more precisely, there is a [[natural isomorphism|natural bijection]] between the set of total preorders on a given set $S$ and the set of strict total preorders on $S$, and one distinguishes them by their notation. 

In [[constructive mathematics]], however, they are irreducibly different. To be specific, if one starts with a total preorder $\leq$ and defines $\lt$ as above, then comparison does not follow; and if one starts with a strict total preorder $\lt$ and defines $\leq$ as above, then totality does not follow. Nevertheless, at least $\leq$ will be a [[preorder]], and least $\lt$ will be a [[quasiorder]]. 

## Examples

An example of a set with a total preorder are the [[dual number|dual]] [[rational numbers]] $\mathbb{Q}[\epsilon]/\epsilon^2$. The dual rational numbers have a strict order $\lt$ given by 
$$(a + b \epsilon \lt c + d \epsilon) \iff (a \lt c)$$
for rational numbers $a$, $b$, $c$, and $d$. This strict order is not [[connected relation|connected]] because $0 \neq \epsilon$, and thus the negation of the strict order, $a \leq b \coloneqq \neg(b \lt a)$, is not [[antisymmetric]]. However, $\leq$ is a total preorder, because the strict order $\lt$ is irreflexive, cotransitive, transitive, and asymmetric, which implies that $\leq$ is reflexive, transitive, and total. 

More generally, any [[ordered local ring]] with strict order $\lt$ has a total preorder $\leq$ defined by negation of $\lt$. The quotient [[ordered field]] by the [[ideal]] of non-invertible elements results in a total preorder $\leq$ which is also a [[total order]]. In [[constructive mathematics]] one has to make sure that $\lt$ is also decidable. 

## Related concepts

* [[preorder]]

* [[prelattice]]

* [[total relation]]

* [[total order]]

[[!redirects total preorder]]
[[!redirects total preorders]]

[[!redirects totally preordered]]
[[!redirects totally preordered set]]
[[!redirects totally preordered sets]]
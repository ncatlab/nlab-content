+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
The &#321;o&#347; [[ultraproduct]] theorem characterizes the [[first-order theory]] of an ultraproduct of $\mathcal{L}$-structures (for $\mathcal{L}$ some [[signature (in logic)|signature]]). It generalizes the _transfer principle_ from [[nonstandard analysis]], by replacing the hyperreals $^*\mathbb{R}$ with an ultraproduct and formulas from the standard reals $\mathbb{R}$ with formulas which are true on an "ultrafilter-large" subset of factors of the ultraproduct. 

## Definition
The theorem is usually given in this form:

+-- {: .num_theorem}
###### Theorem

let $(A_i)_{i \in I}$ be a family of nonempty $\mathcal{L}$-structures, and let $\mathcal{U}$ be an [[ultrafilter]] on $I$. Let $^* A$ be the ultraproduct of $A_i$ with respect to $\mathcal{U}$. Since each $A_i$ was nonempty, $^* A$ is the quotient of the product $\prod_{i \in I} A_i$ by the equivalence relation which identifies sequences which coincide on a subset of indices belonging to $\mathcal{U}$. Let $(a_i)_{i \in I}$ be such a sequence, and let $[(a_i)]$ denote its equivalence class. Then for each $\mathcal{L}$-formula $\varphi(x)$,

$$^* A \models \varphi([a_i]) \iff \{j \in I | A_j \models \varphi(a_j)\} \in \mathcal{U}.$$

 =--

The above follows from a more fundamental fact:
+-- {: .num_prop}
###### Proposition

Any functor

$$[\mathcal{U}] : \mathbf{Set}^I \to \mathbf{Set}$$

which specifies a choice of ultraproduct (and hence comparison maps, since ultraproducts are colimits) is elementary (logical in the terminology of Makkai-Reyes, i.e. a [[pretopos]] morphism.)

=--

+-- {: .proof}
###### Proof

Recall that the ultraproduct sends the family of sets $A_i$ to the colimit of $s \mapsto \prod_{i \in s} A_i$, indexed by $s \in U^op$. $U^op$ (the opposite category of the sub-poset $U \subseteq \mathcal{P}(I)$) is filtered because $U$ is a filter.

A functor is a pretopos morphism precisely when it preserves finite limits, initial objects, disjoint sums, and quotients by internal equivalence relations.

Finite limits: a $s$-indexed product of $J$-indexed limits is a $J$-indexed limit of $s$-indexed products, and finite limits commute with filtered colimits.

Initial objects: a $s$-indexed product of empty sets is empty (as each $s$ is nonempty by properness of $U$), and a colimit of empty sets is empty.

Disjoint sums: a $s$-indexed product of disjoint sums $\prod_{i:s} (A_{0i} + A_{1i})$ is a disjoint sum of products $\sum_{f : s \to 2} \prod_{i:s} A_{f(i)i}$. For any $(f,a)$ in this set, there is a $U$-large subset $t \subset s$ such that the restriction of $f$ to $t$ is constantly $b$ ($b \in \{0,1\}$). Therefore the restriction map identifies $(f,a)$ with $(const_b,a|_t)$, and the $U^op$-indexed colimit of the $\sum_{f : s \to 2} \prod_{i:s} A_{f(i)i}$ is equivalent to the $U^op$-indexed colimit of the $\sum_{b : 2} \prod_{i:s} A_{bi} = \prod_{i:s} A_{0i} + \prod_{i:s} A_{1i}$, and colimits commute with colimits.

Quotients: Given $X_i$ and equivalence relations $E_i \to X_i \times X_i$, a $s$-indexed product of quotients $\prod_{i:s} (X_i / E_i)$ is a quotient of products $(\prod_{i:s} X_i) / (\prod_{i:s} E_i)$ (because the natural map from the latter to the former is an iso, using the axiom of choice), and colimits commute with colimits.
 =--

Now we can show the theorem:

+-- {: .proof}
###### Proof of theorem

Since the ultraproduct functor is elementary, then the process of taking points $M(X)$ of a definable set $X$ inside models $M$ commutes with taking ultraproducts. In symbols,

$$\left(\prod_{i \in I} M_i / \mathcal{U}\right) (X) \simeq \left(\prod_{i \in I} M_i(X) / \mathcal{U}\right).$$

Since this is a filtered colimit, a sequence $\overline{x}$ satisfies that its germ $[\overline{x}]$ is in $\prod_{i \in I} M_i / \mathcal{U}(X)$ if and only if there is some $J \in \mathcal{U}$ such that the restriction of $\overline{x}$ to $J$ is in $\prod_{j \in J} M_j(X)$. i.e. if $x_j \in M_j(X)$ for each $j \in J$.
=--

## Examples

An immediate consequence of the &#321;o&#347; theorem is the [[nonstandard analysis|transfer principle]] for the hyperreals.

The [[compactness theorem]] also follows quickly from the &#321;o&#347; theorem, so anything that you [build](http://math.stackexchange.com/questions/413770/most-astonishing-applications-of-compactness-theorem-outside-logic) using compactness can be realized a bit more concretely as an ultraproduct.

## Remarks

The proposition should be interpreted as saying that [[Set]] simultaneously carries a [[pretopos]] structure and an [[ultracategory]] structure, and that these two structures commute. Indeed, one can view [[Set]] as a [[dualizing object]] for a generalized [[Stone duality]] between pretoposes and ultracategories; this is the starting point of [[Makkai duality]].

There is an analogous statement for ultraproducts of structures in [[continuous logic]].

## Related concepts

* [[ultrafilter]]

* [[ultrapower]]

* [[stalk]]

## References

* Hisashi Aratake, _Sheaves of Structures, Heyting-Valued Structures, and a Generalization of Łoś's Theorem_ , arXiv:2012.04317 (2020). ([abstract](https://arxiv.org/abs/2012.04317))

* [[Michael Makkai]], _Stone duality for first order logic_, Advances in Mathematics, 65(2):97&#8211;170, 1987.

[[!redirects Los theorem]]
[[!redirects Los ultraproduct theorem]]
[[!redirects transfer principle]]

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
A functor is a pretopos morphism precisely when it preserves initial and terminal objects, pullbacks, disjoint sums, and quotients by internal equivalence relations.

Initial objects: a product of empty sets is empty, and a colimit of empty sets is empty.

Terminal objects: a product of terminal objects is terminal, and the quotient of a singleton is a singleton.

Pullbacks: a product of pullbacks is a pullback, and finite limits commute with filtered colimits.

Disjoint sums: a product of disjoint sums is a disjoint sum of products, and colimits commute with colimits.

Quotients: a product of quotients $X_i / E_i$ is a quotient of products $\prod_I X_i / \prod_I E_i$, and colimits commute with colimits.
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

# Intermediate model structures

* table of contents
{: toc}

## Definition

Let $M$ be a [[category]] with two [[model structures]] $(C_1,F_1,W)$ and $(C_2,F_2,W)$ having the same class of [[weak equivalences]].  Moreover, let $(L,R)$ be a [[weak factorization system]] such that $C_1 \subseteq L \subseteq C_2$.

The following theorem is essentially due to [Jardine](#Jardine).

+-- {: .num_theorem #IMS}
###### Theorem
There is a (necessarily unique) **intermediate model structure** $(L,F_i,W)$ with the same weak equivalences and $L$ as the cofibrations.
=--
+-- {: .proof}
###### Proof
Define $F_i$ to be the class of morphisms having the right lifting property with respect to $L\cap W$.  Now we observe the following:

* The assumption $C_1 \subseteq L \subseteq C_2$ implies $F_2 \cap W \subseteq R \subseteq F_2\cap W$.  In particular, $R\subseteq W$.
* We also have $C_1\cap W \subseteq L\cap W \subseteq C_2\cap W$, hence $F_2 \subseteq F_i \subseteq F_1$.
* Finally, $L\cap W\subseteq L$ implies $R\subseteq F_i$.  Thus, $R\subseteq F_i \cap W$.

Now one of the weak factorization systems in the desired model structure is just $(L,R)$.  The other will be $(L\cap W, F_i)$, for which it suffices to verify the existence of factorizations.  Given $f$, we first factor it as $p i$ with $p\in F_2$ (hence also $p\in F_i$) and $i\in C_2\cap W$.  Now factor $i$ as $q j$ with $j\in L$ and $q\in R$, hence also $q\in F_i \cap W$.  Thus, by the 2-out-of-3 property, $j\in W$, so we have $f = (p q) j$ with $j\in L\cap W$ and $p q\in F_i$.

It remains only to show that $F_i \cap W \subseteq R$, and this follows by a standard retract argument.  Given $f\in F_i \cap W$, factor it as $p i$ with $p\in R$ and $i\in L$.  Then $p\in W$, so by 2-out-of-3 $i\in L\cap W$ as well.  Hence $f$ has the right lifting property with respect to $i$, so it is a retract of $p$, hence lies in $R$.
=--

We also have:

+-- {: .num_theorem #CofGen}
###### Theorem
If in the above situation $M$ is a [[locally presentable category]] and either $(C_1,F_1,W)$ or $(C_2,F_2,W)$ is [[cofibrantly generated model category|cofibrantly generated]] (hence [[combinatorial model category|combinatorial]]), and $(L,R)$ is cofibrantly generated, then $(L,F_i,W)$ is also combinatorial.
=--
+-- {: .proof}
###### Proof
The assumption about $(C_1,F_1,W)$ or $(C_2,F_2,W)$ ensures that $Arr_W(C)$ is an accessibly embedded accessible full subcategory of $Arr(C)$.  The rest of the hypotheses of Smith's theorem about [[combinatorial model categories]] are automatically satisfied because we already know that $(L,F_i,W)$ is a model category.
=--

## Examples

### Model structures on diagram categories

Let $C$ be a small category and $M$ a [[combinatorial model category]].  Then $M^C$ has a [[projective model structure]] $(C_{proj},F_{proj},W)$ with $F_{proj}$ the objectwise fibrations, and an [[injective model structure]] $(C_{inj},F_{inj},W)$ with $C_{inj}$ the objectwise cofibrations, and $W$ in both cases the objectwise weak equivalences.

Thus, from any weak factorization system $(L,R)$ on $M^C$ in which (1) every $L$-map is an objectwise cofibration and (2) every $R$-map is an objectwise acyclic fibration, we obtain a new model structure $(L,F_i,W)$ on $M^C$, and dually.

Specific examples include:

* If $S$ is a set of cofibrations in $M^C$ containing the generating projective cofibrations, then by the small object argument it generates a weak factorization system $(L,R)$ with $C_{proj} \subseteq L \subseteq C_{inj}$.  This is the original example.

* If $C$ is a [[Reedy category]] (or a [[generalized Reedy category]]), then we have a weak factorization system consisting of Reedy cofibrations and Reedy trivial fibrations, giving rise to the Reedy model structure.  The dual of the theorem, applied to the weak factorization system of Reedy trivial cofibrations and Reedy fibrations, produces the same Reedy model structure.

* By the [[algebraic small object argument]], we can enhance the two weak factorization systems of $M$ to [[algebraic weak factorization systems]], and then simply apply them objectwise to obtain two weak factorization systems on $M^C$ to which the theorem and its dual can be applied.

## See also

* [[mixed model structure]]

## References

* [[Rick Jardine]], *Intermediate model structures for simplicial presheaves*, Canad. Math. Bull. 49(3) (2006), 407&#8211;413.
 {#Jardine}

* a review is on [p. 12](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=12) of [Field Lectures: Simplicial presheaves](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf)

[[!redirects intermediate model structures]]

## Statement 

The **Tychonoff theorem** is a theorem of [[topology]], which in its classical form is equivalent to the [[axiom of choice]].  Spellings vary; the theorem is named after &#1040;&#1085;&#1076;&#1088;&#1077;&#1081; &#1053;&#1080;&#1082;&#1086;&#1083;&#1072;&#1077;&#1074;&#1080;&#1094; &#1058;&#1080;&#1093;&#1086;&#1085;&#1086;&#1074;, whose name becomes 'Andrey Nikolayevich Tikhonov' in modern English (BGN/PCGN) transliteration, but he originally published in German as 'A.N. Tychonoff'.

The theorem states that a [[product]] of [[topological space|spaces]] (indexed over an arbitrary [[set]]) is [[compact space|compact]] if each of the spaces is compact. (Compare the axiom of choice: a product of sets is [[inhabited set|inhabited]] if each set is inhabited.)

Notice that no choice whatsoever is needed to prove the analogous theorem for [[locale]]s: even in [[constructive mathematics]], a product of locales is compact if each of the locales is compact.  From that perspective, the statement equivalent to the axiom of choice is this: a product of locales is spatial if each of the locales is spatial.  Either of these may be considered a Tychonoff theorem for locales.

To prove the Tychonoff theorem for [[Hausdorff space]]s only, the full axiom of choice is not needed; the [[ultrafilter theorem]] (and possibly [[excluded middle]]) are enough.

## Proof via ultrafilter convergence 

One method of proof uses [[ultrafilter]] convergence. Let $\langle X_\alpha \rangle_{\alpha \in A}$ be a family of compact spaces. 

1. Every ultrafilter $U_\alpha$ on the underlying set of $X_\alpha$ converges to some point $x_\alpha$. (Consider the collection of all closed sets belonging to $U_\alpha$. Finite subcollections have nonempty intersection, so by compactness the intersection of the collection is also nonempty. Let $x_\alpha$ be a point belonging to that intersection. Every closed set disjoint from $x_\alpha$ belongs to the complement of $U_\alpha$, hence every open set containing $x_\alpha$ belongs to $U_\alpha$, i.e., $U_\alpha$ converges to $x_\alpha$.)

1. Let $U$ be an ultrafilter on $\prod_\alpha X_\alpha$. Since the set-of-ultrafilters construction $S \mapsto \beta S$ is [[functor]]ial, we have a push-forward ultrafilter $U_\alpha = \beta(\pi_\alpha)(U)$ on each $X_\alpha$, where $\pi_\alpha$ is a projection map. Choose a point $x_\alpha$ to which $U_\alpha$ converges. Then it is easily checked that $U$ converges to the point $\langle x_\alpha \rangle$ in the product space.

1. Since every ultrafilter $U$ on $\prod_\alpha X_\alpha$ converges to a point, the product is compact. (If it were not, then we could find a collection of nonempty closed sets whose intersection is empty, but closed under finite intersections. This collection generates a filter which is contained in some ultrafilter $U$, by the [[ultrafilter theorem]]. Since every ultrafilter $U$ converges to some $x$, it cannot contain any closed set in the complement of $x$, hence cannot contain some closed set in the original collection, contradiction.) 
+--{.query}
[[Todd Trimble|Todd]]: Here it's not so clear that there's any direct argument. For it's at this point where we have to use the ultrafilter theorem, in order to produce a witnessing ultrafilter. Witness to what? The statement as it stands involves universal quantification over ultrafilters, so the witness would be in view of a contradiction.
=--
 
[[Toby Bartels|Toby]]: Note that we use excluded middle in two places for a proof by contradiction; I\'ll try to remove these if possible. ([[Todd Trimble|Todd]]: I've rearranged the argument in the first step; the first formulation I gave looked unnecessarily "choice-y".) We use the axiom of choice in the middle step to combine the $x_\alpha$ into a single family $\langle x_\alpha \rangle$; if the $X_\alpha$ were Hausdorff, then the $x_\alpha$ would be unique, and we would not need the axiom of choice here.  Finally, we use the ultrafilter theorem in the last step.

+--{.query} 
[[Todd Trimble|Todd]]: Yes, although I'm not too fussed about using indirect arguments, since in a topos, excluded middle follows from AC. I don't know whether it also follows from a weaker choice principle equivalent to the ultrafilter theorem, but I guess I wouldn't be surprised if it did. 
=--

## Proof of converses

Now we will prove that the Tychonoff theorem implies the axiom of choice, while the Tychonoff theorem for Hausdorff spaces implies the ultrafilter theorem.  This is done by judicious choice of examples.

**Tychonoff theorem implies axiom of choice**: let $\{X_\alpha\}_{\alpha \in A}$ be a family of nonempty sets. Let $Y_\alpha$ be obtained by adjoining a point $p$ to $X_\alpha$. Topologize $Y_\alpha$ by taking the nontrivial open sets to be $X_\alpha$ and $\{p\}$. Then $Y_\alpha$ is compact; assuming Tychonoff, $Y = \prod_\alpha Y_\alpha$ is compact. For each $\alpha$, put 

$$K_\alpha = \{y \in Y: y_\alpha \in X_\alpha\}$$ 

Then $K_\alpha$ is closed, and any finite intersection of the $K_\alpha$ is nonempty (use $p$ in all but finitely many components). Hence 

$$\prod_\alpha X_\alpha = \bigcap_\alpha K_\alpha$$ 

is nonempty as well, by compactness. Thus the axiom of choice follows. 

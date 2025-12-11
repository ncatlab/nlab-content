
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Filtered categories
* table of contents
{: toc}


## Idea

The concept of a _filtered category_ is a [[categorification]] of the concept of a [[directed set]].  In addition to having an [[upper bound]] (but not necessarily a [[coproduct]]) for every [[pair]] of [[objects]], there must also be an upper bound (but not necessarily a [[coequaliser]]) for every pair of [[parallel morphisms]].

A [[diagram]] $F \colon D\to C$ where $D$ is a filtered category is called a **filtered diagram**.  A [[colimit]] of a filtered diagram is called a **[[filtered colimit]]**.

The dual notion of *filtered category* is that of  *[[cofiltered category]]*: a category whose [[opposite category|opposite]] is filtered.

## Definitions

### Ordinary filteredness

+-- {: .num_defn}
###### Definition

A **(finitely) filtered category**  is a [[category]] $C$ in which every [[finite category|finite]] [[diagram]] has a [[cocone]].  

=--

More in details, this requirement is that: For any finite category $D$ and any [[functor]] $F \colon D\to C$, there exists an object $c\in C$ and a [[natural transformation]] $F\to \Delta c$ where $\Delta c:D\to C$ is the constant diagram at $c$. If $D^+$ is the result of freely adjoining a terminal object to a category $D$, then the condition is the same as that any functor $F: D \to C$ with finite domain admits an extension $\tilde{F}: D^+ \to C$. 

Equivalently, filtered categories can be characterized as those categories where, for every finite diagram $J$, the [[diagonal functor]] $\Delta \colon C \to C^J$ is [[final functor|final]]. This point of view can be generalized to other kinds of categories whose colimits are well-behaved with respect to a type of limit, such as [[sifted categories]].

All this may be rephrased in more elementary terms by saying that:

* There exists an object of $C$  (the case when $D=\emptyset$)

* For any two objects $c_1,c_2\in C$, there exists an object $c_3\in C$ and morphisms $c_1\to c_3$ and $c_2\to c_3$.

* For any two [[parallel morphisms]] $f,g:c_1\to c_2$ in $C$, there exists a morphism $h:c_2\to c_3$ such that $h f = h g$.

Just as all finite [[colimit|colimits]] can be constructed from initial objects, binary coproducts, and coequalizers, so a cocone on any finite diagram can be constructed from these three.  However, the reduction is a little more sophisticated; see Theorem \ref{FilteredReduction} below.

In [[constructive mathematics]], the elementary rephrasing above is equivalent to every [[Bishop-finite]] diagram admitting a cocone.

### Higher filteredness

More generally, if $\kappa$ is an infinite [[regular cardinal]] (or an [[arity class]]), then a **$\kappa$-filtered category** is one such that any diagram $D\to C$ has a cocone when $D$ has $\lt \kappa$ arrows, or equivalently that any functor $F: D \to C$ whose domain has fewer than $\kappa$ morphisms admits an extension $\tilde{F}: D^+ \to C$. The usual filtered categories are then the case $\kappa = \omega$, i.e., where the $D$ have fewer than $\omega$ morphisms (in other words are finite).  (We could also say in this case "$\aleph_0$-filtered", but $\omega$-filtered is more usual in the literature.) 

Note that a [[preorder]] is $\kappa$-filtered as a category just when it is $\kappa$-[[direction|directed]] as a preorder.

Higher filteredness can also be reduced to two special cases, as observed (without proof) in [Makkai-Paré](#MakkaiParé1989):

\begin{theorem}\label{FilteredReduction}
A category is $\kappa$-filtered if and only if it admits a cocone under every diagram of one of the following shapes:

* The discrete category with $\lambda$ objects, for any $\lambda\lt\kappa$.

* The category with two objects and $\lambda$ parallel arrows between them, for any $\lambda\lt\kappa$.

\end{theorem}
\begin{proof}
Let $C$ have cocones under diagrams of the specified shapes, and let $F:D\to C$ where $D$ has $\lt\kappa$ arrows.  First, let $x\in C$ be the vertex of a cocone under the discrete diagram $ob(F) : ob(D) \to C$ of all the objects in $C$, with coprojections $p_a:F a\to x$ for all $a\in ob (D)$.

Second, for any morphism $f:a\to b$ in $D$, there are two morphisms $p_a : F a \to x$ and $p_b\circ F f : F a \to x$.  Together these form a diagram of the second sort, with $\lambda=2$; let $q_a : x \to y_a$ be a cocone under it.

Third, let $z$ be the vertex of a cocone under the discrete diagram $G:ob(D) \to C$ where $G(a) = y_a$, with coprojections $r_a : y_a \to z$.

Fourth, for each $a\in D$ we have a composite morphism $r_a \circ q_a : x \to z$.  Together these form a diagram of the second sort; let $s:z \to w$ be a cocone under it.

Finally, the composite morphisms $s \circ r_a\circ q_a \circ p_a$ form a cocone under the original diagram $F:D\to C$.
\end{proof}

In [ABLR](#ABLR), they use the term **$\infty$-filtered** for a category that is $\kappa$-filtered for every cardinal $\kappa$. Thus, an $\infty$-filtered category is equivalently one in which every small diagram admits a cocone.

### Generalized filteredness

Even more generally, if $\mathcal{J}$ is a class of small categories, a category $C$ is called **$\mathcal{J}$-filtered** if $C$-colimits commute with $\mathcal{J}$-limits in [[Set]].  When $\mathcal{J}$ is the class of all $\kappa$-small categories for an infinite regular cardinal $\kappa$, then $\mathcal{J}$-filteredness is the same as $\kappa$-filteredness as defined above.  See [ABLR](#ABLR).

If $\mathcal{J}$ is the class consisting of the [[terminal category]] and the [[empty category]] --- which is to say, the class of $\kappa$-small categories when $\kappa$ is the finite regular cardinal $2$ --- then being $\mathcal{J}$-filtered in this sense is equivalent to being [[connected category|connected]].  Note that this is not what the explicit definition given above for infinite regular cardinals would specialize to by simply setting $\kappa=2$ (that would be simply [[inhabited set|inhabitation]]).

## Examples



* A filtered [[preorder]] is the same as a [[direction|directed]] one: a **filtered [[(0,1)-category]]**.

* Every category with a [[terminal object]] is filtered, since a terminal object is a cocone under the whole category, which can be whiskered with any diagram, finite or no, to get a cocone. 

* More generally, any category with a cocone under the identity functor is filtered by the same argument. An important case without a terminal object is the [[walking idempotent]], the delooping $BM$ of the monoid $M$ generated by an idempotent $e^2=e$, which has a cocone under the identity whose component is $e.$ This is a rare example of an important finite filtered category.

* Every category which has finite [[colimit]]s is filtered, since the colimiting cocone is in particular a cocone over any finite diagram.

* A [[product]] of filtered categories is filtered.


## Related concepts

* [[sifted category]], [[sifted (∞,1)-category]]

* [[directed set]], **filtered category**, [[filtered (∞,1)-category]]

* [[direct category]]

* [[filtered colimit]]

## References

* {#MakkaiParé1989} [[Michael Makkai]], [[Robert Paré]],  _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics **104**, American Mathematical Society, (1989) &lbrack;[ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104)&rbrack;

* {#AdámekRosický1994} [[Jiří Adámek]], [[Jiří Rosický]], *[[Locally presentable and accessible categories]]*, London Mathematical Society Lecture Note Series **189**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511600579](https://doi.org/10.1017/CBO9780511600579)&rbrack;


* {#ABLR} [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], and [[Jiří Rosický]], _A classification of accessible categories_, Journal of Pure and Applied Algebra **175** 1-3 (2002) 7-30 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00126-3">doi:10.1016/S0022-4049(02)00126-3</a>&rbrack;

[[!redirects filtered categories]]
[[!redirects filtrant category]]
[[!redirects filtrant categories]]
[[!redirects filtered diagram]]
[[!redirects filtered diagrams]]
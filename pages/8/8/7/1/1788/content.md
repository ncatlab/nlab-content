The notion of weighted limits was introduced in:

* [[Francis Borceux]], p. 10 of: *Une notion de $V$-limite*. Colloque sur l'algèbre des catégories. Amiens 1973. Résumés des conférences &lbrack;[numdam](http://www.numdam.org/item/CTGDC_1973__14_2_153_0/)&rbrack

* [[Francis Borceux]] and [[Gregory Maxwell Kelly]]. *A notion of limit for enriched categories*. Bulletin of the Australian Mathematical Society 12.1 (1975): 49-72.

Textbook accounts:

* {#Kelly} [[Max Kelly]], [section 3.1, p. 37](http://www.emis.de/journals/TAC/reprints/articles/10/tr10.pdf#page=37) in:  _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories, **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

* [[Francis Borceux]], §6.6 in: *[[Handbook of Categorical Algebra]]*, Vol. 2:  *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)&rbrack;

In 

* [[Emily Riehl]], _Weighted limits and colimits_ (2008) ([pdf](http://www.math.jhu.edu/~eriehl/weighted.pdf)) 

is given an account of lectures by [[Mike Shulman]] on the subject. The definition appears there as [definition 3.1, p. 4](http://www.math.jhu.edu/~eriehl/weighted.pdf#page=4) (in a form a bit more general than the one above).

### Presenting homotopy limits

On weighted limits as presentations of [[homotopy limits]]:

* {#Hirschhorn02} [[Philip Hirschhorn]], _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs **99** (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/pshmain.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;

To compare with the above discussion notice that

* The functor
$$
  W \;\coloneqq\; N(K/-)
$$
is discussed there in definition 14.7.8 on p. 269. 

* the $V$-enriched hom-category $[K,V]$ which on $V$-functors $S,T$ is the [[end]] $[K,V](S,T) = \int_{k \in K} V(S(k), T(k))$ appears as $hom^K(S,T)$ in definition 18.3.1 (see bottom of the page).

* for $V$ set to [[SimpSet]] the above definition of homotopy limit appears in example 18.3.6 (2).

### Fiber bundles



In the most general sense, a __bundle__ over an object $B$ in a [[category]] $C$ is a [[morphism]] $p: E \to B$ in $C$.

In appropriate contexts, a __fibre bundle__ over $B$ with standard fibre $F$ may be defined as a bundle over $B$ such that, given any [[global element]] $x: 1 \to B$, the [[pullback]] of $E$ along $x$ is isomorphic to $F$. 
Certainly this definition is appropriate whenever $C$ has a [[terminal object]] $1$ which is a [[separator]], as in a [[well-pointed category]]; even then, however, one often wants the more restrictive notion below.

One often writes a typical fibre bundle in shorthand as $F \to E \to B$ or
$$ \array {
   F & \rightarrow & E \\
     &             & \downarrow \\
     &             & B
} $$
even though there is not a single morphism $F \to E$ but instead one for each global element $x$ (and none at all if $B$ has no global elements!).

If $C$ is a [[site]], then a __[[locally trivial|locally]] [[trivial fibre bundle]]__ over $B$ with typical fibre $F$ is a bundle over $B$ with a [[cover]] $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, the pullback $E_\alpha$ of $E$ along $j_\alpha$ is isomorphic in the [[slice category]] $C/{U_\alpha}$ to the [[trivial bundle]] $U_\alpha \times F$ (a _[[local trivialization]]_).

One can also drop $F$ and define a slightly more general notion of __[[locally trivial]] bundle__ over $B$ as a bundle over $B$ with a cover $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, there is a fibre $F_\alpha$ and an isomorphism in $C/{U_\alpha}$ between the pullback $E_\alpha$ and the trivial bundle $U_\alpha \times F_\alpha$.  Every [[locally trivial]] fibre bundle is obviously a locally trivial bundle; the converse holds if $B$ is [[connected object|connected]].

Now suppose that $E$ is a fibre bundle over $B$ with standard fibre $F$, locally trivialised using the cover $(U_\alpha)_\alpha$.  Given an index $\alpha$ and an index $\beta$, let $U_{\alpha,\beta}$ be the [[fibred product]] (pullback) of $U_\alpha$ and $U_\beta$.  Then we have an [[automorphism]] $g_{\alpha,\beta}$ of $U_{\alpha,\beta} \times F$ in $C/{U_{\alpha,\beta}}$ as follows:
(diagram to come)
The $g_{\alpha,\beta}$ are the __transition morphisms__ of the locally trivial fibre bundle $E$.

Often one considers special kinds of bundles, by requiring structure on the standard fibre $F$ and/or conditions on the transition morphisms $g_{\alpha,\beta}$.  For example:


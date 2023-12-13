
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

# Model structures on enriched categories
* automatic table of contents goes here
{:toc}

## Idea

If $V$ is a [[monoidal model category]], then in many cases there is a [[model category]] of $V$-[[enriched categories]].  This includes the [[model structure on simplicial categories]] and the [[model structure on dg-categories]], for instance.

## Definition

Let $V$ be a monoidal model category.  The localization functor $\gamma: V \to Ho(V)$ is then a [[lax monoidal functor]], and hence any $V$-category $C$ induces a $Ho(V)$-category $\gamma_\bullet C$.  The *homotopy category* of a $V$-category $C$ is the underlying ordinary category $(\gamma_\bullet C)_o$.  We say a $V$-functor $F:C\to D$ is *locally X* if each morphism $F:C(x,y) \to D(F x, F y)$ is X.

Define a $V$-functor $F:C\to D$ to be:

* A **weak equivalence** if $\gamma_\bullet F :\gamma_\bullet C \to \gamma_\bullet D$ is an equivalence of $Ho(V)$-categories (that is, an internal equivalence in the [[2-category]] of $Ho(V)$-categories).  This is equivalent to asking that (1) $F$ is locally a weak equivalence, and (2) the ordinary functor $(\gamma_\bullet F)_o$ is essentially surjective.

* A **naive fibration** if (1) $F$ is locally a fibration, and (2) $\gamma_\bullet F$ is an [[isofibration]].

Define a $V$-category $C$ to be

* **fibrant** if the functor $C\to 1$ is a naive fibration.  This is equivalent to $C$ being locally fibrant, i.e. each $C(x,y)$ is fibrant.

By a theorem of Joyal, these weak equivalences and fibrant objects determine at most one model structure on the category $V Cat$.  When it exists, it is called the **(canonical, categorical) model structure on $V$-categories**.

Usually, the fibrations between fibrant objects in this model structure are precisely the naive fibrations (although between non-fibrant objects, the two classes are distinct).  Usually also, the trivial fibrations are precisely the weak equivalences that are also naive fibrations, which is to say the $V$-functors that are (1) locally trivial fibrations and (2) surjective on objects.

See the references for general conditions under which this model structure exists.

## Existence

\begin{theorem}
(Muro, \cite{Muro}, Theorem 1.1.)
For any combinatorial closed symmetric monoidal model category $V$
satisfying the [[monoid axiom]],
the category $Cat(V)$ admits the Dwyer–Kan model structure.
Moreover, this model structure is combinatorial.
\end{theorem}

## Examples

* The [[model structure on simplicial categories]] which presents [[(∞,1)-categories]] is induced from the Quillen [[model structure on simplicial sets]].

* The [[model structure on simplicial categories]] which presents [[(∞,2)-categories]] is induced from the [[Joyal model structure]] on simplicial sets

* The [[model structure on dg-categories]] is induced from the [[projective model structure on chain complexes]].

* The [[canonical model structure]] on [[Cat]] is induced from the [[trivial model structure]] on [[Set]].

* The canonical (Lack) model structure on $2 Cat$ is induced from the canonical model structure on $Cat$.

* The canonical (Lack) model structure on [[Gray-categories]] is induced from the canonical model structure on $2 Cat$.

## Related concepts

* [[model structure on internal categories]]

* [[model structure on operads]]

## References

* [[Julia E. Bergner]], _A model category structure on the category of simplicial categories_, Transactions of the American Mathematical Society 359:5 (2006), 2043-2058.  [arXiv](https://arxiv.org/abs/math/0406507), [doi](http://dx.doi.org/10.1090/s0002-9947-06-03987-0).

* [[Jacob Lurie]], [[Higher Topos Theory]] section A.3.2

* [[Alexandru Stanculescu]], *Constructing model categories with prescribed fibrant objects*, Theory and Applications of Categories, **29** 23 (2014) 635-653  &lbrack;[arXiv:1208.6005](http://arxiv.org/abs/1208.6005), [tac:29-23](http://www.tac.mta.ca/tac/volumes/29/23/29-23abs.html)&rbrack;

* {#BergerMoerdijk12} [[Clemens Berger]], [[Ieke Moerdijk]], _On the homotopy theory of enriched categories_ ([arXiv:1201.2134](http://arxiv.org/abs/1201.2134))

* {#Muro} [[Fernando Muro]], _Dwyer–Kan homotopy theory of enriched categories_.  [arXiv:1201.1575](https://arxiv.org/abs/1201.1575).

[[!redirects model structures on enriched categories]]

[[!redirects Dwyer-Kan model structure on enriched categories]]
[[!redirects Dwyer–Kan model structure on enriched categories]]

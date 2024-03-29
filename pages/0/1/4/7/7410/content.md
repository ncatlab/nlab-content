
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

**Warning** on terminology: This is a different notion than that of _[[type]]_ in [[type theory]], which is what model theorists call _sorts_.

## Idea
The [[syntactic category]] of a Boolean coherent theory has a Boolean algebra structure on each of its subobject posets. Types are ultrafilters of the Boolean algebras of subobjects of the maximal objects in these syntactic categories (those corresponding to formulas of the form "$x=x$").

If one tries to add a global point to such a syntactic category (i.e. name a constant) "without changing anything", this point must have a sort (in the sense of type from type theory), and hence must pick out a principal ultrafilter of definable sets which live above it in the subobject lattice. Types tell you what kinds of global points you can add. When you have "all possible" such global points plus a homogeneity condition, you're in a saturated [[monster model]].

## Definition
Let $M$ be a model (in $\mathbf{Set}$) of a first-order theory. Let $ \overline{m} = (m_1, \dots, m_n)$ be a tuple of elements from that model. The _type_ of $\overline{m}$ is the [[ultrafilter]] of definable sets of the same _sort_ ([[type]] in the sense of type theory, sort in the sense of Makkai's FOLDS) as $\overline{m}$ containing $\overline{m}$.

Syntactically, if $x$ is a tuple of variables, an _$x$-type_ is a finitely consistent (hence consistent, by the [[compactness theorem]]) set of formulas whose tuple of free variables has the same sort (arity) as $s$. These correspond to filters of definable sets. A type corresponds to an _ultrafilter_ of definable sets if and only if it is a maximally consistent set of formulas; we call such a type _complete_.

By [[Stone duality]], the set of all complete $x$-types of a theory $T$ inherits a Stone topology, and is called the _Stone space_ $S_x(T)$ of the theory $T$.

There are some extension of this notion of type beyond first order, for example the notion of [[Galois type]]s in [[infinitary logic]], which is particularly important in the study of [[abstract elementary class]]es.  

An important method toward classification of theories is study of the number of nonisomorphic models in each cardinality; its study is related to the study of types, 
and the phenomenon of [[forking]] in model theory; that aspect is studied in [[stability theory]]. 

## Saturation and the monster model
If $m$ is a tuple of sort $s$, and $p$ is an $s$-type, we say that $m$ _realizes_ the type $p$ if the type of $m$ is $p$.

By the completeness theorem, we can always realize types in larger elementary extensions if they aren't already realized in your model. For example, this is how one usually obtains a nonstandard model of arithmetic, because one can form the type (with parameters coming from the $\mathbb{N}$, which is small) which says "any realization of this must not equal anything in $\mathbb{N}$."

More generally, let $A$ be a subset of the model $M$. If we also allow parameters from $A$ in our formulas, we can form _types over $A$_. We say that a model is $\kappa$-saturated if all types over $A$ for $|A| = \kappa$ are realized.

Saturated models always exist (maybe modulo some large cardinal assumptions.) For example, an $\aleph_0$-saturated elementary extension of the natural numbers $(\mathbb{N}, \leq)$ equipped with their usual ordering just looks like $\mathbb{N}$ with $\omega$-many copies of $(\mathbb{Z}, \leq)$ stacked on top, each of them comprising points at infinity.

In modern model theory it is customary to work in a Grothendieck universe-sized or class-sized _monster model_, so that all types over small parameter sets are realized. Inside a monster $\mathbb{M}$ things often get more explicitly geometric. For example, two tuples $a$ and $b$ in $\mathbb{M}$ will have the same type if and only if they are $\operatorname{Aut}(\mathbb{M})$-conjugate, i.e. lie in the same orbit of the automorphism group of the monster, and in the presence of two constants the syntactic category is Barr-exact (i.e. eliminates [[imaginary element]]s) if and only if all definable sets can be _coded_: for all $X \in \mathsf{Syn}(T),$ there exists a tuple $x$ such that any automorphism which fixes $X$ setwise fixes $x$ pointwise.

Stated in this form, it's easy to see that the [[theory of algebraically closed fields]] codes at least all finite parameter sets. This paves the way for [[model-theoretic Galois theory]].

## Examples

* In the theory of an equivalence relation with two infinite classes, the type (over the empty set) of a point in any model is isolated in the Stone space by the formula which says which equivalence class that point belongs to.

* Types generalize points by replacing them with their principal ultrafilters of definable sets. The simplest first order theories are generalizations of algebraic geometry where points correspond to special (e.g. maximal, prime) ideals in a ring; types generalize points in some of such cases. Other "spectral" intuition also applies. 

* Finally, one may expand the model $M$ a larger model $M'$. The elements of automorphism group of the larger model will move the "points" around and a type will become an orbit for the larger model $M'$. This point of view is used especially for the generalization, so called [[Galois type]]s.

## Omitting types theorem

We start with some definitions:

* A theory $T$ _locally realizes_ a type $\Sigma$ if there is a formula $\varphi$ in the context of $\Sigma$ such that $\varphi$ is consistent with $T$ and for all $\sigma \in \Sigma$, $T \vDash \varphi \to \sigma$.

* $T$ _locally omits_ $\Sigma$ if and only if $T$ does not locally realize $\Sigma$.

Note that for a complete theory $T$, if $T$ has any model that omits $\Sigma$, then $T$ locally omits $\Sigma$. The omitting types theorem is a converse for any consistent theory in a countable language:

+-- {: .num_example #OmittingTypes}
###### Theorem 
**(Omitting Types Theorem)**
Let $T$ by a consistent theory in a countable language, and let $\Sigma$ be a type. If $T$ locally omits $\Sigma$, then $T$ has a countable model that omits $\Sigma$.
=--

## Relation to measures

## Related concepts

* [[topos of types]]
* [[forking]]
* [[Galois type]]
* [[stability theory]]

## References

* Wikipedia, _[type (model theory)](http://en.wikipedia.org/wiki/Type_%28model_theory%29)_, [forking extension](http://en.wikipedia.org/wiki/Forking_extension)
* Siu-Ah Ng, _Forking_, (Springer Online) Encyclopedia of Mathematics. [web](http://www.encyclopediaofmath.org/index.php?title=Forking&oldid=19231) (note inside the wrong link (cross reference) to a type in the sense of type theory) 
* Lou van den Dries, _An Introduction To Model-Theoretic Stability_, [online notes](http://www.karlin.mff.cuni.cz/~krajicek/vddries-stable.pdf)


[[!redirects type in model theory]]
[[!redirects omitting types theorem]]
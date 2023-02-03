
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Multi-adjoints

* table of contents
{: toc}

## Idea

A **multi-adjoint** is like an [[adjoint functor]] but sends each [[object]] to a family of objects rather than a single one.

## Definition

\begin{defn}\label{MultiAdjoints}
Let $R \colon D\to C$ be a [[functor]].  We say $R$ has a **left multi-adjoint** if for each $x \in C$ there is a [[family]] of [[morphisms]] $\{\eta_{x,i} \colon x \to R L(x,i)\}_{i\in I(x)}$ such that for any morphism $f  \colon x\to R y$ there exists a unique [[pair]] of an index $i\in I(x)$ and a morphism $g \colon L(x, i) \to y$ such that $f = R g \circ \eta_{x,i}$.
\end{defn}

\begin{remark}
Of course, if each set $I(x)$ is always a [[singleton]], then Def. \ref{MultiAdjoints} reduces to the notion of an actual [[left adjoint]].  On the other hand, if we remove the uniqueness requirement, this reduces to the [[solution set condition]].  Thus, a multi-adjoint is "halfway between" the solution-set condition and the actual existence of an adjoint.
\end{remark}

\begin{remark}
If in Def. \ref{MultiAdjoints} we weaken the notion of [[adjunction]] in the opposite way, by removing the uniqueness requirement but keeping $I$ a singleton (or equivalently add to the solution-set condition that $I$ is a singleton), we obtain the notion of a [[weak adjoint]].
\end{remark}

\begin{theorem}
Having a left multi-adjoint can be equivalently characterized as follows:

$R : D \to C$ has a left multi-adjoint $(I, L)$ with $I : Obj(C) \to Set$ and $L : (x : Obj(C)) \to I(x) \to Obj(D)$ if for all $x$ and $y$, there is an isomorphism $\alpha : \Sigma(i \in I(x)).Hom_D(L(x, i), y) \cong Hom_C(x, Ry)$, natural in $y$.
\end{theorem}
\begin{proof}
We first prove the Hom-characterization from the definition. Given $(i, \phi : L(x, i) \to y)$, we get $\alpha(\phi) := R\phi \circ \eta_{x, i} : x \to Ry$. The definition demands that this is an isomorphism. To see naturality, let $\chi : y \to z$.
Then
\[
        R\chi \circ \alpha(i, \phi) = R\chi \circ R\phi \circ \eta_{x,i} = \alpha(i, \chi \circ \phi).
\]

Now let $\alpha$ be given. Then we define $\eta_{x, i} = \alpha(i, id) : x \to RL(x, i)$.
By naturality, $\alpha(i, \phi) = R\phi \circ \eta_{x, i}$. Then invertibility of $\alpha$ proves the condition in the definition.
\end{proof}


## Examples

\begin{example}
Every [[parametric right adjoint]] with [[locally small category|locally small]] codomain has a left multi-adjoint.  And conversely, if $D$ has a [[terminal object]] and $R \colon D\to C$ has a left multi-adjoint, then it is a parametric right adjoint.
\end{example}

\begin{example}\label{MultiInitialObjectsInFields}
The [category of fields](field#category) has a multi-initial object, i.e. the functor $Fld \to 1$ has a left multi-adjoint (Def. \ref{MultiAdjoints}).  This consists of all the "[[prime fields]]", $\mathbb{Q}$ and $\mathbb{F}_p$ for some [[prime number]] $p$.
\end{example}

\begin{example}
The forgetful functor from the category of commutative [[local rings]] and local homomorphisms to the category of sets has a left multi-adjoint.
\end{example} 

## Multi-monads

Any functor $U: A\to B$ which has a left multi-adjoint generates a _multi-monad_ on $B$. Categories $A$ which can be reconstructed from this multi-monad are called multi-monadic ([Diers 80](#Diers1980)).

Multi-monadic categories on $Set$ can be characterized in the following way: they are regular, with connected limits, with coequalizers of coequalizable pairs, their equivalence relations are effective, their forgetful functors preserve coequalizers of equivalence relations and reflect isomorphisms. Unlike  monadic categories they need not have products. Examples include local rings, fields, inner spaces, locally compact spaces, locally compact groups, and complete ordered sets. ([Diers 80, p.153](#Diers1980))

## Diers spectrum

The notion of a multiadjoint functor is used to define the [[Diers spectrum]].
See there for more details.


## References

The notion of multi-adjoints is credited by [Osmond 20a](#Osmond2020a), [20b](#Osmond2020a) to:

* [[Yves Diers]], _Cat&eacute;gories localisables_, PhD thesis. Paris 6 et Centre universitaire de Valenciennes et du Hainaut Cambr&eacute;sis (1977).

* [[Yves Diers]], _Cat&eacute;gories localement multipr&eacute;sentables_, Archiv der Mathematik 34.1 (1980), pp. 344–356.

* [[Yves Diers]], _Une construction universelle des spectres, topologies spectrales et faisceaux structuraux_, Communication in Algebra Volume 12, Issue 17-18 (1984) ([doi:10.1080/00927878408823101](https://doi.org/10.1080/00927878408823101))

(in discussion of the notion of [[spectrum (geometry)|spectra in geometry]]).

See also:

* {#Osmond2020a} [[Axel Osmond]], _On Diers theory of Spectrum I: Stable functors and right multi-adjoints_, ([arXiv:2012.00853](https://arxiv.org/abs/2012.00853))

* {#Osmond2020b} [[Axel Osmond]], _On Diers theory of Spectrum II: Geometries and dualities_, ([arXiv:2012.02167](https://arxiv.org/abs/2012.02167))

* {#Diers1980} [[Yves Diers]], _Multimonads and multimonadic categories_, Journal of Pure and Applied Algebra 17 (1980) 153-170 ([pdf](https://core.ac.uk/download/pdf/82552386.pdf))

[[!redirects left multi-adjoint]]
[[!redirects right multi-adjoint]]
[[!redirects multi-adjoints]]
[[!redirects multiadjoint]]
[[!redirects multiadjoints]]
[[!redirects left multiadjoint]]
[[!redirects left multiadjoints]]

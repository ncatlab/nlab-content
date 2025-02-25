
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

Under mild conditions it is equivalent to the notion of [[parametric right adjoint]].

Every multiadjunction induces a [[multimonad]].

## Definition

\begin{defn}\label{MultiAdjoints}
Let $R \colon D\to C$ be a [[functor]].  We say $R$ has a **left multi-adjoint** if for each $x \in C$ there are

1. a [[small]] set $I(x)$
1. a [[family]] $\{L(x,i)\}_{i \in I(x)}$ of objects of $D$
1. a [[family]] of [[morphisms]] $\{\eta_{x,i} \colon x \to R L(x,i)\}_{i\in I(x)}$

such that for any morphism $f  \colon x\to R y$ there exists a unique [[pair]] of an index $i_f\in I(x)$ and a morphism $g \colon L(x, i_f) \to y$ such that $f = R g \circ \eta_{x,i_f}$:
\begin{tikzcd}
	D &&& C \\
	y && x & Ry \\
	{L(x,i_f)} &&& {RL(x,i_f)}
	\arrow["R", from=1-1, to=1-4]
	\arrow["f", from=2-3, to=2-4]
	\arrow["{\eta(x,i_f)}"', from=2-3, to=3-4]
	\arrow["{\exists! g}", dashed, from=3-1, to=2-1]
	\arrow["Rg"', from=3-4, to=2-4]
\end{tikzcd}
\end{defn}

\begin{remark}
Of course, if each set $I(x)$ is always a [[singleton]], then Def. \ref{MultiAdjoints} reduces to the notion of an actual [[left adjoint]].  On the other hand, if we remove the uniqueness requirement, this reduces to the [[solution set condition]].  Thus, a multi-adjoint is "halfway between" the solution-set condition and the actual existence of an adjoint.
This point of view is taken seriously in [(Arkor,  Di Liberti, Loregian '24)](#ADLL24).
\end{remark}

\begin{remark}
If in Def. \ref{MultiAdjoints} we weaken the notion of [[adjunction]] in the opposite way, by removing the uniqueness requirement but keeping $I$ a singleton (or equivalently add to the solution-set condition that $I$ is a singleton), we obtain the notion of a [[weak adjoint]].
\end{remark}

\begin{theorem}\label{HomCharacterization}
Having a left multi-adjoint can be equivalently characterized as follows:

$R : D \to C$ has a left multi-adjoint $(I, L)$ with $I : Obj(C) \to Set$ and $L : (x : Obj(C)) \to I(x) \to Obj(D)$ if for all $x$ and $y$, there is an isomorphism $\alpha : \Sigma(i \in I(x)).Hom_D(L(x, i), y) \cong Hom_C(x, R y)$, natural in $y$.
\end{theorem}
\begin{proof}
We first prove the Hom-characterization from the definition. Given $(i, \phi : L(x, i) \to y)$, we get $\alpha(\phi) := R\phi \circ \eta_{x, i} : x \to R y$. The definition demands that this is an isomorphism. To see naturality, let $\chi : y \to z$.
Then
\[
        R\chi \circ \alpha(i, \phi) = R\chi \circ R\phi \circ \eta_{x,i} = \alpha(i, \chi \circ \phi).
\]

Now let $\alpha$ be given. Then we define $\eta_{x, i} = \alpha(i, id) : x \to RL(x, i)$.
By naturality, $\alpha(i, \phi) = R\phi \circ \eta_{x, i}$. Then invertibility of $\alpha$ proves the condition in the definition.
\end{proof}

\linebreak

{#FamOp} For the following theorem, let $Fam(D)$ be the category

* whose objects are [[indexed sets]] of objects of $D$, hence pairs $(I, h)$ where $I$ is a [[set]] and $h \colon I \to Obj(D)$,

* whose morphisms $(f, \phi) \colon (I, h) \to (I', h')$ consist of a function $f \colon I' \to I$ (note the contravariance) and $\phi: (i \in I') \to Hom_D\Big(h\big(f(i)\big), h'(i)\Big)$.


Define $J : D \to Fam(D) : d \mapsto (\{*\}, * \mapsto d)$.

Hence $Fam(D)$ is the free [[cartesian monoidal category]] over $D$, with $J$ the unit of the free cartesian monoidal category monad.

(This is dual to the [[free coproduct completion]], an example of a [[Grothendieck construction]], see [here](free+coproduct+completion#AsAGrothendieckConstruction).)

\begin{theorem}
A multi-adjoint to $R \col D \to C$ is a functor $K : C \to Fam(D)$ such that $R$ is [[relative coadjoint functor|$J$-coadjoint to $K$]], meaning that
\[
        \alpha : Hom_{Fam(D)}(K c, J d) \cong Hom_{C}(c, R d),
\]
naturally in $c$ and $d$.
\end{theorem}
\begin{proof}
We use the characterization in theorem \ref{HomCharacterization}.

First of all, note that the type of the object part of $K$ is the same as the type of $(I, L)$; let us identify these.
Next, note that $Hom_{Fam(D)}(K c, J d) \cong \Sigma(i \in I(x)).Hom_D(L(c, i), d)$.

So to show that the characterization here implies the definition, we simply need to forget functoriality of $K$ and naturality in $c$.

Conversely, assume that the object part of $K$ is given. Then we construct a morphism part such that $\alpha$ is natural in $c$.

Take $\phi : Hom_C(c, c')$. We want $K\phi : Hom_{Fam(D)}(Kc, Kc')$, i.e.
\[
        (i' \in I(c')) \to \Sigma(i \in I(c)).Hom_D(L(c, i), L(c', i')),
\]
i.e.
\[
        (i' \in I(c')) \to Hom_{Fam(D)}(Kc, JL(c', i'))
\]
so we can take $K(\phi, i') = \alpha^{-1}(\eta_{c', i'} \circ \phi)$. Denote the components of $K\phi$ as $I\phi : I(c') \to I(c)$ and $L\phi : (i' \in I(i')) \to Hom_D(L(c, I(\phi, i')), L(c', i'))$.

* This preserves the identity: $K(id) = \lambda i.\alpha^{-1}(\eta_{x, i} \circ id) = \lambda i.(i, id)$.

* This preserves composition. Let $\phi : Hom_C(c, c')$ and $\chi : Hom_C(c', c'')$. With some abuse of notation:

  $K \chi \circ K \phi = (I\phi \circ I\chi, \lambda i''.L(\chi, i'') \circ L(\phi, I(\chi, i'')))$
  
  $= \lambda i''.(I(\phi, I(\chi, i'')), L(\chi, i'') \circ L(\phi, I(\chi, i'')))$
  
  $= \lambda i''.JL(\chi, i'') \circ (I(\phi, I(\chi, i'')), L(\phi, I(\chi, i'')))$
  
  $= \lambda i''.JL(\chi, i'') \circ K(\phi, I(\chi, i''))$
  
  $= \lambda i''.JL(\chi, i'') \circ \alpha^{-1}(\eta_{c', I(\chi, i'')} \circ \phi)$
  
  $= \lambda i''.\alpha^{-1}(RL(\chi, i'') \circ \alpha(I(\chi, i''), id_{c'}) \circ \phi)$
  
  $= \lambda i''.\alpha^{-1}(\alpha(I(\chi, i''), L(\chi, i'')) \circ \phi)$
  
  $= \lambda i''.\alpha^{-1}(\alpha(K(\chi, i'')) \circ \phi)$
  
  $= \lambda i''.\alpha^{-1}(\eta_{c'', i''} \circ \chi \circ \phi)$.

Now we prove that $\alpha$ is natural in $c$. Let $\psi : Hom_{Fam(D)}(Kc', Jd)$ and $\phi : Hom_{C}(c, c')$.
Note that $\psi$ is essentially of the form $(i', \chi)$ for $i' \in I(c')$ and $\chi \in \Hom_D(L(c', i), d)$.
With more abuse of notation:

$\alpha(\psi \circ K\phi) = \alpha((i', \chi) \circ K\phi) = \alpha(I(\phi, i'), \chi \circ L(\phi, i'))$

$= \alpha(J\chi \circ K(\phi, i')) = \alpha(J\chi \circ \alpha^{-1}(\eta_{c', i'} \circ \phi))$

$= R\chi \circ \eta_{c', i'} \circ \phi = \alpha(J\chi \circ (i', id_{c'})) \circ \phi = \alpha(i', \chi) \circ \phi = \alpha(\psi) \circ \phi$.
\end{proof}

\begin{proposition}
A functor has a left multiadjoint if and only if it factors (essentially uniquely) as a right adjoint functor followed by a discrete fibration.
\end{proposition}

Since both [[right adjoint]] functors and [[discrete fibrations]] have left multiadjoints, one direction follows from the closure of functors having left multiadjoints under composition.

In the other direction, every functor $R$ factors into a [[final functor]] followed by a [[discrete fibration]] via the [[comprehensive factorisation]]. If $R$ has a left multiadjoint, the final functor will in addition be right adjoint.

For a complete proof, see ([Diers 80, Proposition 1.1](#Diers1980)).

## Examples

\begin{example}
Every [[parametric right adjoint]] $R : D \to C$ with [[locally small category|locally small]] codomain has a left multi-adjoint, where

* $I(c) = Hom_C(c, R\top)$,
* $L$ is the left adjoint to $R^{/\top} : D \to C/R\top : d \mapsto (Rd, R())$.

Conversely, if $D$ has a [[terminal object]] and $R \colon D\to C$ has a left multi-adjoint, then it is a parametric right adjoint. Indeed, using the characterization in theorem \ref{HomCharacterization}, we see immediately that
\[
        Hom_C(c, R\top) \cong \Sigma(i \in I(c)).Hom_D(L(c, i), \top) \cong I(c).
\]
Moreover, by naturality in $d$, for any morphism $\phi : Hom_C(c, Rd)$, the first component of $\alpha^{-1}(\phi)$ is fully determined by $R() \circ \phi : Hom_C(c, R\top)$.
\end{example}

\begin{example}\label{MultiInitialObjectsInFields}
The [[category]] [[Field]] of [[fields]] has a multi-initial object, i.e. the functor $Fld \to 1$ has a left multi-adjoint (Def. \ref{MultiAdjoints}).  This consists of all the "[[prime fields]]", $\mathbb{Q}$ and $\mathbb{F}_p$ for some [[prime number]] $p$.
\end{example}

\begin{example}
The forgetful functor from the category of commutative [[local rings]] and local homomorphisms to the category of sets has a left multi-adjoint.
\end{example}

## Diers spectrum

The notion of a multiadjoint functor is used to define the [[Diers spectrum]].
See there for more details.

## Related pages

* [[multirepresentable functor]]

## References

The notion of multi-adjoints was developed by Diers in a series of publications.

* [[Yves Diers]], _Cat&eacute;gories localisables_, PhD thesis. Paris 6 et Centre universitaire de Valenciennes et du Hainaut Cambr&eacute;sis (1977) &lbrack;[[Categories localisables.pdf:file]]&rbrack;

* [[Yves Diers]], _Cat&eacute;gories localement multipr&eacute;sentables_, Archiv der Mathematik 34.1 (1980), pp. 344–356.

* [[Yves Diers]], _Une construction universelle des spectres, topologies spectrales et faisceaux structuraux_, Communication in Algebra Volume 12, Issue 17-18 (1984) ([doi:10.1080/00927878408823101](https://doi.org/10.1080/00927878408823101))

(in discussion of the notion of [[spectrum (geometry)|spectra in geometry]]). See  the papers by Osmond listed below.

See also:

* {#Diers1980} [[Yves Diers]], _Multimonads and multimonadic categories_, Journal of Pure and Applied Algebra 17 (1980) 153-170 ([pdf](https://core.ac.uk/download/pdf/82552386.pdf))

* {#Osmond2020a} [[Axel Osmond]], _On Diers theory of Spectrum I: Stable functors and right multi-adjoints_, ([arXiv:2012.00853](https://arxiv.org/abs/2012.00853))

* {#Osmond2020b} [[Axel Osmond]], _On Diers theory of Spectrum II: Geometries and dualities_, ([arXiv:2012.02167](https://arxiv.org/abs/2012.02167))

On other notions of adjoint functors and their relation to each other:

* {#ADLL24} [[Nathanael Arkor]], [[Ivan Di Liberti]], [[Fosco Loregian]], _Adjoint functor theorems for lax-idempotent pseudomonads_, ([tac](http://www.tac.mta.ca/tac/volumes/41/20/41-20abs.html), [arxiv](https://arxiv.org/abs/2306.10389))

[[!redirects left multi-adjoint]]
[[!redirects right multi-adjoint]]
[[!redirects multi-adjoints]]
[[!redirects multiadjoint]]
[[!redirects multiadjoints]]
[[!redirects left multiadjoint]]
[[!redirects left multiadjoints]]
[[!redirects multi-adjunction]]
[[!redirects multi-adjunctions]]
[[!redirects multiadjunction]]
[[!redirects multiadjunctions]]
[[!redirects multi-adjoint functor]]
[[!redirects multi-adjoint functors]]
[[!redirects multiadjoint functor]]
[[!redirects multiadjoint functors]]

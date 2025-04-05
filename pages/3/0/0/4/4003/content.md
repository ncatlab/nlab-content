
> This entry is about a notion in [[category theory]]. For a different notion of the same name in ([[stable homotopy theory|stable]]) [[homotopy theory]] see at _[[Goodwillie calculus]]_. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Polynomial functors
* table of contents
{: toc}

## Idea

The concept of _polynomial functor_ is a [[categorification]] of that of _[[polynomial]]_. 

Polynomial endo-functors are used to encode a class of [[inductive types]] called _[[W-types]]_, and also as the underlying data of [[polynomial monads]].

## Definition

Let $C$ be a [[locally cartesian closed category]].  A **polynomial** is a diagram
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z $$
in $C$.  These are also called *bispans* (cf. [Elmanto & Haugseng](#ElmHaug)). The corresponding **polynomial functor** is the composite

$$ 
  C/W 
   \overset{f^*}{\to} 
  C/X 
   \overset{\Pi_g}{\to} 
  C/Y 
   \overset{\Sigma_h}{\to} 
  C/Z
  \,, 
$$

where $\Pi_g$ and $\Sigma_h$ are the [[dependent product]] and [[dependent sum]] operations, right and left adjoint respectively to [[pullback#PullbackFunctor|pullback functors]] $g^*$ and $h^*$.

When $W=Z$, this is a **polynomial endofunctor**.

Sometimes this general notion is called a **dependent polynomial functor** (also **typed** or **colored** ([FMLS, p. 68](#FMLS))), with "polynomial (endo)functor" reserved for the "one-variable" case, when $W=Z=1$ is the [[terminal object]].

The data $f$, $g$, and $h$ that specify a polynomial functor is sometimes referred to as a **container** (or an **indexed container**, with *container* reserved for the case $W=Z=1$).  Other times *container* is used as a synonym for "polynomial functor".  Sometimes the data $f,g,h$ are instead referred to as a **polynomial** to distinguish them from the "polynomial functor" they determine.

If $g$ is an identity, the functor is sometimes called a **linear functor** or a **linear polynomial functor**.  Note that this notion makes sense even if $C$ is not locally cartesian closed; all it needs are [[pullbacks]].  More generally, we can make sense of polynomial functors in any category with pullbacks if we restrict $g$ to be an [[exponentiable morphism]].


## Examples

### On sets
 {#ExamplesOnSets}

For $C$ = [[Set]] the polynomial functor induced from a 
[[function]] $g$

$$
  \ast \stackrel{}{\leftarrow} X \stackrel{g}{\longrightarrow} Y
  \stackrel{}{\longrightarrow} \ast
$$ 

is given by

$$
  S \mapsto P_g(S) = \coprod_{y \in Y} S^{X_y}
  \,,
$$

where $X_y$ is the [[fiber]] of $g$ over $y \in Y$, and where the [[exponential object]] $S^{X_y}$ is the [[function set]] of [[functions]] from the fiber to $S$. The [[cardinality]] of the set on the right is

$$
  {\vert P_g(S)\vert}
   = 
  \sum_{y \in Y} {\vert S\vert}^{\vert X_y\vert}
$$

and it is in this sense that the concept of polynomial functor is a kind of [[categorification]] of that of [[polynomial]].

On the other hand the dependent polynomial functor associated to

$$
  A \stackrel{p_1}{\leftarrow} X \stackrel{id}{\longrightarrow} X
  \stackrel{p_2}{\longrightarrow} B
$$ 

acts by

$$
  (S_a)_{a \in A}
  \mapsto
  \left(\coprod_{a \in A} S_a \times X_{a b} \right)_{b \in B}
  \,.
$$

Under [[cardinality]] this becomes [[matrix multiplication]] acting on [[vectors]] (with entries in the [[natural numbers]]). So in this case the dependent polynomial functor is a linear functor of several variables, an [[integral transform]].

### In a general lextensive category
 {#ExamplesOnLextensiveCats}

Taking the fibres in the previous example to be finite, uniformly bounded (in the sense that all the fibres have size at most $N$), we can partition the set $Y$ as $\coprod_{n \leq N} \{y\in Y\mid |g^{-1}(y)| = n \} = \coprod_{n \leq N} Y_n$. Then, after choosing isomorphisms $g^{-1}(y) \simeq \{1,\ldots,|g^{-1}(y)|\}$ for each $y\in Y$, the polynomial endofunctor $P_g$ is naturally isomorphic to the functor
$$
  S \mapsto  \coprod_{n=0}^N Y_n\times S^n\,,
$$
as the hom-set $S^{\{1,\ldots,n\}} \simeq S^n$.
Thus we have a "literal polynomial" in the object argument of the functor. Such literal polynomials make sense as endofunctors of any [[lextensive category]], for example any [[pretopos]]. However, this does not automatically mean that these endofunctors are actually _polynomial_ endofunctors, strictly speaking. 

+--{: .num_prop}
###### Proposition
Literal polynomial endofunctors on an [[lextensive category]] are polynomial endofunctors.
=--

+-- {: .proof}
###### Proof
Note that in an arbitrary lextensive category there is little guarantee that any dependent products exist. However, the right adjoint to pullback functor associated to an iterated [[codiagonal]] $\coprod_{k=1}^n A\to A$ does exist, for any lextensive category. And this is all that is needed.

Consider, then, the map $g$ defined as
$$
  \coprod_{n=1}^N \left(\coprod_{k=1}^n Y_n \right) \stackrel{\coprod_{n=1}^N \nabla_{Y_n}}{\longrightarrow} \coprod_{n=0}^N Y_n
$$
The pullback along $\nabla_{Y_n}$ of an arbitrary map $f\colon T\to Y_n$ is $\coprod_{k=1}^n T \stackrel{\coprod_{k=1}^n f}{\longrightarrow} \coprod_{k=1}^n Y_n$. The dependent product along $\nabla_{Y_n}$ of an arbitrary map can be written as a composite of dependent product functors, which are themselves coproducts of dependent product along the ordinary codiagonal $Y_n \sqcup Y_n \to Y_n$, and along identity maps. The dependent product of $S\sqcup T \stackrel{f\sqcup g}{\longrightarrow} Y_n \sqcup Y_n$ along the codiagonal can be easily checked to be $S\times_{Y_n} T \to Y_n$. So we know that the functor $\Pi_{\nabla_{Y_n}}$ exists, and it remains to calculate what the polynomial functor associated to $g$ is.

This can be done summand by summand, i.e. for each $n=1,\ldots, N$, since the final dependent sum merely takes the coproduct of each dependent product. So the only thing to double check is that, for each $n$, 
$$
  \Pi_{\nabla_{Y_n}} (\coprod_{k=1}^n Y_n \times S \to \coprod_{k=1}^n Y_n) = (Y_n\times S^n \to Y_n)\,,
$$
which follows from the description of the pullback along $\nabla_{Y_n}$ and the defining properties of products, coproducts, and their interactions in a lextensive category.
There is a boundary case, namely that corresponding to $n=0$, which amounts to dependent product along $0 \to Y_0$. But in an extensive category, initial objects are strict, and so we need to take the dependent product of $0\times S = 0 \to 0$, which is then just the identity map on $Y_0$.

The final dependent product then gives the output of the polynomial functor, which is then the literal polynomial we started with, namely $\coprod_{n=0}^N Y_n\times S^n$.

=--

In the above proof, the only place that the existence of arbitrary pullbacks in a lextensive category was used is in constructing the general dependent product along the codiagonal. Obviously one still needs finite products, just to get off the ground. For the purposes of expressing the literal polynomial as a polynomial functor, this dependent product only need be applied to the projection map $(Y\sqcup Y) \times S \to (Y\sqcup Y)$. Thus while $\Pi_{\nabla_{Y_n}}$ may not exist in a general _extensive_ category with binary products, the composite $\Pi_{\nabla_{Y_n}}\circ (Y\sqcup Y)^*$ does. The extent to which such an endofunctor deserves to be called a polynomial endofunctor is up for debate.

In a lextensive category with _countable_ coproducts (and the corresponding compatibility with pullbacks), for instance an [[infinitary pretopos]] one can extend the above example to endofunctors of the form
$$
  S \mapsto  \coprod_{n=0}^\infty Y_n\times S^n\,,
$$
with practically identical proof and no additional assumptions.

## The 2-category of polynomial functors

Any polynomial functor, as defined above, is automatically equipped with a [[tensorial strength]], when the slice categories of $C$ are regarded as tensored over $C$ in the canonical way.  The following theorem is proven in [Gambino--Kock](#GK):

+--{: .num_theorem}
###### Theorem
There is a [[bicategory]] whose objects are the objects of $C$, whose morphisms from $W$ to $Z$ are diagrams of the form
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z, $$
and whose 2-morphisms are diagrams of the form
$$
\array{ & & X & \to & Y \\
  & \swarrow & \uparrow & & \mathllap{id}\uparrow & \searrow\\
  W && X' \times_{Y'} Y & \to & Y && Z\\
  &\nwarrow & \downarrow & & \downarrow & \nearrow \\
  && X' & \to & Y'. }
$$
This bicategory is equivalent to the 2-category whose objects are slice categories of $C$, whose morphisms are polynomial functors regarded as strong functors, and whose 2-morphisms are strength-respecting natural transformations.
=--

In particular, "being polynomial" is a mere [[stuff, structure, property|property]] of a strong functor between slice categories.  That is, the data $f,g,h$ are uniquely determined, up to isomorphism, by the strong functor they generate.  (Note, though, that the property of "being polynomial" depends on a prior identification of the domain and codomain as being slice categories of some specified ambient category $C$.  In particular, a functor $C/Z \to C/Z$ might be polynomial when its domain and codomain are regarded as slice categories of $C$, but not when they are regarded as slices of $C/Z$ over $1$ --- this happens when $W=Z$ but $h g \neq f$.)

Note that the above bicategory contains, as a locally full sub-bicategory, the usual bicategory of [[spans]].  Thus, as a special case, the bicategory of spans is equivalent to the 2-category of "linear" polynomial functors.  Both of these are instances of [[Lack's coherence theorem]].

There is a particular subclass of the 2-morphism in this bicategory that is also interesting: a 2-morphism corresponds to a [[cartesian natural transformation]] if and only if the map $X' \times_{Y'} Y \to X$ is an isomorphism.  Since anything isomorphic to a pullback is a pullback, in this case the diagram can be drawn more simply by omitting the upper square and merely asking that the lower square *be* a pullback.

Furthermore, this bicategory is actually the horizontal bicategory of a [[double category]], indeed a [[framed bicategory]], in which the vertical arrows are the arrows of $C$, and the cells are diagrams as above but allowing also morphisms $W\to W'$ and $Z\to Z'$ on the left and right.

## The multicategory of single-variable polynomials

Let $\mathcal{E}$ be a category with (chosen) pullbacks and let $\mathcal{D}$ be a class of morphisms in $\mathcal{E}$ called *display maps*.

There is a [[multicategory]] $\mathbf{Poly}(\mathcal{E})$, first introduced by [Garner, 2019](#Garner2019) and attributed to [Weber, 2015](Weber2015), whose: 

* objects are $\mathcal{D}$-maps $p \colon E \rightarrow B$ (that is, a polynomial $* \leftarrow E \rightarrow B \rightarrow *$)

* nullary morphisms $\sigma \colon () \rightarrow p$ are sections of $p$
\begin{tikzcd}[row sep=scriptsize]
	B & B \\
	E & B
	\arrow[Rightarrow, no head, from=1-1, to=1-2]
	\arrow["\sigma"', from=1-1, to=2-1]
	\arrow["p"', from=2-1, to=2-2]
	\arrow[Rightarrow, no head, from=2-2, to=1-2]
\end{tikzcd}

* unary morphisms $(\varphi_{1}, \varphi^{\sharp}) \colon (p_{1}) \rightarrow p$ are pairs of morphisms in $\mathcal{E}$ making the following diagram commute
\begin{tikzcd}[sep=scriptsize]
	{E_{1}} & {B_{1}} \\
	\bullet & B \\
	E & B
	\arrow["{p_{1}}", from=1-1, to=1-2]
	\arrow[from=2-1, to=1-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-1, to=1-2]
	\arrow[from=2-1, to=2-2]
	\arrow["{\varphi^{\sharp}}"', from=2-1, to=3-1]
	\arrow["{\varphi_{1}}"', from=2-2, to=1-2]
	\arrow["p"', from=3-1, to=3-2]
	\arrow[Rightarrow, no head, from=3-2, to=2-2]
\end{tikzcd}

* binary morphisms $(\varphi_{1}, \varphi_{2}, \varphi^{\sharp}) \colon (p_{2}, p_{1}) \rightarrow p$ are triples of morphisms in $\mathcal{E}$ making the following diagram commute: 
\begin{tikzcd}[sep=scriptsize]
	{E_{2}} & {B_{2}} & {E_{1}} & {B_{1}} \\
	\bullet & \bullet & \bullet & B \\
	E &&& B
	\arrow["{p_{2}}", from=1-1, to=1-2]
	\arrow["{p_{1}}", from=1-3, to=1-4]
	\arrow[from=2-1, to=1-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-1, to=1-2]
	\arrow[from=2-1, to=2-2]
	\arrow["{\varphi^{\sharp}}"', from=2-1, to=3-1]
	\arrow["{\varphi_{2}}"', from=2-2, to=1-2]
	\arrow[Rightarrow, no head, from=2-2, to=2-3]
	\arrow[from=2-3, to=1-3]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-3, to=1-4]
	\arrow[from=2-3, to=2-4]
	\arrow["{\varphi_{1}}"', from=2-4, to=1-4]
	\arrow[Rightarrow, no head, from=2-4, to=3-4]
	\arrow["p"', from=3-1, to=3-4]
\end{tikzcd}

* $n$-ary morphisms $(\varphi_{1}, \varphi_{2}, \ldots, \varphi_{n}, \varphi^{\sharp}) \colon (p_{n}, \ldots, p_{2}, p_{1}) \rightarrow p$ are $n+1$ morphisms in $\mathcal{E}$ making the following diagram commute: 
\begin{tikzcd}[sep=scriptsize]
	{E_{n}} & {B_{n}} & {E_{2}} & {B_{2}} & {E_{1}} & {B_{1}} \\
	\bullet & \bullet & \bullet & \bullet & \bullet & B \\
	E &&&&& B
	\arrow["{p_{n}}", from=1-1, to=1-2]
	\arrow["{p_{2}}", from=1-3, to=1-4]
	\arrow["{p_{1}}", from=1-5, to=1-6]
	\arrow[from=2-1, to=1-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-1, to=1-2]
	\arrow[from=2-1, to=2-2]
	\arrow["{\varphi^{\sharp}}"', from=2-1, to=3-1]
	\arrow["{\varphi_{n}}"', from=2-2, to=1-2]
	\arrow["\cdots"{description}, draw=none, from=2-2, to=2-3]
	\arrow[from=2-3, to=1-3]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-3, to=1-4]
	\arrow[from=2-3, to=2-4]
	\arrow["{\varphi_{2}}"', from=2-4, to=1-4]
	\arrow[Rightarrow, no head, from=2-4, to=2-5]
	\arrow[from=2-5, to=1-5]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-5, to=1-6]
	\arrow[from=2-5, to=2-6]
	\arrow["{\varphi_{1}}"', from=2-6, to=1-6]
	\arrow[Rightarrow, no head, from=2-6, to=3-6]
	\arrow["p"', from=3-1, to=3-6]
\end{tikzcd}

* identity morphism on an object $p \colon E \rightarrow B$ is the pair $(1_{B}, 1_{E})$. 

* composition of unary morphisms $(\psi, \psi^{\sharp}) \colon p \rightarrow p'$ and $(\varphi, \varphi^{\sharp}) \colon p' \rightarrow p''$ is given by $(\psi \circ \varphi, \varphi^{\sharp} \circ {\bar{\psi}}^{\sharp}) \colon p \rightarrow p''$ as depicted below 
\begin{tikzcd}[sep=scriptsize]
	E & {} & B \\
	\bullet & \bullet & {B'} \\
	\bullet & \bullet & B \\
	{E''} & {E''} & {B''}
	\arrow[""{name=0, anchor=center, inner sep=0}, "p", from=1-1, to=1-3]
	\arrow[from=2-1, to=1-1]
	\arrow["{\psi^{\sharp}}"', from=2-1, to=2-2]
	\arrow["{p'}"', from=2-2, to=2-3]
	\arrow["\psi"', from=2-3, to=1-3]
	\arrow[from=3-1, to=2-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=3-1, to=2-2]
	\arrow["{\bar{\psi}^{\sharp}}"', from=3-1, to=3-2]
	\arrow["{\varphi^{\sharp} \, \circ \, \bar{\psi}^{\sharp}}"', from=3-1, to=4-1]
	\arrow[from=3-2, to=2-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=3-2, to=2-3]
	\arrow[from=3-2, to=3-3]
	\arrow["{\varphi^{\sharp}}"', from=3-2, to=4-2]
	\arrow["\varphi"', from=3-3, to=2-3]
	\arrow[Rightarrow, no head, from=3-3, to=4-3]
	\arrow[Rightarrow, no head, from=4-1, to=4-2]
	\arrow["{p''}"', from=4-2, to=4-3]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=90}, draw=none, from=2-1, to=0]
\end{tikzcd}
Composition extends to $n$-ary morphisms in an analogous way. 

\begin{proposition}
If the $\mathcal{D}$-maps are [[exponential object|exponentiable]], then the multicategory $\mathbf{Poly}(\mathcal{E})$ is a [[representable multicategory]]. 
([Garner, 2019](#Garner2019))
\end{proposition}

## Related topics

* Polynomial endofunctors are important in the definition of [[W-types]] in categories.

* Polynomial functors are a special case of [[parametric right adjoint|parametric right adjoints]].

* Polynomial functors can be defined using [[exponentiable morphisms]] in a category that may not be locally cartesian closed.  See also [[distributivity pullback]].

* Kripke frames $(R,S)$ (with a transition relation $R$ of arity $2$) as studied in [[modal logic]] are [[coalgebra]]s for the power-set functor $P$. Kripke frames for a more general *modal similarity type* $t$ are a coalgebras of a functor of the form $X\mapsto \product_{d\in t} P(S^{arity(d)})$. Kripke models are coalgebras of functor $K:X\mapsto P(Prop)\times P(X)$ where $Prop$ is the set of propositional variables of the logic in consideration. In particular all the functors appearing here are polynomial functors. So, at least in some aspects, the study of modal logics reduces to the study of (certain) polynomial functors.

## Examples

* [[symmetric polynomial]], [[elementary symmetric polynomial]]

## Related entries

* [[polynomial monad]]

* [[polynomial comonad]]

* [[integral transform]]

* [[Tambara functor]]

* [[polynomial (infinity,1)-functor]]

## References

The standard reference, which considers dependent (multivariate) polynomial functors, is: 

* {#GK} [[Nicola Gambino]], [[Joachim Kock]], _Polynomial functors and polynomial monads_, (2009) ([arXiv:0906.4931](https://arxiv.org/abs/0906.4931)).

The relation of plain polynomial functors to [[trees]] is discussed in

* {#Kock} [[Joachim Kock]], _Polynomial functors and trees_, (2009)  ([arXiv:0807.2874](https://arxiv.org/abs/0807.2874))

The category, $Poly$, of one-variable polynomial functors on $Set$ and its application to [[dynamical systems]] is considered in

* [[David Spivak]], _Poly: An abundant categorical setting for mode-dependent dynamics_, ([arXiv:2005.01894](https://arxiv.org/abs/2005.01894)) 

* {#FMLS} [[Eric Finster]], [[Samuel Mimram]], Maxime Lucas, Thomas Seiller, _A Cartesian Bicategory of Polynomial Functors in Homotopy Type Theory_ ([arXiv:2112.14050](https://arxiv.org/abs/2112.14050)).

Talks on polynomial functors are available at

* _Workshop on Polynomial Functors_, Topos Institute,
15--19 March 2021. ([website](https://topos.site/p-func-2021-workshop/))

* _Workshop on Polynomial Functors 2_, Topos Institute,
March 14–18, 2022. ([website](https://topos.site/events/p-func-workshop/))

Monograph on polynomial functors in view of [[categorical systems theory]]:

* {#SpivakPoly} [[David Spivak]], [[Nelson Niu]], _Polynomial Functors: A General Theory of Interaction_ &lbrack;[webpage](https://topos.site/poly-course/), [pdf](https://topos.site/poly-book.pdf)&rbrack;

Generalization to [[homotopy theory]] and [[higher category theory]] is discussed in 

* [[Joachim Kock]], _Data types with symmetries and polynomial functors over groupoids_,  28th Conference on the Mathematical Foundations of Programming Semantics (Bath, June 2012); in Electronic Notes in Theoretical Computer Science.  ([arXiv:1210.0828](http://arxiv.org/abs/1210.0828))

* [[David Gepner]], [[Rune Haugseng]], [[Joachim Kock]], _∞-Operads as Analytic Monads_, ([arXiv:1712.06469](https://arxiv.org/abs/1712.06469))

* {#Weber14} [[Mark Weber]], _Operads as polynomial 2-monads_ ([arXiv:1412.7599](https://arxiv.org/abs/1412.7599))

* [[Benno van den Berg]], [[Ieke Moerdijk]], _W-types in Homotopy Type Theory_ ([arXiv:1307.2765](https://arxiv.org/abs/1307.2765))
 {#vdBergMoerdijk13}

* {#DAL24} [[Stefania Damato]], [[Thorsten Altenkirch]], [[Axel Ljungström]], *Formalising inductive and coinductive containers* ([arXiv:2409.02603](https://arxiv.org/abs/2409.02603))

See also

* [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]], _Polynomial functors and opetopes_, Adv. Math. __224__, 2010, pp 2690--2737. ([arXiv:0706.1033](https://arxiv.org/abs/0706.1033) [doi](https://doi.org/10.1016/j.aim.2010.02.012))
{#KJBM}

* [[Yde Venema]], _Algebras and Coalgebras_, &#167;6 (p.332--426) in Blackburn, van Benthem, Wolter, _Handbook of modal logic_, Elsevier, 2007.

* {#Weber2015} [[Mark Weber]], *Polynomials in categories with pullbacks*, Theory and Applications of Categories, __30__:16 (2015) 533--598. ([journal](http://tac.mta.ca/tac/volumes/30/16/30-16abs.html))

* Charles Walker, *Universal properties of polynomials*, ([arXiv:1806.10477](https://arxiv.org/abs/1806.10477))

* [[Ross Street]], *Polynomials as spans*, Cahiers de topologie et géométrie différentielle catégoriques, Vol. LXI-2 (2020), pp 113-153 ([pdf](http://cahierstgdc.com/wp-content/uploads/2020/04/STREET-LXI-2.pdf))

* {#Garner2019} [[Richard Garner]], _Polynomial comonads and comodules_, HoTTEST Seminar (2019) &lbrack;[slides](https://www.math.uwo.ca/faculty/kapulkin/seminars/hottestfiles/Garner-2019-12-11-HoTTEST.pdf), [video](https://www.youtube.com/watch?v=tW6HYnqn6eI)&rbrack;

* {#ElmHaug} Elden Elmanto, [[Rune Haugseng]], _On distributivity in higher algebra I: The universal property of bispans_ &lbrack;[arXiv:2010.15722](https://arxiv.org/abs/2010.15722)&rbrack;

Using [[wreath products of groups]]

* [[I. G. Macdonald]], _Polynomial functors and wreath products_, J. Pure Appl. Alg. __18__ (1980) 173--204 [pdf](https://core.ac.uk/download/pdf/82423307.pdf)


[[!redirects polynomial functor]]
[[!redirects polynomial functors]]
[[!redirects polynomial endofunctor]]
[[!redirects polynomial endofunctors]]

[[!redirects dependent polynomial functor]]
[[!redirects dependent polynomial functors]]
[[!redirects dependent polynomial endofunctor]]
[[!redirects dependent polynomial endofunctors]]

[[!redirects linear polynomial functor]]
[[!redirects linear polynomial functors]]
[[!redirects linear polynomial endofunctor]]
[[!redirects linear polynomial endofunctors]]

[[!redirects linear dependent polynomial functor]]
[[!redirects linear dependent polynomial functors]]
[[!redirects linear dependent polynomial endofunctor]]
[[!redirects linear dependent polynomial endofunctors]]

[[!redirects dependent linear polynomial functor]]
[[!redirects dependent linear polynomial functors]]
[[!redirects dependent linear polynomial endofunctor]]
[[!redirects dependent linear polynomial endofunctors]]


[[!redirects container]]
[[!redirects containers]]

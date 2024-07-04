
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

\tableofcontents


## Idea

A **strict factorization system** is like an [[orthogonal factorization system]], but the factorizations are specified uniquely on the nose, rather than merely up to [[isomorphism]].

## Definition

A **strict factorization system** on a category $C$ comprises [[wide subcategories]] $E$ and $M$ of $C$ such that every morphism in $C$ factors *uniquely* (not just uniquely up to unique isomorphism) as $m e$ for $e \in E$ and $m \in M$.

Note that a strict factorization system is not necessarily an [[orthogonal factorization system]], since $E$ and $M$ may not contain the isomorphisms in $C$. However, for every strict factorization system, there is a unique orthogonal factorization system containing it, given by closing $E$ under postcomposition by isomorphisms and closing $M$ under precomposition by isomorphisms (see §2.1 of [Grandis (2000)](#Grandis00)).

## Examples

* Every category has two "trivial" strict factorization systems in which $E$, respectively $M$, consists of the [[identity morphisms]] only.  The corresponding orthogonal factorization systems are those with one class consisting of the isomorphisms.

* Part of the structure of a (non-generalized) [[Reedy category]] is a strict factorization system.

* The category [[Set]], as defined in a [[material set theory]], has a strict factorization system consisting of the surjections and the inclusions of [[subsets]].  Its associated orthogonal factorization system consists of surjections and [[injections]].  Other categories built out of structured sets have similar strict factorization systems.

* Each [[opfibration]] $f \colon A \rightarrow B$ equipped with a [[splitting]] determines a strict factorisation system on $A$ whose classes of morphisms are the chosen opcartesian lifts and the vertical morphisms (those morphisms sent to identities by $f$).  

## As algebras of the factorization 2-monad

[Grandis](#Grandis01), following [Korostenski & Tholen](#KorostenskiTholen), it is shown in detail how strict factorization systems are *strict* algebras for the [[2-monad]] $(-)^\downarrow$.

Such a 2-monad is induced by the comonoid structure of $\downarrow \in \mathbf{Cat}$. Its unit $\eta_X : X \to X^\downarrow$ sends an object $x \in X$ to its identity map, while its multiplication $\mu_X : X^{\downarrow \times \downarrow} \to X^\downarrow$ sends a square $(u,v):f \to g$ in $X$ to its diagonal $vf=gu$. The 2-monad $((-)^\downarrow, \eta, \mu)$ is called by Grandis **factorization monad**.

Notably, every $X^\downarrow$ is equipped with a strict factorization system, given by top trivial and bottom trivial squares:

\begin{tikzcd}
	\cdot & \cdot && \cdot & \cdot & \cdot \\
	\cdot & \cdot && \cdot & \cdot & \cdot
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
	\arrow[dotted, from=1-1, to=2-2]
	\arrow[""{name=0, anchor=center, inner sep=0}, from=1-2, to=2-2]
	\arrow[Rightarrow, no head, from=1-4, to=1-5]
	\arrow[""{name=1, anchor=center, inner sep=0}, from=1-4, to=2-4]
	\arrow[from=1-5, to=1-6]
	\arrow[dotted, from=1-5, to=2-5]
	\arrow[from=1-6, to=2-6]
	\arrow[from=2-1, to=2-2]
	\arrow[from=2-4, to=2-5]
	\arrow[Rightarrow, no head, from=2-5, to=2-6]
	\arrow["{=}"{marking, allow upside down}, draw=none, from=0, to=1]
\end{tikzcd}

In fact, $X^\downarrow$ equipped with such strict fs is the *free strict fs* on $X$. This can be formulated as follows:

\begin{proposition}
The category $X^\downarrow$ with the aforementioned strict fs is universal in the following sense: for each other category $Y$ equipped with a strict fs and functor $F:X \to Y$, there is a functor $G:X^\downarrow \to Y$, factoring $F$ through $\eta_X$ and that strictly preserves factorization systems.
\end{proposition}
\begin{proof}
Define $G(f)$ to be the image of the factorization of $Ff$.
\end{proof}

\begin{remark}
The above also holds weakly for ortoghonal fss, so that $G$ now preserves the fs only up to unique functorial isomorphism.
\end{remark}

We thus displayed $\eta$ as a universal arrow for $(-)^\downarrow$, showcasing its nature as a left 2-adjoint to the forgetful functor $U:\mathbf{FsCat} \to \mathbf{Cat}$. Grandis goes on to show this adjunction is in fact 2-monadic, exhibiting $(-)^\downarrow$-algebras as strict factorization systems.

A strict algebra of $(-)^\downarrow$ is a category $X$ equipped with a functor $t:X^\downarrow \to X$ such that $t.\eta_x = 1_X$ and $t . t^\downarrow = t.\mu_X$.

Let's unpack the correspondence here.

The functor $t$ is easy to conceptualize: it sends a morphism $f:a \to b$ to its *image* $t(f)$, this being the middle object in its (for now, only conjectural) factorization. Indeed, we can recover the desired strict factorization systems by looking at the image of the free factorization system on $X^\downarrow$. Define a map in $X$ to be **left** ($L$) if it equals $t(1,f)$ for some $f:a \to b \in X$, and **right** ($R$) if it equals $t(f,1)$.

Now to show this pair $(L,R)$ is a strict fs we need to prove every morphism factors uniquely.
By unitality $a = t(\eta_X(a))$, so that given $f:a \to b$ in $X$, there are left maps $a \to t(f)$ and right maps $t(f) \to b$ given by the image of the factorization of $\eta_X(f)$ in $X^\downarrow$. These maps must compose to $f$, again by unitality, so $(L,R)$-factorizations exists.
Uniqueness follows by noticing $f = t(h,1)t(1,k)$ implies $f=h=k$.

Notice we didn't use associativity, and in fact it can be proven from unitality alone. Let $(u,v):f \to g$ be an object in $X^{\downarrow \times \downarrow}$, i.e. a commutative square in $X$.
Then $t.t^\downarrow(u,v)$ is the object obtained by factoring $t(u,v)$ (corresponding to the horizontal factorization in the square below) while $t.\mu_X(u,v)$ is the object obtained by factoring $vf$ (corresponds to the diagonal factorization below):

\begin{tikzcd}
	\cdot && \cdot \\
	{t(f)} & {t(t(u,v))} & {t(g)} \\
	\cdot && \cdot
	\arrow["u", from=1-1, to=1-3]
	\arrow["{t(1,f)}"', two heads, from=1-1, to=2-1]
	\arrow["{t(1,vf)}"{pos=0.7}, two heads, from=1-1, to=2-2]
	\arrow[two heads, from=1-3, to=2-3]
	\arrow[two heads, from=2-1, to=2-2]
	\arrow[tail, from=2-1, to=3-1]
	\arrow[tail, from=2-2, to=2-3]
	\arrow["{t(vf,1)}"'{pos=0.3}, tail, from=2-2, to=3-3]
	\arrow["{t(f,1)}", tail, from=2-3, to=3-3]
	\arrow["v"', from=3-1, to=3-3]
\end{tikzcd}

The morphisms in the horizontal factorization can be precomposed with $t(1,f)$ and postcomposed $t(g,1)$ to get a different factorization of $vf$. By uniqueness, we must have $t.t^\downarrow(u,v)=t.\mu_X(u,v)$.

\begin{remark}
A similar story holds for [[orthogonal factorization systems]], which are equivalent to normal (i.e. strictly unital) [[pseudoalgebras]] of the factorization monad.
\end{remark}

## As distributive laws in a bicategory

One reason strict factorization systems are of interest is that they can be identified with [[distributive laws]] in the [[bicategory]] of [[spans]], as shown by [Rosebrugh & Wood (2002)](#RosebrughWood02).

Ordinary orthogonal factorization systems can be similarly characterized by:

* using a type of relaxed [[distributive law]], as in [Rosebrugh & Wood (2002)](#RosebrughWood02);

* using [[wreaths]] as in [Lack & Street (2002)](#LackStreet02);

* by working in the [[bicategory]] of [[profunctors]] instead, as in [Lack (2004)](#Lack04) (see also [[factorization system over a subcategory]]); or by

* using [[weak distributive laws]], as in [Böhm (2012)](#Böhm12).

## References

Strict factorization systems were defined in:

* {#Grandis00} [[Marco Grandis]]. _Weak subobjects and the epi-monic completion of a category_, Journal of Pure and Applied Algebra **154** 1-3 (2000) 193-212. &lbrack;<a href="https://doi.org/10.1016/S0022-4049(99)00191-7">doi:10.1016/S0022-4049(99)00191-7</a>&rbrack;

See also:

* {#RosebrughWood02} [[Robert Rosebrugh]], [[Richard J. Wood]], *Distributive Laws and Factorization*, Journal of Pure and Applied Algebra **175** 1–3 (2002) 327-353 &lbrack;<a href="http://dx.doi.org/10.1016/S0022-4049(02)00140-8">doi:10.1016/S0022-4049(02)00140-8</a>[pdf](http://www.mta.ca/~rrosebru/articles/fac.pdf)&rbrack;

* {#LackStreet02} [[Stephen Lack]], [[Ross Street]], *The formal theory of monads II*, J. Pure Appl. Alg. **175** 1–3 (2002) 243-265 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00137-8">doi:10.1016/S0022-4049(02)00137-8</a>&rbrack;

* {#Lack04} [[Stephen Lack]], *Composing PROPs*, Theory and Applications of Categories, **13** 9 (2004) 147-163 &lbrack;[tac:13-09](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html)&rbrack;

* {#Böhm12} [[Gabriella Böhm]], *Factorization systems induced by weak distributive laws*, Appl. Categ. Structures **20** 3 (2012) 275-302 &lbrack;[doi:10.1007/s10485-010-9243-y](https://doi.org/10.1007/s10485-010-9243-y), [arXiv:1009.0732](https://arxiv.org/abs/1009.0732)&rbrack;

* {#KorostenskiTholen} Mareli Korostenski, [[Walter Tholen]], _Factorization systems as Eilenberg-Moore algebras, ([doi](https://doi.org/10.1016/0022-4049%2893%2990171-O))

* {#Grandis01} [[Marco Grandis]], _On the monad of proper factorisation systems in categories_, 2001, ([doi](https://doi.org/10.1016/S0022-4049%2801%2900114-1), [arxiv](https://arxiv.org/abs/math/0101154))



[[!redirects strict factorization systems]]
[[!redirects strict factorisation system]]
[[!redirects strict factorisation systems]]


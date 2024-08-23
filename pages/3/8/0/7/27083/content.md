[[!redirects Diary on Higher Category and its applications]]
[[!redirects Diary on Higher Category and its applications]]
[[!redirects Notes on derived cats and k-linear cats]]
[[!redirects Notes on derived cats and k-linear cats]]
[[!redirects Private notes on derived cats and k-linear cats]]
[[!redirects Private notes on derived cats and k-linear cats]]

# Why these Notes
Unlike notes where one usually incorporates structure and some level of self-containment, the following write-up could be seen more like a diary and a means to guide one's learning journey towards some more sophisticated references. In the cases where good references are lacking, we will aim to provide full detail or accumulate material that was hard to find (or stuff that is never spelled out in other references). In that way, we hope this will be of value to someone in the future.

#Contents#
* table of contents
{:toc}

\section{Straightening & Unstraightening}
For other Nlab entries see: [[(infinity,1)-Grothendieck construction]], [[straightening functor]], [[Grothendieck construction]], ...

### Idea
Mathematical objects very often come in families. One quick example is the following: Let $\text{Ab}$ denote the category of [[abelian group|abelian groups]], and fix a commutative ring $R$. Then the there is a well defined category

$$\text{Mod}_R \coloneqq \text{Mod}_R(\text{Ab})$$
 
of $R$-modules (see also [[module object]]). Now every homomorphism of commutative rings $\varphi \colon R \to S$ induces two functors

$$\varphi^\star \colon \text{Mod}_S \to \text{Mod}_R, \qquad \varphi_! \colon \text{Mod}_R \to \text{Mod}_S$$

which are referred to as [[restriction of scalars]] and [[extension of scalars]], respectively. It turns out that both these assignments are functorial: We have two functors


\begin{tikzcd}
	{\text{CRings}} && {\text{Cat}} && {\text{CRings}^\text{op}} && {\text{Cat}} \\
	R && {\text{Mod}_R} && R && {\text{Mod}_R} \\
	S && {\text{Mod}_S} && S && {\text{Mod}_S}
	\arrow["{\text{Mod}_\bullet^\text{cov}}", from=1-1, to=1-3]
	\arrow["{\text{Mod}_\bullet^\text{contra}}", from=1-5, to=1-7]
	\arrow[maps to, from=2-1, to=2-3]
	\arrow[""{name=0, anchor=center, inner sep=0}, "\varphi"', from=2-1, to=3-1]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\varphi_!}", from=2-3, to=3-3]
	\arrow[maps to, from=2-5, to=2-7]
	\arrow[""{name=2, anchor=center, inner sep=0}, "\varphi"', from=2-5, to=3-5]
	\arrow[maps to, from=3-1, to=3-3]
	\arrow[maps to, from=3-5, to=3-7]
	\arrow[""{name=3, anchor=center, inner sep=0}, "{\varphi^\star}"', from=3-7, to=2-7]
	\arrow[shorten <=14pt, shorten >=14pt, maps to, from=0, to=1]
	\arrow[shorten <=15pt, shorten >=15pt, maps to, from=2, to=3]
\end{tikzcd}

It is often more convenient to encode the functoriality of the (covariant or contravariant) construction $R \mapsto \text{Mod}_R$ in a different way. In fact, to every functor $U \colon \mathcal{C} \to \text{Cat}$, one can associate a new category $\text{Un}(U)$, referred to as the [[category of elements]], the [[Grothendieck construction]], or the [[unstraightening]] of the functor $U$, which comes endowed with a "bundle map"
$$\text{Un}(U) \to \mathcal{C}$$
More generally, for an $\infty$-category $\mathcal{C}$ there is an (adjoint) equivalence of $\infty$-categories


\begin{tikzcd}
	{\infty\text{Cat}_{/\mathcal{C}} \supset\{\text{"nice" bundle maps with codomain }\mathcal{C}\}} & \simeq & {\text{Fun}(\mathcal{C}, \infty\textup{Cat})}
\end{tikzcd}

Here by "nice" bundle maps we really mean [[cocartesian fibrations]] (in particular, there is another equivalence which encodes contravariant functors with domain $\mathcal{C}$ and target $\infty\text{Cat}$).
This equivalence is referred to as the Straightening/Unstraightening equivalence and it is certainly one of the most foundational and important tools (maybe second only to the [[yoneda lemma]]) used to define functors in higher category theory. The idea is that, usually when we want to define a functor with values in $\infty$-categories we would have to specify an infinite amount of coherences which might be completely unfeasible; thus instead we go unstraightened and find us a nice bundle map (i.e. [[cococartesian fibration]]) that encodes the functor we are after. Some applications for this fibrational approach are e.g. the theory of [[stack|stacks]]the definition of [[monoidal (infinity,1)-category|monoidal $\infty$-categories]] (or more generally for [[(infinity,1)-operad|$\infty$-operads]]), [[algebra over an operad |operad algebras]], [[covering space|Covering spaces]], the calculation of [[(∞,1)-limit| $\infty$-(co)limits]], ...


We shall discover that when one seeks to pursue algebra in a [[homotopy coherent diagram|homotopy coherent manner]], $\infty$-operads present the ideal framework. In fact, all of [[higher algebra]] is written in the language of [[(infinity,1)-operads]]. But the thing that keeps the machine of $\infty$-operads well oiled, or makes riding it even possible is the theory of [[cocartesian fibrations]] and in turn therefore the Straightening/Unstraightening Equivalence. 

\subsection{(Co)Cartesian Fibrations - Warm up}
See also [[Cartesian morphism]].
####Functoriality of Fibers
Given a functor $U \colon \mathcal{E} \to \mathcal{C}$ of $\infty$-categories, a natural construction is to look at the fibers of $U$, that is, for $c \colon \mathcal{C}$ an object, the fiber of $U$ at $c$, denoted by $\mathcal{E}_c$ is given by the pullback diagram:

\begin{tikzcd}
	{\mathcal{E}_c} & {\mathcal{E}} \\
	{\Delta^0} & {\mathcal{C}}
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-2]
	\arrow["U", from=1-2, to=2-2]
	\arrow["c"', from=2-1, to=2-2]
\end{tikzcd}

Now the question is: When do the fibers have contra- or covariant dependence with regards to the category $\mathcal{C}$. It is certainly false that every functor $U \colon \mathcal{E} \to \mathcal{C}$ induces a "straightened" functor:

\begin{tikzcd}
	{\mathcal{C}} & c & {\tilde{c}} \\
	{\infty\text{Cat}} & {\mathcal{E}_c} & {\mathcal{E}_{\tilde{c}}}
	\arrow["{\text{St}(U)}"', from=1-1, to=2-1]
	\arrow[""{name=0, anchor=center, inner sep=0}, "f", from=1-2, to=1-3]
	\arrow[maps to, from=1-2, to=2-2]
	\arrow[maps to, from=1-3, to=2-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\text{St}(U)(f)}"', from=2-2, to=2-3]
	\arrow[shorten <=4pt, shorten >=4pt, maps to, from=0, to=1]
\end{tikzcd}

that retains all the information that was present in the original functor $U \colon \mathcal{E} \to \mathcal{C}$.
In fact, an easy counter example is the following. 

\begin{example}Let $\mathcal{E}$ be the category with three objects $e_1, e_2, e_3$ such that there exists precisely one arrow from $e_1$ to $e_2$ and one from $e_1$ to $e_3$. On the other hand, let $\mathcal{C}$ be the category with two objects $c_1, c_2$ with precisely one arrow from $c_1$ to $c_2$ (i.e. $\mathcal{C} \simeq \Delta^1$). Define the functor $U \colon \mathcal{E} \to \mathcal{C}$ by the assignment
$$Ue_1 = c_1,\; Ue_2= Ue_3 = c_2,\; U(e_1 \to e_2) = (c_1 \to c_2),\; U(e_1 \to e_3) = (c_1 \to c_3)$$

Put graphically, we have

\begin{tikzcd}
	& \textcolor{rgb,255:red,0;green,3;blue,179}{e_2} &&& \textcolor{rgb,255:red,246;green,60;blue,73}{c_1} \\
	\textcolor{rgb,255:red,246;green,60;blue,73}{e_1} && {} & {} \\
	& \textcolor{rgb,255:red,0;green,3;blue,179}{e_3} &&& \textcolor{rgb,255:red,0;green,3;blue,179}{c_2}
	\arrow[color={rgb,255:red,153;green,92;blue,214}, from=1-5, to=3-5]
	\arrow[color={rgb,255:red,153;green,92;blue,214}, from=2-1, to=1-2]
	\arrow[color={rgb,255:red,153;green,92;blue,214}, from=2-1, to=3-2]
	\arrow["U", from=2-3, to=2-4]
\end{tikzcd}

where the colors indicate where objects and morphisms are mapped to. Now the fibers $\mathcal{E}_{c_1}$ and $\mathcal{E}_{c_2}$ are given by the terminal category $\Delta^0 \simeq \{e_1\}$ and the disjoint union of two terminal categories $\Delta^0 \coprod \Delta^0 \simeq \{e_2,e_3\}$, respectively. There is now two (different) choices for a functor
$$\mathcal{C} \simeq \Delta^1 \to \text{Cat} \subset \infty\text{Cat}$$
which is really just a functor $\mathcal{E}_{c_1} \simeq \{e_1\} \to \{e_2,e_3\} \simeq \mathcal{E}_{c_2}$. Thus the choices are either $e_1 \mapsto e_2$ or $e_1 \mapsto e_3$, and both these functors are far from ever being able to recover all the information of the original functor $U \colon \mathcal{E} \to \mathcal{C}$.
\end{example}
####Slick Definition
We shall first give slick, quick and abstract [[model-independent]] definitions, and then after we shall unravel these definitions (in the $1$-categorical setting) to give some intuition.

\begin{definition}[Aaron Mazel-Gee, 2015](#usersguideCocart)
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a functor of $\infty$-categories, and let $\varphi \colon e \to \tilde{e}$ be a morhpism in $\mathcal{E}$.

* $\varphi$ is called $U$-cocartesian morphism if it induces a pullback square:
\begin{tikzcd}
	{\mathcal{E}_{\tilde{e}/}} & {\mathcal{E}_{e/}} \\
	{\mathcal{C}_{U\tilde{e}/}} & {\mathcal{C}_{Ue/}}
	\arrow["{\varphi^\star}", from=1-1, to=1-2]
	\arrow["U"', from=1-1, to=2-1]
	\arrow["U", from=1-2, to=2-2]
	\arrow["{(U\varphi)^\star}"', from=2-1, to=2-2]
\end{tikzcd}
* $\varphi$ is called $U$-cartesian morphism if it induces a pullback square:

\begin{tikzcd}
	{\mathcal{E}_{/\tilde{e}}} & {\mathcal{E}_{/e}} \\
	{\mathcal{C}_{/U\tilde{e}}} & {\mathcal{C}_{Ue/}}
	\arrow["{\varphi_\star}", from=1-1, to=1-2]
	\arrow["U"', from=1-1, to=2-1]
	\arrow["U", from=1-2, to=2-2]
	\arrow["{(U\varphi)_\star}"', from=2-1, to=2-2]
\end{tikzcd}

\end{definition}

\begin{definition}
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a functor of $\infty$-categories, and denote by $U\text{-CoCart}$ (resp. $U\text{-Cart}$) the full subcategory of the arrow category $\text{Ar}\mathcal{E} \coloneqq \mathcal{E}^{\Delta^1}$ spanned by the $U$-cocartesian morphisms (resp. cartesian morphisms). 

* $U$ is called cocartesian fibration, if the (induced) dashed arrow in the diagram below is an equivalence of $\infty$-categories:

\begin{tikzcd}
	{U\text{-CoCart}} \\
	& \bullet & {\text{Ar}\mathcal{C}} \\
	& {\mathcal{E}} & {\mathcal{C}}
	\arrow["\sim"{description}, dotted, from=1-1, to=2-2]
	\arrow[shift left=2, hook, from=1-1, to=2-3]
	\arrow["s"', shift right=2, from=1-1, to=3-2]
	\arrow[dashed, from=2-2, to=2-3]
	\arrow[dashed, from=2-2, to=3-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=2-2, to=3-3]
	\arrow["s", from=2-3, to=3-3]
	\arrow["U"', from=3-2, to=3-3]
\end{tikzcd}
where the functors $s$ denote the source projections, respectively.

* $U$ is called cartesian fibration, if the (induced) dashed arrow in the diagram below is an equivalence of $\infty$-categories:

\begin{tikzcd}
	{U\text{-Cart}} \\
	& \bullet & {\text{Ar}\mathcal{C}} \\
	& {\mathcal{E}} & {\mathcal{C}}
	\arrow["\sim"{description}, dotted, from=1-1, to=2-2]
	\arrow[shift left=2, hook, from=1-1, to=2-3]
	\arrow["t"', shift right=2, from=1-1, to=3-2]
	\arrow[dashed, from=2-2, to=2-3]
	\arrow[dashed, from=2-2, to=3-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=2-2, to=3-3]
	\arrow["t", from=2-3, to=3-3]
	\arrow["U"', from=3-2, to=3-3]
\end{tikzcd}
where the functors $t$ denote the target projections, respectively.


\end{definition}

####Unraveling in $1$-Category-land
#####On the definitions
Let us unravel both these definitions. For $\varphi \colon e \to \tilde{e}$ to be a $U$-cocartesian morphism really boils down to saying that for each object $\overline{e} \colon \mathcal{E}$ we have a pullback square:

\begin{tikzcd}
	{\mathcal{E}(\tilde{e}, \overline{e})} \\
	\\
	& {\mathcal{E}(e, \overline{e})\times_{\mathcal{C}(Ue, U\overline{e})} \mathcal{C}(U\tilde{e}, U\overline{e})} && {\mathcal{E}(e, \overline{e})} \\
	\\
	& {\mathcal{C}(U\tilde{e}, U\overline{e})} && {\mathcal{C}(Ue, U\overline{e})}
	\arrow["\sim"{description}, dotted, from=1-1, to=3-2]
	\arrow["{\varphi^\star}", from=1-1, to=3-4]
	\arrow["U"', shift right=5, shorten >=9pt, from=1-1, to=5-2]
	\arrow[dashed, from=3-2, to=3-4]
	\arrow[dashed, from=3-2, to=5-2]
	\arrow["U", from=3-4, to=5-4]
	\arrow["{(U\varphi)^\star}"', from=5-2, to=5-4]
\end{tikzcd}

Let us suppose now that $\mathcal{C}, \mathcal{E}$ are [[1-category|1-categories]], then the above equivalence of morphism spaces is really just a bijection of hom-sets. In particular, for this morphism to be a bijection is equivalent to the following: For every $\psi \colon e \to \overline{e}$, and for every $\omega \colon U\tilde{e} \to U\overline{e}$ such that $\omega U\varphi = U\psi$, there exists a unique lift $w\colon \tilde{e}\to \overline{e}$ of $\omega$, i.e. 

$$Uw = \omega$$

such that 

$$\psi = w \circ \varphi$$

Writing this down by means of a diagram yields:

\begin{tikzcd}
	{\mathcal{E}} & e && {\tilde{e}} \\
	&& {\overline{e}} \\
	& Ue && {U\tilde{e}} \\
	{\mathcal{C}} && {U\overline{e}}
	\arrow["U"', from=1-1, to=4-1]
	\arrow["\varphi", from=1-2, to=1-4]
	\arrow["{\forall \psi}"', color={rgb,255:red,225;green,5;blue,23}, from=1-2, to=2-3]
	\arrow["{\exists! w}", dotted, from=1-4, to=2-3]
	\arrow["{U\varphi}", from=3-2, to=3-4]
	\arrow["{U\psi}"', from=3-2, to=4-3]
	\arrow["{\forall\omega}", color={rgb,255:red,225;green,5;blue,23}, from=3-4, to=4-3]
\end{tikzcd}

The above graphical representation thus encodes what it means for a morphism $\varphi \colon e \to \widetilde{e}$ to be $U$-cocartesian (for $U \colon \mathcal{E} \to \mathcal{C}$ a functor between $1$-categories. Staying in the $1$-categorical setting, let us look at the second condition, namely that we have an equivalence of categories

\begin{tikzcd}
	{U\text{-Cart}} \\
	& P & {\text{Ar}\mathcal{C}} \\
	& {\mathcal{E}} & {\mathcal{C}}
	\arrow["\sim"{description}, dotted, from=1-1, to=2-2]
	\arrow[shift left=2, hook, from=1-1, to=2-3]
	\arrow["s"', shift right=2, from=1-1, to=3-2]
	\arrow[dashed, from=2-2, to=2-3]
	\arrow[dashed, from=2-2, to=3-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=2-2, to=3-3]
	\arrow["s", from=2-3, to=3-3]
	\arrow["U"', from=3-2, to=3-3]
\end{tikzcd}
Here the important bit is really only that the dotted arrow is essentially surjective: The objects of $P$ are really just arrows $f \colon c \to \tilde{c}$ such that there exists an $e \colon \mathcal{E}$ so that $c = Ue$. Hence essential surjectivity tells us that for any arrow $f\colon Ue \to \tilde{c}$, there exists a $U$-cocartesian lift 

$$\text{Lift}_{e}^{f} \colon e \to t(\text{Lift}_{e}^{f})$$

of $f$.
\begin{remark}
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a functor of $1$-categories. Then a morphism $\varphi \colon e\to \overline{e}$ is 
* $U$-cocartesian if and only if
\begin{tikzcd}
	{\Delta^{\{0<1\}}} \\
	{\Lambda_2^2} & {\mathcal{E}} \\
	{\Delta^2} & {\mathcal{C}}
	\arrow[hook, from=1-1, to=2-1]
	\arrow["\varphi", from=1-1, to=2-2]
	\arrow["\forall"{description}, from=2-1, to=2-2]
	\arrow[hook, from=2-1, to=3-1]
	\arrow["U", from=2-2, to=3-2]
	\arrow["{\exists!}"{description}, dotted, from=3-1, to=2-2]
	\arrow["\forall"', from=3-1, to=3-2]
\end{tikzcd}
* $U$-cartesian if and only if
\begin{tikzcd}
	{\Delta^{\{1<2\}}} \\
	{\Lambda_2^2} & {\mathcal{E}} \\
	{\Delta^2} & {\mathcal{C}}
	\arrow[hook, from=1-1, to=2-1]
	\arrow["\varphi", from=1-1, to=2-2]
	\arrow["\forall"{description}, from=2-1, to=2-2]
	\arrow[hook, from=2-1, to=3-1]
	\arrow["U", from=2-2, to=3-2]
	\arrow["{\exists!}"{description}, dotted, from=3-1, to=2-2]
	\arrow["\forall"', from=3-1, to=3-2]
\end{tikzcd}
\end{remark}
\begin{remark}
There is another reformulation for $\varphi$ to be a $U$-(co)cartesian morphism: $\varphi$ is $U$-cocartesian if and only if the induced functor
$$
\mathcal{E}_{\varphi/} \overset{\sim}{\to} \mathcal{E}_{\overline{e}/} \times_{\mathcal{C}_{U\overline{e}}} \mathcal{C}_{U\varphi/}
$$
is a (surjective) equivalence (see [[Cartesian morphism]] Proposition 2.4).
\end{remark}
#####Functoriality
Now assume $U\colon \mathcal{E} \to \mathcal{C}$, a functor of $1$-categories, is a cocartesian fibration. 

We define the [[pseudofunctor]] $\text{St}(U) \colon \mathcal{C} \to \text{Cat}$ with values in the $2$-category of small categories as follows:

\begin{tikzcd}
	{\mathcal{C}} & c & {\mathcal{E}_c} \\
	{\text{Cat}} & {\overline{c}} & {\mathcal{E}_{\overline{c}}}
	\arrow["{\text{St}(U)}"', from=1-1, to=2-1]
	\arrow[maps to, from=1-2, to=1-3]
	\arrow[""{name=0, anchor=center, inner sep=0}, "f"', from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{f_!}", from=1-3, to=2-3]
	\arrow[maps to, from=2-2, to=2-3]
	\arrow[shorten <=6pt, shorten >=6pt, maps to, from=0, to=1]
\end{tikzcd}
which on objects $c \colon \mathcal{C}$ assigns the fibers $\mathcal{E}_c$, while for a morphism $f \colon c \to \overline{c}$, the functor 

$$f_! \coloneqq\text{St}(U)(f) \colon \mathcal{E}_c \to \mathcal{E}_{\overline{c}}$$

is defined as follows:

* for any object $e \colon \mathcal{E}_c$ (meaning $Ue = c$), by assumption, there exists a cocartesian lift 
$$\text{Lift}_e^{f} \colon e \to t(\text{Lift}_e^f)$$
This yields a family of lifts $(\text{Lift}_e^f)_{e \colon \mathcal{E}}$ which we fix. Now, define the value of the functor $f_!$ on the object $e$ to be the target of the lift associated to $e$ and $f$: 
$$f_!(e) \coloneqq t(\text{Lift}_e^f)$$
* for a morphism $z \colon e \to \overline{e}$ in $\mathcal{E}_c$, we define $f_!(z)$ by means of the unique lift induced by the universal property of the cocartesian morphism:

\begin{tikzcd}
	{\mathcal{E}} & e && {t(\text{Lift}_e^f)} \\
	&& {\overline{e}} \\
	&&& {t(\text{Lift}_{\overline{e}}^f)} \\
	& c && {\overline{c}} \\
	&& c \\
	{\mathcal{C}} &&& {\overline{c}}
	\arrow["U"', from=1-1, to=6-1]
	\arrow["{\text{Lift}_e^f}", from=1-2, to=1-4]
	\arrow["z"', from=1-2, to=2-3]
	\arrow["{\exists! f_!(z)}", dotted, from=1-4, to=3-4]
	\arrow["{\text{Lift}_{\overline{e}}^f}"', from=2-3, to=3-4]
	\arrow["f", from=4-2, to=4-4]
	\arrow[Rightarrow, no head, from=4-2, to=5-3]
	\arrow[Rightarrow, no head, from=4-4, to=6-4]
	\arrow["f"', from=5-3, to=6-4]
\end{tikzcd}

* $f_!$ thus defined is a functor $\mathcal{E}_c \to \mathcal{E}_{\tilde{c}}$ by uniqueness of lifts:
\begin{tikzcd}
	e && {t(\text{Lift}_e^f)} \\
	& {\overline{e}} && {t(\text{Lift}^f_{\overline{e}})} \\
	&& {e'} && {t(\text{Lift}^f_{e'})}
	\arrow["{\text{Lift}_e^f}", from=1-1, to=1-3]
	\arrow["z"', from=1-1, to=2-2]
	\arrow["{f_!(z)}", from=1-3, to=2-4]
	\arrow["{\text{Lift}_{\overline{e}}^f}"{description}, from=2-2, to=2-4]
	\arrow["{z'}"', from=2-2, to=3-3]
	\arrow["{f_!(z')}", from=2-4, to=3-5]
	\arrow["{\text{Lift}_{e'}^f}"', from=3-3, to=3-5]
\end{tikzcd}
implying $f_!(z')f_!(z) = f_!(z'z)$ (and thus functoriality).

Next up, we want to verify that the construction of $\text{St}(U)$ is actually a [[pseudofunctor]]. In order to verify this, let us prove a quick lemma:
\begin{lemma}
For $\varphi, \tilde{\varphi}$ composable morphisms of $\mathcal{E}$ with $\varphi'$ $U$-cocartesian and $\varphi' \coloneqq \tilde{\varphi}\varphi$, we have that $\varphi$ is $U$-cocartesian if and only if $\varphi'$ is $U$-cocartesian. In particular, $U$-cocartesian morphisms are closed under composition.
\end{lemma}
\begin{proof}
For $U$-cocartesian morphisms $e \overset{\varphi}{\to} \overline{e} \overset{\tilde{\varphi}}{\to} \tilde{e}$ we have a pasting of pullback squares which by [[pasting law for pullbacks]] yields the desired claim:

\begin{tikzcd}
	{\mathcal{E}_{\tilde{e}/}} & {\mathcal{E}_{\overline{e}/}} & {\mathcal{E}_{e/}} \\
	{\mathcal{C}_{U\tilde{e}}/} & {\mathcal{C}_{U\overline{e}/}} & { \mathcal{E}_{Ue/}}
	\arrow["{\tilde{\varphi}^\star}", from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-2]
	\arrow["{\varphi^\star}", from=1-2, to=1-3]
	\arrow[from=1-2, to=2-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-2, to=2-3]
	\arrow[from=1-3, to=2-3]
	\arrow["{(U\tilde{\varphi})^\star}"', from=2-1, to=2-2]
	\arrow["{(U\varphi)^\star}"', from=2-2, to=2-3]
\end{tikzcd}

\end{proof}

\begin{theorem}
$\text{St}(U)$ is a [[pseudofunctor]].
\end{theorem}
\begin{proof}
We have specified what $\text{St}(U)$ does on objects and what it does on morphisms in $\mathcal{C}$. All that remains is to prove that this assignment is pseudo-functorial. For this, let $c \overset{f}{\to} \overline{c} \overset{g}{\to} \tilde{c}$ be a composable pair of morphisms in $\mathcal{C}$ and consider for an object $e \colon \mathcal{E}_c$ the diagram:

\begin{tikzcd}
	e && {t(\text{Lift}_{e}^{gf})} \\
	\\
	{t(\text{Lift}_e^f)} && {t(\text{Lift}_{t(\text{Lift}^{g}_{e})})}
	\arrow["{\text{Lift}_{e}^{gf}}", from=1-1, to=1-3]
	\arrow["{\text{Lift}_e^f}"', from=1-1, to=3-1]
	\arrow["{\exists!}", shift left=2, dotted, from=1-3, to=3-3]
	\arrow["{\text{Lift}^g_{t(\text{Lift}^{f}_{e^f})}}"', from=3-1, to=3-3]
	\arrow["{\exists!}", shift left=2, dotted, from=3-3, to=1-3]
\end{tikzcd}

where the (unique) dotted arrows are induced by the lifting property of the $U$-cocartesian morphisms $\text{Lift}^{gf}_{e}$ and $\text{Lift}_{t(\text{Lift}^{g}_{e^f})}\text{Lift}_e^f$, respectively (justified by the above Lemma). In fact, again by uniqueness the dotted arrows must be mutually inverse isomorphisms - these will be the components of our natural isomorphism witnessing functoriality.

Moreover, by uniqueness yet again, we have a commutative diagram

\begin{tikzcd}
	{g_!f_!(e)} & {(gf)_!(e)} \\
	{g_!f_!(\overline{e})} & {(gf)_!(\overline{e})}
	\arrow["\cong"{description}, draw=none, from=1-1, to=1-2]
	\arrow["{g_!f_!(z)}"', from=1-1, to=2-1]
	\arrow["{(gf)_!(z)}", from=1-2, to=2-2]
	\arrow["\cong"{description}, draw=none, from=2-1, to=2-2]
\end{tikzcd}
which proves that we have a natural isomorphism
$$g_! f_! \cong (gf)_!$$
An analogous argument shows the remaining axioms of pseudo-functoriality.
\end{proof}

\begin{remark}
One can now define a category of cocartesian fibrations with codomain $\mathcal{C}$, denoted $\text{CoCart}(\mathcal{C})$, whose objects are cocartesian fibrations and whose morphisms are "bundle" maps which preserve cocartesian morphisms:
\begin{tikzcd}
	{\mathcal{E}} && {\mathcal{F}} \\
	& {\mathcal{C}}
	\arrow[from=1-1, to=1-3]
	\arrow[from=1-1, to=2-2]
	\arrow[from=1-3, to=2-2]
\end{tikzcd}
Now the construction $U \mapsto \text{St}(U)$ extends to a functor
$$\text{CoCart}(\mathcal{C}) \to \text{PseudoFun}(\mathcal{C}, \text{Cat})$$
with values in the category of [[pseudofunctors]] from $\mathcal{C}$ to $text{Cat}$. It then turns out that this construction yields an equivalence of categories (see [[Grothendieck construction]]). We will spell this out for the more general case of $\infty$-categories over the course of the next few chapters.
\end{remark}

###(Co)Cartesian fibrations of simplicial sets
[[Lurie]]'s definition of (co)cartesian fibrations in the setting of quasicategories (or more generally simplicial sets) is the following:

\begin{definition}(see [[Kerodon]], [Definition 5.1.1.1](https://kerodon.net/tag/01T5))

Let $U \colon \mathcal{E} \to \mathcal{C}$ be a morphism of [[simplicial set|simplicial sets]], and let $\varphi$ be an edge of $\mathcal{E}$.
 
* We say that $\varphi$ is $U$-cartesian if every lifting problem 
\begin{tikzcd}
	{\{n-1<n\}} \\
	{\Lambda_n^n} & {\mathcal{E}} \\
	{\Delta^n} & {\mathcal{C}}
	\arrow[hook, from=1-1, to=2-1]
	\arrow["\varphi", from=1-1, to=2-2]
	\arrow["\forall"{description}, from=2-1, to=2-2]
	\arrow[from=2-1, to=3-1]
	\arrow["U", from=2-2, to=3-2]
	\arrow["\exists"{description}, dotted, from=3-1, to=2-2]
	\arrow["\forall"', from=3-1, to=3-2]
\end{tikzcd}
admits a solution, provided that $n \geq 2$.

* We say that $\varphi$ is $U$-cocartesian if every lifting problem 
\begin{tikzcd}
	{\{0<1\}} \\
	{\Lambda_0^n} & {\mathcal{E}} \\
	{\Delta^n} & {\mathcal{C}}
	\arrow[hook, from=1-1, to=2-1]
	\arrow["\varphi", from=1-1, to=2-2]
	\arrow["\forall"{description}, from=2-1, to=2-2]
	\arrow[from=2-1, to=3-1]
	\arrow["U", from=2-2, to=3-2]
	\arrow["\exists"{description}, dotted, from=3-1, to=2-2]
	\arrow["\forall"', from=3-1, to=3-2]
\end{tikzcd}
admits a solution, provided that $n \geq 2$.

\end{definition}
The definition for a (co)cartesian fibration of simplicial sets is spelled out in [Definition 5.1.4.1.](https://kerodon.net/tag/01UA).
The general theory of fibrations of $\infty$-categories is explained in [[Kerodon]] [Chapter 5](https://kerodon.net/tag/01J2). In this Nlab section, we will primarily concern ourselves with [[Kerodon]] [Section 5.5](https://kerodon.net/tag/01YV) and [Section 5.6](https://kerodon.net/tag/027M) and we will stick to the notation used in [[Kerodon]]. However, a very short recap on the most important constructions in the previous sections of chapter 5 in [[Kerodon]] cannot hurt:
###(Parametrized) Covariant/Contravariant Transport
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a cocartesian fibration of $\infty$-categories. To every morphism $f\colon C \to D$ in the $\infty$-category $\mathcal{C}$, we want to associate a functor $f_! \colon \mathcal{E}_C \to \mathcal{E}_D$ (uniquely determined up to isomorphism by [Proposition 5.2.2.8](https://kerodon.net/tag/01VS)), which [[Lurie]] calls [[covariant transport functor]]. We will skip a few steps and instead of proving existence of such a covariant transport functor $f_!$ for a single $f$, we shall immediately construct a functorial assignment $f \mapsto f_!$ for $f \colon \text{Hom}_\mathcal{C}(C,D)$. This is referred to as [[parametrized covariant transport]] in [[Lurie]]'s [[Kerodon]].

\begin{definition}[Definition 5.2.8.1](https://kerodon.net/tag/02RM)
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a cocartesian fibration of simplicial sets and let $C,D$ be vertices of $\mathcal{C}$. We will say that a morphism
$$F \colon \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C \to \mathcal{E}_D$$

is given by [[parametrized covariant transport]] if there exists a morphism 

$$\widetilde{F} \colon \Delta^1 \times \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C \to \mathcal{E}$$

satisfying the following conditions:

* We have a commutative diagram

\begin{tikzcd}
	{\Delta^1\times \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C} & {\mathcal{E}} \\
	{\Delta^1\times \text{Hom}_\mathcal{C}(C,D)} & {\mathcal{C}}
	\arrow["{\widetilde{F}}", from=1-1, to=1-2]
	\arrow["{\text{proj}}"', from=1-1, to=2-1]
	\arrow["U", from=1-2, to=2-2]
	\arrow["{\text{incl}}"', from=2-1, to=2-2]
\end{tikzcd}

where the lower horizontal map is induced by the inclusion $\text{Hom}_\mathcal{C}(C,D) \hookrightarrow \text{Fun}(\Delta^1, \mathcal{C})$ by [[currying]].

* The restriction $\widetilde{F}|_{0\times\text{Hom}_\mathcal{C}(C,D)\times\mathcal{E}_C}$ is given by projection onto $\mathcal{E}_C$, and the restriction $\widetilde{F}|_{1\times\text{Hom}_\mathcal{C}(C,D)\times \mathcal{E}_C}$ is equal to $F$.

* For every edge $f \colon C \to D$ of $\mathcal{C}$ and every object $X \colon \mathcal{E}_C$, the composite map 

$$\Delta^1 \times \{f\} \times \{X\} \hookrightarrow \Delta^1 \times \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C \overset{\widetilde{F}}{\to} \mathcal{E}$$

is a $U$-cocartesian edge of $\mathcal{E}$.


\end{definition}
\begin{remark}
Let us unravel these conditions:

* The first condition (the commutative diagram) really just says that $U\widetilde{F}$ evaluated at $(0 \to 1, f)$ is equal to the constant diagram $\mathcal{E}_C \to \text{Ar}\mathcal{C}$ with value $f$. In other words, plugging in $f$ into $\widetilde{F}$ yields a lift for $f$.

* The second condition says that $\widetilde{F}$, interpreted as a [[natural transformation]] between [[(infinity,1)-functor|$\infty$-functors]] has domain and target as depicted:

\begin{tikzcd}
	{\text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C} && {\mathcal{E}}
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\text{projection}_\mathcal{E}}", shift left=4, from=1-1, to=1-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, "F"', shift right=4, from=1-1, to=1-3]
	\arrow["{\widetilde{F}}", shorten <=2pt, shorten >=2pt, Rightarrow, from=0, to=1]
\end{tikzcd}

* Finally, the third condition just states that the diagram $\widetilde{F}$ encodes, for every morphism $f \colon \text{Hom}_\mathcal{C}(C,D)$ and every object $X \colon \mathcal{E}_C$, a $U$-cocartesian edge $\widetilde{f}_X\colon X \to f_!(X)$ in $\mathcal{E}$, with $f_!(X) \coloneqq t(\widetilde{f}_X)$. 

\end{remark}

\begin{remark}
As already hinted at in the previous remark: For every edge $f \colon C \to D$, the composite map 

$$\{f\}\times \mathcal{E}_C \hookrightarrow \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C \overset{F}{\to} \mathcal{E}_D$$

is given by covariant transport along $f$ (see also [Definition 5.2.2.4](https://kerodon.net/tag/019N)).
\end{remark}

\begin{example}(see [Example 5.2.8.3.](https://kerodon.net/tag/02RP))
Let $\text{Set}_*$ denote the category of pointed sets, and let $V \colon \text{Set}_* \to \text{Set}$ denote the forgetful functor $(X, x \colon X) \mapsto X$. Then $V$ is a cocartesian fibration (in fact, it is a left covering map), whose fiber over an object $X \colon Set$ may be identified with $\{(X,x)\}_{x\colon X} \cong X$. For every pair of sets $X,Y$, the evaluation map

$$\text{Hom}_\text{Set}(X,Y) \times X \to Y, \qquad (f,x) \mapsto f(x)$$

is given by parametrized covariant transport.
\end{example}

\begin{theorem}(see [Proposition 5.2.8.4](https://kerodon.net/tag/02RQ))\label{existence}
Let $U \colon \mathcal{E}\to \mathcal{C}$ be a cocartesian fibration of simplicial sets, and let $C,D$ be vertices of $\mathcal{C}$. Then we have the following:
1. There exists a morphism $F \colon \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C \to \mathcal{E}_D$ which is given by [[parametrized covariant transport]].
2. An arbitrary diagram $F' \colon \text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C \to \mathcal{E}_D$ is given by parametrized covariant transport if and only if it is isomorphic to $F$ (as an object of the $\infty$-category $\text{Fun}(\text{Hom}_\mathcal{C}(C,D) \times \mathcal{E}_C, \mathcal{E}_D)$).
\end{theorem}

In order to prove this, we need a lemma

\begin{lemma}
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a cocartesian fibration of simplicial sets, let $K$ be a simplicial set, and suppose we are given a lifting problem

\begin{tikzcd}
	{\{0\}\times K} && {\mathcal{E}} \\
	\\
	{\Delta^1\times K} && {\mathcal{C}}
	\arrow["{H_0}", from=1-1, to=1-3]
	\arrow[from=1-1, to=3-1]
	\arrow["U", from=1-3, to=3-3]
	\arrow["H", dotted, from=3-1, to=1-3]
	\arrow["{\overline{H}}"', from=3-1, to=3-3]
\end{tikzcd}

Then we have:
1. The lifting problem admits a solution $H \colon \Delta^1 \times K \to \mathcal{E}$ which is a $U$-cocartesian lift of $\overline{H}$.
2. Let $F$ be any object of the $\infty$-category $\text{Fun}_{/\mathcal{C}}(\{1\} \times K, \mathcal{E})$. Then $F$ is isomorphic to $H|_{1\times K}$ (as an object of $\text{Fun}_{/\mathcal{C}}(\{1\} \times K, \mathcal{E})$) if and only if $F = H'|_{1\times K}$, where $H'$ is yet another $U$-cocartesian lift of $\overline{H}$ which solves the above lifting problem.
\end{lemma}

\begin{proof}
This follows by means of the [[currying]] isomorphism and the fact that postcompositon with a cocartesian fibration is itself a cocartesian fibration. Therefore, the lifting problem reduces to $K = \Delta^0$. In this case, $U$ being a cocartesian fibration readily implies the first part, while Remark [5.1.3.8](https://kerodon.net/tag/01U5) does the second part.
\end{proof}
Theorem \ref{existence} now follows as a special case of the above lemma (see [Proposition 5.2.8.4.](https://kerodon.net/tag/02RQ)).


###The $\infty$-categories $\mathcal{S}$ and $\mathcal{QC}$
This is a summary of [Section 5.5](https://kerodon.net/tag/01YV) in [[Kerodon]].

Given a [[locally Kan simplicial category]] $\mathcal{C}$, there is a canonical slice and coslice construction $\mathcal{C}_{/X}$ and $\mathcal{C}_{X/}$ for an object $X \colon \mathcal{C}$. The main question is now does this behave with regards to the [[homotopy coherent nerve]] operation?

Before adressing this, one has yet another natural defintion: For $\mathcal{C}$ locally Kan as above, one can define
$$\mathcal{C}^{\triangleleft}, \qquad \mathcal{C}^{\triangleright}$$

locally Kan enriched left and right cone categories. For those we have canonical isomorphisms:
$$N_\bullet^{\text{hc}}(\mathcal{C}^{\triangleleft}) \cong N_\bullet^{\text{hc}}(\mathcal{C})^{\triangleleft}, \qquad N_\bullet^{\text{hc}}(\mathcal{C}^{\triangleright}) \cong N_\bullet^{\text{hc}}(\mathcal{C})^{\triangleright}$$

\begin{definition}
Let $\mathcal{C}$ be a simplicially enriched category and let $Y \colon \mathcal{C}$.
We have a functor $(\mathcal{C}_{/Y})^\triangleright \overset{V}{\to} \mathcal{C}$ which sends objects $(C, f) \colon \mathcal{C}_{/Y}$ to $C$, and carries the cone point $\infty$ to the object $Y$. If $(C,f)$ and $(D,g)$ are objects of $\mathcal{C}_{/Y}$, then the induced map of simplicial sets
$$\text{Hom}_{(\mathcal{C}_{/Y})^\triangleright}((C,f), (D,g)) \hookrightarrow \text{Hom}_\mathcal{C}(V(C,f), V(D,g)) = \text{Hom}_\mathcal{C}(C, D)$$
is simply given by the inclusion map.
*If $(C,f)$ is an object of $\mathcal{C}_{/Y}$, then the induced map 
$$\Delta^0 = \text{Hom}_{(\mathcal{C}_{/Y})^\triangleright}((C,f), \infty) \to \text{Hom}_\mathcal{C}(V(C,f), V(\infty)) = \text{Hom}_\mathcal{C}(C, Y)$$
is equal to $\Delta^0 \overset{f}{\to} \text{Hom}_\mathcal{C}(C,Y)$. This is referred to as the right [[cone contraction functor]].
\end{definition}

Analogously we have a functor $V \colon (\mathcal{C}_{X/})^\triangleleft \to \mathcal{C}$, which is referred as the left [[cone contraction functor]].
We then have the following useful result:

\begin{proposition}[Propositon 5.5.2.16](https://kerodon.net/tag/01ZM)
We have a bijection

\begin{tikzcd}
	{\Big\{\text{simplicial functors }F \colon \mathcal{D} \to \mathcal{C}_{/Y}\Big\}} \\
	\\
	{\Big\{\text{simplicial functors } G \colon \mathcal{D}^{\triangleright} \to \mathcal{C}\text{ such that } G(\infty) = Y\Big\}}
	\arrow["\cong", from=1-1, to=3-1]
\end{tikzcd}

induced by postcomposition with the right [[cone contraction functor]]. The dual result holds too of course.
\end{proposition}

Now we realize that there is a map
$$N_\bullet^{\text{hc}}(\mathcal{C}_{/X})^\triangleright \cong N_\bullet^{\text{hc}}(\mathcal{C}_{/X}^\triangleright) \to N_\bullet^{\text{hc}}(\mathcal{C})$$
carrying the cone point to the vertex $X$. Therefore by the above bijection we obtain the slice comparison morphism
$$c \colon N_\bullet^{\text{hc}}(\mathcal{C}_{/X}) \to N_\bullet^\text{hc}(\mathcal{C})_{/X}$$

This map is a [[monomorphism]], but it is generally not an isomorphism, nor is it a homotopy equivalence in all cases. However, in good situation it will be a homotopy equivalence.

\begin{theorem}[Theorem 5.5.2.21](https://kerodon.net/tag/01ZS)
Let $\mathcal{C}$ be locally Kan and let $X$ be an object of $\mathcal{C}$ with the following property:
For every morphism $f \colon X \to Y$ and every object $Z \colon \mathcal{C}$, the morphism of simplicial sets
\begin{equation}
\text{Hom}_\mathcal{C}(Y,Z)_\bullet \overset{f^*}{\to} \text{Hom}_\mathcal{C}(X,Z)_\bullet
\end{equation}
is a Kan fibration. Then the coslice comparison morphism $c' \colon N_\bullet^\text{hc}(\mathcal{C}_{X/}) \to N_\bullet^{\text{hc}}(\mathcal{C})_{X/}$ is an equivalence of $\infty$-categories.

\end{theorem}

This result is useful for the following reason: Later on in Chapter 5.5 Lurie defines a chain of $\infty$-categories:
\begin{tikzcd}
	{N_\bullet^{\text{hc}}(\text{QCat}_\star)} & {\mathcal{QC}_\star = N_\bullet^{\text{hc}}(\text{QCat})_\star} & {\mathcal{QC}_\text{Obj}} & {\mathcal{QC}_{\text{Ob}}^{(\infty,2)}}
	\arrow["\sim", hook, from=1-1, to=1-2]
	\arrow[hook, from=1-2, to=1-3]
	\arrow[hook, from=1-3, to=1-4]
\end{tikzcd}
where the first morphism is an equivalence by Proposition [5.5.6.6](https://kerodon.net/tag/020Y) (this is really a corollary of the above theorem).

We can describe the above categories informally as follows: All the above categories have the same collection of objects. For the morphisms we have quite different situations however:
Morphisms in $N_\bullet^{\text{hc}}(\text{QCat}_*)$ are really just (strictly) commutative triangles:
\begin{tikzcd}
	& {*} \\
	{\mathcal{C}} && {\mathcal{D}}
	\arrow["C"', from=1-2, to=2-1]
	\arrow["D", from=1-2, to=2-3]
	\arrow["F"', from=2-1, to=2-3]
\end{tikzcd}
Morphisms in $\mathcal{QC}_\star$ are triangles that commute up to isomorphism in the $\infty$-category $\mathcal{D}$:
\begin{tikzcd}
	& {*} \\
	{\mathcal{C}} && {\mathcal{D}}
	\arrow["C"', from=1-2, to=2-1]
	\arrow[""{name=0, anchor=center, inner sep=0}, "D", from=1-2, to=2-3]
	\arrow["F"', from=2-1, to=2-3]
	\arrow["\simeq"{description, pos=0.6}, draw=none, from=2-1, to=0]
\end{tikzcd}
Morphisms in $\mathcal{QC}_\text{Obj}$ are diagrams
\begin{tikzcd}
	& {*} \\
	{\mathcal{C}} && {\mathcal{D}}
	\arrow["C"', from=1-2, to=2-1]
	\arrow[""{name=0, anchor=center, inner sep=0}, "D", from=1-2, to=2-3]
	\arrow["F"', from=2-1, to=2-3]
	\arrow[shorten <=8pt, shorten >=8pt, Rightarrow, from=2-1, to=0]
\end{tikzcd}
with the comparison morphism not necessarily being an isomorphism.
Finally, the last play in the game $\mathcal{QC}_{\text{Ob}}^{(\infty,2)}$ is not an $(\infty,1)$-category but an $(\infty,2)$-category, with the same objects and morphisms as $\mathcal{QC}_\text{Obj}$, but with non-invertible natural transformations between functors.



## Derived Categories
###Homological Algebra
For amazing Nlab lecture notes see [[An Introduction to Homological Algebra]].
### Differential-Graded Categories
### Derived $\infty$-categories of (Grothendieck) abelian Categories
#### Derived Categories of Rings
#### Derived Categories of (quasicoherent) Sheaves

##Stable Homotopy Theory
### Motivation from Classical homotopy Theory: Suspension-Loop Adjunction
Amazing Nlab Lecture notes at [[Introduction to Stable Homotopy Theory]].
### Freudenthal-Suspension Theorem
###Stable $\infty$-Categories
For now see [[stable (infinity,1)-category]].
####The Stable Yoneda Lemma
###How to Stabilize - All about Spectrum Objects
###Brown Representability
###A universal Example - Spectra

##Let there be algebra - Operadic Yoga
###$\mathbb{E}_n$-operads
###Module-Operads
###Operad-Algebras
###Monoidal Categories
####Definition and Intuition
####Algebra Objects
####Derived Categories
####Spectra
### Brave new Algebra
####Ring Spectra, modules, algebras

##Presentable and Accessible Categories
###Why size matters
###Cocompletions
###Presentability and the Adjoint Functor Theorem
###Lurie Tensor Product

##Lax Stuff via (Co)Ends

##Enriched $\infty$-Categories

##$k$-linear presentable stable $\infty$-Categories

##Derived Representation Theory
### Recollements
### Generalized BGP Reflection Functors
### Ladkani's Theorem in the context of Ring Spectra




## References
* {#usersguideCocart}[[Aaron Mazel-Gee]], _A user's guide to co/cartesian fibrations_, [arXiv:1510.02402](http://arxiv.org/abs/1510.02402) (2015).

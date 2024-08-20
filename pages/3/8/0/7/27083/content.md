[[!redirects Private notes on derived cats and k-linear cats]]
[[!redirects Private notes on derived cats and k-linear cats]]

# Why these Notes
The idea is that these notes should become an accessible and user friendly introduction to derived mathematics, higher algebra and enriched higher category theory.
# Contents
* this block creates the table of contents, leave as is
{: toc}

## The holy Grail: Straightening & Unstraightening
For other Nlab entries see: [[(infinity,1)-Grothendieck construction]], [[straightening functor]], [[Grothendieck construction]], ...

In the following we will mostly follow [[Kerodon]].

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

###(Co)Cartesian morphisms and (Co)Cartesian Fibrations
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
####"Nice" Bundle maps that allow for functorial fibers - (co)cartesian fibrations

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
Let $U \colon \mathcal{E} \to \mathcal{C}$ be a functor of $\infty$-categories, and denote by $U\text{-Cocart}$ (resp. $U\text{-Cart}$) the full subcategory of the arrow category $\text{Ar}\mathcal{E} \coloneqq \mathcal{E}^{\Delta^1}$ spanned by the $U$-cocartesian morphisms (resp. cartesian morphisms). 

* $U$ is called cocartesian fibration, if the (induced) dashed arrow in the diagram below is an equivalence of $\infty$-categories:

\begin{tikzcd}
	{U\text{-Cart}} \\
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
#####Functoriality
Now assume $U\colon \mathcal{E} \to \mathcal{C}$, a functor of $1$-categories, is a cocartesian fibration. 

We define the functor $\text{St}(U)$ as follows:

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
For a morphism $z \colon e \to \overline{e}$ in $\mathcal{E}_c$, we define $f_!(z)$ by means of the unique lift induced by the universal property of the cocartesian morphism:

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



## Derived Categories
### Differential-Graded Categories
### Derived $\infty$-categories of (Grothendieck) abelian Categories
#### Derived Categories of Rings
#### Derived Categories of (quasicoherent) Sheaves

##Stable Homotopy Theory
### Motivation from Classical homotopy Theory: Suspension-Loop Adjunction
### Freudenthal-Suspension Theorem
###Stable $\infty$-Categories
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

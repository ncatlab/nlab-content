+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* toc
{:toc}

## Idea 

A *Grothendieck fibration* (named after [[Alexander Grothendieck]], also called a *fibered category* or just a *fibration*) is a [[functor]] $p \colon E\to B$ such that the [[fibers]] $E_b = p^{-1}(b)$ depend (contravariantly) [[pseudofunctor|pseudofunctorially]] on $b\in B$. 

One also says that $E$ is a *fibered category* over $B$.
One calls $E$ the *total category* of the fibration (not to be confused with the independent notion of *[[total category]]*) and $B$ its *base category*.  

[[formal duality|Dually]], in a (Grothendieck) *opfibration* the dependence is [[covariant functor|covariant]].

There is an [[equivalence of categories|equivalence]] of [[strict 2-category|2-categories]] 

$$
  Fib(B) 
   \overset
    {\simeq}
    {\leftrightarrow} 
  [B^{op}, Cat] 
  \;\colon\;
  \textstyle{\int}
$$

between the 2-category of fibrations, cartesian functors, and vertical natural transformations over $B$, and the 2-category $[B^{op},Cat]$ of contravariant [[pseudofunctor]]s from $B$ to [[Cat]], also called $B$-[[indexed categories]].

The "[[Grothendieck construction]]" $\int \colon [B^{op}, Cat] \to Fib(B) \colon F \mapsto \int F$ constructs the fibration corresponding to a pseudofunctor.  

Those fibrations corresponding to pseudofunctors that factor through [[Grpd]] are called **[[categories fibered in groupoids]]**.



## Definition 
 {#Definition}

\begin{definition}\label{CartesianMorphism}
**([[cartesian morphism]])**
\linebreak
Given a [[functor]] $P \,\colon\, \mathcal{E} \longrightarrow \mathcal{B}$,
a [[morphism]] $f \colon x \to y$ in its [[domain]] [[category]] $\mathcal{E}$ is called *[[cartesian morphism|cartesian]]* if for any morphism $g \colon z\to y$ in $\mathcal{E}$ and $w \colon P(z)\to P(x)$ in $\mathcal{B}$ such that $P(f)\circ w = P(g)$, there exists a *unique* $\widehat{w} \,\colon\, z\to x$ such that $g = f \circ \widehat{w}$ and $P(\widehat{w}) = w$:

\begin{tikzcd}[
  sep=20pt
]
  &
  z
  \ar[
    drrr, 
    bend left=20, 
   "{ \forall \, g }"{description}
  ]
  \ar[
    dr, 
    dashed, 
    "{ 
       \exists! \, \widehat{w} 
    }"{description}
  ]
  \\
  \mathcal{E}
  \ar[dd, "{ P }"]
  &&
  x 
  \ar[
     rr, 
     "{ f }"{description},
     "{ \mathrm{cartesian} }"{swap, yshift=-1pt}
  ]  
  && 
  y
  \\
  & 
  P(z)
  \ar[drrr, bend left=20, "{ P(g) }"{description}]
  \ar[
    dr,
    "{ \forall \, w }"{description}
  ]
  \\
  \mathcal{B}
  &&
  P(x) 
  \ar[rr, "{ P(f) }"{description}]
  && 
  P(y)
\end{tikzcd}
 

\end{definition}

\begin{definition}\label{GrothendieckFibration}
**(Grothendieck fibration)**
\linebreak
A [[functor]] $P \colon \mathcal{E} \to \mathcal{B}$ is a *fibration* if for all [[objects]] $y \in \mathcal{E}$ and [[morphisms]] $f_0 \colon x_0 \to P(y)$, there is a cartesian morphism $f \colon x \to y$ (Def. \ref{CartesianMorphism}) such that $P(f) = f_0$.  
\end{definition}

Such $f$ is also called a "cartesian lifting" of $P(f)$ to $y$, and a choice of cartesian lifting for every $y$ and $P(f)$ is called a *[[cleavage]]*.  Thus, assuming the [[axiom of choice]], a functor is a fibration iff it admits some cleavage.

\begin{remark}
**(weakly cartesian morphisms)**
\linebreak
We say that a morphism $f$ is [[prefibered category|weakly cartesian]] if it has the property of a Cartesian morphism (Def. \ref{CartesianMorphism}) only when $w$ is an [[identity morphism]].  

One can prove that $P$ is a fibration (Def. \ref{GrothendieckFibration}) if and only if firstly, it has the above property with "Cartesian" replaced by "weakly cartesian," and secondly, the composite of weakly cartesian arrows is weakly cartesian.  

In a fibration, every weakly cartesian lifting $f$ of $P f$ to $y$ is in fact cartesian (as one can show by combining the [[universal properties]] of $f$ and of a given cartesian lifting to $e$), but this is not true in general.  

Some sources say "cartesian" and "strongly cartesian" instead of "weakly cartesian" and "cartesian," respectively.  If weakly cartesian liftings exist but weakly cartesian arrows are *not* necessarily closed under composition, one sometimes speaks of a [[prefibered category]].
\end{remark}

\begin{definition}\label{MorphismOfFibrations}
**(morphism of fibrations -- [[fibered functor]])**
\linebreak
For $P$ and $P'$ fibrations (Def. \ref{GrothendieckFibration}), a [[commuting square]] of [[functors]] of the form
\[
  \label{DiagramForFiberedFunctor}
  \array{
    \mathcal{E}' 
     & 
    \longrightarrow 
    & 
    \mathcal{E}
    \\ 
    \mathllap{{}^{P'}}\big\downarrow 
    && 
    \big\downarrow 
    \mathrlap{{}^{P}}
    \\ 
    \mathcal{B}' 
      & \longrightarrow & 
    \mathcal{B}
  }
\]
is a *morphism of fibrations* (also called a *cartesian square* or *[[fibred functor]]*) if the top functor preserves Cartesian morphisms (Def. \ref{CartesianMorphism}).  
\end{definition}

\begin{definition}\label{TwoMorphismOfFibrations}
**([[2-morphisms]] of fibrations -- [[fibered natural transformation]])**
\linebreak
A [[2-morphism]] (or *[[fibered natural transformation]]*) between morphisms of fibrations (Def. \ref{MorphismOfFibrations}) is a pair of [[natural transformations]], one lying over the other in (eq:DiagramForFiberedFunctor).
\end{definition}

\begin{remark} 
If the functor on base categories is an [[identity functor|identity]], then a 2-morphism (Def. \ref{TwoMorphismOfFibrations}) is a [[natural transformations]] between total categories which is "vertical" in that its component morphisms lie in [[fibers]].
\end{remark}


## Fibrations versus pseudofunctors

Given a fibration $p:E\to B$, we obtain a pseudofunctor $B^{op}\to Cat$ by sending each $b\in B$ to the category $E_b = p^{-1}(b)$ of objects mapping onto $b$ and morphisms mapping onto $1_b$.  To obtain the action on morphisms, given an $f:a\to b$ in $B$ and an object $e\in E_b$, we choose a cartesian arrow $\phi:e'\to e$ over $f$ and call its [[source]] $f^*(e)$.  The universal factorization property of cartesian arrows then makes $f^*$ into a functor $E_b \to E_a$, and it is easy to verify that it is a pseudofunctor.  The functor in the other direction is called the [[Grothendieck construction]].  This yields a [[strict 2-equivalence of 2-categories]] between

* fibrations over $B$, morphisms of fibrations over $Id_B$, and 2-cells over $id_{Id_B}$, and

* [[pseudofunctors]] of the form $B^{op}\to Cat$, [[pseudonatural transformations]], and [[modifications]].

In fact, this is an instance of the general theory of representability for [[generalized multicategories]].  There is a monad $T$ whose pseudoalgebras are pseudofunctors $B^{op}\to Cat$, and whose "generalized multicategories" are functors $E\to B$.  Such a multicategory is "representable" precisely when it is a fibration, and moreover there is an induced monad $\hat{T}$ on $Cat/B$ which is [[lax-idempotent 2-monad|colax-idempotent]] and whose pseudoalgebras are precisely the fibrations.

This correspondence also generalizes to the correspondence between arbitrary functors over $B$ and [[displayed categories]] over $B$, i.e. normal lax functors $B\to Prof$.

## Fibrations versus presheaves of categories

The [[Grothendieck construction]] is an equivalence of [[bicategories]]
from the bicategory of presheaves of categories to the bicategory of Grothendieck fibrations.

As explained there, this equivalence, interpreted as a functor between 1-categories,
has both a left and a right adjoint (which are equivalent in the bicategorical context).
Roughly speaking, the left adjoint strictifies a Grothendieck fibration
by adding formal pullbacks of objects, which themselves pullback strictly,
whereas the right adjoint strictifies a Grothendieck fibration
by equipping object with a functorial choice of a pullback for each possible morphism.
See [[Grothendieck construction]] for more details.

These two adjunctions can be turned into [[Quillen equivalences]] of [[model categories]].
This can be deduced, for example, from two [[Quillen equivalences]]
between [[cartesian fibrations]] and [[presheaves]] of [[marked simplicial sets]]
on the [[quasicategory]] given by the [[nerve]] of $C$.
See [[straightening functor]] for more details.


## Remarks

* Fibrations are a "nonalgebraic" structure, since the base change functors $f^*$ are determined by universal properties, hence uniquely up to isomorphism.  By contrast, pseudofunctors are an "algebraic" structure, since the functors $f^*$ are specified, together with the necessary coherence data and axioms; the latter come for free in a fibration because of the universal property.

* A [[stack]], being a particular type of pseudofunctor, can also be described as a particular sort of fibration.  This was the original application for which Grothendieck introduced the notion.


## Examples 

\begin{example}
Let [[VectBund|$\VBun$]] denote the category whose [[objects]] are [[pairs]] $(M,V)\in\Man\times\Man$ of [[manifolds]] where $q:V\longrightarrow M$ is a [[vector bundle|vector bundle]] over $M$. A morphism $(M_{1},V_{1})\longrightarrow (M_{2},V_{2})$ is a [[commutative square]]: 
\begin{center}
\begin{tikzcd}
V_{1} \arrow[r, "g"] \arrow[d, "q_{1}"'] & V_{2} \arrow[d, "q_{2}"] \\
M_{1} \arrow[r, "f"']                    & M_{2}                   
\end{tikzcd}
\end{center}
where $f$ is a smooth map, and $g$ is a smooth map such that $g\mid_{q_{1}^{-1}(m)}:q_{1}^{-1}(m)\longrightarrow q_{2}^{-1}(f(m))$ is linear for every $m\in M_{1}$. Composition is given as in the [[arrow category|arrow category]]. There is a forgetful functor $\mathcal{P}:\VBun\longrightarrow\Man$ which projects onto the base data. To see that this functor is a Grothendieck fibration, first consider a morphism of the form: 
\begin{center}
\begin{tikzcd}
f^{*}M_{2} \arrow[r] \arrow[d] & V_{2} \arrow[d, "q_{2}"] \\
M_{1} \arrow[r, "f"']                      & M_{2}                   
\end{tikzcd}
\end{center}
given by the [[pullback bundle|pullback bundle]] of a vector bundle $V_{2}\longrightarrow M_{2}$ along a smooth map $M_{1}\longrightarrow M_{2}$. Certainly, the [[universal construction|universal property]] of the [[pullback|pullback]] will supply the conditions for this square to define a [[Cartesian morphism|cartesian morphism]] in $\VBun$ with respect to the the functor $\mathcal{P}$. We show that these are in fact all the cartesian morphisms in $\VBun$.
Let $e' = (V_{1},M_{1})$, $e = (V_{2},M_{2})$, and $e'' = (V,M)$, then by applying the definition from above directly, we see that a morphism $\phi:e'\longrightarrow e$ in $\VBun$, i.e., a square:
\begin{center}
\begin{tikzcd}
V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M_{1} \arrow[r]                    & M_{2}                   
\end{tikzcd}
\end{center}
is cartesian, if given any morphism $\psi:e''\longrightarrow e$ in $\VBun$, i.e., a square (which we draw around the first):
\begin{center}
\begin{tikzcd}
V \arrow[rrd, bend left] \arrow[dd, "e''"']   &                           &                 \\
                                      & V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M \arrow[rr, bend right, shift right] & M_{1} \arrow[r]           & M_{2}          
\end{tikzcd}
\end{center}
and any morphism $g:\mathcal{P}(e'')\longrightarrow \mathcal{P}(e')$ in $\Man$ such that $\mathcal{P}(\phi)\circ g = \mathcal{P}(\psi)$, i.e. a smooth map $g:M\longrightarrow M_{1}$ that fills in the above diagram to a commuting diagram:
\begin{center}
\begin{tikzcd}
V \arrow[rrd, bend left] \arrow[dd, "e''"']             &                           &                 \\
                                                & V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M \arrow[rr, bend right, shift right] \arrow[r, "g"] & M_{1} \arrow[r]           & M_{2}          
\end{tikzcd}
\end{center}
then there exists a unique morphism $\chi:e''\longrightarrow e'$ in $\VBun$ such that $\psi = \phi\circ\chi$ and $\mathcal{P}(\chi) = g$, i.e., there exists a unique morphism $V\longrightarrow V_{1}$ that further fills the diagram to a commuting diagram:
\begin{center}
\begin{tikzcd}
V \arrow[rrd, bend left] \arrow[dd, "e''"'] \arrow[rd, dashed] &                           &                 \\
                                                       & V_{1} \arrow[r] \arrow[d, "e'"'] & V_{2} \arrow[d, "e"] \\
M \arrow[rr, bend right, shift right] \arrow[r, "g"]        & M_{1} \arrow[r]           & M_{2}          
\end{tikzcd}
\end{center}
It immediately follows from the above unfolding of the definition that $\VBun(e'',e')\cong\VBun(e'',p)$ naturally in $e''$, where $p$ is the pullback bundle of $V_{2}\longrightarrow M_{2}$ along $M_{1}\longrightarrow M_{2}$, and thus by the [[Yoneda lemma#YonedaCorollaries|Yoneda lemma]] $e'\cong p$, and thus $V_{1}\cong\mathcal{P}(e')^{*}V_{2}$. Note that the isomorphisms $e'\cong p$ preserve the commutativity of the diagrams we have drawn above by the universal property of the pullback, and by the definition of a cartesian morphism. Now that we have identified the cartesian morphisms, the statement that $\mathcal{P}:\VBun\longrightarrow\Man$ is a Grothendieck fibration is equivalent to the statement that vector bundles can be pulled back along smooth maps. This is of course true, and thus $\mathcal{P}:\VBun\longrightarrow\Man$ is a Grothendieck fibration.
The associated functors $f^{*}$ are the [[pullback#PullbackFunctor|pullback pseudofunctors]] $f^{*}:\VBun_{M_{2}}\longrightarrow \VBun_{M_{1}}$ that pullback vector bundles over a manifold $M_{2}$ to vector bundles over a manifold $M_{1}$ along a smooth map $f:M_{1}\longrightarrow M_{2}$.
\end{example}

\begin{example}
Let [[Ring]] be the category of [[ring|rings]], and [[Mod]] the category of pairs $(R,M)$ where $R$ is a ring and $M$ is a (left) $R$-module.  Then the evident forgetful functor $Mod\to Ring$ is a fibration and an opfibration.  The functors $f^*$ are given by restriction of scalars, $f_!$ is extension of scalars, and the right adjoint $f_*$ is coextension of scalars.
\end{example}

\begin{example}
Let $C$ be any category with [[pullbacks]] and $\mathbf{2}$ the [[free-living]] arrow, so that $C^{\mathbf{2}}$ is the category of arrows and commutative squares in $C$.  Then the "codomain" functor $C^{\mathbf{2}} \to C$ is a fibration and opfibration.  The cartesian arrows are precisely the pullback squares, and the functors $f_!$ are just given by composition.  The right adjoints $f_*$ exist iff $C$ is [[locally cartesian closed category|locally cartesian closed]].  The term "cartesian" is motivated by this example, which is usually called the **[[codomain fibration]]** over $C$.
\end{example}

\begin{example}
\label{SimpleFibration}
Let $C$ be a category with binary [[cartesian products]]. Then for each object $\Gamma$, we can construct an indexed comonad $C \to Comonad$, the [[coreader comonad|environment comonad]] $\Gamma \times -$ on $C$, and taking [[Kleisli categories]] we get a functor $C^{op} \to Cat$. The corresponding fibration is called the [[simple fibration]] (e.g., in [Jacobs 1998](#Jacobs98)) over $C$ because it can be used to give semantics to simply-typed [[lambda calculus]]. The simple fibration can be seen as a full subfibration of the [[codomain fibration]], with objects being the [[projections]] $\Gamma \times A \to \Gamma$.
\end{example}

\begin{example}\label{FreeCoproductCompletion}
**([[families]], [[free coproduct completion]])**
\linebreak
Let $C$ be any category and let $Fam(C)$ be the category of set-indexed [[families]] of objects of $C$ (the [[free coproduct completion]] of $C$, which is a [[Grothendieck construction]] by the discussion [there](free+coproduct+completion#AsAGrothendieckConstruction)).  The forgetful functor $Fam(C)\to Set$ taking a family to its indexing set is a fibration; the functors $f^*$ are given by reindexing.  They have left adjoints iff $C$ has small coproducts, and right adjoints iff $C$ has small products.
\end{example}

\begin{example} 
A [[group extension]] of a group $H$ by a group $K$, 
$$1 \to K \overset{i}{\to} G \overset{p}{\to} H \to 1,$$ 
can be viewed as a fibration $p: G \to H$ between one-object categories, with $K$ playing the role of fiber. In selecting a cleavage, effectively a [[section]] $s: H \to G$ between the underlying sets, one is led to a pseudofunctor 
$$H \to Cat$$ 
that takes the single object of $H$ to the category $K$, and morphisms $h$ of $H$ to inner automorphisms $h^\ast$ (qua functors) on $K$ by conjugation $k \mapsto s(h)^{-1}k s(h)$, hence a map $\psi: H \to Aut(K)$. Moreover, taking into account pseudofunctoriality, the isomorphisms $h_2^\ast h_1^\ast \cong (h_1 h_2)^\ast$ are tracked by (nonabelian) group 2-cocycle data 
$$\chi: H \times H \to K: (h_1, h_2) \mapsto s(h_1 h_2)^{-1} s(h_1)s(h_2),$$
as described [here](group+extension#SchreierTheoryTraditional). The reconstruction of the group structure of $G$ from the data  $\psi: H \to Aut(K)$ and $\chi: H \times H \to K$, as described in traditional Schreier theory, is then revealed as a special case of the Grothendieck construction. See [here](https://nforum.ncatlab.org/discussion/778/grothendieck-fibration/?Focus=123242#Comment_123242) for further related discussion. 
\end{example} 


## Properties

* It is easy to verify that fibrations are closed under   [[pullback]] in [[Cat]], and that the composite of fibrations is a fibration.  This latter property is notably difficult to even express in the language of pseudofunctors.

* Every fibration (or opfibration) is a [[Conduché functor]], and therefore an [[exponentiable morphism]] in [[Cat]].

* Every fibration or opfibration is an [[isofibration]].  In particular, [[strict 2-limit|strict 2-pullbacks]] of fibrations are also [[2-pullbacks]].

* {#FiberedLimit} Suppose that $p\colon A\to B$ is a fibration, and $B$ has $I$-indexed [[limits]]. Then $A$ has $I$-indexed limits and $p$ strictly preserves them if and only if $p$ has $I$-indexed [[fibered limit|fibred limits]]. This is in [Gray 66](#Gray); for a general perspective, see [Hermida 99, Corollary 4.9](#Hermida). Concretely, for instance, from right to left, given a [[diagram]] $f\colon I\to A$, let $L$ be the limit of $p f\colon I\to B$, with projections $\phi_i\colon L \to p(f(i))$.  Then for each $i\in I$, let $g(i) = \phi_i^*(f(i)) \in p^{-1}(L)$; these objects form a diagram $g\colon I\to p^{-1}(L)$ whose limit is the limit of $f$. 

* Dually, if $p\colon A\to B$ is an opfibration, then [[colimits]] in $A$ can be constructed out of those in $B$ and in the fiber categories.

* Suppose that $p\colon A\to B$ is a fibred [[cartesian closed category]] with [[simple products]]. Then if $B$ is cartesian closed, so is $A$ and $p$ preserves the structure. (See [Hermida 99, Corollary 4.12](#Hermida).) But the converse does not hold, see Section 4.3.2 of [Hermida's thesis](#HermidaThesis). 

* If $p\colon A\to B$ is a fibration and $B$ admits an [[orthogonal factorization system]] $(E,M)$, then there is a factorization system $(E',M')$ on $A$, where $M'$ is the class of cartesian arrows whose image in $B$ lies in $M$, and $E'$ is the class of all arrows whose image in $B$ lies in $E$.  A dual construction is possible if $p$ is an opfibration.  If it is a bifibration (or more generally, an [[ambifibration]] over $(E,M)$), then these together form a [[ternary factorization system]].

* Under suitable hypotheses, versions of the preceding fact can be shown  [[weak factorization systems]] and [[model structures]] as well.

* Generalizing in a different direction, if $p\colon A\to B$ is a fibration and $(E,M)$ is a [[factorization structure for sinks]] on $B$, then $A$ admits a factorization structure for sinks $(E',M')$, where $M'$ is the class of cartesian arrows whose image in $B$ lies in $M$, and $E'$ is the class of all arrows whose image in $B$ lies in $E$.  Similarly, we can lift factorization structures for *cosinks* along an opfibration.  To lift in the "opposite" way we require more of $p$; see [[topological concrete category]].


## Variations 

### Discrete and groupoidal fibrations

One important special case of a fibration is when each fiber is a [[groupoid]]; these correspond to pseudofunctors $B^{op}\to Grpd$.  These are also called *categories fibered in groupoids*.  A fibration $E\to B$ is fibered in groupoids precisely when *every* morphism in $E$ is cartesian.

Another important special case is when each fiber is a [[discrete category]]; these correspond to functors $B^{op}\to Set$.  These are also called *[[discrete fibrations]]*.  A functor $p\colon E\to B$ is a discrete fibration precisely when for every $e\in E$ and $f\colon b\to p(e)$ there is a *unique* lifting of $f$ to a morphism $e'\to e$.


### Opfibrations and bifibrations

We say that $p\colon E\to B$ is an **opfibration** if $p^{op}:E^{op}\to B^{op}$ is a fibration.  These correspond to covariant pseudofunctors $B\to Cat$.  A functor that is both a fibration and an opfibration is called a **[[bifibration]]**.  It is not hard to see that a fibration is a bifibration iff each functor $f^*$ has a left adjoint, written $f_!$ or $\Sigma_f$.  In many cases $f^*$ also has a right adjoint, written $f_*$ or $\Pi_f$, but this is not as easily expressible in fibrational language.

Grothendieck originally called an opfibration a *cofibered category*, and if the fibers are groupoids a [[category cofibered in groupoids]] (cf. [[SGA I]], [[Higher Topos Theory]]).  However, that term has fallen out of favor in the homotopy-theory and category-theory communities (though still used sometimes in algebraic geometry), because an opfibration still has a _lifting_ property, as is characteristic of other notions of [[fibration]], as opposed to the _extension_ property exhibited by [[cofibrations]] in [[homotopy theory]].

Note that an opfibration is the same as an internal fibration in the 2-category $Cat^{co}$, while it is the fibrations in the 2-category $Cat^{op}$ which are more deserving of the name "cofibration."

Note also that a given pseudofunctor $B^{op}\to Cat$ can be represented both by a fibration $E_1\to B$ and by an opfibration $E_2\to B^{op}$.  However $E_2$ is _not_ the opposite category of $E_1$.


### Version respecting the Principle of equivalence {#StreetFibration}

There is something apparently in violation of the [[principle of equivalence]] about the notion of fibration, namely the requirement that for every $f:a\to b$ and $e\in E_b$ there exists a $\phi:e'\to e$ such that $p(e')$ is _[[equality|equal]]_, rather than merely [[isomorphism|isomorphic]], to $a$.  This is connected with the fact that we use strict fibers, rather than [[essential fiber]]s, and that fibrations and pseudofunctors can be recovered from each other up to isomorphism rather than merely equivalence.

Note that almost any fibration between "concrete" categories that arises in practice does satisfy this strict property.  However, even stating the strict property requires our categories to be [[strict categories]] (i.e. to have a notion of equality of objects), so when working in a context where not all categories are strict (such as [[internal categories in homotopy type theory]], or with objects in a [[bicategory]]) it is problematic.  Sometimes (such as in type theory) this can be avoided by working with [[displayed categories]] instead, but in some cases (such as internally in a bicategory) one does not have classifying objects either, so it is sometimes useful to have a version which manifestly accords to the [[principle of equivalence]].

The correct modification, first given by [[Ross Street]], is simply to require that for any $f:a\to b$ and $e\in E_b$ there exists a cartesian $\phi:e'\to e$ and an _isomorphism_ $h:p(e') \cong a$ such that $f\circ h = p(\phi)$; the definition of "cartesian" is unchanged; this gives the notion of [[Street fibration]].  Every [[equivalence of categories]] is a Street fibration, which is not true for the concept of Grothendieck fibrations according to the [[principle of equivalence]], but every Street fibration can be factored as an equivalence of categories followed by a Grothendieck fibration.

We might also think that it violates the [[principle of equivalence]] to say that the target of the cartesian arrow $\phi$ is equal to the given object $e$, akin to the topological distinction between [[Serre fibrations]] and [[Dold fibrations]], where the initial point of a lifted path can only be specified up to homotopy.  However, this part of the definition is really better regarded as a typing assertion, akin to saying, in the definition of a [[product]] of two objects $A$ and $B$, that the target of the two projections $A\times B\to A$ and $A\times B \to B$ are *equal* to $A$ and $B$.  Moreover, any weakening along these lines would actually be equivalent to the version above: if we demand only that for any $f\colon a\to b$ in $B$ and $e\in E_b$, there exists a cartesian $\phi\colon e' \to \hat{e}$ with $p(\phi)=f$ and an isomorphism $\hat{e}\cong e$ in the fiber $E_b$, then you can just compose $\phi$ with the isomorphism $\hat{e}\cong e$ to get a cartesian arrow $\hat{\phi}\colon e'\to e$ with $p(\phi)=f$ still.  The reason this doesn't work in topology is that paths come with parametrizations, and requiring the lower triangle (in the square drawn at [[Dold fibration]]) to commute strictly prevents the reparametrization necessary to compose with a vertical homotopy.

The idea of [[proto-fibration]] is closely related to this.

### Internal version 

In a [[strict 2-category]] $K$, a morphism $p:E\to B$ is called a fibration if for every object $X$, $K(X,E)\to K(X,B)$ is a fibration of categories, and for every morphism $f:Y\to X$, the square
$$\array{ K(X,E) & \to & K(Y,E) \\ \downarrow && \downarrow \\ K(X,B) & \to & K(Y,B)}$$
is a morphism of fibrations.  There is an alternate characterization in terms of [[comma object]]s and adjoints, see [[fibration in a 2-category]].  The same definition works in a [[bicategory]], as long as we use the version in accord with the [[principle of equivalence]] above.  Interpreted in [[Cat]] we obtain the explicit notion we started with.


### Two-sided version 

A **two-sided fibration**, or a **fibration from $B$ to $A$**, is a span $A \leftarrow E \rightarrow B$ such that $E\to A$ is a fibration, $E\to B$ is an opfibration, and the structure "commutes" in a natural way.  Such two-sided fibrations correspond to pseudofunctors $A^{op}\times B \to Cat$.  If they are discrete, they correspond to functors $A^{op}\times B\to Set$, i.e. to [[profunctors]] from $B$ to $A$.

See [[two-sided fibration]] for more details.

Note that a pseudofunctor $A^{op}\times B \to Cat$ can also be represented by an opfibration $E_1\to A^{op}\times B$ and by a fibration $E_2\to A\times B^{op}$, but there is no simple relationship between the three categories $E$, $E_1$, and $E_2$.

### Higher categorical versions 

There is also a notion of fibration for 2-categories that has been studied by Hermida.  See [[n-fibration]] for a general version.

For [[(∞,1)-category|(∞,1)-categories]] the notion of fibered category is modeled by the notion of [[Cartesian fibration]] of simplicial sets. The corresponding analog of the Grothendieck construction is discussed at [[(∞,1)-Grothendieck construction]].

### Versions for other categorical structures

* There is an analog for [[multicategories]]. See [[fibration of multicategories]].

* For higher multicategories, see [[Cartesian fibration of dendroidal sets]].

* For [[double categories]], see [[double fibration]].

## Alternate definitions

There are several alternate characterizations of when a functor is a fibration, some of which are more convenient for [[fibration in a 2-category|internalization]].  Here we mention a few.

### In terms of adjoints

Since Grothendieck fibrations are a [[strict category|strict]] notion, in what follows we denote by $B\downarrow p$ the [[strict category|strict]] [[comma category]] (i.e. determined up to [[isomorphism]], not merely up to [[equivalence of categories|equivalence]]) and by $Cat/B$ the [[strict slice 2-category]].

+--{: .un_lemma}
###### Lemma
A functor $p \colon E \to B$ is a cloven fibration if and only if the canonical functor $i \colon E \to B\downarrow p$ has a right adjoint $r$ in $Cat / B$.
=--
+-- {: .proof }
###### Proof
First, recall that the strict slice 2-category $Cat/X$ has objects the functors $C \to X$, as morphisms the commuting triangles
$$\array{C & \stackrel{h}{\to} & C' \\ & f \searrow \swarrow g &  \\  & X,  & }$$
and as 2-cells the natural transformations $\alpha : h_1 \to h_2$ such that $g\alpha = id_f$.

Next, recall that the [[comma category]] $B\downarrow p$ has objects the triples $(x, e, k)$, with $k \colon x \to p e$.  Let $\pi \colon B\downarrow p \to B$ denote the projection $(x, e, k) \mapsto x$.

The canonical morphism $i:E \to B\downarrow p$ is simply the inclusion functor of identity maps $i e  = 1_{p e} \colon p e \to p e$.

Somewhat imprecisely, seeing both categories $E$ and $B\downarrow p$ as sitting over $B$ means that functors between those should be the identity on the $b$ component, and natural transformations should have the identity as their $b$ component.

To give an adjunction $i \dashv r$ it suffices to give, for each $k \colon x \to p e$ in $B\downarrow p$, an object $r k$ in $E$ such that $p r k = x$ and an arrow $i r k = 1_x \to k$ in $B\downarrow p$ that is [[universal arrow|universal]] from $i$ to $k$.  For the adjunction to live in $Cat / B$ we must have that $\pi \circ i r k = 1_{p r k} = 1_x$, so the universal arrow must be of the form
$$
\array{
  x & \overset{1}{\to} & x \\
  \mathllap{1} \downarrow & & \downarrow \mathrlap{p \epsilon_k} \\
  x & \underset{k}{\to} & p e
}
$$
and thus amounts to a choice of $\epsilon_k \colon r k \to e$ in $E$ such that $p \epsilon_k = k$.

The universal property of $\epsilon_k$ tells us that for any other morphism in $B\downarrow p$ from some $i y$ to $k$, i.e., for any $y$ and any pair $(f,g)$ making the square
$$
\array{
  p y & \stackrel{1}{\to} & p y \\
  \mathllap{f} \downarrow & & \downarrow \mathrlap{p g} \\
  x & \underset{k}{\to} & p e
}
$$
commute, there is a unique map $h \colon y \to r k$ in $B$ such that the above square factors in $B\downarrow p$ as
$$
\array{
  p y & \stackrel{1}{\to} & p y \\
  \mathllap{p h} \downarrow &  & \downarrow \mathrlap{p h} \\
  \mathllap{p r k =} x & \stackrel{1}{\to} & x \mathrlap{= p r k}\\
  \mathllap{1} \downarrow & & \downarrow \mathrlap{p \epsilon_k} \\
  x & \underset{k}{\to} & p e.
}
$$

In other words, the universal property provides a unique $h$ such that $\epsilon_k h = g$ and $p h = f$, which exactly asserts that $\epsilon_k$ is a cartesian lift of $k$.

So the existence of a right adjoint to $i$ means precisely that for each morphism $k \colon x \to p e$ a choice is given of a cartesian lift of $k$, which means in turn that $p$ is a cloven fibration.
=--

### In terms of pseudoalgebras

Fibrations are pseudoalgebras for a [[lax-idempotent pseudomonad]] (see there for more details).

## Related concepts

* [[opfibration]], [[bifibration]] 

  [[two-sided fibration]]

* [[small fibration]], [[locally small fibration]]

* [[monoidal fibration]]

* [[fibration of 2-categories]]

* [[n-fibration]]

* [[Cartesian fibration]]

* [[foliated category]]

* [[Grothendieck construction]], [[category of elements]]

## References 
 {#References}

The concept was introduced in the context of [[descent theory]] and in the guise now known as [[indexed categories]], in

* {#Grothendieck60} [[Alexander Grothendieck]], p. 300 in: *Technique de descente et théorèmes d’existence en géométrie algébrique. I. Généralités. Descente par morphismes fidèlement plats*, Séminaire [[N. Bourbaki]] exp. no190 (1960) 299-327 &lbrack;[numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/?id=SB_1958-1960__5__299_0)&rbrack;

and then elaborated on in

* [[Alexander Grothendieck]], expos&#233; VI of: _Rev&#234;tements Etales et Groupe Fondamental - S&#233;minaire de G&#233;ometrie Alg&#233;brique du Bois Marie 1960/61_ ([[SGA 1]]) , LNM **224** Springer (1971) &lbrack;updated version with comments by M. Raynaud: [arxiv.0206203](http://arxiv.org/abs/math/0206203)&rbrack;

Another important early reference:

* {#Gray} [[John W. Gray]], *Fibred and Cofibred Categories*, pp. 21-83 in: [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

Early development of the theory:

* {#Bénabou1975} [[Jean Bénabou]], _Fibrations petites et localement petites_, C. R. Acad. Sci. Paris **281** Série A (1975) 897-900 &lbrack;[gallica](http://gallica.bnf.fr/ark:/12148/bpt6k6228235m/f171.image#)&rbrack;

* {#Bénabou1985} [[Jean Bénabou]], *Fibered Categories and the Foundations of Naive Category Theory*,  The Journal of Symbolic Logic, Vol. **50** 1 (1985) 10-37 &lbrack;[doi:10.2307/2273784](http://dx.doi.org/10.2307/2273784)&rbrack;

reviewed in:

* {#Streicher18} [[Thomas Streicher]], _Fibred Categories &#224; la Jean Bénabou_,  &lbrack;[arXiv:1801.02927](https://arxiv.org/abs/1801.02927)&rbrack;


Further review with emphasis on [[descent]] and Grothendieck fibrations as incarnations of [[stacks]]:

*  [[Angelo Vistoli]], _Grothendieck topologies, fibered categories and descent theory_ &lbrack;[math.AG/0412512](http://arxiv.org/abs/math/0412512), [MR2223406](http://www.ams.org/mathscinet-getitem?mr=2223406)&rbrack;  in: Fantechi et al. (eds.), _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001)&rbrack;  

* [[Barbara Fantechi]], [[Lothar Göttsche]], [[Luc Illusie]], [[Steven L. Kleiman]], [[Nitin Nitsure]], [[Angelo Vistoli]], Chapter 3 of: _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. (2005) &lbrack;[MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001), [ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [lecture notes](http://indico.ictp.it/event/a0255/other-view?view=ictptimetable)&rbrack;

* {#Warner12} [[Garth Warner]]: *Fibrations and Sheaves*, EPrint Collection, University of Washington (2012) &lbrack;[hdl:1773/20977](http://hdl.handle.net/1773/20977), [pdf](https://sites.math.washington.edu//~warner/Warner_FIBRATIONS%20AND%20SHEAVES.pdf), [[Warner-FibrationsAndSheaves.pdf:file]]&rbrack;

Textbook accounts:

* [[Michael Barr]], [[Charles Wells]], Chapter 12 of: *Category Theory for Computing Science* , Prentice Hall 1995&#179;. ([TAC reprints no.22 (2012)](http://www.tac.mta.ca/tac/reprints/articles/22/tr22abs.html))

* [[Francis Borceux]], Chapter 8 of: *[[Handbook of Categorical Algebra]] vol. 2*, Cambridge UP 1994.

* {#Jacobs98} [[Bart Jacobs]], Chapters 1 and 9 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (in the context of [[categorical semantics of dependent types]])

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol.1, Oxford UP 2002. (Part B)

  > (beware that this uses the non-standard terms "prone" and "supine" for "cartesian" and "opcartesian" morphisms)

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Chapter 9 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

See also:

* André Joyal, *[[joyalscatlab:Grothendieck fibrations]]*

* Wikipedia, *[Fibered category](http://en.wikipedia.org/wiki/Fibred_category)*


On the [[2-category]] of fibrations and application to [[computer science]]:

* {#Hermida} [[Claudio Hermida]], *Some properties of $Fib$ as a fibred 2-category*, Journal of Pure and Applied Algebra **134** (1999) 83-109 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(97)00129-1">doi:10.1016/S0022-4049(97)00129-1</a>&rbrack;

* {#HermidaThesis} [[Claudio Hermida]], [PhD thesis, University of Edinburgh](https://era.ed.ac.uk/bitstream/handle/1842/14057/Hermida1993.Pdf)

A [[2-comonad]] characterizing Grothendieck fibrations:

* [[Jacopo Emmenegger]], [[Luca Mesiti]], [[Giuseppe Rosolini]], [[Thomas Streicher]], *A comonad for Grothendieck fibrations* &lbrack;[arXiv:2305.01474](https://arxiv.org/abs/2305.01474)&rbrack;

On the connection between Grothendieck fibrations and [[factorisation systems]] (see also [[stable factorisation system]]):

* J. Hughes and [[Bart Jacobs]], _Factorization systems and fibrations: Toward a fibred Birkhoff variety
theorem_, Electr. Notes in Theor. Comp. Sci., 69 (2002)

* [[Jiří Rosický ]], [[Walter Tholen]], _Factorization, fibration and torsion_, [arxiv/0801.0063](http://arxiv.org/abs/0801.0063), Journal of homotopy and Related Structures

* Miloslav Štěpán, _Factorization systems and double categories_, [arXiv:2305.06714](https://arxiv.org/abs/2305.06714).

See also:

* [[Ronnie Brown|R. Brown]], R. Sivera, _Algebraic colimit calculations in homotopy theory using fibred and cofibred categories_, TAC **22** (2009) pp.222-251. ([pdf](http://www.tac.mta.ca/tac/volumes/22/8/22-08.pdf))

[[!redirects Grothendieck fibrations]]
[[!redirects Grothendieck opfibration]]
[[!redirects Grothendieck cofibration]]
[[!redirects Grothendieck opfibrations]]
[[!redirects Grothendieck cofibrations]]
[[!redirects opfibration]]
[[!redirects opfibrations]]

[[!redirects fibered category]]
[[!redirects fibred category]]
[[!redirects fibered categories]]
[[!redirects fibred categories]]

[[!redirects cofibered category]]
[[!redirects cofibered categories]]

[[!redirects cofibred category]]
[[!redirects cofibred categories]]

[[!redirects (Grothendieck) fibration]]
[[!redirects (Grothendieck) fibrations]]


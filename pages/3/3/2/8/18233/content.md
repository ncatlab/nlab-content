# Displayed categories

* table of contents
{: toc}

## Idea

A **displayed category** over a [[category]] $C$ is the "classifying map" of a category over $C$.  That is, it is equivalent to the data of a category $D$ and a functor $F:D\to C$, but organized differently as a "functor" associating to each object or morphism of $C$ the [[fiber]] over it.  The operation (which is an [[equivalence]]) taking a displayed category to the corresponding functor $F:D\to C$ is a generalization of the [[Grothendieck construction]]. This Grothendieck construction is an instance of the [[T-Grothendieck construction]] where $T$ is the theory of categories.

Displayed categories are particularly useful in [[type theory]] (especially [[internal categories in homotopy type theory]]) and to preserve the [[principle of equivalence]], since they allow a more "category-theoretic" formulation of various notions (such as [[identity-on-objects]] and [[Grothendieck fibrations]] and strict [[creation of limits]]) that, if stated in terms of a functor $F:D\to C$, would involve equality of objects.

## Definitions

### By components

A **displayed category** $D$ over a category $C$ consists of

* for each object $a:C$, a type $D(a)$
* for each object $a:C$ and $b:C$, morphism $f:a \to b$, and element $x:D(a)$ and $y:D(b)$, a set of morphisms $Hom_f(x, y)$ from $x$ to $y$ over $f$
* for each object $a:C$ and element $x:D(a)$, a morphism $id_x:Hom_{id_a}(x, x)$
* for each object $a:C$, $b:C$, and $c:C$, morphism $f:a \to b$ and $g:b \to c$, and elements $x:D(a)$, $y:D(b)$, $z:D(c)$, a function: 
$$(-)\circ_{a, b, c, f, g, x, y, z}(-):Hom_g(y, z) \times Hom_f(x, y) \to Hom_{g \circ f}(x, z)$$
such that 
* for all morphisms $k:Hom_f(x, y)$, there is the dependent identification 
$$\lambda(k):id_y \circ k =_* k$$
* for all morphisms $k:Hom_f(x, y)$, there is the dependent identification 
$$\rho(k):k \circ id_x =_* k$$
* for all morphisms $k:Hom_f(x, y)$, $l:Hom_f(y, z)$, $m:Hom_f(z, w)$, 
$$(k \circ l) \circ m =_* k \circ (l \circ m)$$

...

### Abstract definition

A **displayed category** over a category $C$ is a [[lax functor]] from $C$, regarded as a bicategory with only identity 2-cells, to the [[bicategory]] [[Span]].

Better, it is a lax [[double functor]] from $C$, regarded as a [[double category]] "horizontally" with only identity vertical arrows and 2-cells, to the (pseudo) double category $Span$ with sets as objects, functions as vertical arrows, and spans as horizontal arrows.  Although this produces an equivalent notion, it is better because a **displayed functor** is then a [[vertical transformation]] between such lax double functors.

A displayed category may equivalently be described as a *[[normal lax functor|normal]]* lax functor from $C$ to [[Prof]] (either the bicategory or the double category, as appropriate), meaning one that strictly preserves identities.  Formally, this is because $Prof = Mod(Span)$, where $Mod(-)$ denotes the double category of horizontal monads and modules, and $Mod$ is a [[right adjoint]] to the inclusion of [[virtual double categories]] and [[normal lax functor|normal (lax) functors]] into all (lax) functors; see [(CS, Prop. 5.14)](#CS).

Equivalently, it is a [[double profunctor]] between $C$ and the terminal double category $1$, i.e., a double presheaf on $C$.

## Correspondence to slices

The category over $C$ corresponding to a displayed category $D:C\to Span$ is the pullback
$$ \array{ D & \to & Span_* \\ \downarrow & & \downarrow \\ C & \to & Span }$$
Where $Span_*=Span(Set_*)$ is the bicategory (or double category) of [[pointed sets]] and pointed spans.  This is a strict pullback, which exists in the 2-category of bicategories (or double categories) and lax functors because the projection $Span_* \to Span$ is not just lax but  strong.  Equivalently, it is the pullback
$$ \array{ D & \to & Prof_* \\ \downarrow & & \downarrow \\ C & \to & Prof }$$
where $Prof_*$ consists of pointed categories and pointed profunctors, a pointed profunctor $H:(A,a_0)&#8696;(B,b_0)$ being equipped with an element of $H(a_0,b_0)$.

This construction induces an [[equivalence of categories]] $Disp(C) \to Cat/C$, which restricts to the following equivalences:

* A displayed category factors through the inclusion $Set \hookrightarrow Span$ (or equivalently $Set \hookrightarrow Prof$) if and only if $F:D\to C$ is a [[discrete opfibration]].  Similarly, it factors through $Set^{op}$ if and only if $F$ is a discrete fibration.

* A factorization of a displayed category $C\to Prof$ through the inclusion $Cat^{op} \hookrightarrow Prof$ (as co[[representable profunctors]]) is equivalent to giving $F:D\to C$ the structure of a [[cloven fibration|cloven]] [[prefibred category]], i.e. equipped with a choice of weakly cartesian liftings.  The factorization is a [[pseudofunctor]] precisely when $F:D\to C$ is a [[Grothendieck fibration]]; in this case we see the usual [[Grothendieck construction]] of a pseudofunctor.

* Similarly, factorizations through $Cat\hookrightarrow Prof$ corresponds to cloven Grothendieck (pre)opfibrations.

* An arbitrary displayed category $C\to Prof$ is a pseudofunctor if and only if $F:D\to C$ is a [[Conduché functor]], i.e. an exponentiable morphism in $Cat$.

### The construction, explicitly
As mentioned above, there is a construction $\int$ turning a normal lax functor $F:C \to Prof$ into a functor $\pi_F : \int F \to C$. Here we spell it out.

But first, let us explictly remark how the opposite construction works. Using notation from [Benaboù's lectures](#Benabou), the normal lax functor $dP : C \to Prof$ associated to a functor $P:E \to C$ is obtained by 'taking fibers'. On objects, it maps $x:C$ to the category $P^{-1}x$ of objects and maps of $E$ mapping to $x$ and its identity arrow, respectively. On morphisms, it maps an arrow $f:x \to y$ to the profunctor $P^{-1}y^{op} \times P^{-1}x \to Set$ mapping a choice of objects $y'$ and $x'$ 'lifting' $y$ and $x$ respectively to the set of maps $f^\sharp : x'\to y'$ that project down to $f$, i.e.~the 'fiber over $f$' of the arrow part of $P$ (which is defined given two objects).

#### The generalized Grothendieck construction
The category $\int F$ is built as follows:

* objects are pairs $(x:C, x' : Fx)$

* a morphism $(x,x') \to (y,y')$ is given by a pair of morphisms $(f,f^\sharp)$ where $f:x \to y$ is an arrow in $C$ and $f^\sharp \in Ff(y',x')$

* identities are given by picking $1_x : x \to x$ and $1_x^\sharp = 1_{x'} \in F(1_x)(x',x') = \mathrm{Hom}_{Fx}(x',x')$

* composition is defined componentwise: given $(f,f^\sharp) : (x,x') \to (y,y')$ and $(g,g^\sharp):(y,y') \to (z,z')$, the composite is the pair $(gf, \ell_{f,g}(y', f^\sharp, g^\sharp))$, where $(y', f^\sharp, g^\sharp)$ is the equivalence class of the coend defining the composition $Fg \circ Ff$ (see [[profunctor]]) and $\ell_{f,g}$ is the laxator of $F$.

Finally, the functor $\pi_F$ simply discards the second component on objects and morphisms.

One can readily observe how this construction reduces to the usual [[Grothendieck construction]] when $F$ factors through $Cat$.

##### On morphisms
The above construction is functorial and turns 'morphisms of normal lax functors into $Prof$' into morphisms in $Cat/C$.
To describe this, is useful to notice the category of normal lax functors into Prof is given by $Dbl_{normal,lax}^{vertical}(hC, Cat)$, where $hC$ is the casting of $C$, a category, as a double category whose vertical and 2-cells are all trivial.

This category has as objects normal lax [[double functors]] $C \to Cat$, where $Cat$ is the [[proarrow equipment]] of categories, functors (in the vertical/tight direction), profunctors (in the horizontal/loose direction) and suitable natural transformations as 2-cells. The morphisms are then [[vertical natural transformations]] between them.

Let's spell out the definition of one of these vertical natural transformations $\phi : F \Rightarrow G$. Its components are given by functors (i.e. vertical cells in $Cat$) $\phi_x : Fx \to Gx$, indexed by objects $x:C$, and squares

\begin{centre}
\begin{tikzcd}[ampersand replacement=\&,sep=scriptsize]
	Fx \&\& Fy \\
	\\
	Gx \&\& Gy
	\arrow["Ff", "\shortmid"{marking}, from=1-1, to=1-3]
	\arrow["Gf"', "\shortmid"{marking}, from=3-1, to=3-3]
	\arrow["{\phi_x}"', from=1-1, to=3-1]
	\arrow["{\phi_y}", from=1-3, to=3-3]
	\arrow["{\mathrm{st}^\phi}"{description}, shorten <=11pt, shorten >=11pt, Rightarrow, from=1-3, to=3-1]
\end{tikzcd}
\end{centre}

indexed by morphisms $f:x\to y$ in $C$. These have, moreover, to satisfy various 'natural' conditions of compatibility with horizontal composition of squares in $Cat$ and so on.

The equivalence $\int$ converts this data back to a commutative triangle
\begin{centre}
\begin{tikzcd}[ampersand replacement=\&,row sep=scriptsize]
	{\int F} \&\& {\int G} \\
	\& C
	\arrow["{\pi_F}"', from=1-1, to=2-2]
	\arrow["{\pi_G}", from=1-3, to=2-2]
	\arrow["{\int \phi}", from=1-1, to=1-3]
\end{tikzcd}
\end{centre}

The crucial thing to notice here is that, fundamentally, such a functor over $C$ is defined 'fiberwise', in the sense that, choosen an object $x:C$, $\int \phi$ has to restrict to a functor $\int\phi_x : \pi_F^{-1}x \to \pi_G^{-1}x$. But these categories are, by definition, $Fx$ and $Gx$, so that $\int \phi_x$ can be naturally defined to be $\phi_x$ itself.

Now what's left to define is the action of $\int \phi$ on those arrows that cross fibers (in a sense, all the arrows except those that map to identities in $C$ -- or, put differently again, the above discussion pinned down the object part of $\int \phi$).

Thus let $(f,f^\sharp):(x,x') \to (y,y')$ be a morphism in $\int F$. We know how to map $(x,x')$ and $(y,y')$ using $\phi_x$ and $\phi_y$ respectively, so that $\int \phi(f,f^\sharp)$ has to be an arrow $(x,\phi_x(x')) \to (y,\phi_y(y'))$.
The exact arrow is picked by the last piece of data from the vertical transformation $\phi$, the 'strength' $\mathrm{st}^{\phi}$. In fact this is a natural transformation whose components are $\mathrm{st}^{\phi}_{x',y'} : Ff(x',y') \to Gf(\phi_x(x'),\phi_y(y'))$, which is exactly the data needed to define the arrow part of $\int \phi$.

Functoriality of $\int \phi$ is a direct consequence of the properties required to $\phi$, which are spelled out at [[vertical natural transformation]].

## Properties of functors through properties of the reindexing

Let $F:E \to B$ be a functor, call $dF : B^{op} \to Prof$ the associated lax normal functor.
By requiring a different degree of laxity to $dF$ or which subcategory of $Prof$ it hits, we can express different properties of $F$:

1. If $dF$ is a pseudofunctor, then $F$ is a [[Conduché fibration]], i.e. an exponential morphism in $Cat$
2. If $dF$ factors through the inclusion $Cat \to Prof$, then $F$ is a [[prefibration]]
3. If $dF$ is both Conduché and a prefibration, then $F$ is a [[Grothendieck fibration]]
4. Call *partial functor* a profunctor $\phi : X \to Psh(Y)$ that factors through $(y,0) : Y + 1 \to Psh(Y)$, which is the Yoneda embedding on $Y$ and picks the empty presheaf otherwise. When $dF$ factors through the subcategory of partial functors it is called a [[foliated category|foliation]].

These and more examples are discussed in [Benabou](#Benabou).

## References

The correspondence between categories over $C$ and [[normal lax functors]] $C\to Prof$ was observed by [[Jean Benabou|B&#233;nabou]] already in 1972:

* [[Jean Benabou|Jean B&#233;nabou]], *2-dimensional limits and colimits of distributors (or how to glue together categories)*, [[Oberwolfach]] 'Tagungsbericht', 1972, [(web)](https://oda.mfo.de/handle/mfo/1575)

A more detailed account of Benabou's work on this topic can be found at:

* {#Benabou} Jean B&#233;nabou, *Distributors at work*, Notes by Thomas Streicher from lectures given at TU Darmstadt, 2000, [pdf](http://www.mathematik.tu-darmstadt.de/~streicher/FIBR/DiWo.pdf)

* [[Graham Manuell]], _Monoid extensions and the Grothendieck construction_, Semigroup Forum **105** (2022) 488–507 &lbrack;[doi:10.1007/s00233-022-10294-2](https://doi.org/10.1007/s00233-022-10294-2)&rbrack;

The term "displayed category", and the applications to type theory, are due to:

* [[Benedikt Ahrens]], [[Peter LeFanu Lumsdaine]], _Displayed Categories_, Logical Methods in Computer Science **15** 1, (2019) &lbrack;<a href="https://doi.org/10.23638/LMCS-15(1:20)2019">doi:10.23638/LMCS-15(1:20)2019</a>, [arXiv:1705.04296](https://arxiv.org/abs/1705.04296)&rbrack; 

An unpacking of the definition as lax functors into [[Span]] is in 2.2 of

* [[Duško Pavlović]], [[Samson Abramsky]], _Specifying Interaction Categories_, Lecture Notes in Computer Science **1290** (1997) 147–158. &lbrack;[doi:10.1007/BFb0026986](https://doi.org/10.1007/BFb0026986)&rbrack;

Also cited above:

* {#CS} [[Geoff Cruttwell]], [[Mike Shulman]], _A unified framework for generalized multicategories_, Theory and Applications of Categories **24** 21 (2010) 580-655.  &lbrack;[TAC](http://tac.mta.ca/tac/volumes/24/21/24-21abs.html)&rbrack;

[[!redirects displayed categories]]
[[!redirects displayed functor]]
[[!redirects displayed functors]]

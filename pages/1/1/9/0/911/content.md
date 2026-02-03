
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
* table of contents
{:toc}

## Idea

The _category of elements_ of a [[functor]] $F \colon \mathcal{C} \to \mathbf{Set}$ is a [[category]] $p \colon el(F) \to \mathcal{C}$ sitting over the [[domain]] [[category]] $\mathcal{C}$, such that the [[fiber]] over an [[object]] $c \in \mathcal{C}$ is the set $F(c)$. Or more precisely, the discrete category $\text{disc}(F(c))$. 

This is a special case of the [[Grothendieck construction]] for [[covariant functors]], by considering sets as discrete categories.  There is a similar special case of the Grothendieck construction for [[contravariant functors]] which takes a functor $F:\mathcal{C}^{op} \to \mathrm{Set}$ to a category over $\mathcal{C}$. In fact, there is a common construction which generalises these, the so-called **two-sided category of elements** for a [[profunctor]], which we will discuss later in this article.

We may think of [[Set]] as the [[classifying space]] of "[[Set]]-bundles;" see [[generalized universal bundle]].  The category of elements of $F$ is, in this sense, the [[Set]]-bundle classified by $F$.  It comes equipped with a projection to $\mathcal{C}$ which is a [[discrete opfibration]], and provides an equivalence between $\mathbf{Set}$-valued functors and discrete opfibrations. There is a dual category of elements that applies to contravariant $\mathbf{Set}$-valued functors, i.e. [[presheaves]], and produces [[discrete fibrations]]. And the two-sided version applies to profunctors, producing [[two-sided fibration|two-sided fibrations]].

Forming a category of elements can be thought of as "unpacking" a [[concrete category]]. For example, consider a concrete category $\mathcal{C}$ consisting of two objects $X,Y$ and two non-trivial morphisms $f,g$

<img src="http://ncatlab.org/nlab/files/explode.jpg" width = "275"/>

The individual elements of $X,Y$ are "unpacked" and become objects of the new category. The "unpacked" morphisms are inherited in the obvious way from morphisms of $\mathcal{C}$.

Note that an "unpacked" category of elements can be "repackaged".

<img src="http://ncatlab.org/nlab/files/implode.jpg" width = "275"/>

The generalization of the category of elements for functors landing in [[Cat]], rather than just $\mathbf{Set}$, is called the [[Grothendieck construction]].


## Definition

### For covariant Set-valued functors

Given a functor $F \colon \mathcal{C} \to \mathbf{Set}$, the **category of elements** $el(F)$ or $El_F(\mathcal{C})$ (or obvious variations) may be understood in any of these equivalent ways:

* It is the [[category]] whose objects are pairs $(c,x)$ where $c$ is an object in $\mathcal{C}$ and $x$ is an element in $F(c)$ and morphisms $(c,x) \to (c',x')$ are morphisms $u \colon c \to c'$ such that $F(u)(x) = x'$.

* It is the [[pullback]] along $F$ of the [[generalized universal bundle|universal Set-bundle]] $U : \mathbf{Set}_* \to \mathbf{Set}$

 
   where $U$ is the [[forgetful functor]] from [[pointed set|pointed sets]] to sets.

* It is the [[comma category]] $(*/F)$, where $*$ is the inclusion of the one-point set $* \colon  * \to \mathbf{Set}$ and $F \colon \mathcal{C} \to \mathbf{Set}$ is itself:

\begin{center}
\begin{tikzcd}
  \text{El}_F(\mathcal{C})
  \arrow[r, ""]
  \arrow[d, "\pi_F"]
  & \mathbf{Set}_*
  \arrow[d, "U"]
\\
  \mathcal{C}
  \arrow[r, ""]
  & \mathbf{Set}
\end{tikzcd}
\end{center}

* Its [[opposite category|opposite]] is the [[comma category]] $(Y/F)$, where $Y$ is the [[Yoneda embedding]] $\mathcal{C}^{op}\to [\mathcal{C},\mathbf{Set}]$ and $F$ is the functor $*\to [\mathcal{C},\mathbf{Set}]$ which picks out $F$ itself:

\begin{center}
\begin{tikzcd}
  \text{El}_F(\mathcal{C})^{op}
  \arrow[r, "\pi_F^{op}"]
  \arrow[d, ""]
  & \mathcal{C}^{op}
  \arrow[d, "U"]
\\
  *
 \arrow[r, "F"]
  & {[\mathcal{C}, \mathbf{Set}]}
\end{tikzcd}
\end{center}

  $El_F(\mathcal{C})$ is also often written with [[end|coend]] notation as $\int^\mathcal{C} F$, $\int^{c: \mathcal{C}} F(c)$, or $\int^c F(c)$.  This suggests the fact the set of objects of the category of elements is the [[disjoint union]] (sum) of all of the sets $F(c)$.

* It is the (strict) [[oplax colimit]] of the composite $\mathcal{C} \xrightarrow{F} \mathbf{Set} \xrightarrow{disc} \mathbf{Cat}$; see [[Grothendieck construction]].

When $\mathcal{C}$ is a [[concrete category]] and the functor $F:\mathcal{C}\to \mathbf{Set}$ is simply the [[forgetful functor]], we can define a functor

$$
  Explode(-) \coloneqq El_F(-)
  \,.
$$

This is intended to illustrate the concept that constructing a category of elements is like "unpacking" or "exploding" a category into its elements.

### For Profunctors

Applying the above construction to a presheaf $P \colon \mathcal{C}^{op} \to \mathbf{Set}$ produces a category $el(P)$ with a projection $\pi \colon el(P) \to \mathcal{C}^{op}$. However, the _true_ category of elements for a presheaf is normally taken to have a projection into $\mathcal{C}$ itself - this can be accomplished by taking the [[opposite category]], producing $\pi^{op} \colon el(P)^{op} \to \mathcal{C}$. In fact, both the covariant and contravariant constructions are special cases of the _category of elements of a profunctor_, whose construction we now outline.

Take a profunctor $P$, viewed as a functor $\mathcal{C}^{op} \times \mathcal{D} \to \mathbf{Set}$. For $c \in \mathcal{C}, d \in \mathcal{D}$, we can view the elements $\alpha \in P(c, d)$ as [[heteromorphism|heteromorphisms]] $\alpha \colon c \nrightarrow d$. The action of the profunctor can be encoded in a "composition" operation of these heteromorphisms with ordinary morphisms, defining $g \circ \alpha \circ f \colon c' \nrightarrow d' := P(f, g)(\alpha)$ for $f \colon c' \to c$ and $g \colon d \to d'$. The unit and associativity laws for this composition operation encode the fact that $P$ preserves identities and composites.

This gives a nice visual picture for the category of elements of $P$ - it is a "heteromorphic [[arrow category]]"! More precisely, it is the category whose objects are triples $(c, d, \alpha)$ for $c \in \mathcal{C}, d \in \mathcal{D}, \alpha \in P(c, d)$, and whose morphisms $(c, d, \alpha) \to (c', d', \alpha')$ are pairs $f \colon c \to c', g \colon d \to d'$ with $g \circ \alpha = \alpha' \circ f$. Much like the arrow category, this has a projection functor $\pi \colon el(P) \to \mathcal{C} \times \mathcal{D}$ that is a [[two-sided fibration]].

We also have a [[coend]] formula for this category:

$$el(P) \cong \int^{c, d} P(c, d) \times \mathcal{C} / c \times d / \mathcal{D}$$

, where $\mathcal{C}/c$ is a [[slice category]] and $d / \mathcal{D}$ is a [[under category|coslice category]].

The category of elements of a set-valued functor $F \colon \mathcal{C} \to \mathbf{Set}$ and of a presheaf $G \colon \mathcal{C}^{op} \to \mathbf{Set}$ then arise as categories of elements of the profunctors $\mathbf{1}^{op} \times \mathcal{C} \to \mathbf{Set}$ and $\mathcal{C}^{op} \times \mathbf{1} \to \mathbf{Set}$ respectively, where $\mathbf{1}$ is the [[terminal category]].



## Properties

The category of elements defines a functor $el \colon \mathbf{Set}^{\mathcal{C}^{op} \times \mathcal{D} } \to \mathbf{Cat}$.  This is perhaps most obvious when viewing it as an oplax colimit.  Furthermore we have:

\begin{remark}
  \label{ColimitPreserving}
  The functor $el \colon \mathbf{Set}^{\mathcal{C}^{op} \times \mathcal{D} } \to \mathbf{Cat}$ is [[cocontinuous functor|cocontinuous]].
\end{remark}

It's easiest to prove this by showing that, in fact, it has a right adjoint:

\begin{theorem}
  \label{ColimitPreserving2}
  The functor $el \colon \mathbf{Set}^{\mathcal{C}^{op} \times \mathcal{D} } \to \mathbf{Cat}$ has a right adjoint.
\end{theorem}

\begin{proof}
  By a simple coend computation:
$$
\begin{aligned}
\mathbf{Cat}(el(P), E) &\cong \mathbf{Cat}\left( \int^{c, d} \delta(P(c, d)) \times \mathcal{C}/c \times d/\mathcal{D}, E \right) \\
&\cong \int_{c, d} \mathbf{Cat} \big ( \delta(P(c, d)) \times \mathcal{C}/c \times d /\mathcal{D}, E \big) \\
&\cong \int_{c, d} \mathbf{Set} \big ( P(c, d), [\mathcal{C}/c \times d/\mathcal{D}, E]_0 \big) \\
&\cong \mathbf{Set}^{\mathcal{C}^{op} \times \mathcal{D} }(P, K(E))
\end{aligned}
$$
  where $K(E) \colon (c, d) \mapsto [\mathcal{C}/c \times d/\mathcal{D}, E]_0$, sending a pair $(c, d)$ to the set of objects of the functor category $[\mathcal{C}/c \times d/\mathcal{D}, E]$.
\end{proof}

Now for any $\mathcal{C}, \mathcal{D}$, the terminal object of $\mathbf{Set}^{\mathcal{C}^{op} \times \mathcal{D}}$ is the functor $\Delta 1$ constant at the [[point]].  The category of elements of $\Delta 1$ is easily seen to be just $\mathcal{C} \times \mathcal{D}$ itself, so the unique transformation $P \to \Delta 1$ induces a _projection functor_ $\pi_P: el(P) \to \mathcal{C} \times \mathcal{D}$ defined by $(c,d,\alpha)\mapsto (c, d)$ and $(f, g) \mapsto (f, g)$.  The projection functor is a [[two-sided fibration]], and can be viewed also as a $\mathcal{C}^{op} \times \mathcal{D}$-indexed [[family of sets]].  When we regard $\el(P)$ as equipped with $\pi_P$, we have an embedding of $\mathbf{Set}^{\mathcal{C}^{op} \times \mathcal{D} }$ into $\mathbf{Cat}/(\mathcal{C} \times \mathcal{D})$.

Note that the canonical projection $el(P) \to \mathcal{C} \times \mathcal{D}$ is not usually [[full functor|full]]. For example, let $\mathbf{B}\mathbb{N}$ be the one-object category which carries the monoid $(\mathbb{N}, +)$ as its endomorphism monoid, and let $F$ be the action of $(\mathbb{N}, +)$ on the set $\mathbb{N}$ by $n.m = m + n$. Then the image of any hom-set between $k, k'$ is a subsingleton subset of $\mathbb{N}$.

More generally, the [[universal covering groupoid]] of a groupoid is just the category of elements of its action on itself by composition. Since this action is faithful and transitive,  hom-sets in the category of elements are always $0$ or $1$, while objects in the groupoid might have nontrivial automorphism groups.

Categories of elements of set-valued functors and presheaves have a close tie to representability:

\begin{proposition}
The category of elements of $F$ has an [[initial object]] if and only if $F$ is a [[representable functor]]. In this case, if the initial object is $(i \in F(x))$, then $F$ is isomorphic to the functor $\hom(x,-)$. 
\end{proposition}

## Examples

### Representable Presheaves

Let $Y(c):\mathcal{C}^{op}\to \mathbf{Set}$ be a [[representable functor|representable presheaf]] with $Y(c)(d)=Hom_{\mathcal{C}}(d,c)$. Consider the contravariant category of elements $\int_\mathcal{C} Y(c)$ . This has objects $(d_1,p_1)$ with $p_1\in Y(c)(d_1)$, hence $p_1$ is just an arrow $d_1\to c$ in $\mathcal{C}$. A map from $(d_1, p_1)$ to $(d_2, p_2)$ is just a map $u:d_1\to d_2$ such that $p_2\circ u =p_1$ but this is just a morphism from $p_1$ to $p_2$ in the [[overcategory|slice category]] $\mathcal{C}/c$. Accordingly we see that $\int_\mathcal{C} Y(c)\simeq \mathcal{C}/c$ .

This equivalence comes in handy when one wants to compute [[category of presheaves|slices of presheaf toposes]] over representable presheaves $Y(c)$ since $PSh(\int_\mathcal{C} F) \simeq PSh(\mathcal{C})/F$ in general for presheaves $F:\mathcal{C}^{op}\to \mathbf{Set}$ , whence $PSh(\mathcal{C})/Y(c) \simeq PSh(\mathcal{C}/c)$ . An instructive example of this construction is spelled out in detail at [[hypergraph]].

### Action Groupoid

In the case that $\mathcal{C} = \mathbf{B}G$ is the [[delooping]] [[groupoid]] of a [[group]] $G$, a functor $\varrho : \mathbf{B}G \to \mathbf{Set}$ is a [[permutation representation]] $X$ of $G$ and its category of elements is the corresponding [[action groupoid]] $X/\!/G$.
+-- {: .proof}
###### Proof
This is easily seen in terms of the characterization $el(\varrho)\cong (*/\varrho)$, the category having as objects triples $(*,*; *\to \varrho(*)=X)$, namely elements of the set $X=\varrho(*)$, and as arrows $x\to y$ those $g\in \mathbf{B}G$ such that
\begin{center}
\begin{tikzcd}
  *
  \arrow[r, "x"]
  \arrow[d, "1"]
  & X
  \arrow[d, "g"]
\\
  *
  \arrow[r, "y"]
  & X
\end{tikzcd}
\end{center}
commutes, namely $g . x=\varrho(g)(x)=y$. We can also present the right adjoint to $el(-)$: one must consider the functor $J\colon \mathbf{B}G^{op}\to \mathbf{Cat}$, which represents $G$ in $\mathbf{Cat}$, and sends the unique object $*\in \mathbf{B}G$ to $*/\mathbf{B}G\cong G/\!/G$, the _left_ action groupoid of $G$. The functor $J$ sends $h\in G$ to an automorphism of $G/\!/G$, obtained multiplying _on the right_ $x\to g x$ to $x h\to x g h$.

Now for any category $D$, $K( D)(*)$ is exactly the set of functors $[G/\!/G, D]$, which inherits from $G/\!/G$ an obvious action: given $F\in [G/\!/G,  D]$ we define $F^h=J(h)^*F=F \circ J(h) \colon g \mapsto F(g h)$.
=--
### Category of simplices

For a [[simplicial set]] regarded as a [[presheaf]] on the [[simplex category]], the corresponding category of elements is called its _[[category of simplices]]_. See there for more. As we have suggested at the beginning of this article, the category of elements of a covariant functor is defined differently than the category of elements of a presheaf, so the [[category of simplices]] is not an instance of the definition given above.

### Categories of cones

Let $J \colon I \to C$ be a [[diagram]]. Then we can define a presheaf $Cone_J \colon C^{op} \to \mathbf{Set}$ mapping $c \in C$ to the set of [[cone|cones]] over $J$ with tip $c$, with the functorial action given by precomposition of cone morphisms. The category of elements of this presheaf is precisely the category of cones over $J$! Thus, we observe that this presheaf is representable if and only if the category of cones has a terminal object - or, in more familiar terms, $J$ has a limit if and only if there exists a _universal_ cone.

### Comma Categories

Let $F \colon C \to E$ and $G \colon D \to E$ be functors. We can form a profunctor $P \colon C^{op} \times D \to \mathbf{Set}$ by defining $P(c, d) := E(F(c), G(d))$, the set of morphisms in $E$ between $F(c)$ and $G(d)$. We can use the functorial actions of $F$ and $G$ to "compose" these heteromorphisms with ordinary morphisms $f \colon c' \to c, g \colon d \to d'$, sending $\alpha \colon F(c) \to G(d)$ to $G(g) \circ \alpha \circ F(f) \colon F(c') \to G(d')$, which defines the action of $P$ on morphisms.

Then, the category of elements of this profunctor is precisely the [[comma category]] $F \downarrow G$! Which has a projection functor $\pi_P \colon el(P) \to C \times D$ that forms a [[two-sided fibration]].

As a special case, taking the category of elements of $Hom : C^{op} \times C \to \mathbf{Set}$, viewed as a profunctor from $C$ to $C$, produces the familiar [[arrow category]]. On the other hand, if we simply apply the ordinary "covariant" category of elements construction to produce a category with a projection to $C^{op} \times C$, we obtain the [[twisted arrow category]].

This illustrates an important general point - when taking the category of elements of a functor, it's not enough to simply specify the domain. We need to specify it as a profunctor with chosen domain and codomain categories, so that the resulting heteromorphisms have the desired domain and codomain, and we get the correct kind of projection.

## Related concepts

* [[Grothendieck construction]]

* [[graph of a profunctor]]

* [[2-Grothendieck construction]], [[2-category of elements]]

* [[(∞,1)-Grothendieck construction]]

* [[semi-direct product]]

## Reference

A very nice introduction emphasizing the connections to [[monoid|monoid theory]] is ch. 12 of

* [[Michael Barr]], [[Charles Wells]], _Category Theory for Computing Science_ , Prentice Hall 1995&#179;. ([TAC reprints no.22 (2012)](http://www.tac.mta.ca/tac/reprints/articles/22/tr22abs.html))

[[!redirects Exploding a Category]]
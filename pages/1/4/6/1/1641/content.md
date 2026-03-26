
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents


> **Terminology warning.** Here the term *topological category* is understood in a tradition motivated by examples of [[concrete categories]] in [[topology]] and does *not* refer to [[internal category|categories internal to]] or [[enriched category|enriched in]] in [[Top]] (cf. *[[topologically enriched category]]* instead).  The term *[[topological groupoid]]* (which *is* an [[internal groupoid]] in [[Top]]) is not taken by this tradition; indeed, the only groupoid that is a topological category over $Set$, in the sense used here, is [[terminal category|trivial]].  On the other hand, there is use of the term 'topological functor', which  we tend to avoid other than below.


## Idea

A _topological category_ is a [[concrete category]] with nice features matching the ability to form [[weak topology|weak]] and [[strong topology|strong]] [[topologies]] in [[Top]].


## Definition

The following definition \ref{TheDefinition} relates to a [[functor]] $U\colon C \to D$ (such as the [[forgetful functor]] from $Top$ to [[Set]]), which one may think of as exhibiting $C$ as a [[bundle]] over $D$. 

Sometimes, when $D =$ [[Set]], the category $C$ satisfying the properties described below is called a _topological construct_ [Preuss 2002](#Preuss2002). Usually $C$ and $D$ will be [[large categories]].

In this context one also says:

* _spaces_ for the [[objects]] of $C$, 

* _algebras_ for the [[objects]] of $D$,  

* _maps_ for the [[morphism]] in $C$, 

* _homomorphisms_ for the [[morphisms]] in $D$. 

This alludes to the typical example situation where $C$ is a category of [[spaces]] with some kind of [[topological space|topological]] [[structure]] while $D$ is, if not [[Set]] then some kind of algebraic category.

We now first state the default definition (Def. \ref{TheDefinition}) and then comment on some variants (Rem. \ref{AmnesticVersion} and Rem. \ref{WeakVersion}).

\begin{definition}\label{TheDefinition}
Given a [[functor]] $U \colon C \longrightarrow D$, it exhibits its [[domain]] [[category]] $C$ as a __topological category__ over $D$ if, given 

1. any [[object]] $X \in D$ (an "algebra") 

1. any (possibly [[large set|large]]) [[indexed set]] $\big\{S_i \in C\big\}_{i \in I}$ (of "spaces") 

1. [[homomorphisms]] $f_i \colon X \to U(S_i)$ (that is, a "$U$-structured [[sink|source]] from $X$"), 

then there exists an [[initial lift]] (think: "smallest topology rendering the $f_i$ continuous"), which is to say

1. a "space" $T \in C$ such that $U(T) = X$, and maps $m_i \colon T \to S_i$ such that $U(m_i) = f_i$, 

1. given any space $T'$, homomorphism $g'\colon U(T') \to X$, and maps $m'_i\colon T' \to S_i$, if each [[composition|composite]] $f_i \circ g$ equals $U(m'_i)$, then there exists a unique map $n\colon T' \to T$ such that $U(n) = g'$ and $m_i \circ n = m'_i$:

\begin{tikzcd}
  T'
  \ar[
    dd, dashed, "{ \exists!\, n }"{swap}
  ] 
  \ar[
    ddr, "{ m'_i }"
  ]
  && & 
  U(T')
  \ar[
    dd, "{ U(n) }"{swap}
  ] 
  \ar[
    ddr, "{ g' }"
  ]
  \ar[
    ddrr, "{ U(m'_i) }"
  ]
  &[-50pt]
  \\
  && \mapsto
  \\
  T
  \ar[
    r, "{ m_i }"{swap}
  ]
  &
  S_i
  &&
  U(T)
  \ar[
    rr, bend right=20, "{ U(m_i) }"{swap}
  ]
  \ar[r, equals]
  & 
  X
  \ar[r, "{ f_i }"]
  &
  U(S_i)
  \mathrlap{\,.}
\end{tikzcd}

\end{definition}


The conditions in Def. \ref{TheDefinition} imply the following crucial further property (which is often included as an assumption in the definition, in which case the uniqueness of $n$ can be left out):

\begin{proposition}\label{FaithfulnessIsImplies}
  If a functor $U\colon C \to D$ exhibits a topological category in the sense of Def. \ref{TheDefinition}, then it is [[faithful functor|faithful]] and in this sense exhibits $C$ as a *[[concrete category]]* over $D$.
\end{proposition}
\begin{proof}
  See Theorem 21.3 of [Adámek, Herrlich & Strecker 1990](#AdámekHerrlichStrecker90). \end{proof}

Thus we may think of objects of a topological category $C$ as objects of $D$ equipped with [[extra structure]]. The idea is then that $T$ is $X$ equipped with the __initial structure__ or __[[weak structure]]__ determined by the requirement that the homomorphisms $f_i$ be structure-preserving maps.

The following says that the notion is "self-[[formal duality|dual]]":

\begin{proposition}\label{SelfDuality}
A functor $U\colon C \to D$ is topological, in the sense of Def. \ref{TheDefinition}, if and only if the [[opposite functor]] $U^op\colon C^op \to D^op$ is so.  
\end{proposition}

(This may be understood as a [[categorification]] of the theorem that any complete [[semilattice]] is a [[complete lattice]].)

Thus, every topological category also has __final__ (not usually called _terminal_) or __[[strong structure|strong]]__ structures, each determined by a family of homomorphisms $f_i\colon U(S_i) \to X$ (a $U$-structured [[sink]] to $X$).

\begin{remark}
Both of these results (faithfulness, Prop. \ref{FaithfulnessIsImplies}, and self-duality, Prop. \ref{SelfDuality}) depend on the assumption in Def. \ref{TheDefinition} that the family $\{S_i\}$ is allowed to be *[[large]]*. 

Otherwise, there exists [[counterexamples]]: For instance, if $C$ is a [[large category]] with all (small) [[products]], then the functor $C \to 1$ to the [[terminal category]] satisfies the lifting property in Def. \ref{TheDefinition} for small families $\{S_i\}$.  However, it need not satisfy the dual property (unless $C$ also has all small coproducts) nor need it be faithful.
\end{remark}

It also follows that:

\begin{proposition}\label{GrothendieckFibrancyImplies}
If $U \colon C \longrightarrow D$ exhibits a topological category (Def. \ref{TheDefinition}), then $U$ is a [[Grothendieck fibration]] and an [[opfibration]].
\end{proposition}



\begin{remark}\label{AmnesticVersion}
**(amnestic version)**
Since initial lifts have a [[universal property]], they are unique up to unique [[isomorphism]].  However, some authors (such as [AHS90](#AdámekHerrlichStrecker90)) ask that they be literally unique. This is tantamount to deciding that $U$ should be an [[amnestic functor]].  A drawback (from an [[nPOV]]) is that this condition violates the [[principle of equivalence]], and arguably doesn't add anything mathematically important.

Thus, although it occurs in the literature, here we will consider it purely optional. (It is possible that some results recorded here about topological categories will depend on this assumption, but only results not respecting the [[principle of equivalence]] could be affected.)
\end{remark}


\begin{remark}\label{WeakVersion}
**(weak version)**
\linebreak
On the other hand, the default definition \ref{TheDefinition} does already refer to [[equality]] of objects in the condition $U(T) = X$; thus as stated it *already* violates the [[principle of equivalence]], just as the notion of [[Grothendieck fibration]] does.  But (also as for Grothendieck fibrations) this other use of equality of objects is really more of a "[[type|typing]] [[judgment]]", which can be made precise by working with [[displayed categories]] instead.  (In the context of [[homotopy type theory]], the amnestic condition is equivalent to "fiberwise [[internal category in homotopy type theory|univalence]]".)

However, if we want to, we can also formulate a "fully isomorphism-invariant" version of the definition, corresponding to the weakened bicategorical notion of [[Street fibration]].  In this case, an initial lift consists of:

* a space $T$, an [[isomorphism]] $g\colon U(T) \to X$, and maps $m_i\colon T \to S_i$ such that $f_i \circ g = U(m_i)$ for all $i \in I$ and,

* given any space $T'$, homomorphism $g'\colon U(T') \to X$, and maps $m'_i\colon T' \to S_i$, if $f_i \circ g' = U(m'_i)$ for all $i \in I$, then there exists a unique map $n\colon T' \to T$ such that $g \circ U(n) = g'$ and $m_i \circ n = m'_i$:

\begin{tikzcd}
  T'
  \ar[
    dd, dashed, "{ \exists!\, n }"{swap}
  ] 
  \ar[
    ddr, "{ m'_i }"
  ]
  && & 
  U(T')
  \ar[
    dd, "{ U(n) }"{swap}
  ] 
  \ar[
    ddr, "{ g' }"
  ]
  \ar[
    ddrr, "{ U(m'_i) }"
  ]
  &[-50pt]
  \\
  && \mapsto
  \\
  T
  \ar[
    r, "{ m_i }"{swap}
  ]
  &
  S_i
  &&
  U(T)
  \ar[
    rr, bend right=20, "{ U(m_i) }"{swap}
  ]
  \ar[r, shorten=-4pt, "{ \sim }"{swap}, "{ g }"]
  & 
  X
  \ar[r, "{ f_i }"]
  &
  U(S_i)
  \mathrlap{\,.}
\end{tikzcd}


\end{remark}


## Examples

*  The name 'topological category' comes from these examples from point-set [[topology]]; these are all topological over [[Set]]:

   *  the category [[Top]] of [[topological spaces]],

   *  the category of [[convergence spaces]] (or of [[pseudotopological space|pseudotopological]] or of [[pretopological space|pretopological]] spaces),

   *  the category of [[uniform spaces]] or of [[Cauchy spaces]],

   *  lots more in this vein.

*  In contrast, the category of [[locales]] is *not* topological over $Set$; not even the category of *spatial* locales (equivalent to the category of [[sober spaces]]) is topological, essentially because soberification of a topological space may not preserve the underlying set.

*  Also, the category [[Diff]] of [[smooth manifolds]] is not topological but most categories of [[generalized smooth space]]s are.

*  Outside of topology, the category of [[measurable spaces]] is topological over $Set$.

* The category [[PreOrd]] of [[preordered sets]] (equivalent to the category of [[Alexandroff topology|Alexandroff spaces]]) is topological over $Set$.  Given a family of preordered sets $\{(S_i, \prec_i)\}$ and a family of $\{f_i \colon X \to S_i\}$, the induced preorder is $(\leq) \subseteq X^2 = \{(x,x') \mid \forall i \cdot f_i(x) \prec_i f_i(x') \}$.

*  The category of [[topological groups]] is topological over [[Grp]], the category of [[topological vector spaces]] is topological over $\mathbb{R}$-[[Vect]], etc.


## Further properties

*  If $C$ is topological over $D$, then so is any full [[retract]] of $C$, as long as the functors involved live in $Cat/D$.

*  In particular, a [[reflective subcategory|reflective]] or [[coreflective subcategory|coreflective]] subcategory of $C$ is topological, as long as the reflectors or coreflectors become [[identity morphisms]] in $D$.

*  The forgetful functor $U\colon C \to D$ is not only faithful but also (because every algebra must have an initial/indiscrete topology determined by the empty source) [[essentially surjective functor|essentially surjective]] (in fact surjective on the nose for the non-weak definitions).  Thus it is never [[full functor|full]] (except in the trivial case where $U$ is an [[equivalence of categories|equivalence]], of course).

*  If $D$ is [[complete category|complete]] or [[cocomplete category|cocomplete]], then so is $C$.

* If $D$ is [[total category|total]] or cototal, then so is $C$; see [[solid functor]].

* If $D$ is [[mono-complete category|mono-complete]] or epi-cocomplete, then so is $C$.

*  If $D$ is [[well-powered category|well-powered]] or co-well-powered, then so is $C$.

* If $D$ has a [[factorization structure for sinks]] $(E,M)$, then $C$ has one $(E',M')$, where $M'$ is the collection of morphisms in $C$ lying over $M$-morphisms in $D$, and $E'$ the collection of *final* sinks in $C$ lying over $E$-sinks in $D$.  This generalizes the lifting of [[orthogonal factorization systems]] along [[Grothendieck fibrations]].

*  If $D$ is [[concrete category|concrete]], then so is $C$.  More generally, if $D$ has a [[generator]], then $C$ is concrete over $D$.

*  In particular, if $D$ is [[Set]], then $C$ is a concrete category that is complete, cocomplete, well powered, and well copowered and has a factorization structure for sinks.


## Functors

* A functor $F\colon C\to C'$ between topological concrete categories $C/D$, $C'/D$ with the same base category $D$ preserves initial lifts iff it is right adjoint. It preserves final lifts iff it is left adjoint.

* More generally: If a functor $F\colon C\to C'$ between topological concrete categories $C/D$, $C'/D'$ with different base categories lying over a functor $F_0: D\to D'$. If $F$ is right (left) adjoint, then $F_0$ is right (left) adjoint and $F$ preserves initial (final) lifts. A partial converse holds: If $F_0$ is right (left) adjoint to $G_0$ and $F$ preserves initial (final) lifts, then there is functor $G$ lying over $G_0$ so that $F$ is right (left) adjoint to $G_0$.


## Special cases

*  If $X$ is any algebra, then there is a _[[discrete space]]_ over $X$ induced by the empty family of maps.  Similarly, we have an _indiscrete space_ with the final structure induced by no maps.  This defines functors $disc, indisc\colon D \to C$ that are respectively left and right [[adjoint functor|adjoints]] of $U$.

*  Suppose that $D$ has an [[initial object]] $0_D$.  Then the discrete space $0_C$ over $0_D$ is initial in $C$.  Similarly, the indiscrete space over a [[terminal object]] in $D$ is terminal in $C$.

*  More generally, suppose that $D$ has [[products]] or [[coproducts]] (indexed by whichever [[cardinal number|cardinalities]] you may wish to consider).  Then $C$ also has (co)products, lying over the (co)products in $D$, with structures induced by the product projections or coproduct inclusions.

*  More general [[limits]] and [[colimits]] are constructed in a similar way.  However, it is _not_ typically the case that $U$ _[[created limit|creates]]_ (co)limits in $C$ because creation of a limit requires that every preimage of the limiting cone is limiting. This fails for $U: \mathrm{Top} \to \mathrm{Set}$ since we can coarsen the topology on the limit vertex to obtain a counterexample.

*  If a single algebra $X$ has been given the structure of several spaces, then there are a _[[supremum]]_ structure and an _[[infimum]]_ structure on $X$ induced (as the initial and final structures) by the various incarnations of its [[identity morphism|identity]] homomorphism.  Exploiting this shows how to construct final structures out of initial ones and conversely.

*  If $X$ is a [[regular monomorphism|regular]] [[subobject|subalgebra]] of some $U(S)$, then the inclusion homomorphism makes $X$ into a _[[subspace]]_ of $S$, which is also a subobject in $C$.  Every regular subobject of $S$ is of this form; note however that there may be nonregular subobjects in $C$ even if all subobjects in $D$ are regular.


## Familiarly fibrations

The theory of topological functors can be developed along the lines of Grothendieck's theory of fibrations, where  _cartesian morphisms_  are replaced by  _cartesian families_. In this way just as by definition  "A functor is a _fibration_ if it creates cartesian morphisms and cartesian morphism compose", there is the definition "A functor is _topological_  if it creates cartesian families and cartesian families compose". 


## References

* J. Martin Harvey: _Topological functors from factorization_, in: *Categorical Topology*, Lecture Notes in Mathematics **719**, Springer (1979) &lbrack;[doi:10.1007/BFb0065263](https://doi.org/10.1007/BFb0065263)&rbrack;

* {#AdámekHerrlichStrecker90} [[Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]]: *[[Abstract and Concrete Categories -- The Joy of Cats]]*, Wiley (1990), reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 &lbrack;[tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/), [pdf](http://www.tac.mta.ca/tac/reprints/articles/17/tr17.pdf)&rbrack;

* {#Preuss2002} Gerhard Preuß: _Foundations of Topology: An Approach to Convenient Topology_; Kluwer (2002) &lbrack;ISBN 1-4020-0891-0, [doi:10.1007/978-94-010-0489-3](https://doi.org/10.1007/978-94-010-0489-3)&rbrack;
 
* [[Richard Garner]], *Topological functors as total categories*, Theory and Applications of Categories **29** 15 (2014) 406-421 &lbrack;[tac:29-15](http://www.tac.mta.ca/tac/volumes/29/15/29-15abs.html)&rbrack;

* [[Eduardo J. Dubuc]], Luis Espa&#241;ol, *Topological functors as familiarly fibrations* &lbrack;[arXiv:0611701](https://arxiv.org/abs/math/0611701)&rbrack;



[[!redirects topological concrete category]]
[[!redirects topological concrete categories]]

[[!redirects topological construct]]
[[!redirects topological constructs]]

[[!redirects topological category]]
[[!redirects topological categories]]

[[!redirects topological functor]]
[[!redirects topological functors]]

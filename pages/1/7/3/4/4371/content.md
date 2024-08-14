
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Double negation
* table of contents
{: toc}

## Idea

In [[logic]], double negation is the operation that takes $P$ to $\neg{\neg{P}}$, where $\neg$ is [[negation]].  In other words, double negation is the [[composite]] of [[negation]] with itself. This is a [[closure operator]]/[[modality]] and as such a special case of a [[continuation monad]].

The _[[double negation translation]]_ says that a [[proposition]] $P$ is provable in [[classical logic]] precisely if its double negation $\not \not P$ is provable in [[constructive logic]].

The _double negation topology_ closes morphisms under double negation (def. \ref{DoubleNegationTopology} below), and its [[category of sheaves]] forms a [[boolean topos]] (prop. \ref{DoubleNegationSheavesFormBooleanTopos} below). This notably serves to capture the _[[forcing]]_ of [[set theory]] in terms of [[topos theory]] ([[classifying topoi]]), see also remark \ref{RelationToForcing} below. 

## In logic

In [[classical logic]], the double negation of any [[truth value]] or [[proposition]] is itself.  More abstractly, double negation is the [[identity function]] on any [[boolean algebra]].


In [[intuitionistic logic]], double negation is weaker than the identity.  That is, we have $P \Rightarrow \neg{\neg{P}}$ but not conversely.  In [[paraconsistent logic]], it is the other way around.  More abstractly, this holds in any [[Heyting algebra]] (intuitionistic) or its dual (paraconsistent).

In [[linear logic]], double negation is the identity again, although linear logic also has notions of intuitionistic negation and paraconsistent negation which act as above.


## In locale theory{#double_negation_locale}

Even in [[classical mathematics]], a [[frame]] is a Heyting algebra but not a boolean algebra.  Accordingly, double negation is usually not the identity on a frame.  However, the operation of double negation is a [[nucleus]] on any frame.

Thus, every [[locale]] $L$ has a [[sublocale]] given by that nucleus, called the __double negation sublocale__ and denoted $L_{\neg\neg}$.  This sublocale is [[dense sublocale|dense]], and in fact it is the smallest dense sublocale of $L$, the [[intersection]] of all dense sublocales.

In [[classical mathematics]], if $L$ is a [[spatial locale]], then we have $L = L_{\neg\neg}$ if and only if $L$ is the [[discrete locale]] on some [[set]] $S$ of points.  In [[constructive mathematics]], the same holds except that $S$ must also have [[decidable equality]].

+-- {: .num_example}
###### Example

Let $\mathcal{O}_X$ be the sheaf of [[continuous map|continuous]] (or [[smooth map|smooth]], or [[holomorphic map|holomorphic]], or [[regular map|regular]]) functions on a [[topological space]] (or [[smooth manifold]], or [[complex manifold]], or [[reduced scheme]]) $X$. Then the [[direct image|pushforward]] of the [[inverse image|pullback]] of $\mathcal{O}_X$ to the smallest dense sublocale of $X$ is the sheaf of [[meromorphic functions]] on $X$ (i.e. sections over an open subset $U$ are given by sections of $\mathcal{O}_X$ defined on some dense open subset $V \subseteq U$).
=--


## In topos theory {#topology}

The notion of double negation sublocale may be [[categorification|categorified]] from locales to [[toposes]].  

If $E$ is a(n [[elementary topos|elementary]]) [[topos]] with [[subobject classifier]] $\Omega$, there is a [[negation]] operator $\neg \colon \Omega \to \Omega$, defined by virtue of the fact that $\Omega$ is an [[internalisation|internal]] [[Heyting algebra]].  


\begin{remark}
A topos $\mathcal{E}$ such that $\mathcal{E}_{\neg\neg}$ is an [[open subtopos]] is called _$\bot$-scattered_. They play a role in the modeling of [[provability logic]] (cf. [[scattered topos]]).
\end{remark}

\begin{remark}
The booleanization $\mathcal{E}_{\neg\neg}$ of a topos $\mathcal{E}$ has a close relative: the [[De Morganization]] $\mathcal{E}_m$.
\end{remark}


### Definition

+-- {: .num_defn #DoubleNegationTopology}
###### Definition/Proposition
**(double negation topology)**

The double negation morphism

$$
  \not \not \colon \Omega \to \Omega
$$

constitutes a [[Lawvere-Tierney topology]] on $\mathcal{E}$.

This is called the **double negation topology**.
=--

+-- {: .proof}
###### Proof 
The topology axioms can be formulated in purely equational form, i.e., as equations between operations of the form $\Omega^n \to \Omega$. By the Yoneda lemma, it suffices to verify the corresponding equations between transformations $Hom(-, \Omega)^n \to Hom(-, \Omega)$, which boils the problem down to checking the equations for ordinary Heyting algebras in $Set$. For ordinary Heyting algebras, proofs may be found [here](Heyting+algebra#ToBooleanAlgebras).
=--

+-- {: .num_example}
###### Example
{#quiv}In case of $Set^{\rightrightarrows}$, the presheaf topos of directed graphs, the action of $\neg\neg$ as a [[closure operator]] on subgraphs $X\subseteq Y$ amounts to adding to the edge set of $X$ all the edges in $Y$ between vertices that are in $X$. The patient reader will find further details on the $\neg\neg$-topology for this elementary example spelled out at length at [[Quiv]].
=--

### Properties
  {#Properties}

Let $\mathcal{E}$ be a(n [[elementary topos|elementary]]) [[topos]].

\begin{definition}
\label{DoubleNegationSheavesFormBooleanTopos}
The sheaf topos $\mathcal{E}_{\not \not} \hookrightarrow \mathcal{E}$ corresponding to the [double negation topology](#DoubleNegationTopology) (def. \ref{DoubleNegationTopology}) is a [[Boolean topos]].
\end{definition}

This appears for [[sheaf toposes]] $\mathcal{E}$ as [MacLane & Moerdijk, theorem VI 3](#MacLaneMoerdijk), and in the general case of [[elementary toposes]] as a special case of [Johnstone, Lem. A4.5.21](#Johnstone)).

The following says that $\mathcal{E}_{\not \not}$ is the smallest subtopos $\mathcal{E}_j$ such that $\emptyset$ is a $j$-sheaf. This property looks innocent but when thinking of $\mathcal{E}$ as a generalized (topological) space becomes, as in the case of locales, rather remarkable.

\begin{proposition}
\label{smallest_dense_subtopos}
$\mathcal{E}_{\not \not} \hookrightarrow \mathcal{E}$ is the smallest [[dense subtopos]].
\end{proposition}

([Johnstone 2002, below Cor. A4.5.20](#Johnstone), or [Johnstone 1977, p.140](#Johnstone77))

Another, slightly more general, way to state this is the following (cf. [Blass & Scedrov 1983](#BlassScedrov83), p.19, [Caramello 2012](#Caramello12), p.9):

\begin{proposition}\label{smallest_j-dense}
A [[Grothendieck topology|topology]] $j$ satisfies $j\le\neg\neg$, i.e. $j$ is [[dense subtopos|dense]], iff $(\mathcal{E}_j)_{\not\not}=\mathcal{E}_{\not\not}$.
\end{proposition}

\begin{proposition}
$\mathcal{E}_{\not \not} \hookrightarrow \mathcal{E}$ is the largest [[Boolean topos|Boolean subtopos]].
\end{proposition}

This follows from [Johnstone 2002, Lemma A4.5.21](#Johnstone).

From these two results, we can deduce the following characterization of the double negation topology.

\begin{proposition}\label{largest_boolean}
$\not\not$ is the unique topology $j$ such that (1) $j$ is [[dense subtopos|dense]], i.e. $j(0)=0$, and (2) the sheaf topos $\mathcal{E}_j$ is [[Boolean topos|Boolean]].
\end{proposition}


\begin{example}
\label{ForSierpinskiTopos}
Consider the [[Sierpinski topos]] $Set^{\to}$ (the [[arrow category]] of Set). It has exactly two dense subtoposes: the topos itself and the double-negation topos whose sheaves are the [[bijections]]. It has three Boolean subtoposes: the above, the subcategory on the arrows whose codomain is the terminal object, and the degenerate subtopos consisting of just the identity morphism of the terminal object. Observe that the two non-degenerate Boolean toposes, which complement each other in the [[lattice of subtoposes]], are both [[equivalence of categories|equivalent]] to the [[Set|topos of sets]], which incidentally shows that merely requiring the equivalence $(\mathcal{E}_j)_{\neg\neg}\simeq \mathcal{E}_{\neg\neg}$ in Prop. \ref{negdense} wouldn't do.
\end{example}

There are several other characterizations of the double negation topology:

+-- {: .num_prop #Sierpinski}
###### Proposition
$\not \not$ is the smallest topology $j$ on $\mathcal{E}$ such that the canonical mono $(\top,\bot)\, \colon \; 2 \,=\, 1\coprod 1 \, \rightarrowtail\, \Omega$ is $j$-dense.
=--

This is theorem 2.4. in [Caramello (2009)](#Caramello09).

+--{: .num_prop #Boolean_mono}
###### Proposition
$\neg\neg$ is the smallest [[Lawvere-Tierney topology|topology]] $j$ on $\mathcal{E}$ such that all monomorphisms of the form $A\vee\neg A\rightarrowtail E$ for subobjects $A\rightarrowtail E$ in $\mathcal{E}$ are $j$-dense.
=--

This appears as proposition 6.2 in [Caramello (2012a)](#Caramello12a).

As the smallest dense subtopos, $\mathcal{E}_{\not\not}$ becomes important for Lawvere's calculus of [[Aufhebung]]:

+-- {: .num_prop #RelationToAufhebungof01}
###### Proposition

The smallest  _essential_ subtopos $\mathcal{E}_j$ that is dense (in other words the [[Aufhebung]] of $0 \dashv 1$) has the property that $\mathcal{E}_{\neg\neg}\le \mathcal{E}_j$ and concides with $\mathcal{E}_{\neg\neg}$ in case the latter is an [[essential geometric morphism|essential]] subtopos: $\mathcal{E}_j=\mathcal{E}_{\neg\neg}$ (cf. [Lawvere-Menni 2015](#LawvereMenni15)).[^law]
=--

For further discussion of this relation see at [[dense subtopos]].

[^law]: [Lawvere (1991)](#Lawvere91) says around p.8: "_The base in fact seems in examples to be determined by the given category of Being itself, either as the latter's QD reflection with the extra localness condition supplying the right adjoint pure Becoming inclusion, or else (for example simplicial sets) as the double-negation sheaves with the extra essentialness condition supplying the left adjoint inclusion (in the latter case it is in [[Aufhebung|Hegelian fashion]] always the smallest level for which both 0,1 are sheaves)"_.

The double negation topology is closely related to the class of [[skeletal geometric morphism|skeletal geometric morphims]] i.e. $f:\mathcal{F}\to\mathcal {E}$ that restrict to a geometric morphism $\mathcal{F}_{\neg\neg}\to\mathcal{E}_{\neg\neg}$ e.g. skeletal geometric morphisms are the 1-cells in 2-category of toposes in which Boolean toposes are co-reflective (cf. Johnstone (2002, p.1008)).

The next propositions consider the important special case of $\neg\neg$ on [[presheaf toposes]]:

+-- {: .num_prop}
###### Proposition
Let $C$ be a small category admitting a [[calculus of fractions|right calculus of fractions]] with respect to the set $\Sigma$ of _all_ morphisms and let $G$ be the free groupoid generated by $C$, i.e. $G\cong C\Sigma^{-1}$. Then the following holds:
$$
Sh_{\neg\neg}(Set^{C^{op}})\cong Set^{G^{op}}\quad .
$$
=--

This appears as ex.5.2 in [Johnstone (1977, p.162)](#Johnstone77). It applies e.g. to $C$ a commutative monoid.

+-- {: .num_prop}
###### Proposition
For every [[presheaf topos]] $[C^{op}, Set]$ the double negation topology coincides with the [[dense topology]].
=--

This appears as [MacLaneMoerdijk, corollary VI 5](#MacLaneMoerdijk).

+-- {: .num_prop #DoubleNegationSheavesSatisfyAxiomOfChoice}
###### Proposition

Let $C$ be a [[poset]]. Then the double negation sheaf topos
$ Sh_{\not \not}(C) \hookrightarrow [C^{op}, Set]$
satisfies the [[axiom of choice]].
=--

This appears as [MacLaneMoerdijk, corollary VI 9](#MacLaneMoerdijk).  

+-- {: .num_remark #RelationToForcing}
###### Remark
**(relation to [[forcing]])**

Essentially because of prop. \ref{DoubleNegationSheavesSatisfyAxiomOfChoice}, double-negation sheaves on posets are the basic context for _[[forcing]]_ in [[set theory]] (since set theorists generally want the [[axiom of choice]] to be preserved in forcing models). For such a use of double negation in the so called **Cohen topos** see at _[[continuum hypothesis]]_.

=--



## In higher topos theory
 {#InHigherToposTheory}

[[classical logic|Classically]] the double negation modality is equivalent to the [[n-truncation modality]] for $n = -1$ (the [[bracket type]]).  In general, it\'s still true that double negation takes any type (object in the higher topos) to a $(-1)$-type, but the bracket type ${\|A\|_{-1}}$ only entails the double negation $\neg(\neg{A})$:

there is a canonical [[function]]

$$
  {\|A\|_{-1}} \longrightarrow \neg(\neg{A})
$$

and this is a [[1-epimorphism]] precisely if the [[law of excluded middle]] holds.


## Related entries 

* [[law of double negation]]

* [[Heyting algebra]] 

* [[Boolean algebra]] 

* [[double negation translation]] 

* [[dense subtopos]]

* [[logical topology]], [[synthetic differential topology]]

* [[skeletal geometric morphism]]

* [[de Morganization]]

* [[scattered topos]]

[[!include logic symbols -- table]]

## References

Informal exposition of double negation with an eye towards [[physics]] is in

* [[Andrej Bauer]], _[Intuitionistic mathematics for physics](http://math.andrej.com/2008/08/13/intuitionistic-mathematics-for-physics/)_, 2008

In [[topos theory]]:

* {#Johnstone77} [[Peter Johnstone]], _Topos Theory_ , Academic Press 1977 (Dover reprint 2014). (pp.139-140) 

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vols. I,II_, Oxford UP 2002. (pp.211,219-220,1008)

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (chap. VI, in particular sec.VI.1)

In [[homotopy type theory]]:

* [[Univalent Foundations Project]], section 3.4 of  _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

Discussion in relation to [[cohesion]] and the [[sharp modality]] is in 

* {#Lawvere91} [[F. W. Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ , pp.1-13 in LNM **1488** Springer Heidelberg 1991.

More detailed discussion of this is in 

* {#LawvereMenni15} [[William Lawvere]], [[Matías Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_, TAC **30** no. 26 (2015) pp.909-932. ([abstract](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

* {#Menni18} [[Matías Menni]], _The unity and identity of opposites between decidable objects and double-negation sheaves_ , JSL to appear. ([preprint](https://drive.google.com/file/d/18P2qsihtZG7_eCT5VdjvQ1I7T-U_S7y9/view))

Other useful references include

* {#BlassScedrov83}[[Andreas Blass]], Andrej Scedrov, _Boolean Classifying Topoi_ , JPAA **28** (1983) pp.15-30.

* {#Caramello09}[[Olivia Caramello]], _De Morgan classifying toposes_ , Advances in Mathematics **222** no.6 (2009) pp.2117-2144. ([arXiv:0808.1519](http://arxiv.org/abs/0808.1519))

* {#Caramello12a}[[Olivia Caramello]], _Universal models and definability_ , Math. Proc. Cam. Phil. Soc. (2012) pp.279-302. ([arXiv:0906.3061](http://arxiv.org/abs/0906.3061))

* {#Caramello12}[[Olivia Caramello]], _Topologies for intermediate logics_ , arXiv:1205.2547 (2012). ([abstract](http://arxiv.org/abs/1205.2547))

* D. S. Mcnab, _Some applications of double-negation sheafification_ , Proc. Edinburgh Math. Soc. **20** (1977) pp.279-285.


[[!redirects double negation]]
[[!redirects double negations]]
[[!redirects double-negation]]

[[!redirects not not]]
[[!redirects not-not]]

[[!redirects double negation sublocale]]
[[!redirects double negation sublocales]]
[[!redirects double-negation sublocale]]
[[!redirects double-negation sublocales]]
[[!redirects double negation nucleus]]
[[!redirects double negation nuclei]]

[[!redirects double-negation nucleus]]
[[!redirects double-negation nuclei]]

[[!redirects double negation topology]]
[[!redirects double negation topologies]]
[[!redirects double-negation topology]]
[[!redirects double-negation topologies]]

[[!redirects double negation modality]]
[[!redirects double negation modalities]]

[[!redirects double negation monad]]
[[!redirects double negation monads]]

[[!redirects boolean truncation]]
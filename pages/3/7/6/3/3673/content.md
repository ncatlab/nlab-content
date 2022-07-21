
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $C$ a [[category]] with the structure of a [[model category]] and $U:D\to C$ a functor having an [[adjoint]], under certain conditions it is possible to _transfer_ the model structure from $C$ to a model structure on $D$ by declaring the weak equivalences, and the fibrations (if $U$ is a right adjoint) or cofibrations (if $U$ is a left adjoint), in $D$ to be precisely those morphisms whose images under $U$ are such in $C$.  If $U$ is a right adjoint this is called the **right transferred**, **right induced**, or **right lifted** model structure, and dually in the left case.

Typically this arises in situations where $D$ consist of the "same" objects as $C$ but equipped with extra [[stuff, structure, property]], and $U$ is the corresponding [[forgetful functor]] sending objects in $D$ to their underlying objects in $C$.  Then a left adjoint $F$ of $U$ is the corresponding [[free functor]], while a right adjoint $G$ is a [[cofree functor]].

## Definition

### Right transfer
 {#RightTransfer}

\begin{definition}\label{RightTransferredModelStructure}
**(right transferred model structure)**
\linebreak
Let $C$ be a [[model category]] and

$$
  (F \dashv U )
  \;\colon\; 
  D 
  \underoverset  
    {\underset{U}{\longrightarrow}}
    {\overset{F}{\longleftarrow}}
    {\;\;\;\bot\;\;\;}
  C
$$

an [[adjoint functor|adjunction]] with [[right adjoint]] $U$.  Define a morphism in $D$ to be

* a **fibration** or **weak equivalence** precisely if its image under $U$ is so, respectively, in $C$;

* a **cofibration** precisely if it has the [[left lifting property]] with respect to the fibrations that are weak equivalences.

If these classes of maps define a model category structure on $D$, then it is called the **right transferred model structure** (or sometimes **right induced model structure** or **right lifted model structure**) from $C$ along $U$.
\end{definition}



In the above situation of Def. \ref{RightTransferredModelStructure} it is clear what one means by an [[acyclic fibration]] in $D$, but the notion of [[acyclic cofibration]] in $D$ is, *a priori*, ambiguous. For the purpose of stating the following Thm. \ref{NeccSuff} we declare that:

1. an *[[acyclic fibration]]* in $D$ is (of course) a morphism that is both a fibration and a weak equivalence, or equivalently whose image under $U$ is an acyclic fibration in $C$.  

1. a morphism is $D$ is

   1. a **cofibration weak equivalence** if it is both a cofibration and a weak equivalence in the sense of Def. \ref{RightTransferredModelStructure};

   1. an **anodyne map** if it has the [[left lifting property]] with respect to all fibrations.  

   Of course, if the transferred model structure exists, then these two classes of maps coincide.  

Conversely we have:

\begin{theorem}\label{NeccSuff}
A necessary and sufficient condition for the existence of the right transferred model structure (Def. \ref{RightTransferredModelStructure}) is that:

1. Every morphism in $D$ factors as 

   1. a cofibration followed by a trivial fibration, 

   1. an anodyne map followed by a fibration;

1. every anodyne map is a weak equivalence.

\end{theorem}

\begin{proof}
Clearly the conditions are necessary.  For the converse, the weak equivalences have the [[2-out-of-3 property]], all the classes of maps are closed under retracts, the lifting properties hold by definition (for the anodyne maps), and we have assumed the factorization properties (for the anodyne maps), so it remains to show that every cofibration weak equivalence is anodyne.  This follows by the standard retract argument: if $f \colon A \longrightarrow B$ is a cofibration weak equivalence, factor it as $f = p i$ with $i$ anodyne and $p$ a fibration.  Then since anodyne maps are weak equivalences and weak equivalences satisfy [[2-out-of-3]], $p$ is an acyclic fibration.  Thus $f$ has the left lifting property against $p$, hence $f$ is a [[retract]] of $i$ and thus also anodyne.
\end{proof}


### Left transfer
 {#LeftTransfer}

[[formal duality|Dually]], if $C$ is a model category and we have an [[adjoint functor|adjunction]]
$$
  (U \dashv G )
  \;\colon\; 
  D
  \underoverset
    {
      \underset{G}{\longleftarrow}
    }
    {
      \overset{U}{\longrightarrow}
    }
    {\;\;\;\bot\;\;\;} 
  C
$$
with $U$ [[left adjoint]],  define a morphism in $D$ to be

* a **cofibration** or **weak equivalence** precisely if its image under $U$ is, respectively, in $C$.

* a **fibration** precisely if it has the [[right lifting property]] with respect to the cofibrations that are [[weak equivalences]].

If these classes of maps define a model structure on $D$, it is called the **left transferred model structure** (or sometimes **left induced model structure** or **left lifted model structure**) from $C$.

The above necessary and sufficient conditions dualize directly.


## Existence

### Constructing factorizations
 {#ConstructingFactorizations}


#### For right transfer
 {#ConstructingFactorizationsForRightTransfer}

The most traditional way to obtain the factorization properties in the right-transferred case (Thm. \ref{NeccSuff}) is to assume that $C$ is [[cofibrantly generated]].

\begin{proposition}\label{SufficientConditions}
In the right-transferred situation (Def. \ref{RightTransferredModelStructure}), suppose that

1. $C$ is [[cofibrantly generated]],

1. the functor $F$ preserves [[small objects]] 

   (which is the case, in particular, when $U$ preserves [[filtered colimits]]),

then every morphism in $D$ factors as a cofibration followed by a trivial fibration, and as an anodyne map followed by a fibration.  

Moreover, if every anodyne map is a weak equivalence so that the transferred model structure on $D$ exists (by Thm. \ref{NeccSuff}), then it is is itself cofibrantly generated, and for $I$ (resp. $J$) a set of [[generating cofibrations]] (resp. acyclic cofibrations) in $C$, the image set $F(I)$ (resp. $F(J)$) forms a set of generating cofibrations (resp. acyclic cofibrations) in $D$.
\end{proposition}

\begin{proof}
By the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the [[adjoint pair]] $F\dashv U$, a morphism $f$ is a fibration (resp. trivial fibration) if and only if it has the right lifting property against the maps in $F(I)$ (resp. $F(J)$).  Since $F$ preserves small objects, the sets $F(I)$ and $F(J)$ permit the small object argument in $D$, which therefore yields (cofibration, trivial fibration) and (anodyne, fibration) factorizations.
\end{proof}

Another way to produce these factorizations is to generate them by a functorial factorization:

+-- {: .num_lemma #AlgebraicLift}
###### Lemma
Suppose $F \colon C \rightleftarrows D \colon U$ is an [[adjoint functor|adjunction]], where $D$ has [[pushouts]], and that

1. $C$ has a [[functorial factorization]] $(L,R)$ with a [[right weak composition law for factorizations]] (e.g. if it is [[awfs|algebraic]]),

1. the induced functorial factorization on $D$ permits Garner's [[small object argument]] (e.g. if $C$ and $D$ are locally presentable and all functors are accessible).

Then there is an induced ([[awfs|algebraic]]) weak factorization system on $D$ whose right class consists precisely of those maps whose $U$-image admits an $R$-algebra structure.
=--
+-- {: .proof}
###### Proof
Given a morphism $f:A\to B$ in $D$, factor it as follows, where the upper commutative square is a pushout:
$$\array{
  F U A & \longrightarrow & A 
  \\
  \mathllap{ {}^{F ((U f)_L)} }
  \big\downarrow & & \big\downarrow 
  \\
  F E (U f) & & E f 
  \\
  \mathllap{ {}^{F ((U f)_R)} }
  \big\downarrow & & \big\downarrow 
  \\
  F U B & \longrightarrow & B
}$$
This yields a functorial factorization $(L',R')$ on $D$.  By the universal property of pushout, an $R'$-algebra structure on $f$ is determined by a diagonal lifting in the square
$$ 
  \array{
    F U A & \longrightarrow & A 
    \\
    \mathllap{ {}^{F ((U f)_L)} }
    \big\downarrow & & \big\downarrow \mathrlap{{}^f} 
    \\
    F E (U f) 
    & 
    \underset{F ((U f)_R)}{\longrightarrow}
    & 
    B 
  }
$$
which corresponds by adjunction to precisely an $R$-algebra structure on $U f$.  Thus, the right weak composition law for $R$-algebras lifts to a right weak composition law for $R'$-algebras.  Garner's small object argument applied to $(L',R')$ then produces a monad over $cod$ with a right strong composition law, which is therefore an [[algebraic weak factorization system]] whose algebraic right maps are the $R'$-algebras, and in particular whose underlying right chlass is as desired those maps whose $U$-image is in $R$.
=--

In particular, therefore, the factorizations of any [[accessible model structure]] right-lift along any adjunction between locally presentable model categories, whether or not they are cofibrantly generated.  But the cofibrantly generated case can also be subsumed, by taking $(L,R)$ to be the one-step factorization produced by the generating left maps.

Left-lifting is generally rather trickier.  But by invoking fancier categorical machinery, one can show more generally:

\begin{lemma}
  Suppose given a functor $U:D\to C$ between locally presentable categories and an [[accessible weak factorization system]] $(L,R)$ on $C$.

  1. If $U$ has a left adjoint $F$, then $(L,R)$ right-lifts along $U$ to an accessible wfs on $D$.
  1. If $U$ has a right adjoint $G$, then $(L,R)$ left-lifts along $U$ to an accessible wfs on $D$.

  Moreover, if $(L,R)$ is cofibrantly generated, so are the lifted wfs.

\end{lemma}
\begin{proof}
  See [HKRS15](#HKRS15) and [GKR18](#GKR18) for the lifting of accessible wfs.  Cofibrant generation of a right-lifted wfs follows as in Theorem \ref{SufficientConditions} above, while in the left-lifted case it is Remark 3.8 of [MR13](#MR13).
\end{proof}

This sort of result seems to be necessary for the case of left-lifting; the simpler cofibrantly-generated argument does not dualize as directly.


#### For left transfer
 {#ConstructingFactorizationsForLeftTransfer}

\begin{proposition}
\label{RecognitionOfLeftTransferUnderCofibrantlyGeneration}
Given a pair of [[adjoint functors]]
$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {\;\;\bot\;\;}
  \mathcal{C}
$
such that:

1. $\mathcal{C}$ and $\mathcal{D}$ are [[locally presentable categories]],

1. $\mathcal{C}$ is equipped with the [[mathematical structure|structure]] of a [[cofibrantly generated model category]] (hence a [[combinatorial model category]]) with [[class|classes]] of ([[cofibration|co]]-)/[[fibrations]] and [[weak equivalences]] $Cof, Fib, W \,\subset\, Mor(\mathcal{C})$,

1. $RLP\big( L^{-1} Cof \big) \,\subset\, L^{-1}(W)$ (i.e. co-anodyne maps are weak equivalences),

then the left-transferred model category structure on $\mathcal{D}$ exists (i.e. with cofibrations $L^{-1}(Cof)$ and weak equivalences $L^{-1}(W)$) and is itself [[cofibrantly generated model category|cofibrantly generated]].
\end{proposition}

([BHKKRS 2015, Thm. 2.23](#BHKKRS15))

### Verifying acyclicity

The "acyclicity condition" in Thm. \ref{NeccSuff}, i.e. that anodyne maps are weak equivalences, is usually the most difficult to check.  Sometimes useful is the observation that for right-lifting in the cofibrantly generated case, it suffices to show that [[sequential colimits]] of [[pushouts]] of [[images]] under $F$ of the generating acyclic cofibrations in $C$ (i.e. forming $F(J)$-[[cell complexes]]) yield weak equivalences in $D$.  This is because the small object actually factors any map as such an $F(J)$-cell complex followed by a fibration; hence by the retract argument every anodyne map is a retract of an $F(J)$-cell complex.

Another useful sufficient condition is the following, going back roughly to section II.4 of ([Quillen](#Quillen)).

\begin{proposition}\label{PathObjects}
In the situation of right transfer (Def. \ref{RightTransferredModelStructure}), where $U \colon D\to C$ is a [[right adjoint]], suppose that

1. $D$ has a [[fibrant replacement functor]] (in fact it suffices for individual objects and morphisms to have fibrant replacements, while functoriality is not necessary),

1. $D$ has [[path objects]] for fibrant objects, i.e. a factorization of the [[diagonal]] $\Delta : A \to A \times A$ as a weak equivalence followed by a fibration $\Delta \colon A \stackrel{\simeq}{\to} P(A) \stackrel{fib}{\to} A \times A$.

Then any anodyne map in $D$ is a weak equivalence.  Thus, if the two factorizations exist in $D$, then the transferred model structure exists.
\end{proposition}

\begin{proof}
The notation in the following is mostly that of [Rezk 02, Lemma 7.6](#Rezk02).  
Let $R$ be a fibrant replacement functor, with natural weak equivalence $j \colon Id \to R$, suppose $f \colon X\to Y$ is anodyne, and consider the following [[commuting diagram]]:

\begin{center}
\begin{tikzcd}
X \ar[dr,"i" description] \ar[r,"f"] \ar[d,"{(1,f)}"'] &
Y \ar[r,"{j_Y}"] & R Y \ar[d] \\
X\times Y \ar[dr,"{j_X \times j_Y}"'] &
P R f \ar[r] \ar[d]  & P R Y \ar[d]\\
& R X \times R Y \ar[d,"{\mathrm{pr}_1}"'] \ar[r,"{R f \times 1}"'] & R Y \times R Y \ar[d,"{\mathrm{pr}_1}"'] \\
& R X \ar[r,"R f"'] & R Y
\end{tikzcd}
\end{center}

Both squares are [[pullbacks]], defining the object $P R f$ and the morphism $i$ making the following square commute:

\begin{center}
\begin{tikzcd}
X \ar[d,"f"'] \ar[r,"i"] & P R f \ar[r,"\pi"] \ar[d] & R X\\
Y \ar[r,"{j_Y}"'] \ar[ur,dashed,"g"] & R Y.
\end{tikzcd}
\end{center}

The morphism $\pi$ is the composite $P R f\to R X \times R Y \to R X$ at the top, which is a pullback of $P R Y \to R Y$; but the latter is a fibration (as the composite $P R Y \to R Y \times R Y \to R Y$) and a weak equivalence (as a retraction for $R Y \to P R Y$), so it and hence also $\pi$ are acyclic fibrations.  Moreover, since $\pi i = j_X$, by [[2-out-of-3]] $i$ is also a weak equivalence.

Now the projection $P R f\to P Y$ is a fibration, so since $f$ is anodyne there is a lift $g$ in the second square as shown.  Since $i$ and $j_Y$ are weak equivalences, by [[2-out-of-6]] it follows that $f$ is a weak equivalence.
\end{proof}

Note that this condition also dualizes straightforwardly to the left-transferred case.


## Properties

### General

\begin{lemma}
If $C$ carries the structure of a [[right proper model category]], then also a right-transferred model structure on $D$ (Def. \ref{RightTransferredModelStructure}) is right proper.
\end{lemma}

\begin{proof}
Let 

$$
  \array{
     A \times_C B &\stackrel{f}{\to}& B
     \\
     \downarrow && \downarrow^{\mathrlap{\in Fib}}
     \\
     A &\stackrel{\simeq}{\to}& C
  }
$$

be a [[pullback]] diagram in $D$, with the bottom morphism a weak equivalence and the right morphism a fibration. We need to show that then also the top morphism $f$ is a weak equivalence. By definition of transfer, this is equivalent to $U(f)$ being a  weak equivalence in $C$. 

Since $U$ is a [[right adjoint]] it preserves pullbacks, so that also

$$
  \array{
     U(A \times_{C} B) &\stackrel{U(f)}{\to}& U(B)
     \\
     \downarrow && \downarrow^{\mathrlap{\in Fib}}
     \\
     U(A) &\stackrel{\simeq}{\to}& U(C)
  }
$$

is a pullback diagram in $C$. Since by definition of the transferred model strucure this is still the pullback of a weak equivalence along a fibration, and since $C$ is assumed to be right proper, it follows that $U(f)$ is a weak equivalence in $C$, hence that $f$ is a weak equivalence in $D$.
\end{proof}



### Enrichment {#Enrichment}

Often the underlying model category $C$ is an [[enriched model category]] over some [[monoidal model category]] $S$ and one wishes to transfer also the model enrichment.

\begin{proposition}
Assume the adjunction

$$
  (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

satisfies the conditions of the above proposition for right transfer, so that the model structure on $C$ is transferred to $D$. Consider the case that $C$ is moreover an $S$-[[enriched model category]] and that $D$ can be equipped with the structure of a $S$-[[enriched category]] that is also  $S$-[[power]]ed and [[copower]]ed. 

Assume now that the $S$-powering of $D$ is taken by $U$ to the $S$-powering of $C$, in that $U(d^{(s_1 \to s_2)}) = U(d)^{(s_1 \to s_2)}$.

Then the transferred model structure and the $S$-enrichment on $D$ are compatible and make $D$ an $S$-enriched model category.
\end{proposition}

\begin{proof}
By the axioms of [[enriched model category]] one sufficient condition to be checked is that for $s \to t$ any cofibration in $S$ and for $X \to Y$ any fibration in $D$, we have that the induced morphism

$$
  X^t \to X^s \times_{Y^s} Y^{t}
$$

is a fibration, which is a weak equivalence if at least one of the two input morphisms is. By the induced model structure, this is checked by applying $U$. But by assumption $U$ commutes with the powering, and since $U$ is a [[right adjoint]] it commutes with taking the pullback, so that under $U$ the morphism is

$$
  U(X)^t \to U(X)^s \times_{U(Y)^s} U(Y)^{t}
$$

which is the morphism induced from $U(X) \to U(Y)$. That this is indeed an (acyclic) fibration follows now from the fact that $C$ is an $S$-enriched model category.
\end{proof}


## Examples

* The [[projective model structure on functors]] $M^D$ is right-transferred from the product model structure on $M^{ob D}$.  Dually, the [[injective model structure on functors]], when it exists, is left-transferred from $M^{ob D}$.

* The [[model structure on algebraic fibrant objects]] is right-transferred from the underlying model category by forgetting the choice of fillers.

* If $T$ is an [[accessible functor|accessible]] [[strict 2-monad]] on a [[locally finitely presentable category|locally finitely presentable 2-category]] $K$. then the category $T Alg_s$ of strict $T$-[[algebra over a monad|algebras]] admits a right-transferred model structure from the [[2-trivial model structure]] on $K$.  The acyclicity condition is proved by using [[pseudolimits]] of arrows for path objects, and the (cofibration, trivial fibration) factorization is constructed using a version of the construction of Lemma \ref{AlgebraicLift} (since the 2-trivial model structure on $K$ may not be cofibrantly generated).

* A non-example is provided as Example 3.7 of ([GoerssSchemmerhorn](#GoerssShemm)). Let $k$ be a field of characteristic 2 and consider the adjunction
$$
 (S \dashv U )\; : \; CGA_k \stackrel{\overset{S}{\leftarrow}}{\underset{U}{\to}} Ch_*k
$$
of the symmetric algebra functor and the forgetful functor between graded commutative DGAs and chain complexes. One sees that $S$ does not preserve the weak equivalence between 0 and the complex with one copy of $k$ in degrees $n$ and $n-1$. Since all chain complexes are cofibrant this means that $(S \dashv U )$ cannot be upgraded to a Quillen adjunction. 

* A more category-theoretic non-example is that the [[Reedy model structure]] on [[directed graphs]] internal to [[Cat]] does not right-transfer to the category [[DblCat]] of [[double categories]] along the free-forgetful adjunction.  One of the generatic trivial cofibrations for the Reedy model structure "transports" a horizontal arrow (in double-category terminology) along two vertical isomorphisms, which is a levelwise equivalence.  But upon pushing out the free double category generated by this along a map into some other double category, new composite horizontal arrows may be generated in the codomain that are not isomorphic to the image of anything in the domain; thus the pushout is no longer a levelwise equivalence.  So, the acyclicity condition fails.


## References

The arguments for right transfers of model structures go back to

* {#Quillen} [[Dan Quillen]], _Homotopical Algebra_ , Lecture Notes in Math. 43, Springer-Verlag, Berlin-eidelberg-New York, 1967.

The explicit study of right transfers of model structures on model categories is originally due to 

* {#Crans} [[Sjoerd Crans]], _Quillen closed model structure for sheaves_ ([doi](http://dx.doi.org/10.1016/0022-4049(94)00033-f), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.7459))


Further proofs can be found in 

* {#GoerssJardine} [[Paul Goerss]], [[J. F. Jardine]], _[[Simplicial homotopy theory]]_ , Progress Mathematics 174, Birkhäuser Verlag, Basel, 1999.


See also prop. 1.4.23 of

* {#Cisinski} [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))

The above proof of acyclicity in the presence of path objects is taken from

* {#Rezk02} [[Charles Rezk]], Every homotopy theory of simplicial algebras admits a proper model. Topology Appl. 119 (2002), no. 1, 65--94, [arxiv:math/0003065](https://arxiv.org/abs/math/0003065)

A summary of the result is on [p. 20](http://arxiv.org/PS_cache/math/pdf/0609/0609537v2.pdf#page=20) of

* {#GoerssShemm} [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv](http://arxiv.org/abs/math.AT/0609537))


and on p. 6 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_  ([pdf](http://www.math.uu.nl/publications/preprints/1242.pdf))

Discussion of left transfer in the accessible case:

* {#BHKKRS15} [[Marzieh Bayeh]], [[Kathryn Hess]], [[Varvara Karpova]], [[Magdalena Kedziorek]], [[Emily Riehl]], [[Brooke Shipley]], *Left-induced model structures and diagram categories*, in: *Women in Topology: Collaborations in Homotopy Theory*, Contemporary Mathematics **641** American Mathematical Society (2015) &lbrack;[arXiv:1401.3651](http://arxiv.org/abs/1401.3651), [ISBN:978-1-4704-2495-4](https://bookstore.ams.org/conm-641)&rbrack;

* {#HKRS15} [[Kathryn Hess]], [[Magdalena Kedziorek]], [[Emily Riehl]], [[Brooke Shipley]], *A necessary and sufficient condition for induced model structures*, J. Topology **10** 2  (2017) 324-369 &lbrack;[arXiv:1509.08154](http://arxiv.org/abs/1509.08154), [doi:10.1112/topo.12011](https://doi.org/10.1112/topo.12011)&rbrack;  

Beware that [HKRS15](#HKRS15) contains an error, corrected by:

* {#GKR18} [[Richard Garner]], [[Magdalena Kedziorek]], [[Emily Riehl]], *Lifting accessible model structures*, J. Topology **13** 1 (2020) 59-76 &lbrack;[arXiv:1802.09889](https://arxiv.org/abs/1802.09889), [doi:10.1112/topo.12123](https://doi.org/10.1112/topo.12123)&rbrack;

Discussion in the the combinatorial (cofibrantly generated) case:

* [[Higher Topos Theory]], Appendix A

* {#MR13} [[M. Makkai]], [[J. Rosický]], _Cellular categories_ (2013) &lbrack;[arXiv:1304.7572](https://arxiv.org/abs/1304.7572)&rbrack;

The right-transferred model structure on algebras for a 2-monad is from

* {#Lack06} [[Steve Lack]], *Homotopy-theoretic aspects of 2-monads*, [arXiv](http://arxiv.org/abs/math.CT/0607646)


[[!redirects transferred model category]]
[[!redirects transferred model categories]]
[[!redirects transferred model category structure]]
[[!redirects transferred model category structures]]
[[!redirects transferred model structure]]
[[!redirects transferred model structures]]

[[!redirects induced model category]]
[[!redirects induced model categories]]
[[!redirects induced model category structure]]
[[!redirects induced model category structures]]
[[!redirects induced model structure]]
[[!redirects induced model structures]]

[[!redirects lifted model category]]
[[!redirects lifted model categories]]
[[!redirects lifted model category structure]]
[[!redirects lifted model category structures]]
[[!redirects lifted model structure]]
[[!redirects lifted model structures]]

[[!redirects right-transferred model category]]
[[!redirects right-transferred model categories]]
[[!redirects right-transferred model category structure]]
[[!redirects right-transferred model category structures]]
[[!redirects right-transferred model structure]]
[[!redirects right-transferred model structures]]

[[!redirects right-induced model category]]
[[!redirects right-induced model categories]]
[[!redirects right-induced model category structure]]
[[!redirects right-induced model category structures]]
[[!redirects right-induced model structure]]
[[!redirects right-induced model structures]]

[[!redirects right-lifted model category]]
[[!redirects right-lifted model categories]]
[[!redirects right-lifted model category structure]]
[[!redirects right-lifted model category structures]]
[[!redirects right-lifted model structure]]
[[!redirects right-lifted model structures]]

[[!redirects left-transferred model category]]
[[!redirects left-transferred model categories]]
[[!redirects left-transferred model category structure]]
[[!redirects left-transferred model category structures]]
[[!redirects left-transferred model structure]]
[[!redirects left-transferred model structures]]

[[!redirects left-induced model category]]
[[!redirects left-induced model categories]]
[[!redirects left-induced model category structure]]
[[!redirects left-induced model category structures]]
[[!redirects left-induced model structure]]
[[!redirects left-induced model structures]]

[[!redirects left-lifted model category]]
[[!redirects left-lifted model categories]]
[[!redirects left-lifted model category structure]]
[[!redirects left-lifted model category structures]]
[[!redirects left-lifted model structure]]
[[!redirects left-lifted model structures]]

[[!redirects Kan transfer theorem]]

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

+-- {: .num_defn}
###### Definition
Let $C$ be a [[model category]] and

$$
  (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

an [[adjunction]] with [[right adjoint]] $U$.  Define a morphism in $D$ to be

* a **fibration** or **weak equivalence** precisely if its image under $U$ is, respectively, in $C$.
* a **cofibration** precisely if it has the left lifting property with respect to the fibrations that are weak equivalences.

If these classes of maps define a model structure on $D$, it is called the **right transferred model structure** (or sometimes **right induced model structure** or **right lifted model structure**) from $C$.
=--

Of course, in the above situation by a **trivial fibration** in $D$ we mean a morphism that is both a fibration and a weak equivalence, or equivalently whose image under $U$ is a trivial fibration in $C$.  The term "trivial cofibration", however, is *a priori* ambiguous: for the nonce let us call a morphism in $D$ a **cofibration weak equivalence** if it is both a cofibration and a weak equivalence and an **anodyne map** if it has the left lifting property with respect to all fibrations.  Of course, if the transferred model structure exists, then these two classes of maps coincide.  Conversely we have:

+-- {: .num_theorem #NeccSuff}
###### Theorem
Necessary and sufficient conditions for the existence of the transferred model structure are:

1. Every morphism in $D$ factors as a cofibration followed by a trivial fibration, and as an anodyne map followed by a fibration.
1. Every anodyne map is a weak equivalence.
=--
+-- {: .proof}
###### Proof
Clearly the conditions are necessary.  For the converse, the weak equivalences have the 2-out-of-3 property, all the classes of maps are closed under retracts, the lifting properties hold by definition (for the anodyne maps), and we have assumed the factorization properties (for the anodyne maps), so it remains to show that every cofibration weak equivalence is anodyne.  This follows by the standard retract argument: if $f:A\to B$ is a cofibration weak equivalence, factor it as $f = p i$ with $i$ anodyne and $p$ a fibration.  Then since anodyne maps are weak equivalences and weak equivalences satisfy 2-out-of-3, $p$ is a trivial fibration.  Thus $f$ has the left lifting property against $p$, hence $f$ is a retract of $i$ and thus also anodyne.
=--

### Left transfer

Dually, if $C$ is a model category and we have an adjunction
$$
  (U \dashv G )\; : \; D \stackrel{\overset{G}{\leftarrow}}{\underset{U}{\to}} C
$$
with $U$ left adjoint, we define a morphism in $D$ to be

* a **cofibration** or **weak equivalence** precisely if its image under $U$ is, respectively, in $C$.
* a **fibration** precisely if it has the right lifting property with respect to the cofibrations that are weak equivalences.

If these classes of maps define a model structure on $D$, it is called the **left transferred model structure** (or sometimes **left induced model structure** or **left lifted model structure**) from $C$.

The above necessary and sufficient conditions dualize directly.

## Existence

### Constructing factorizations

The most traditional way to obtain the factorization properties in the right-transferred case is to assume that $C$ is [[cofibrantly generated]].

+-- {: .num_prop #SufficientConditions}
###### Proposition
In the right-transferred situation, suppose that

1. $C$ is [[cofibrantly generated]], and

1. The functor $F$ preserves [[small objects]] (which is the case in particular when $U$ preserves [[filtered colimits]]).

Then every morphism in $D$ factors as a cofibration followed by a trivial fibration, and as an anodyne map followed by a fibration.  Moreover, if every anodyne map is a weak equivalence so that the transferred model structure on $D$ exists, then it is is cofibrantly generated, and for $I$ (resp. $J$) a set of generating cofibrations (resp. trivial cofibrations) in $C$, the image set $F(I)$ (resp. $F(J)$) forms a set of generating cofibrations (resp. trivial cofibrations) in $D$.
=--
+-- {: .proof}
###### Proof
By the adjunction $F\dashv U$, a morphism $f$ is a fibration (resp. trivial fibration) if and only if it has the right lifting property against the maps in $F(I)$ (resp. $F(J)$).  Since $F$ preserves small objects, the sets $F(I)$ and $F(J)$ permit the small object argument in $D$, which therefore yields (cofibration, trivial fibration) and (anodyne, fibration) factorizations.
=--

Another way to produce these factorizations is to generate them by a functorial factorization.

+-- {: .num_lemma #AlgebraicLift}
###### Lemma
Suppose $F: C \rightleftarrows D : U$ is an adjunction, where $D$ has [[pushouts]], and that

* $C$ has a [[functorial factorization]] $(L,R)$ with a [[right weak composition law for factorizations]] (e.g. if it is [[awfs|algebraic]]).
* The induced functorial factorization on $D$ permits Garner's [[small object argument]] (e.g. if $C$ and $D$ are locally presentable and all functors are accessible).

Then there is an induced ([[awfs|algebraic]]) weak factorization system on $D$ whose right class consists precisely of those maps whose $U$-image admits an $R$-algebra structure.
=--
+-- {: .proof}
###### Proof
Given a morphism $f:A\to B$ in $D$, factor it as follows, where the upper commutative square is a pushout:
$$\array{
  F U A & \to & A \\
  ^{F ((U f)_L)}\downarrow & & \downarrow \\
  F E (U f) & & E f \\
  ^{F ((U f)_R)}\downarrow & & \downarrow \\
  F U B & \to & B
}$$
This yields a functorial factorization $(L',R')$ on $D$.  By the universal property of pushout, an $R'$-algebra structure on $f$ is determined by a diagonal lifting in the square
$$ \array{
  F U A & \to & A \\
  ^{F ((U f)_L)}\downarrow & & \downarrow^f \\
  F E (U f) & \xrightarrow{F ((U f)_R)} & B }
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


### Verifying acyclicity

The "acyclicity condition" that anodyne maps are weak equivalences is usually the most difficult to check.  Sometimes useful is the observation that for right-lifting in the cofibrantly generated case, it suffices to show that [[sequential colimit]] of [[pushouts]] of images under $F$ of the generating trivial cofibrations in $C$ (i.e. an $F(J)$-[[cell complex]]) yields a weak equivalence in $D$.  This is because the small object actually factors any map as such an $F(J)$-cell complex followed by a fibration; hence by the retract argument every anodyne map is a retract of an $F(J)$-cell complex.

Another useful sufficient condition is the following, going back roughly to section II.4 of ([Quillen](#Quillen)).

+-- {: .num_prop #PathObjects}
###### Proposition
In the situation of right transfer, where $U:D\to C$ is a right adjoint, suppose that

* $D$ has a [[fibrant replacement functor]] (in fact it suffices for individual objects and morphisms to have fibrant replacements; functoriality is not required).

* $D$ has [[path objects]] for fibrant objects, i.e. a factorization of the [[diagonal]] $\Delta : A \to A \times A$ as a weak equivalence followed by a fibration $\Delta : A \stackrel{\simeq}{\to} P(A) \stackrel{fib}{\to} A \times A$.

Then any anodyne map in $D$ is a weak equivalence.  Thus, if the two factorizations exist in $D$, then the transferred model structure exists.
=--
+-- {: .proof}
###### Proof
The notation here is mostly that of [Rezk 02, Lemma 7.6](#Rezk02).  Let $R$ be a fibrant replacement functor, with natural weak equivalence $j : Id \to R$, suppose $f:X\to Y$ is anodyne, and consider the following diagram:
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
Both squares are pullbacks, defining the object $P R f$ and the morphism $i$ making the following square commute:
\begin{center}
\begin{tikzcd}
X \ar[d,"f"'] \ar[r,"i"] & P R f \ar[r,"\pi"] \ar[d] & R X\\
Y \ar[r,"{j_Y}"'] \ar[ur,dashed,"g"] & R Y.
\end{tikzcd}
\end{center}
The morphism $\pi$ is the composite $P R f\to R X \times R Y \to R X$ at the top, which is a pullback of $P R Y \to R Y$; but the latter is a fibration (as the composite $P R Y \to R Y \times R Y \to R Y$) and a weak equivalence (as a retraction for $R Y \to P R Y$), so it and hence also $\pi$ are acyclic fibrations.  Moreover, since $\pi i = j_X$, by [[2-out-of-3]] $i$ is also a weak equivalence.

Now the projection $P R f\to P Y$ is a fibration, so since $f$ is anodyne there is a lift $g$ in the second square as shown.  Since $i$ and $j_Y$ are weak equivalences, by [[2-out-of-6]] it follows that $f$ is a weak equivalence.
=--

Note that this condition also dualizes straightforwardly to the left-transferred case.


## Properties

### General

+-- {: .num_lemma}
###### Observation

If $C$ carries the structure of a [[right proper model category]], then also a right-transferred model structure on $D$ is right proper.

=--

+-- {: .proof}
###### Proof

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


=--



### Enrichment {#Enrichment}

Often the underlying model category $C$ is an [[enriched model category]] over some [[monoidal model category]] $S$ and one wishes to transfer also the model enrichment.

+-- {: .num_prop}
###### Observation

Assume the adjunction

$$
  (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

satisfies the conditions of the above proposition for right transfer, so that the model structure on $C$ is transferred to $D$. Consider the case that $C$ is moreover an $S$-[[enriched model category]] and that $D$ can be equipped with the structure of a $S$-[[enriched category]] that is also  $S$-[[power]]ed and [[copower]]ed. 

Assume now that the $S$-powering of $D$ is taken by $U$ to the $S$-powering of $C$, in that $U(d^{(s_1 \to s_2)}) = U(d)^{(s_1 \to s_2)}$.

Then the transferred model structure and the $S$-enrichment on $D$ are compatible and make $D$ an $S$-enriched model category.

=--

+-- {: .proof}
###### Proof

By the axioms of [[enriched model category]] one sufficient condition to be checked is that for $s \to t$ any cofibration in $S$ and for $X \to Y$ any fibration in $D$, we have that the induced morphism

$$
  X^t \to X^s \times_{Y^s} Y^{t}
$$

is a fibration, which is a weak equivalence if at least one of the two input morphisms is. By the induced model structure, this is checked by applying $U$. But by assumption $U$ commutes with the powering, and since $U$ is a [[right adjoint]] it commutes with taking the pullback, so that under $U$ the morphism is

$$
  U(X)^t \to U(X)^s \times_{U(Y)^s} U(Y)^{t}
$$

which is the morphism induced from $U(X) \to U(Y)$. That this is indeed an (acyclic) fibration follows now from the fact that $C$ is an $S$-enriched model category.


=--


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

The arguments for (right-)transfer of model structures go back to

* {#Quillen} [[Dan Quillen]], _Homotopical Algebra_ , Lecture Notes in Math. 43, Springer-Verlag, Berlin-eidelberg-New York, 1967.


Proofs can be found in 

* {#GoerssJardine} [[Paul Goerss]], Jardine, J. F., _Simplicial homotopy theory_ , Progress Mathematics 174, Birkhäuser Verlag, Basel, 1999.


The explicit study of (right-)transfer of model structures (on categories of sheaves) is apperently originally due to 

* {#Crans} [[Sjoerd Crans]], _Quillen closed model structure for sheaves_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.7459))


See also prop. 1.4.23 of

* {#Cisinski} [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))

The above proof of acyclicity in the presence of path objects is taken from

* {#Rezk02} [[Charles Rezk]], Every homotopy theory of simplicial algebras admits a proper model. Topology Appl. 119 (2002), no. 1, 65--94, [arxiv:math/0003065](https://arxiv.org/abs/math/0003065)

A summary of the result is on [p. 20](http://arxiv.org/PS_cache/math/pdf/0609/0609537v2.pdf#page=20) of

* {#GoerssShemm} [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv](http://arxiv.org/abs/math.AT/0609537))


and on p. 6 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_  ([pdf](http://www.math.uu.nl/publications/preprints/1242.pdf))

Left transfer in the accessible case is studied in

* Marzieh Bayeh, [[Kathryn Hess]], [[Varvara Karpova]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _Left-induced model structures and diagram categories_ ([arXiv:1401.3651](http://arxiv.org/abs/1401.3651))

* {#HKRS15} [[Kathryn Hess]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _A necessary and sufficient condition for induced model structures_ ([arXiv:1509.08154](http://arxiv.org/abs/1509.08154)).  This paper contains an error, corrected by:

* {#GKR18} [[Richard Garner]], Magdalena Kedziorek, [[Emily Riehl]], _Lifting accessible model structures_, [arXiv:1802.09889](https://arxiv.org/abs/1802.09889)

while in the combinatorial (cofibrantly generated) case it is studied in

* [[Higher Topos Theory]], Appendix A

* {#MR13} [[M. Makkai]], [[J. Rosický]], _Cellular categories_, 2013, [arXiv:1304.7572](https://arxiv.org/abs/1304.7572)

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


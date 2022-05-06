
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

For $C$ a [[category]] with the structure of a [[model category]] and $F:C\rightleftarrows D:U$ an [[adjunction]] with $U$ [[right adjoint]], under certain conditions it is possible  to _transfer_ the model structure from $C$ to a model structure on $D$ by declaring the fibrations and weak equivalences in $D$ to be precisely those morphisms whose images under $U$ are fibrations or weak equivalences, respectively, in $C$.

Typically this arises in situations where $D$ consist of the "same" objects as $C$ but equipped with extra [[stuff, structure, property]], and $U$ is the corresponding [[forgetful functor]] sending objects in $D$ to their underlying objects in $C$. Then $F$ is the corresponding [[free functor]].

## Definition and Existence

+-- {: .num_defn}
###### Definition
Let $C$ be a [[model category]] and

$$
  (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

an [[adjunction]] with [[right adjoint]] $U$.  Define a morphism in $D$ to be

* a **fibration** or **weak equivalence** precisely if its image under $U$ is, respectively, in $C$.
* a **cofibration** precisely if it has the left lifting property with respect to the fibrations that are weak equivalences.

If these classes of maps define a model structure on $D$, it is called the **transferred model structure** (or sometimes **induced model structure**) from $C$.
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

### Constructing factorizations

The most common way to obtain the factorization properties is to assume that $C$ is [[cofibrantly generated]].

+-- {: .num_prop #SufficientConditions}
###### Proposition
In the above situation, suppose that

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

In particular, therefore, the factorizations of any [[algebraic model structure]] lift along any adjunction between locally presentable model categories, whether or not they are cofibrantly generated.  But the cofibrantly generated case can also be subsumed, by taking $(L,R)$ to be the one-step factorization produced by the generating left maps.


### Verifying acyclicity

The "acyclicity condition" that anodyne maps are weak equivalences is usually the most difficult to check.  Sometimes useful is the observation that in the cofibrantly generated case, it suffices to show that [[sequential colimit]] of [[pushouts]] of images under $F$ of the generating trivial cofibrations in $C$ (i.e. an $F(J)$-[[cell complex]]) yields a weak equivalence in $D$.  This is because the small object actually factors any map as such an $F(J)$-cell complex followed by a fibration; hence by the retract argument every anodyne map is a retract of an $F(J)$-cell complex.

Another useful sufficient condition is the following.

+-- {: .num_prop #PathObjects}

###### Proposition
In the above situation, suppose that

* $D$ has a [[fibrant resolution functor]], and

* $D$ has functorial [[path objects]] for fibrant objects, i.e. a functorial factorization of the [[diagonal]] $\Delta : A \to A \times A$ as a weak equivalence followed by a fibration $\Delta : A \stackrel{\simeq}{\to} P(A) \stackrel{fib}{\to} A \times A$.

Then any anodyne map in $D$ is a weak equivalence.  Thus, if the two factorizations exist in $D$, then the transferred model structure exists.
=--
+-- {: .proof}
###### Proof
This argument goes back to section II.4 of ([Quillen](#Quillen)).  A proof for one set of sufficient conditions in is chapter II of ([GoerssJardine](#GoerssJardine)). Then ([Crans](#Crans)) and ([Cisinski](#Cisinski)).
=--


## Properties

### General

+-- {: .num_lemma}
###### Observation

If $C$ carries the structure of a [[right proper model category]], then also the transferred model structure on $D$ is right proper.

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

satisfies the conditions of the above proposition so that the model structure on $C$ is transferred to $D$. Consider the case that $C$ is moreover an $S$-[[enriched model category]] and that $D$ can be equipped with the structure of a $S$-[[enriched category]] that is also  $S$-[[power]]ed and [[copower]]ed. 

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

* The [[model structure on algebraic fibrant objects]] is transferred from the underlying model category by forgetting the choice of fillers.

* If $T$ is an [[accessible functor|accessible]] [[strict 2-monad]] on a [[locally finitely presentable category|locally finitely presentable 2-category]] $K$. then the category $T Alg_s$ of strict $T$-[[algebra over a monad|algebras]] admits a transferred model structure from the [[2-trivial model structure]] on $K$.  The acyclicity condition is proved by using [[pseudolimits]] of arrows for path objects, and the (cofibration, trivial fibration) factorization is constructed using a version of the construction of Lemma \ref{AlgebraicLift} (since the 2-trivial model structure on $K$ may not be cofibrantly generated).

* A non-example is provided as Example 3.7 of ([GoerssSchemmerhorn](#GoerssShemm)). Let $k$ be a field of characteristic 2 and consider the adjunction
$$
 (S \dashv U )\; : \; CGA_k \stackrel{\overset{S}{\leftarrow}}{\underset{U}{\to}} Ch_*k
$$
of the symmetric algebra functor and the forgetful functor between graded commutative DGAs and chain complexes. One sees that $S$ does not preserve the weak equivalence between 0 and the complex with one copy of $k$ in degrees $n$ and $n-1$. Since all chain complexes are cofibrant this means that $(S \dashv U )$ cannot be upgraded to a Quillen adjunction. 

* A more category-theoretic non-example is that the [[Reedy model structure]] on [[directed graphs]] internal to [[Cat]] does not transfer to the category [[DblCat]] of [[double categories]] along the free-forgetful adjunction.  One of the generatic trivial cofibrations for the Reedy model structure "transports" a horizontal arrow (in double-category terminology) along two vertical isomorphisms, which is a levelwise equivalence.  But upon pushing out the free double category generated by this along a map into some other double category, new composite horizontal arrows may be generated in the codomain that are not isomorphic to the image of anything in the domain; thus the pushout is no longer a levelwise equivalence.  So, the acyclicity condition fails.


## References

The arguments for transfer of model structures go back to

* {#Quillen} [[Dan Quillen]], _Homotopical Algebra_ , Lecture Notes in Math. 43, Springer-Verlag, Berlin-eidelberg-New York, 1967.


Proofs can be found in 

* {#GoerssJardine} [[Paul Goerss]], Jardine, J. F., _Simplicial homotopy theory_ , Progress Mathematics 174, Birkhäuser Verlag, Basel, 1999.


The explicit study of transfer of model structures (on categories of sheaves) is apperently originally due to 

* {#Crans} [[Sjoerd Crans]], _Quillen closed model structure for sheaves_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.7459))


See also prop. 1.4.23 of

* {#Cisinski} [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 


A summary of the result is on [p. 20](http://arxiv.org/PS_cache/math/pdf/0609/0609537v2.pdf#page=20) of

* {#GoerssShemm} [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv](http://arxiv.org/abs/math.AT/0609537))


and on p. 6 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_  ([pdf](http://www.math.uu.nl/publications/preprints/1242.pdf))

The dual notion of transfer, "left induced" instead of "right induced", is discussed in

* Marzieh Bayeh, [[Kathryn Hess]], Varvara Karpova, Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _Left-induced model structures and diagram categories_ ([arXiv:1401.3651](http://arxiv.org/abs/1401.3651))

See also

* {#HKRS15} [[Kathryn Hess]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _A necessary and sufficient condition for induced model structures_ ([arXiv:1509.08154](http://arxiv.org/abs/1509.08154)).  This paper contains an error, corrected by:

* [[Richard Garner]], Magdalena Kedziorek, [[Emily Riehl]], _Lifting accessible model structures_, [arXiv:1802.09889](https://arxiv.org/abs/1802.09889)

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

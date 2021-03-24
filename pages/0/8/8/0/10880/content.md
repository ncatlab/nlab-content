
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Wirthm&#252;ller context_ is a pair of two [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] $(\mathcal{X}, \otimes_X, 1_{X})$, $(\mathcal{Y}, \otimes_Y, 1_Y)$ which are connected by an [[adjoint triple]] of [[functors]] such that the middle one is a [[closed monoidal functor]].

This is the variant/special case of the [[yoga of six operations]] consisting of two [[adjoint pairs]] $(f_! \dashv f^!)$ and $(f^\ast \dashv f_\ast)$ and the [[tensor product]]/[[internal hom]] [[adjunctions]] $((-)\otimes B \dashv [B,-])$,  specialized to the case that  $f^! \simeq f^\ast$:

$$
  f_! \dashv (f^! = f^\ast) \dashv f_\ast
  \;\colon\;
  \mathcal{X}
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^! = f^\ast }{\leftarrow}}{\underset{f_\ast}{\longrightarrow}}}
  \mathcal{Y}
  \,.
$$

(The other specialization of the [[six operations]] to $f_\ast \simeq f_!$ is called the _[[Grothendieck context]]_).

Often one is interested in the case that there is an [[object]] $C \in \mathcal{X}$ and an [[equivalence]]

$$
  f_\ast 1_{X} \simeq f_! C
  \,.
$$

If this induces a [[natural equivalence]]

$$
  f_\ast A  \simeq f_!(A \otimes_X C)
$$

for $A \in \mathcal{X}$, then one says this is a _Wirthm&#252;ller isomorphism_, following ([Wirthmueller 74](#Wirthmueller74)).
In particular there is a canonical [[natural transformation]] 

$$
  f_\ast A  \longrightarrow f_!(A \otimes_X C)
$$

and one can ask this to be an equivalence, hence a Wirthm&#252;ller isomorphism ([May 05](#May05)).


## Definition

+-- {: .num_defn #WirthmullerContext}
###### Defininition

Let $(\mathcal{X}, \otimes_X, 1_{X})$, $(\mathcal{Y}, \otimes_Y, 1_Y)$ be two [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] and let 

$$
  f_! \dashv (f^! = f^\ast) \dashv f_\ast
  \;\colon\;
  \mathcal{X}
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^! = f^\ast }{\leftarrow}}{\underset{f_\ast}{\longrightarrow}}}
  \mathcal{Y}
$$

be an [[adjoint triple]] of [[functors]] between them. We call this setup

* a _pre-Wirthm&#252;ller context_ if $f^\ast$ is a [[strong monoidal functor]]:

* a _Wirthm&#252;ller context_ if $f^\ast$ is in addition a [[strong closed functor]], hence a strongly [[closed monoidal functor]].

=--

([May 05, def. 2.12](#May05))


+-- {: .num_defn }
###### Definition (Notation)

We write $[-,-]$ for the [[internal hom]] functors. For $A \in \mathcal{X}$ we write

$$
  \mathbb{D}A \coloneqq [A,1_X]
$$

for the [[internal hom]] from $A$ into the [[unit object]], hence for dual of $A$ with respect to the [[closed category]] structure, its [[dual object in a closed category]]. 

We say "$A$ is dualizable" to mean that it is a [[dualizable object]] with respect, insead, to the (symmetric) [[monoidal category]] structure $\otimes_X$. If $A$ is dualizable we write $A^\vee$ for its monoidal [[dual object]].

Similarly for $B \in \mathcal{Y}$.

=--

+-- {: .num_remark }
###### Remark

If all objects in $\mathcal{X}$ and $\mathcal{Y}$ are [[dualizable object|dualizable]], hence if they are [[compact closed categories]], then they are in particular also [[star-autonomous categories]] with [[dualizing object]] the [[tensor unit]]. As such their [[internal logic]] is _[[linear logic]]_ and their [[type theory]] is _[[linear type theory]]_. In terms of this a Wirthm&#252;ller morphism, def. \ref{WirthmullerContext}, is the linear analog of a [[context extension]] morphism in a [[hyperdoctrine]]: it defines a _[[dependent linear type theory]]_. See there for more.

=--

## Properties
 {#Properties}

### The comparison maps
 {#TheComparisonMaps}

+-- {: .num_remark #QuasiMonoidalnessOfLeftAdjoint}
###### Remark

In a pre-Wirthm&#252;ller context, def. \ref{WirthmullerContext}, 
there is a canonical [[natural transformation]]

$$
  f_!(A \otimes_X B)
    \longrightarrow
  (f_! A) \otimes_Y (f_! B)
  \,,
$$

(not necessarily an [[equivalence]]) being the [[adjunct]] of the composite

$$
  A \otimes_X B
  \stackrel{}{\longrightarrow}
  (f^\ast f_! A) \otimes_X (f^\ast f_! B)
  \stackrel{\simeq}{\longrightarrow}
  f^\ast ( (f_! A) \otimes_Y (f_! B) )
  \,,
$$

where the first morphism is the [[tensor product]] of two copies of the
[[unit of an adjunction|adjunction unit]] and where the second
is the [[equivalence]] that exhibits $f^\ast$ as a [[strong monoidal functor]].


=--

+-- {: .num_defn #ComparisonMaps}
###### Definition

In a pre-Wirthm&#252;ller context, def. \ref{WirthmullerContext},
write $\overline {\pi}$ for the [[natural transformation]]

$$
  \overline{\pi}
  \;\colon\;
  f_! ((f^\ast B) \otimes A) 
  \longrightarrow 
  B \otimes f_! A
$$

given as the composite

$$
  \overline{\pi}
  \;\colon\;
  f_! ((f^\ast B) \otimes A) 
   \stackrel{}{\longrightarrow}
  (f_! f^\ast B) \otimes_Y (f_! A)
   \longrightarrow 
  B \otimes f_! A
  \,,
$$

where the first morphism is that of remark \ref{QuasiMonoidalnessOfLeftAdjoint} and where the second 
is the $(f_! \dashv f^\ast)$ [[counit of an adjunction|counit]] (tensored with an identity).

Also write

$$
  \overline{\gamma}
    \;\colon\;
  [f_iA,B]
   \longrightarrow
  f_\ast [A, f^\ast B]
$$

for the $(f^\ast \dashv f_\ast)$ [[adjunct]] of the [[natural transformation]] given as the composite

$$
  f^\ast [A,f_i B]
   \stackrel{\simeq}{\longrightarrow}
  [f^\ast A, \, f^\ast f_i B]
   \longrightarrow
  [A, f^\ast B]  
  \,,
$$

where the first map exhibits $f^\ast$ as a [[closed monoidal functor]] and where the second is the $(f_! \dashv f^\ast)$-[[unit of an adjunction|unit]] (under the [[internal hom]]).

=--

see ([May 05, prop. 2.11](#May05))

+-- {: .num_prop #ComparisonIsEquivalenceOnDualizables}
###### Proposition

In a pre-Wirthm&#252;ller context, def. \ref{WirthmullerContext}, the comparison maps of def. \ref{ComparisonMaps} are [[equivalences]]
when the argument $B \in (\mathcal{Y}, \otimes_Y, 1_Y)$ is a [[dualizable object]].

If either of the two happens to be a [[natural equivalence]] (hence an equivalence for all arguments), then so is the other.

=--

([May 05, prop. 2.8 and prop. 2.11](#May05))

+-- {: .num_prop #InWirthmuellerContextProjectionIsEquivalence}
###### Proposition

Precisely if the pre-Wirthm&#252;ller context is a Wirthm&#252;ller context, def. \ref{WirthmullerContext}, are both comparison maps of def. \ref{ComparisonMaps} are natural equivalences.

=--

+-- {: .proof}
###### Proof

For all $A \in \mathcal{X}$ and $B,C \in \mathcal{Y}$ we have
by the $(f_! \dashv f^\ast)$-[[adjunction]] and the
tensor$\dashv$hom-adjunction a [[commuting diagram]] of the form


$$
  \array{
    \mathcal{Y}(B \otimes f_! A, \, C  )
     &
      \stackrel{
        \mathcal{Y}(\overline{\pi}(A,B), C)
      }{
        \longrightarrow
     }
     &
    \mathcal{Y}(f_! ((f^\ast B) \otimes A),\, C)
    \\
    \downarrow^{\mathrlap{\simeq}}
     &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{X}(A, f^\ast [B,C])
    &\stackrel{}{\longrightarrow}&
    \mathcal{X}(A, [(f^\ast B), (f^\ast C)])
  }
  \,.
$$

By naturality in $A$ and by the [[Yoneda lemma]] this shows
that $\overline{\pi}$ is an equivalence precisey if 
$f^\ast$ is strong closed.

For $\overline{\gamma}$ the same statement follows from this with 
prop. \ref{ComparisonIsEquivalenceOnDualizables}.

=--


+-- {: .num_remark }
###### Remark

The first [[natural equivalence]] of prop. \ref{InWirthmuellerContextProjectionIsEquivalence} 

$$
  f_!(f^\ast A \otimes B) \simeq A \otimes f_!(B)
$$

is often called the *[[projection formula]]*. In [[representation theory]] this is also sometimes called *[[Frobenius reciprocity]]*, though mostly that term is used for (just) the existence of the $(f_! \dashv f^\ast)$-[[adjunction]], where in representation theory the [[left adjoint]] $f_!$ forms [[induced representations]].

=--


### Comparison of push-forwards and Wirthm&#252;ller isomorphism
 {#ComparisonOfPushForwardsAndWirthmuelleriso}

+-- {: .num_cor #PushforwardsIntertwinedByDuality}
###### Corollary

In a pre-Wirthm&#252;ller context, def. \ref{WirthmullerContext}, the functors $f_!$ and $f_\ast$ are intertwined by dualization, in that there is a [[natural equivalence]]

$$
  \mathbb{D}(f_! A) \simeq f_\ast(\mathbb{D} A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the special case of the property of $\overline{\gamma}$ in  prop. \ref{ComparisonIsEquivalenceOnDualizables}  for $B = 1_Y$:

$$
  \mathbb{D}(f_! A)
  =  
  [f_! A, 1_Y]
   \underoverset{\simeq}{\overline{\gamma}}{\longrightarrow}
  f_\ast [A, f^\ast 1_Y]
  \simeq
  f_\ast [A, 1_Y]
  =
  f_\ast \mathbb{D} A
  \,.
$$

=--

+-- {: .num_remark #LinearDeMorganDualityForPushForwards}
###### Remark

With a Wirthm&#252;ller context regarded as [[categorical semantics]] for [[dependent linear type theory]] (see there), then the statement of cor. \ref{PushforwardsIntertwinedByDuality} is an instance of [[de Morgan duality]] where linear [[dual object|dualization]] intertwines linear [[dependent sum]] $\sum$ and [[dependent product]]  $\prod$

$$
  \prod_f \mathbb{D} \simeq \mathbb{D} \sum_f
  \,.
$$

For more on this see also ([[schreiber:Quantization via Linear homotopy types|Schreiber 14, section 3.3]]).

=--

+-- {: .num_example}
###### Example

In a pre-Wirthm&#252;ller context

$$
  f_\ast 1_X \simeq \mathbb{D}(f_! 1_X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By cor. \ref{PushforwardsIntertwinedByDuality}, 
since $\mathbb{D} 1_X \simeq 1_X$.

=--


+-- {: .num_prop #AbstractWirthmuellerIso}
###### Proposition
**(Wirthm&#252;ller isomorphism)**

In a Wirthm&#252;ller context, def. \ref{WirthmullerContext} if $f_! 1_X$ is a [[dualizable object]] with dual $f_! C$, then there is a [[natural equivalence]]

$$
  \omega
   \;\colon\;
  f_\ast f^\ast A \stackrel{\simeq}{\longrightarrow} f_!((f^\ast A) \otimes C)
  \,.
$$

=--

([May 05, prop. 4.13](#May05)).


+-- {: .num_remark #MonadCommutesWithDualityUpTotwist}
###### Remark

In particular if there is $D \in \mathcal{Y}$ with

$$
  \mathbb{D}(f_! f^\ast 1_Y) \simeq f_! f^\ast D
$$


(hence if $C \simeq f^\ast D$ in the notation of prop. \ref{AbstractWirthmuellerIso}) and using that by cor. \ref{PushforwardsIntertwinedByDuality},
$
  f_\ast f^\ast  \mathbb{D}B
  \simeq
  f_\ast \mathbb{D} f^\ast B
  \simeq
  \mathbb{D}(f_! f^\ast B)$
then prop. \ref{AbstractWirthmuellerIso} gives a natural equivalence of the form

$$
  \mathbb{D}(f_! f^\ast B)
    \stackrel{\simeq}{\longrightarrow}
   f_! f^\ast ((\mathbb{D}B) \otimes D)
  \,,
$$

saying that the [[comonad]] $f_! f^\ast$ commutes with dualization up to a "twist" given by tensoring with $D$.

=--




## Examples

### Cartesian Wirthm&#252;ller contexts in toposes
 {#CartesianWirthmuellerContexts}

For $\mathbf{H}$ a [[topos]] and $f \colon X \longrightarrow Y$
any [[morphism]], then in the induced [[base change]] [[etale geometric morphism]]

$$
  (\sum_f \dashv f^\ast \dashv \prod_f)
  \;\colon\;
  \mathbf{H}_{/X}
  \longrightarrow
  \mathbf{H}_{/Y}
$$

the [[inverse image]]/[[context extension]] is a [[cartesian closed functor]] (see there for the proof). Therefore any base change of [[toposes]] constitutes a cartesian Wirthm&#252;ller context.

Conversely, this means that systems of Wirthm&#252;ller contexts are generalizations of [[categorical logic]] ([[hyperdoctrines]]) to non-cartesian contexts (see at _[[dependent linear type theory]]_). 

Notice that in a cartesian Wirthm&#252;ller context duality is trivial, in that $\mathbb{D}X \simeq 1$ for all objects $X$. Therefore to the extent that the [[six operations]] yoga involves duality, it is interesting only the more non-cartesian (non-classical) the ambient Wirthm&#252;ller context is.

For instance the [[projection formula]] $\overline{\gamma}$ in def. \ref{ComparisonMaps} for base change along a pointed connected type $\mathbf{B}G \to \ast$ equivalently says that genuine ([[Bredon cohomology|Bredon]]) [[equivariant cohomology]] reduces to [[Borel equivariant cohomology]] when the action on the coefficients is trivial. See at _[[equivariant cohomology]]_ for more on this.

### Pointed objects with smash product
 {#PointedObjects}

A first step away from the Cartesian example [above](#CartesianWirthmuellerContexts) is the following.

Let $\mathbf{H}$ be a [[topos]]. For $X \in \mathbf{H}$ any [[object]], write 

$$
  \mathcal{C}_X \coloneqq \mathbf{H}_{/X}^{X/}
$$

for the [[category of pointed objects]] in the [[slice topos]] $\mathbf{H}_{/X}$. Equipped with the [[smash product]] $\wedge_X$ this is a [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}_X, \wedge_X, X \coprod X)$.

+-- {: .num_prop}
###### Proposition

For $f \colon X \longrightarrow Y$ any [[morphism]] in $\mathbf{H}$, the [[base change]] [[inverse image]] $f^\ast$ restricts to a functor $f^\ast \colon \mathcal{C}_Y \longrightarrow \mathcal{C}_X$ which is a Wirthm&#252;ller context.

=--

This appears as ([Shulman 07, examples 12.13 and 13.7](#Shulman07)) and ([Shulman 12, example 2.33](#Shulman12)).

+-- {: .proof}
###### Proof

For $f \colon X \longrightarrow Y$ any [[morphism]] in $\mathbf{H}$ then the [[base change]] [[inverse image]] $f^\ast \colon \mathbf{H}_{/Y} \longrightarrow \mathbf{H}_{/X}$ preserves pointedness, and the [[pushout]] functor $f_! \colon \mathbf{H}^{X/} \longrightarrow \mathbf{H}^{/Y}$ preserves co-pointedness. These two functors hence form an [[adjoint pair]]
$(f_1 \dashv f^\ast) \colon \mathcal{C}_X \longrightarrow \mathcal{C}_Y$.
Moreover, since [[colimits]] in the under-over category $\mathbf{H}_{/X}^{X/}$ are computed as colimits in $\mathbf{H}$ of [[diagrams]] with an [[initial object]] adjoined, and since by the [[Giraud axioms]] in the [[topos]] $\mathbf{H}$ [[pullback]] preserves these colimits, it follows that $f^\ast \colon \mathcal{C}_Y \to \mathcal{C}_X$ preserves colimits. 
Finally by the discussion at _[[category of pointed objects]]_ we have that $\mathcal{C}_X$ and $\mathcal{C}_Y$ are [[locally presentable categories]], so that by the [[adjoint functor theorem]] it follows that $f^\ast$ has also a [[right adjoint]] $f_\ast \colon \mathcal{C}_X \to \mathcal{C}_Y$.

To see that $f^\ast$ is a [[strong monoidal functor]] observe that the [[smash product]] is, by the discussion there, given by a [[pushout]] over [[coproducts]] and [[products]] in the [[slice topos]]. As above these are all preserved by [[pullback]]. Finally to see that $f^\ast$ is also a [[strong closed functor]] observe that the [[internal hom]] on [[pointed objects]] is, by the discussion there, a [[fiber product]] of cartesian internal homs. These are preserved by [the above case](#CartesianWirthmuellerContexts), and the fiber product is preserved since $f^\ast$ preserves all limits. Hence $f^\ast$ preserves also the internal homs of pointed objects.

 
=--


### Bundles of modules

For $R$ a [[ring]], $R Mod$ its [[category of modules]], there is a [[functor]]

$$
  [-, R Mod] \;\colon\; Set^{op} \longrightarrow ClMonCat
$$

which sends a [[set]] $X$ to the [[closed monoidal category]] of $R$-[[modules]] parameterized over $X$. 

This takes values in Wirthm&#252;ller morphisms. ([Shulman 12, example 2.2, 2.17](#Shulman12)).

### Bundles of $\infty$-modules

for [[(infinity,1)-module bundles]]: ([[schreiber:master thesis Nuiten|Nuiten 13]], [Hopkins-Lurie](#HopkinsLurie), [[schreiber:Homotopy-type semantics for quantization|Schreiber 14]])
 
### Becker-Gottlieb transfer

A _[[transfer context]]_ is a Wirthm&#252;ller context in which also $f_\ast$ satisfies its [[projection formula]]. In this context there is an abstract concept of _[[Becker-Gottlieb transfer]]_. See there for more.

### In equivariant stable  homotopy theory

In [[equivariant stable homotopy theory]], see ([May 05b](#May05b)).

### For quasicoherent sheaves (in $E_\infty$-geometry)
 {#ForQuasicoherentSheaves}

Pull-push of [[quasicoherent sheaves]] is usually discussed as a [[Grothendieck context]] of [[six operations]], but under some conditions it also becomes a Wirthm&#252;ller context.

Using results of Lurie this follows in the full generality of [[E-∞ geometry]] ([[spectral geometry]]).

Consider quasi-compact and quasi-separated [[E-∞ algebraic spaces]] ([[spectral algebraic spaces]]). (This includes precisely those [[spectral Deligne-Mumford stacks]] which have a [[scallop decomposition]], see [here](derived+Deligne-Mumford+stack#RelationToDerivedAlgebraicSpaces).)

If $f \;\colon\; X \longrightarrow Y$ is a map between these which is

1. locally almost of finite presentation;

1. strongly proper;

1. has finite [[Tor-amplitude]]

then the left adjoint to pullback of [[quasicoherent sheaves]] exists

$$
  (f_! \dashv f^\ast)
    \;\colon\;
  QCoh(X)
    \stackrel{\overset{f_!}{\longrightarrow}}{\underset{f^\ast}{\longleftarrow}}
  QCoh(Y)
  \,.
$$

([[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|LurieProper, proposition 3.3.23]])

If $f$ is

* quasi-affine

then the right adjoint exists

$$
  (f^\ast \dashv f_\ast)
    \;\colon\;
  QCoh(X)
    \stackrel{\overset{f^\ast}{\longleftarrow}}{\underset{f_\ast}{\longrightarrow}}
  QCoh(Y)
  \,.
$$

([[Quasi-Coherent Sheaves and Tannaka Duality Theorems|LurieQC, prop. 2.5.12]], [[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|LurieProper, proposition 2.5.12]])

The [[projection formula]] in the dual form

$$
  f_\ast A \otimes B \longrightarrow f_\ast (A\otimes f^\ast B)
$$

for $f$ quasi-compact and quasi-separated appears as ([[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|LurieProper, remark 1.3.14]]).

Now if all the conditions on $f$ hold, so that $(f_! \dashv f^\ast \dashv f_\ast) \;\colon\; QCoh(X) \longrightarrow QCoh(Y)$, then passing to opposite categories $QCoh(X)^{op} \longrightarrow QCoh(Y)^{op}$ exchanges the roles of $f_!$ and $f_\ast$, makes the projection formula be as in the above discussion and hence yields a Wirthm&#252;ller context.

The existence of [[dualizing modules]] $K$

$$
  D X = [X,K]
$$ 

is discussed in ([[Representability theorems|Lurie, Representability theorems, section 4.2]].)

## Related concepts

* [[Verdier-Grothendieck context]]

* [[Grothendieck context]]

* [[Beck-Chevalley condition]]

* [[ambidextrous adjunction]]

## References

The Wirthmüller isomorphism in [[equivariant stable homotopy theory]] goes back to and is named after

* {#Wirthmueller74} [[Klaus Wirthmüller]], _Equivariant homology and duality_. Manuscripta Math. 11(1974), 373-390
 
see Theorem II.6.2 in 

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger (with contributions by J.E. McClure), _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))


see also

* {#Nardin12} [[Denis Nardin]], section 2.6 and A.3 of _Stability and distributivity over orbital ∞-categories_, 2012 ([hdl.handle.net/1721.1/112895]( http://hdl.handle.net/1721.1/112895), [pdf](https://www.math.univ-paris13.fr/~nardin/thesis.pdf))


A clear discussion of axioms of [[six operations]] and their consequences, with emphasis on the Wirthm&#252;ller isomorphisms, is in 

* {#May05} [[Halvard Fausk]], P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_, Theory and Applications of Categories , Vol. 11, 2003, No. 4, pp 107-131. ([TAC](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 

* [[Paul Balmer]], [[Ivo Dell'Ambrogio]], [[Beren Sanders]], _Grothendieck-Neeman duality and the Wirthm&#252;ller isomorphism_, Compositio Mathematica 152.8 (2016): 1740-1776 ([arXiv:1501.01999](http://arxiv.org/abs/1501.01999))

Discussion of the original Wirthm&#252;ller isomorphism in [[equivariant stable homotopy theory]], based on this, is in

* {#May05b} [[Peter May]], _The Wirthm&#252;ller isomorphism revisited_, Theory and Applications of Categories 11.5 (2003): 132-142 ([TAC:11/5/11-05](http://www.tac.mta.ca/tac/volumes/11/5/11-05abs.html), [K-theory:0574](http://www.math.uiuc.edu/K-theory/0574/WirthRev.pdf))
 

More elaboration of the Wirthm&#252;ller context is in 

* Baptiste Calm&#232;s, Jens Hornbostel, section 4 of _Tensor-triangulated categories and dualities_, Theory and Applications of Categories, Vol. 22, 2009, No. 6, pp 136-198 ([TAC](http://www.tac.mta.ca/tac/volumes/22/6/22-06abs.html), [arXiv:0806.0569](http://arxiv.org/abs/0806.0569))

Discussion in the context of [[pure motives]] includes

* {#Deglise} [[Frédéric Déglise]], around prop. 1.34 of _Finite correspondences and transfers over a regular base_, [pdf](http://www.math.uiuc.edu/K-theory/0765/regular_base.pdf).

Wirthm&#252;ller morphisms between pointed objects and between bundles of modules are discussed in 

* {#Shulman07} [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, in  Theory and Applications of Categories,  Vol. 20, 2008, No. 18, pp 650-738.  ([arXiv:0706.1286](http://arxiv.org/abs/0706.1286), [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))
 

* {#Shulman12} [[Mike Shulman]], _Enriched indexed categories_ ([arXiv:1212.3914](http://arxiv.org/abs/1212.3914))
 


Discussion in [[E-∞ geometry]] is in

* {#Lurie} [[Jacob Lurie]], section 3.3. of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_
 

* [[Jacob Lurie]], section 4.2 of _[[Representability theorems]]_

* {#HopkinsLurie} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_
 

[[!redirects Wirthmüller contexts]]

[[!redirects Wirthmueller context]]
[[!redirects Wirthmueller contexts]]

[[!redirects Wirthmuller context]]
[[!redirects Wirthmuller contexts]]


[[!redirects Wirthmüller isomorphism]]
[[!redirects Wirthmüller isomorphisms]]

[[!redirects Wirthmueller isomorphism]]
[[!redirects Wirthmueller isomorphisms]]

[[!redirects Wirthmuller isomorphism]]
[[!redirects Wirthmuller isomorphisms]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


# Idempotent monads
* table of contents
{: toc}

## Idea
 {#Idea}

An _idempotent monad_ is a [[monad]] that "squares to itself" in the evident [[category theory|category-theoretic]] sense. Idempotent monads hence serve as [[categorification|categorified]] [[projection]] operators, in that they encode [[reflective subcategories]] and the reflection/[[localization]] onto these. 

In terms of [[type theory]] idempotent monads interpret (co-)[[modal operators]]; see [[modal type theory]].

## Definition 


+-- {: .num_defn #IdempotentMonad}
###### Definition

An __idempotent monad__  is a [[monad]] $(T,\mu,\eta)$ on a [[category]] $\mathcal{C}$ such that one (hence all) of the following equivalent statements are true:

1. $\mu\colon T T \to T$ is a [[natural isomorphism]]. 

2. All components of $\mu \,\colon\, T T \to T$ are [[monomorphisms]].

3. The [[maps]] $T\eta, \eta T \,\colon\, T \to T T$ are [[equality|equal]] (that is, $(T, \eta)$ is a [[well-pointed endofunctor]]). 

4. For every $T$-[[algebra over a monad|algebra]] (aka: $T$-module) $(M,u)$, the corresponding $T$-[[action]] $u\colon T M \to M$ is an [[isomorphism]] (i.e. every algebra is a [[fixed point]]).

5. The [[forgetful functor]] $\mathcal{C}^T \to \mathcal{C}$ (where $C^T$ is the [[Eilenberg-Moore category]] of $T$-algebras) is a [[full and faithful functor]].

6. There exists a pair of [[adjoint functors]] $F \dashv U$ such that the induced monad $(T \colon U F, \mu \coloneqq U \epsilon F, \eta)$ is [[isomorphism|isomorphic]] to $(T,\mu, \eta)$ and $U$ is a [[full and faithful functor]].

   {#SixPrime} 6'. 

   There is a [[full subcategory]] $U \colon C^T \hookrightarrow C$ and a [[natural bijection]] of the form

   $$
     \array{
     Hom_{\mathcal{C}}\big(
       T(c)
       ,\,
       U(a)
     \big)
     &
     \overset{\sim}{\longrightarrow}
     &
     Hom_{\mathcal{C}}\big(
       c
       ,\,
       U(a)
     \big)
     \\
     \big(
       T(c) \overset{f}{\longrightarrow} U(a)
     \big)
     &\mapsto&
     \big(
       c
         \overset{\eta}{\longrightarrow}
       T(c) 
         \overset{f}{\longrightarrow} 
       U(a)
     \big)
     }
   $$

   > (This is the form in which [[modal operators]] tend to be axiomatized in [[modal type theory]], e.g. [UP13, Def. 7.7.1](modal+homotopy+type+theory#HoTTBook).)

7. The [[identity]] [[natural transformation]] $T T \Rightarrow T T$ is a [[distributive law]].

=--

e.g. ([Borceux, prop. 4.2.3](#Borceux)). For (7) see Lemma 3.4 of [RW95](#RosebrughWood95).

+-- {: .num_prop #EquivalentConditions}
###### Proposition

The conditons in Def. \ref{IdempotentMonad} are indeed equivalent.

=--

+-- {: .proof}
###### Proof (in more than one way).

* $1\Rightarrow 2$ 

  This is trivial.

* $2\Rightarrow 3$ 

  Compositions $\mu\circ T\eta$ and $\mu\circ\eta T$ are always the identity (unit axioms for the monad), and in particular agree; if $\mu$ has all components monic, this implies $T\eta = \eta T$. 

* $3\Rightarrow 4$ 

  Compatibility of action and unit is $u \circ \eta_M = id_M$, hence also $T(u)\circ T(\eta_M) = id_{T M}$. If $T\eta = \eta T$ then this implies $id_{T M} = T(u)\circ \eta_{T M} = \eta_M\circ u$, where the naturality of $\eta$ is used in the second equality. Therefore we exhibited $\eta_M$ both as a left and a right inverse of $u$. 

* $4\Rightarrow 1$ 

  If every action is iso, then the components of multiplication $\mu_M\colon T T M\to T M$ are isos as a special case, namely of the free action on $T M$. 

* $4\Rightarrow 5$ 

  For any monad $T$, the forgetful functor from Eilenberg-Moore category $C^T$ to $C$ is faithful: a morphism of $T$-algebras is always a morphism of underlying objects in $C$. To show that it is also full, we consider any pair $(M,u)$, $(M',u')$ in $C^T$ 
and must show that any $f\colon M\to M'$ is actually 
a map $f\colon (M,u)\to (M',u')$; i.e. $u'\circ T f = f\circ u$. But we know that $\eta_M, \eta_{M'}$ are inverses of $u,u'$ respectively and the naturality for $\eta$ says $\eta_{M'}\circ f = T f \circ \eta_M$. Compose that equation with $u$ on the right and $u'$ on the left with the result (notice that we used just the invertibility of $u$).  

* $5\Rightarrow 6$ 

  Because the Eilenberg-Moore construction induces the original monad by the standard recipe. 

* $6\Rightarrow 3$ 

  By $6$ the counit $\epsilon$ is iso, hence $U\epsilon F$ has a unique 2-sided inverse; by [[triangle identities]], $T\eta$ and $\eta T$ are both right inverses of $U\epsilon F$, hence 2-sided inverses, hence they are equal.

* $6 \Leftrightarrow 6'$ 

  This is the special case of the characterization ([here](adjoint+functor#CollectionOfUniversalArrowsEquivalentToAdjointFunctor)) of ([[adjunction units]] of) [[adjoint functors]] $F \dashv U$ as systems of [universal arrows](adjoint+functor#UniversalArrows) when $U$ is [[fully faithful functor|fully faithful]].

* $6\Rightarrow 1$ 

  If $F\dashv U$ is an adjunction with $U$ fully faithful, 
then the counit $\epsilon$ is iso. Since $D(FU X,Y)\simeq C(UX,UY)\simeq D(X,Y)$ where the last equivalence holds since $U$ is full and faithful; hence by essential unicity of the representing object there is an isomorphism $FUX\stackrel{\sim}{\to} X$ ; let $X=Y$ then the adjoint of this identity is the counit of the adjunction; since the hom objects correspond bijectively, the counit is an isomorphism. Hence the multiplication of the induced monad $\mu = U\epsilon F$ is also an iso.

=--

Part 5 means that in such a case $C^T$ is, up to equivalence a full [[reflective subcategory]] of $C$.  Conversely, the monad induced by any reflective subcategory is idempotent, so giving an idempotent monad on $C$ is equivalent to giving a reflective subcategory of $C$.

In the language of [[stuff, structure, property]], an idempotent monad may be said to equip its algebras with _properties only_ (since $C^T\to C$ is fully faithful), unlike an arbitrary monad, which equips its algebras with _at most structure_ (since $C^T\to C$ is, in general, faithful but not full).

If $T$ is idempotent, then it follows in particular that an object of $C$ admits at most one structure of $T$-algebra, that this happens precisely when the  unit $\eta_X\colon X\to T X$ is an isomorphism, and in this case the $T$-algebra structure map is $\eta_X^{-1}\colon T X \to X$.  However, it is possible to have a non-idempotent monad for which any object of $C$ admits at most one structure of $T$-algebra, in which case $T$ can be said to equip objects of $C$ with [[property-like structure]]; an easy example is the monad on [[semigroups]] whose algebras are [[monoids]].

+-- {: .num_remark}
###### Remark
Let us be in a $2$-category $K$. Part of the structure of an idempotent monad $(C,T,\eta,\mu)$ in $K$ is of course an idempotent morphism $T:C\to C$. More precisely (Definition 1.1.9) considers $\mu$ as part of the structure such that an idempotent 1-cell has a 2-isomorphism $\mu:TT\to T$ such that $\mu T=T\mu$. Equivalently an idempotent morphism is a normalized pseudofunctor from the two object monoid $\{*,e\}$ with $e^2=e$ to $K$.

Recall that a *splitting of an idempotent* $(T,\mu)$ consists of a pair of 1-cells $I:D\to C$ and $R:C\to D$ and a pair of 2-isomorphisms $a:R I\to id_D$ and $b:T\to I R$ such that $\mu=b^{-1}(I\circ s\circ R)(b\circ b)$ where $\circ$ denotes horizontal composition of 2-cells. Equivalently an splitting of an idempotent is a limit or a colimit of the defining pseudofunctor. If $K$ has equalizers or coequalizers, then all its idempotents split.

Now if $(I,R,a,b)$ is a splitting of an idempotent monad, then $R\dashv I$ are adjoint. And in this case the splitting of an idempotent is equivalently an Eilenberg-Moore object for the monad $(C,T,\eta,\mu)$. In this case $D$ is called an *adjoint retract of $C$*.

=--

([[Sketches of an Elephant|Johnstone, B 1.1.9, p.248-249]])


+-- {: .num_remark}
###### Remark

Equivalences (resp. cores) in an allegory are precisely those symmetric idempotents which are idempotent monads (resp. comonads). In an allegory the following statements are equivalent: all symmetric idempotents split, idempotent monads split, idempotent comonads split. A similar statement holds at least for some 2-categories.

=--

+-- {: .num_remark}
###### Remark
Given an algebra $(X, u:TX\to X)$ , by (1) and (4) the action $u$ yields an isomorphism in $C^T$ between the free algebra $(TX, \mu_X)$ and $(X,u)$ i.e. for an idempotent monad the Eilenberg-Moore and the Kleisli categories coincide.
=--


## Properties
 {#Properties}

### Algebras for an idempotent monad and Localization
 {#AlgebrasForAnIdempotentMonad}

+-- {: .num_prop}
###### Proposition

Let $(T, \eta, \mu)$ be an idempotent monad on a category $E$. The following conditions on an object $e$ of $E$ are equivalent: 

1. The object $e$ carries an $T$-[[algebra for a monad|algebra structure]]. 

2. The [[unit of a monad|unit]] $\eta e\colon e \to T e$ is a [[split monomorphism]]. 

3. The [[unit of a monad|unit]] $\eta e$ is an [[isomorphism]]. 

(It follows from 3. that there is at most one algebra structure on $e$, given by $\xi = (\eta e)^{-1}\colon T e \to e$.) 

=-- 



+-- {: .proof} 
###### Proof 

The implication 1. $\Rightarrow$ 2. is immediate. Next, if $\xi\colon T e \to e$ is any retraction of $\eta e$, we have both $\xi \circ \eta e = 1_e$ and 
$$\array{
\eta e \circ \xi & = & (T \xi)(\eta T e) & & \text{naturality of}\, \eta \\
 & = & (T \xi)(T \eta e) & & \text{see definitions above} \\
 & = & T(\xi \circ \eta e) & & \text{functoriality} \\
 & = & 1_{T e} & & 
}$$
so 2. implies 3. Finally, if $\eta e$ is an isomorphism, put $\xi = (\eta e)^{-1}$. Then $\xi \circ \eta e = 1_e$ (unit condition), and the associativity condition for $\xi$, 

$$\xi \circ \mu e = \xi \circ T \xi,$$

follows by inverting the naturality equation $\eta T e \circ \eta e = T \eta e \circ \eta e$. Thus 3. implies 1. 

=-- 


+-- {: .num_remark #ReflectiveSubcategoryOfIdempotentMonad}
###### Remark

This means that the [[Eilenberg-Moore category]] of an [[idempotent monad]] is equivalently the [[reflective subcategory]] (a "[[localization]]" of the ambient category) whose embedding-reflection [[adjunction]] gives the idempotent monad.

=--

See also ([Borceux, volume 2, corollary 4.2.4](#Borceux)).

+-- {: .num_remark}
###### Remark

Hence [[duality|dually]] the co-algebras over an idempotent [[comonad]] form a [[coreflective subcategory]], hence a "co-localization" of the ambient category.

=--

+-- {: .num_remark}
###### Remark

In [[modal type theory]] one thinks of a (idempotent) (co-)monad as a (co-)[[modal operator]] and of its algebras as (co-)[[modal types]]. In this terminology the above says that categories of (co-)modal types are precisely the (co-)reflective [[localizations]] of the ambient type system.

=--

### The associated idempotent monad of a monad
 {#AssociatedIdemopotentMonad}

We discuss here how under suitable conditions, for every [[monad]] $T$ there is a "completion" to an idempotent monad $\tilde T$ in that the completion construction is [[right adjoint]] to the inclusion of idempotent monads into the category of all monads on a given category, exhibiting the subcategory of idempotent monads as a [[coreflective subcategory]]. Here $\tilde T$ inverts the same morphisms that $T$ does and hence exhibits the [[localization]] ([[reflective subcategory]]) at the $T$-equivalences, and in fact the factorization of any [[adjunction]] inducing $T$ through that localization ([Fakir 70](#Fakir70), [Applegate-Tierney 70](#ApplegateTierney70), [Day 74](#Day74) [Casacuberta-Frei 99](#CasacubertaFrei99). [Lucyshyn-Wright 14](#Lucyshyn-Wright14)).


\begin{theorem}\label{ExistenceOfIdempotentCore}
**([Fakir 70](#Fakir70))**
\linebreak
Let $C$ be a [[complete category|complete]], [[well-powered category]], and let $M\colon C \to C$ be a [[monad]] with [[unit of a monad|unit]] $u\colon 1 \to M$ and multiplication $m\colon M M \to M$. Then there is a universal idempotent monad, giving a [[right adjoint]] to the inclusion

$$IdempotentMonad(C) \hookrightarrow Monad(C)$$ 

\end{theorem}

+-- {: .proof} 
###### Proof

Given a [[monad]] $M$, define a [[functor]] $M'$ as the [[equalizer]] of $M u$ and $u M$:  

$$M' \hookrightarrow M \stackrel{\overset{u M}{\longrightarrow}}{\underset{M u}{\longrightarrow}} M M.$$ 

This $M'$ acquires a unique monad structure such that $M' \hookrightarrow M$ is a morphism of monads (see this [MathOverflow thread](http://mathoverflow.net/questions/147264/regarding-a-difficulty-in-the-fakir-article-about-associated-idempotent-triple/147272#147272) for some detailed discussion). It might not be an idempotent monad (although it will be if $M$ is [[left exact functor|left exact]]). However we can apply the process again, and continue transfinitely. Define $M_0 = M$, and if $M_\alpha$ has been defined, put $M_{\alpha+1} = M_{\alpha}'$; at limit ordinals $\beta$, define $M_\beta$ to be the inverse limit of the chain 

$$\ldots \hookrightarrow M_{\alpha} \hookrightarrow \ldots \hookrightarrow M$$

where $\alpha$ ranges over ordinals less than $\beta$. This defines the monad $M_\alpha$ inductively; below, we let $u_\alpha$ denote the [[unit of a monad|unit]] of this monad. 

Since $C$ is [[well-powered category|well-powered]] (i.e., since each object has only a small number of [[subobjects]]), the large limit 

$$E(M)(c) = \underset{\alpha \in Ord}{\lim} M_\alpha(c)$$ 

exists for each $c$. Hence the large limit $E(M) = \underset{\alpha \in Ord}{\lim} M_\alpha$ exists as an endofunctor. The underlying functor 

$$Monad(C) \to Endo(C)$$ 

reflects limits (irrespective of size), so $E = E(M)$ acquires a monad structure defined by the limit. Let $\eta\colon 1 \to E$ be the unit and $\mu\colon E E \to E$ the multiplication of $E$. For each $\alpha$, there is a monad map $\pi_\alpha\colon E \to M_\alpha$ defined by the limit projection. 

=--

+-- {: .num_lemma}
###### Lemma
$E$ is idempotent. 
=--

+-- {: .proof} 
###### Proof


For this it suffices to check that $\eta E = E \eta\colon E \to E E$. This may be checked objectwise. So fix an object $c$, and for that particular $c$, choose $\alpha$ so large that $\pi_\alpha (c)\colon E(c) \to M_\alpha(c)$ and $\pi_\alpha E(c)\colon E E(c) \to M_{\alpha} E(c)$ are isomorphisms. In particular, $\pi_\alpha \pi_\alpha(c)\colon E E (c) \to M_\alpha M_\alpha(c)$ is invertible. 

Now $u_\alpha M_\alpha(c) = M_{\alpha} u_{\alpha} c$, since $\pi_\alpha\colon E \to M_\alpha$ factors through the equalizer $M_{\alpha + 1} \hookrightarrow M_\alpha$. Because $\pi_\alpha$ is a monad morphism, we have 

$$\array{
\eta E(c) & = & (\pi_\alpha \pi_\alpha (c))^{-1} (u_\alpha M_\alpha(c))\pi_\alpha(c) \\
       & = & (\pi_\alpha \pi_\alpha (c))^{-1} (M_\alpha u_\alpha(c))\pi_\alpha(c) \\
       & = & E \eta(c)
}$$

as required. 

Finally we must check that $M \mapsto E(M)$ satisfies the appropriate universal property. Suppose $T$ is an idempotent monad with unit $v$, and let $\phi\colon T \to M$ be a monad map. We define $T \to M_\alpha$ by induction: given $\phi_\alpha\colon T \to M_\alpha$, we have 

$$(u_\alpha M_\alpha)\phi_\alpha = \phi_\alpha \phi_\alpha (v T) = \phi_\alpha \phi_\alpha (T v) = (M_\alpha u_{\alpha})\phi_\alpha$$ 

so that $\phi_{\alpha}$ factors uniquely through the inclusion $M_{\alpha + 1} \hookrightarrow M_\alpha$. This defines $\phi_{\alpha + 1}\colon T \to M_{\alpha + 1}$; this is a monad map. The definition of $\phi_\alpha$ at limit ordinals, where $M_\alpha$ is a limit monad, is clear. Hence $T \to M$ factors (uniquely) through the inclusion $E(M) \hookrightarrow M$, as was to be shown.  
=-- 

+-- {: .num_theorem #FactorizationOfIdempotentCore}
###### Theorem 

For 
$
  (L \dashv R)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{L}{\longrightarrow}}{\underset{R}{\longleftarrow}}
  \mathcal{D}
$
a pair of [[adjoint functors]] with induced [[monad]] $T = R\circ L$ on the complete and well-powered category $\mathcal{C}$, then the idempotent monad $\tilde T$ of theorem \ref{ExistenceOfIdempotentCore} corresponds via remark \ref{ReflectiveSubcategoryOfIdempotentMonad} to a [[reflective subcategory]] inclusion $\mathcal{C}_T \stackrel{i}{\hookrightarrow} \mathcal{C}$ which factors the original adjunction

$$
  (L\dashv R)
  \;\colon\;
  \mathcal{C}
    \stackrel{\overset{}{\longrightarrow}}{\underset{i}{\longleftarrow}}
  \mathcal{C}_T
    \stackrel{\overset{L'}{\longrightarrow}}{\underset{}{\longleftarrow}}
  \mathcal{D}
$$ 

such that $L'$ is a [[conservative functor]].

=--

([Lucyshyn-Wright 14, theorem 4.15](#LucyshynWright14))

+-- {: .num_remark #IdempotentFactorizationAndBousfieldLocalization}
###### Remark

The factorization in theorem \ref{FactorizationOfIdempotentCore} has its analog in [[homotopy theory]] in the concept of [[Bousfield localization of model categories]]: given a [[Quillen adjunction]]

$$
  (L \dashv R) 
  \;\colon\;
  \mathcal{C}
    \stackrel{\longrightarrow}{\longleftarrow}
  \mathcal{D}
$$

then (if it exists) the [[Bousfield localization of model categories|Bousfield localized]] [[model category]] structure $\mathcal{C}_W$ obtained from $\mathcal{C}$ by adding the $L$-weak equivalences factors this into two consecutive Quillen adjunctions of the form

$$
  \mathcal{C}
   \stackrel{\overset{id}{\longrightarrow}}{\underset{id}{\longleftarrow}}
  \mathcal{C}_{W}
    \stackrel{\overset{L}{\longrightarrow}}{\underset{R}{\longleftarrow}}
  \mathcal{D}
  \,.
$$

On the [[(∞,1)-categories]] [[presentable (∞,1)-category|presented]] by these model categories this gives a factorization of the [[derived functor|derived]] [[(∞,1)-adjunction]] through [[localization of an (∞,1)-category|localization]] onto a [[reflective sub-(∞,1)-category]] followed by a [[conservative (∞,1)-functor]].

=--

+-- {: .num_example}
###### Example

Let $A$ be a commutative ring, and let $f\colon A \to B$ be a flat (commutative) $A$-algebra. Then the [[forgetful functor]]

$$f^\ast = Ab^f\colon Ab^B \to Ab^A$$ 

from $B$-modules to $A$-modules has a [[left exact functor|left exact]] [[left adjoint]] $f_! = B \otimes_A -$. The induced monad $f^\ast f_!$ on the category of $B$-modules preserves [[equalizers]], and so its associated idempotent monad $T$ may be formed by taking the equalizer 

$$T(M) \to B \otimes_A M \stackrel{\overset{f^\ast f_! \eta M}{\longrightarrow}}{\underset{\eta f^\ast f_! M}{\longrightarrow}} B \otimes_A B \otimes_A M$$ 

=--

+-- {: .query}

(To be continued. This example is based on how Joyal and Tierney introduce effective descent for commutative ring homomorphisms, in An Extension of the Galois Theory of Grothendieck. I would like to consult that before going further -- Todd.) 

[[Mike Shulman]]: How about some examples of monads and their associated idempotent monads?

Do 2-monads have associated lax-, colax-, or pseudo-idempotent 2-monads?

=--
 
### Idempotent strong monads are commutative


\begin{theorem} 
Let $(\mathcal{C}, \otimes, I)$ be a monoidal category and let $(T, \mu, \eta)$ be an idempotent monad on $\mathcal{C}$ equipped with compatible left and right [[strong monad|strengths]] $t_{A, B} : TA \otimes B \to T(A \otimes B)$ and $t'_{A, B} : A \otimes TB \to T(A \otimes B)$. Then $T$ is a [[commutative monad]], or equivalently a [[monoidal monad]].
\end{theorem}

\begin{proof} 
The commutativity equation is obtained using the strength axioms, the monad axioms, and the fact that $\eta_T = T \eta$ for an idempotent monad:
\begin{tikzcd}[column sep=2em]
	{TA\otimes TB} && {TA \otimes TB} & {T(TA \otimes B)} & {T^2(A\otimes B)} && {T(A\otimes B)} \\
	& {T^2A\otimes TB} & {T(TA \otimes TB)} & {T^2(TA \otimes B)} & {T^3(A\otimes B)} & {T^2(A \otimes B)} \\
	{TA \otimes TB} & {T(A \otimes TB)} && {T^2(A\otimes B)} & {T^2(A \otimes B)} & {T^2(A \otimes B)} & {T(A \otimes B)}
	\arrow[Rightarrow, no head, from=1-1, to=3-1]
	\arrow[Rightarrow, no head, from=1-1, to=1-3]
	\arrow["t"', from=3-1, to=3-2]
	\arrow["\mu"', from=3-6, to=3-7]
	\arrow["{t'}", from=1-3, to=1-4]
	\arrow["{Tt}", from=1-4, to=1-5]
	\arrow["\mu", from=1-5, to=1-7]
	\arrow[Rightarrow, no head, from=1-7, to=3-7]
	\arrow["{T\eta \otimes TB}"{description}, from=3-1, to=2-2]
	\arrow["{\eta_T \otimes TB}"', from=1-3, to=2-2]
	\arrow["t"', from=2-2, to=2-3]
	\arrow["\eta"{description}, from=1-3, to=2-3]
	\arrow["{Tt'}", from=2-3, to=2-4]
	\arrow["{T\mu}", from=2-5, to=2-6]
	\arrow["\mu"', from=2-6, to=3-7]
	\arrow["{T^2t}", from=2-4, to=2-5]
	\arrow["\mu"{description}, from=2-5, to=3-6]
	\arrow["\eta"', from=1-7, to=2-6]
	\arrow["{T(\eta \otimes TB)}"{description}, from=3-2, to=2-3]
	\arrow["{Tt'}"', from=3-2, to=3-4]
	\arrow["{T^2(\eta \otimes B)}", from=3-4, to=2-4]
	\arrow["{T^2(\eta)}"{description}, from=3-4, to=2-5]
	\arrow[Rightarrow, no head, from=3-4, to=3-5]
	\arrow["{T(\eta_T)}"{description}, from=3-5, to=2-5]
	\arrow[Rightarrow, no head, from=3-5, to=3-6]
\end{tikzcd}
\end{proof}

Alternatively we can deduce this from the fact that that [[thunk-force category|thunkable]] morphisms are [[premonoidal category|central]], since a monad is idempotent iff every Kleisli map is thunkable, and a monad is commutative iff every Kleisli map is central. (This fact is proved by Paul Levy [there](https://www.cs.bham.ac.uk/~pbl/papers/thunkcentral.pdf).) 

\begin{theorem}
If furthermore $\mathcal{C}$ is a [[monoidal category with diagonals]] $\Delta_A : A \to A \otimes A$, then the induced [[monoidal monad]] structure on $T$ is [[idempotent monoidal functor|idempotent]] in the sense that the following diagram commutes:
\begin{tikzcd}
  TA & {TA \otimes TA} \\
  & {T(A \otimes A)}
  \arrow["{\Delta_{TA}}", from=1-1, to=1-2]
  \arrow[from=1-2, to=2-2]
  \arrow["{T\Delta_A}"', from=1-1, to=2-2]
\end{tikzcd}
\end{theorem}

\begin{proof}
See [1Lab](#1Lab), *Strong idempotent monads*.
\end{proof}

## Examples

* The free/forgetful adjunction between [[group | groups]] and [[abelian group | abelian groups]] generates an idempotent monad.  

## Related concepts

* [[idempotent monoid in a monoidal category]]

* [[idempotent adjunction]]

* [[reflective subcategory]]

* [[closure operator]], [[modality]]

* [[lax-idempotent 2-monad]]

* [[idempotent (∞,1)-monad]]

* The analog in [[model category]] theory of the localization at idempotent monad is the content of the [[Bousfield-Friedlander theorem]] ("[[Quillen idempotent monad]]").

## References
 {#References}

* [[Harry Appelgate]], [[Myles Tierney]], Section 6 in: *Categories with models*, p. 156-244 In: [[Beno Eckmann]] (ed.) *Seminar on Triples and Categorical Homology Theory* Lecture Notes in Mathematics, **80**, Springer  1969  ([doi:10.1007/BFb0083086](https://doi.org/10.1007/BFb0083086), [pdf](https://link.springer.com/content/pdf/10.1007/BFb0083086))

Textbook accounts:

* {#Borceux} [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_, vol.2, p. 196.

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_, A.4.3.11, p.194, B1.1.9, p.249

See also:
 
* [[Pierre Gabriel]], [[Michel Zisman]], _[[Calculus of fractions and homotopy theory]]_

The idempotent monad which exhibits the [[localization]] at the $T$-equivalences for a given monad $T$ is discussed in 

* {#ApplegateTierney70} [[Harry Applegate]], [[Myles Tierney]], _Iterated cotriples_, Lecture Notes in Math. **137** (1970) 56-99 ([doi:10.1007/BFb0060440](https://doi.org/10.1007/BFb0060440))

* {#Fakir70} S. Fakir, _Monade idempotente associ&#233;e &#224; une monade_, C. R. Acad. Sci. Paris Ser. A-B 270 (1970), A99-A101. ([gallica](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f103.image))

* {#Day74} [[Brian Day]], _On adjoint-functor factorisation_, Lecture Notes in Math. 420 (1974), 1-19. ([springer](https://link.springer.com/content/pdf/10.1007/BFb0063097.pdf))

* {#CasacubertaFrei99} [[Carles Casacuberta]], Armin Frei, _Localizations as idempotent approximations to completions_, Journal of Pure and Applied Algebra 142 (1999) 25--33 ([pdf](http://atlas.mat.ub.es/personals/casac/articles/cfre1.pdf))


and for [[enriched category theory]] in 

* {#LucyshynWright14} [[Rory Lucyshyn-Wright]], _Completion, closure, and density relative to a monad, with examples in functional analysis and sheaf theory_, Theory Appl. Cat. 29 (2014) 31, 896--928 [abs](http://emis.ams.org/journals/TAC/volumes/29/31/29-31abs.html) [arXiv:1406.2361](http://arxiv.org/abs/1406.2361) 

Discussion in [[algebraic topology]] ([[localization of a space|localization]], [[completion of a space|completion]]):

* [[John Frank Adams]], [[Zbigniew Fiedorowicz]], *Localisation and Completion with an addendum on the use of Brown-Peterson homology in stable homotopy*, based on 1973 lectures by Adams &lbrack;[arXiv:1012.5020](https://arxiv.org/abs/1012.5020)&rbrack; 


Extension of idempotent monads along subcategory inclusions is discussed in

* [[Carles Casacuberta]], Armin Frei, Tan Geok Choo, _Extending localization functors_ ,  Journal of Pure and Applied Algebra 103 (1995), 149-165 ([pdf](http://atlas.mat.ub.es/personals/casac/articles/cft.pdf))

* A. Deleanu, A. Frei, [[Peter Hilton|P. Hilton]], _Idempotent triples and completion_, Math. Z. **143** (1975) pp.91-104. ([pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN266833020_0143&divID=LOG_0014&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN266833020_0143%7C&targetFileName=PPN266833020_0143_LOG_0014.pdf&))

Discussion of idempotent comonads and their relation to adjoint strings is contained in

* {#RosebrughWood95} [[Robert Rosebrugh]], [[Richard Wood]] *Distributive adjoint strings*, Theory and applications of categories (1995) 119--145.

Formalisation in [[cubical Agda]]:

* {#1Lab} [[1lab]], *[Idempotent monads](https://1lab.dev/Cat.Diagram.Monad.Idempotent.html)*

[[!redirects idempotent monad]]
[[!redirects idempotent monads]]
[[!redirects idempotent comonad]]
[[!redirects idempotent comonads]]
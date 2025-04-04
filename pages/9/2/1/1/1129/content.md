
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}

## Definition

There is a very general notion of _injective objects_ in a [[category]] $C$, and then there is a sequence of more concrete notions as $C$ is equipped with more [[stuff, structure, property|structure and property]], in particular for $C$ an [[abelian category]] [[additive and abelian categories|or a relative]] thereof.

The concept of [[resolutions]] by injective objects -- [[injective resolutions]] -- is crucial notably in the discussion of [[derived functors]] (in the context of [[abelian categories]]: [[derived functors in homological algebra]]).

Being injective is a *property* of an object; the corresponding *structure* is called an [[algebraic injective]].

### General definition 

Let $C$ be a [[category]] and $J \subset Mor(C)$ a [[class]] of [[morphisms]] in $C$.  

+-- {: .num_example}
###### Example

Frequently $J$ is the class of all [[monomorphisms]] or a related class.  

This is notably the case for  $C$ is a [[category of chain complexes]] equipped with the injective [[model structure on chain complexes]] and $J$ is its class of [[cofibrations]].

=--

+-- {: .num_defn #InjectiveObjects}
###### Definition

An object $I$ in $C$ is **$J$-injective** if all diagrams of the form

$$
  \array{
    X &\to& I
    \\
    {}^{\mathllap{j \in J}}\downarrow 
    \\
    Z
  }
$$

admit an [[extension]]

$$
  \array{
    X &\to& I
    \\
    {}^{\mathllap{j \in J}}\downarrow & \nearrow_{\mathrlap{\exists}}
    \\
    Z
  }
  \,.
$$

If $J$ is the class of all [[monomorphisms]], we speak merely of an **injective object**.  

=--

\begin{remark}\label{InjectiveObjectsAsInjectiveMorphisms}
If $C$ has a [[terminal object]] $\ast$, then the $J$-injective objects $I$ according to def. \ref{InjectiveObjects} are those for which the unique morphism $I \stackrel{\exists!}{\to} \ast$ is a $J$-[[injective morphism]].
\end{remark}


+-- {: .num_defn #EnoughInjectives}
###### Definition

One says that a category $C$ has **enough injectives** if every object admits a [[monomorphism]] into an injective object.


=--

(The [[formal duality|dual]] notion is that of a *[[projective object]]*.)


Assuming the [[axiom of choice]], we have the following easy result:

+-- {: .num_prop}
###### Proposition 

Any [[small set|small]] [[Cartesian product]] of injective objects is injective. 

=--

+-- {: .num_remark}
###### Remark


If $C$ has a [[terminal object]] $*$ then these extensions are equivalently [[lifts]]

$$
  \array{
    X &\longrightarrow& I
    \\
    \mathllap{{}^{j \in J}}
    \big\downarrow 
    & 
    \nearrow_{\mathrlap{\exists}}
    &
    \big\downarrow
    \\
    Z
    &\longrightarrow&
    *
  }
$$

and hence the $J$-injective objects are precisely those that have the [[right lifting property]] against the class $J$.

=--

+-- {: .num_remark}
###### Remark

If $C$ is a [[locally small category]] then $I$ is $J$-injective precisely if the [[hom-functor]]

$$
  Hom_C(-,I) 
  \,\colon\, 
  C^{op} \longrightarrow Set
$$

takes morphisms in $J$ to [[epimorphism]]s in [[Set]].

=--



### In abelian categories 

The term _injective object_ is used most frequently in the context that $C$ is an [[abelian category]].  

+-- {: .num_prop}
###### Proposition


For $C$ an [[abelian category]] the class $J$ of monomorphisms is the same as the class of morphisms $f : A \to B$ such that $0 \to A \stackrel{f}{\to} B$ is [[exact sequence|exact]].  

=--

+-- {: .proof}
###### Proof

By definition of [[abelian category]] every monomorphism $A \hookrightarrow B$ is a [[kernel]], hence a [[pullback]] of the form

$$
  \array{
    A &\to& 0
    \\
    \downarrow && \downarrow
    \\
    B &\to& C
  }
$$

for $0$ the (algebraic) [[zero object]]. By the <a href="http://ncatlab.org/nlab/show/pullback#Pasting">pasting law</a> for pullbacks we find that also the left square in 

$$
  \array{
    0 &\to& A &\to& 0
    \\
    \downarrow && \downarrow && \downarrow
    \\
    0 &\to& B &\to& C
  }
$$

is a pullback, hence $0 \to A \to B$ is exact.

=--

+-- {: .num_cor #EquivalentCharacterizationOfInjectivesInAbelianCategories}
###### Corollary

An [[object]] $I$ of an abelian category $C$ is then **injective** if it satisfies the following equivalent conditions:

* the [[hom-functor]] $Hom_C(-, I) : C^{op} \to \mathscr{Ab}$ is [[exact functor|exact]] where $\mathscr{Ab}$ is the category of abelian groups;

* for all [[morphism]]s $f : X \to Y$ such that $0 \to X \to Y$ is [[exact sequence|exact]] and for all $k : X \to I$, there exists $h : Y \to I$ such that $ h\circ f = k$.

$$
  \array{
    0 &\to& X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{\mathrlap{k}} & \swarrow_{\mathrlap{\exists h}}
    \\
    &&
    I 
  }
  \,.
$$

=--

By the [[formal dual]] of [this prop.](projective+module#NProjectiveIFFHomNExact).

### In chain complexes

See [[homotopically injective object]] for a relevant generalization to categories of chain complexes, and its relationship to ordinary injectivity.


## Examples

### Injective modules
 {#InjectiveModules}

Let $R$ be a [[commutative ring]] and  $C = R Mod$ the category of $R$-[[modules]]. We discuss [[injective modules]] over $R$ (see there for more).

The following criterion says that for identifying [[injective modules]] it is sufficient to test the [[right lifting property]] which characterizes injective objects by def. \ref{InjectiveObjects}, only on those [[monomorphisms]] which include an [[ideal]] into the base ring $R$.

+-- {: .num_theorem #BaerTheorem}
###### Proposition 
**([[Baer's criterion]])**

If the [[axiom of choice]] holds, 
then a [[module]] $Q \in R Mod$ is an [[injective module]] precisely if for $I$ any left $R$-[[ideal]] regarded as an $R$-module, any [[homomorphism]] $g : I \to Q$ in $C$ can be extended to all of $R$ along the inclusion $I \hookrightarrow R$.

=-- 

This is due to ([Baer](#Baer)).

+-- {: .proof} 
###### Sketch of proof 

Let $i \colon M \hookrightarrow N$ be a [[monomorphism]] in $R Mod$, and let $f \colon M \to Q$ be a map. We must extend $f$ to a map $h \colon N \to Q$. Consider the [[poset]] whose elements are pairs $(M', f')$ where $M'$ is an intermediate [[submodule]] between $M$ and $N$ and $f' \colon M' \to Q$ is an extension of $f$, ordered by $(M', f') \leq (M'', f'')$ if $M''$ contains $M'$ and $f''$ extends $f'$. By an application of [[Zorn's lemma]], this poset has a [[maximal element]], say $(M', f')$. Suppose $M'$ is not all of $N$, and let $x \in N$ be an element not in $M'$; we show that $f'$ extends to a map $M'' = \langle x \rangle + M' \to Q$, a [[contradiction]]. 

The set $\{r \in R: r x \in M'\}$ is an ideal $I$ of $R$, and we have a module [[homomorphism]] $g \colon I \to Q$ defined by $g(r) = f'(r x)$. By [[hypothesis]], we may extend $g$ to a module map $k \colon R \to Q$. Writing a general element of $M''$ as $r x + y$ where $y \in M'$, it may be shown that 

$$f''(r x + y) = k(r) + f'(y)$$ 

is well-defined and extends $f'$, as desired. 
=-- 

+-- {: .num_corollary #DirectSumInjectives}
###### Corollary
(Assume that the [[axiom of choice]] holds.) Let $R$ be a [[Noetherian ring]], and let $\{Q_j\}_{j \in J}$ be a collection of [[injective modules]] over $R$. Then the [[direct sum]] $Q = \bigoplus_{j \in J} Q_j$ is also injective. 
=-- 

+-- {: .proof}
###### Proof 

By Baer's criterion, theorem \ref{BaerTheorem}, it suffices to show that for any [[ideal]] $I$ of $R$, a module [[homomorphism]] $f \colon I \to Q$ extends to a map $R \to Q$. Since $R$ is Noetherian, $I$ is [[finitely generated module|finitely generated]] as an $R$-module, say by elements $x_1, \ldots, x_n$. Let $p_j \colon Q \to Q_j$ be the [[projection]], and put $f_j = p_j \circ f$. Then for each $x_i$, $f_j(x_i)$ is nonzero for only finitely many summands. Taking all of these summands together over all $i$, we see that $f$ factors through 

$$\prod_{j \in J'} Q_j = \bigoplus_{j \in J'} Q_j \hookrightarrow Q$$ 

for some finite $J' \subset J$. But a [[product]] of injectives is injective, hence $f$ extends to a map $R \to \prod_{j \in J'} Q_j$, which completes the proof. 

=-- 

+-- {: .num_prop}
###### Proposition

Conversely, $R$ is a [[Noetherian ring]] if [[direct sums]] of injective $R$-[[modules]] are injective. 

=--

This is due to Bass and Papp. See ([Lam, Theorem 3.46](#Lam)).

### Injective abelian groups

Let $C = \mathbb{Z} Mod \simeq $ [[Ab]]  be the [[abelian category]] of [[abelian groups]]. 

+-- {: .num_prop #InjectiveAbelianGroupIsDivisibleGroup}
###### Proposition

If the [[axiom of choice]] holds, 
then an [[abelian group]] $A$ is an injective object in [[Ab]] precisely if it is a [[divisible group]], in that for all [[integers]] $n \in \mathbb{N}$ we have $n G = G$.

=--

This follows for instance using [[Baer's criterion]], prop. \ref{BaerTheorem}.

An explicit proof is spelled out at 
[Planet math -- abelian group is divisible if and only if it is an injective object](https://planetmath.org/abeliangroupisdivisibleifandonlyifitisaninjectiveobject)


+-- {: .num_example}
###### Example

By prop. \ref{InjectiveAbelianGroupIsDivisibleGroup} the following [[abelian groups]] are injective in [[Ab]].

The group of [[rational numbers]] $\mathbb{Q}$ is injective in [[Ab]], as is the additive group of [[real numbers]] $\mathbb{R}$ and generally that underlying any [[field]] of characteristic zero. The additive group underlying any [[vector space]] is injective. The [[quotient]] of any injective group by any other group is injective.

=--

+-- {: .num_example}
###### Example

**Not** injective in [[Ab]] is for instance the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ for $n \gt 1$.

=--

### In toposes 

In any [[topos]], the [[subobject classifier]] $\Omega$ is an injective object, as is any [[powering|power]] of $\Omega$ ([[Mac Lane-Moerdijk]], IV.10). 

Also one can define various notions of *internally* injective objects. These turn out to be equivalent:

+-- {: .num_prop #EquivalenceOfInternalNotionsOfInjectivity}
###### Proposition

In any [[elementary topos]] $\mathcal{E}$ with a [[natural numbers object]], the following statements about an object $I \in \mathcal{E}$ are equivalent.

1. The functor $[-, I] : \mathcal{E}^op \to \mathcal{E}$ maps monomorphisms in $\mathcal{E}$ to epimorphisms.
2. The functor $[-, I] : \mathcal{E}^op \to \mathcal{E}$ maps monomorphisms in $\mathcal{E}$ to morphisms for which any global element of the target locally (after [[change of base]] along an epimorphism) possesses a preimage.
3. For any morphism $p : A \to 1$ in $\mathcal{E}$, the object $p^*I$ has property 1. as an object of $\mathcal{E}/A$.
4. For any morphism $p : A \to 1$ in $\mathcal{E}$, the object $p^*I$ has property 2. as an object of $\mathcal{E}/A$.
5. The interpretation of the statement "$I$ is an injective object" using the [[stack semantics]] of $\mathcal{E}$ holds.

=--

+-- {: .proof}
###### Proof

The implications "1. $\Rightarrow$ 2.", "3 $\Rightarrow$ 4.", "3. $\Rightarrow$ 1.", and "4. $\Rightarrow$ 2." are trivial.

The equivalence "3. $\Leftrightarrow$ 5." follows directly from the interpretation rules of the stack semantics.

The implication "2. $\Rightarrow$ 4." employs the [[base change#GeometricMorphism|extra left-adjoint]] $p_! : \mathcal{E}/A \to \mathcal{E}$ to $p^* : \mathcal{E} \to \mathcal{E}/A$, as in the usual proof that injective sheaves remain injective when restricted to smaller open subsets: We have that $p_* \circ [-, p^*I]_{\mathcal{E}/A} \cong [-, I]_{\mathcal{E}} \circ p_!$, the functor $p_!$ preserves monomorphisms, and one can check that $p_*$ reflects the property that global elements locally possess preimages. Details are in ([Harting, Theorem 1.1](#Harting)).

The implication "4. $\Rightarrow$ 3." follows by performing an extra change of base, since any non-global element becomes a global element after a suitable change of base.

=--

Somewhat surprisingly, and in stark contrast with the situation for [[internally projective objects]], internal injectivity coincides with external injecticity.

+-- {: .num_prop #EquivalenceOfInternalAndExternalInjectivity}
###### Proposition

Let $\mathcal{E}$ be the topos of [[sheaves]] over a [[locale]]. Then an object $I \in \mathcal{E}$ is internally injective (in any of the senses given by Proposition \ref{EquivalenceOfInternalNotionsOfInjectivity}) if and only if $I$ is injective as in Definition \ref{InjectiveObjects}.

=--

+-- {: .proof}
###### Proof

Let $I$ be an externally injective object. Then $I$ satisfies condition 2. of Proposition \ref{EquivalenceOfInternalNotionsOfInjectivity}, even without having to pass to a cover.

Conversely, let $I$ be an internally injective object. Let $m : X \to Y$ be a monomorphism and let $k : X \to I$ be an arbitrary morphism. We want to show that there exists an extension $Y \to I$ of $k$ along $m$. To this end, consider the sheaf
$$ F \coloneqq \{ k' : \mathcal{H}om(Y,I) | k' \circ m = k \}. $$
One can check that $F$ is [[flabby sheaf|flabby]] (this is particularly easy using the [[internal language]], details will be added later) and therefore has a global section.

=--

+-- {: .num_remark}
###### Remark

The analogs of Proposition \ref{EquivalenceOfInternalNotionsOfInjectivity} and Proposition \ref{EquivalenceOfInternalAndExternalInjectivity} for abelian group objects instead of unstructured objects hold as well, with mostly the same proofs. Condition 1. then refers to the functor $[-, X] : Ab(\mathcal{E})^op \to Ab(\mathcal{E})$.

=--
### In topological spaces 

In the category [[Top]] of all topological spaces, the injective objects are precisely the [[inhabited set|inhabited]] [[indiscrete spaces]]. 

In the category of $T_0$ spaces (see [[separation axiom]]), the injective objects are the terminal spaces.

In the above two cases, this refers to injectivity with respect to monomorphisms.

In the category of $T_0$ spaces, the injective objects with respect to homeomorphic embeddings are precisely those given by [[Scott topologies]] on [[continuous lattices]]; as [[locales]] these are [[local compactum|locally compact]] and [[spatial locale|spatial]]. (Such spaces are usually called, perhaps confusingly, *injective spaces*.) 

In the category of all spaces, the injectives with respect to homeomorphic embeddings (i.e., [[regular monomorphisms]]) are the spaces whose $T_0$ reflections are continuous lattices under the Scott topology.

### In Boolean algebras 

Injective objects in the category of [[Boolean algebras]] are precisely [[complete Boolean algebras]]. This is the dual form of a theorem of Gleason, saying that the [[projective objects]] in the category of [[Stone spaces]] are the [[extremally disconnected topological space|extremally disconnected]] ones (the closure of every open set is again open). 

## Properties

### Preservation of injective objects

+-- {: .num_lemma #RightAdjointsOfExactFunctorsPreserveInjectives}
###### Lemma

Given a pair of [[additive functor|additive]] [[adjoint functors]]

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{B}
    \stackrel{\overset{L}{\longleftarrow}}{\underset{R}{\longrightarrow}}
  \mathcal{A}
$$

between [[abelian categories]] such that the [[left adjoint]] $L$ is a [[left exact functor]] (thus automatically exact), then the [[right adjoint]] preserves injective objects.

=--

+-- {: .proof}
###### Proof

Observe that an object is injective precisely if the [[hom-functor]] into it sends [[monomorphisms]] to [[epimorphisms]], and that $L$ preserves monomorphisms by assumption of (left-)exactness. With this the statement follows via adjunction isomorphism

$$
  Hom_{\mathcal{A}}(-,R(I))\simeq Hom_{\mathcal{B}}(L(-),I)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Additivity of the left adjoint follows from the remaining assumptions, since [[additive functor#SufficientConditions|exact functors preserve biproducts]].

=--

The preceding lemma has the following variant:

+-- {: .num_prop #Adjuncts_Injectives}
###### Proposition
Let $\mathcal{C}$, $\mathcal{D}$ be categories and $L\dashv R:\mathcal{D}\to\mathcal{C}$ be an adjunction. If $L$ maps monos to monos, then $R$ maps injectives to injectives.
=--

+-- {: .proof}
###### Proof
Let $I\in\mathcal{D}$ be injective. Consider the following diagram in $\mathcal{C}$:

$$
\array{
A & \overset{m}{\rightarrowtail} & B
\\
f\downarrow &    &
\\
R(I) &   &
}
$$

Let $\theta: Hom_\mathcal{C}(X,R(Y))\overset{\simeq}{\rightarrow}Hom_\mathcal{D}(L(X),Y)$ the natural bijection given by the adjunction. Consider now the following diagram in $\mathcal{D}$ where the assumptions ensure that $L(m)$ is mono:

$$
\array{
L(A) & \overset{L(m)}{\rightarrowtail} & L(B)
\\
\theta(f)\downarrow &    &
\\
I &   &
}
$$
Since $I$ is injective, there there exists a filler $\theta(g):L(B)\to I$ which by the adjunction must come from a uniquely determined $g:B\to R(I)$. But the naturality of the bijection with respect to composition says that

\[
\frac{L(A)\overset{L(m)}{\rightarrowtail} L(B)\overset{\theta(g)}{\rightarrow}I}{A\overset{m}{\rightarrowtail} B\overset{g}{\rightarrow}R(I)}
\]

correspond to each other under the bijection whence $\theta(g\circ m)=\theta(g)\circ L(m)$ but from the commutativity of the second diagram we have $\theta(g)\circ L(m)=\theta(f)=\theta(g\circ m)$. Since $\theta$ is a bijection it follows that $f=g\circ m$ which proves that $R(I)$ is injective.

=--

+-- {: .num_remark}
###### Remark

The proof transposes the proof of the dual statement 10.2. in  ([Hilton-Stammbach 1971](#HiltonStammbach71), p. 82): In situation $L\dashv R$, if $R$ maps epis to epis then $L$ maps projectives to projectives.

=--

+-- {: .num_remark #Exponential_injectives}
###### Remark
Let $X\in\mathcal{C}$ such that ${}_-\times:\mathcal{C}\to\mathcal{C}$ exists and has a right adjoint ${}_-\times X\dashv (_-)^X$. Since it is easy to check that ${}_-\times X$ preserves monos it follows that $(_-)^X$ preserves injectives.

In particular, for toposes this implies that all power objects $\Omega^X$ are injective since the injectivity of $\Omega$ follows more or less straightforwardly from its classifying properties.
=--

### Existence of enough injectives
 {#ExistenceOfEnoughInjectives}

We discuss a list of classes of categories that have _enough injectives_
according to def. \ref{EnoughInjectives}.

+-- {: .num_prop}
###### Proposition

Every [[topos]] has enough injectives.  

=--

+-- {: .proof}
###### Proof

Every [[power object]] can be shown to be injective (cf. the above [remark](#Exponentials_injectives)), and every object embeds into its power object by the "singletons" map.

=--

+-- {: .num_prop #AbHasEnoughInjectives}
###### Proposition

Assuming some form of the [[axiom of choice]], the category of [[abelian groups]] has enough injectives.  

=--

Full AC is much more than required, however; [[small violations of choice]] suffices.

+-- {: .proof} 
###### Proof 

By prop. \ref{InjectiveAbelianGroupIsDivisibleGroup} an [[abelian group]]
is an injective $\mathbb{Z}$-module precisely if it is a [[divisible group]]. So we need to show that every [[abelian group]] is a [[subgroup]] of a [[divisible group]].

To start with, notice that the group $\mathbb{Q}$ of [[rational numbers]] is divisible and hence the canonical embedding $\mathbb{Z} \hookrightarrow \mathbb{Q}$ shows that the additive group of [[integers]] embeds into an injective $\mathbb{Z}$-module.

Now by the discussion at _[[projective module]]_ every [[abelian group]] $A$ receives an [[epimorphism]] $(\oplus_{s \in S} \mathbb{Z}) \to A$ from a [[free group|free]] abelian group, hence is the [[quotient group]] of a [[direct sum]] of copies of $\mathbb{Z}$. Accordingly it embeds into a quotient $\tilde A$ of a direct sum of copies of $\mathbb{Q}$.

$$
  \array{
    ker &\stackrel{=}{\to}& ker 
    \\
    \downarrow && \downarrow
    \\
    (\oplus_{s \in S} \mathbb{Z}) &\hookrightarrow& (\oplus_{s \in S} \mathbb{Q})
    \\
    \downarrow && \downarrow
    \\
    A &\hookrightarrow& \tilde A
  }
$$

Here $\tilde A$ is divisible because the [[direct sum]] of divisible groups is again divisible, and also the [[quotient group]] of a divisible groups is again divisble. So this exhibits an embedding of any $A$ into a divisible abelian group, hence into an injective $\mathbb{Z}$-module.


=--


+-- {: .num_lemma #TransferOfEnoughInjectivesAlongAdjunctions}
###### Lemma

Given a pair of [[additive functor|additive]] [[adjoint functors]]

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{B}
    \stackrel{\overset{L}{\longleftarrow}}{\underset{R}{\longrightarrow}}
  \mathcal{A}
$$

between [[abelian categories]] such that the [[left adjoint]] $L$ is 

1. an [[exact functor]],

1. a [[faithful functor]]. 

Then if $\mathcal{B}$ has enough injectives, also $\mathcal{A}$ has enough injectives.

=--

+-- {: .proof}
###### Proof

Consider $A \in \mathcal{A}$. By the assumption that $\mathcal{B}$ has enough injectives, there is an injective object $I \in \mathcal{B}$ and a monomorphism $i \colon L(A) \hookrightarrow I$. The [[adjunct]] of this is a morphism

$$
  \tilde i \colon A \longrightarrow R(I)
$$

and so it is sufficient to show that

1. $R(I)$ is injective in $\mathcal{A}$;

1. $\tilde i$ is a monomorphism.

The first point is the statement of lemma \ref{RightAdjointsOfExactFunctorsPreserveInjectives}.

For the second point, consider the [[kernel]] of $\tilde i$ as part of the [[exact sequence]]

$$
  ker(\tilde i)\longrightarrow A \stackrel{\tilde i}{\longrightarrow} R(I)
  \,.
$$

By the assumption that $L$ is an [[exact functor]], the image of this sequence under $L$ is still exact

$$
  L(ker(\tilde i)) \longrightarrow L(A) \stackrel{L(\tilde i)}{\longrightarrow} L(R(I))
  \,.
$$

Now observe that $L(\tilde i)$ is a monomorphism: this is because its composite $L(A) \stackrel{L(\tilde i)}{\longrightarrow} L(R(I)) \stackrel{\epsilon}{\longrightarrow} I$ with the [[adjunction unit]] is (by the formula for [[adjuncts]]) the original morphism $i$, which by construction is a monomorphism. Therefore the exactness of the above sequence means that $L(ker(\tilde i)) \to L(A)$ is the [[zero morphism]]; and by the assumption that $L$ is a [[faithful functor]] this means that already $ker(\tilde i) \to A$ is zero, hence that $ker(\tilde i) = 0$, hence that $\tilde i$ is a monomorphism.

=--

+-- {: .num_prop #RModHasEnoughInjectives}
###### Proposition

As soon as the category [[Ab]] of [[abelian groups]] has enough injectives, so does the [[abelian category]] $R$[[Mod]] of [[modules]] over some [[ring]] $R$.  

In particular if the [[axiom of choice]] holds, then $R Mod$ has enough injectives.

=--

+-- {: .proof}
###### Proof

Observe that the [[forgetful functor]] $U\colon R Mod \to AbGp$ has both a [[left adjoint]] $R_!$ ([[extension of scalars]] from $\mathbb{Z}$ to $R$) and a right adjoint $R_*$ ([[coextension of scalars]]).  Since it has a left adjoint, it is [[exact functor|exact]]. Thus the statement follows via lemma \ref{TransferOfEnoughInjectivesAlongAdjunctions} from prop. \ref{AbHasEnoughInjectives}.

=--

+-- {: .num_prop}
###### Proposition

For $R = k$ a [[field]], hence $R$[[Mod]] = $k$[[Vect]], every object is both injective as well as [[projective object|projective]].

=--

+-- {: .num_prop #AbelianSheavesHaveEnoughProjectives}
###### Proposition

The category of [[abelian sheaves]] $Ab(Sh(C))$ on any [[small site]] $C$, hence the category of abelian groups in the [[sheaf topos]] over $C$, has enough injectives.

=--

A proof of can be found in [[Peter Johnstone]]'s book *Topos Theory*, p261.

+-- {: .num_remark}
###### Remark

This is in stark contrast to the situation for [[projective objects]], which generally do not exist in categories of sheaves.  

=--

+-- {: .num_cor}
###### Corollary

The category of sheaves of modules over any [[sheaf of rings]] on any [[small site]] also enough injectives.

=--

+-- {: .proof}
###### Proof

Combining prop. \ref{AbelianSheavesHaveEnoughProjectives} with prop. \ref{AbHasEnoughInjectives} (which relativizes to any topos).  

=--

This slick proof of this important fact was pointed out by [[Colin McLarty]] in an email to the categories list dated 10 Oct 2010.


### Injective resolutions
 {#InjectiveResolutions}

+-- {: .num_prop}
###### Proposition

Let $\mathcal{A}$ be an [[abelian category]]. Then for every object
$X \in \mathcal{A}$ there is an [[injective resolution]], hence
a [[chain complex]]

$$
  J^\bullet = [J^0 \to \cdots \to J^n \to \cdots] \in Ch_(\mathcal{A})
$$ 

equipped with a a [[quasi-isomorphism]] of [[cochain complexes]]  $X \stackrel{\sim}{\to} J^\bullet$

$$
  \array{
    X &\to& 0 &\to& \cdots &\to& 0 &\to& \cdots
    \\
    \downarrow && \downarrow && && \downarrow
    \\
    J^0 &\to& J^1 &\to& \cdots &\to& J^n &\to& \cdots
  }
  \,.
$$

=--


## Related concepts

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

* **injective object**, [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[algebraically injective object]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]

* [[orthogonality]]

## References

The notion of [[injective modules]] was introduced in 

* {#Baer}R. Baer, _Abelian groups that are direct summands of every containing abelian group_ , Bulletin AMS **46** no. 10 (1940) pp.800-806. ([projecteuclid](http://projecteuclid.org/euclid.bams/1183503234))
 

The dual notion of [[projective modules]] was considered explicitly only much later in

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], *[[Homological Algebra]]*, Princeton Univ. Press (1956), Princeton Mathematical Series **19** (1999) &lbrack;[ISBN:9780691049915](https://press.princeton.edu/books/paperback/9780691049915/homological-algebra-pms-19-volume-19), [doi:10.1515/9781400883844](https://doi.org/10.1515/9781400883844), [pdf](http://www.math.stonybrook.edu/~mmovshev/BOOKS/homologicalalgeb033541mbp.pdf)&rbrack;
 

Textbook accounts:

* {#HiltonStammbach71} [[Peter Hilton]],  [[Urs Stammbach]], p. 30 in: _A course in homological algebra_, Springer-Verlag, New York, 1971, Graduate Texts in Mathematics, Vol. 4 ([doi:10.1007/978-1-4419-8566-8](https://link.springer.com/book/10.1007/978-1-4419-8566-8), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/hilton-stammbach.pdf))

(used, e.g., for the proof of [Lemma](#Adjuncts_Injectives)); 


* [[Masaki Kashiwara]], [[Pierre Schapira]], sections 9.5, 14.1 of:_[[Categories and Sheaves]]_


Using tools from the theory of [[accessible categories]], injective objects are discussed in

* [[Jiri Rosicky]], _Injectivity and accessible categories_ ([ps](http://www.math.muni.cz/~rosicky/papers/acc5.ps))

[Baer's criterion](#Baer) is discussed in many texts, for example 

* N. Jacobsen, _Basic Algebra II_, W.H. Freeman and Company, 1980. 

See also 

* 
{#Lam} T.-Y. Lam, _Lectures on modules and rings_, Graduate Texts in Mathematics 189, Springer Verlag (1999). 

For injective objects in a [[topos]] see

* [[Francis Borceux]], _Handbook of Categorical Algebra vol. 3_ , Cambridge UP 1994. (section 5.6, pp.314-315)

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], _Sheaves in geometry and Logic_ , Springer Heidelberg 1994. (section IV.10, pp.210-213)

* D. Higgs, _Injectivity in the topos of complete Heyting algebra valued sets_ , Can. J. Math. **36** (1984) pp.550-568. ([pdf](http://cms.math.ca/openaccess/cjm/v36/cjm1984v36.0550-0568.pdf))

* [[Peter Johnstone]], [[Fred Linton]], [[Robert Paré]], _Injective Objects in Topoi II: Connections with the axiom of choice_ , pp.207-216 in LNM **719** Springer Heidelberg 1979.


* T. Kenney, _Injective Power Objects and the Axiom of Choice_ ,  JPAA **215** (2011) pp.131&#8211;144.

* [[Fred Linton]], _Injective Objects in Topoi III: Stability under coproducts_ , Bull. Acad. Polon. Sci. S&#233;r. Sci. Math. Astronom. Phys. **29** (1981) pp.341-347.

* [[Fred Linton]], [[Robert Paré]], _Injective Objects in Topoi I: Representing coalgebras as algebras_ , pp.196-206 in LNM **719** Springer Heidelberg 1979.

Discussion of injective objects ([[types]]) in [[homotopy type theory]]:

* {#Escardo19} [[Martín Escardó]], _Injectives types in univalent mathematics_ ([arXiv:1903.01211](https://arxiv.org/abs/1903.01211))

For a detailed discussion of internal notions of injectivity see

* {#Harting} Roswitha Harting, _Locally injective abelian groups in a topos_, Communications in Algebra 11 (4), 1983.

For injective toposes in the 2-category of [[bounded topos|bounded toposes]] see

* [[Peter Johnstone]], _Injective Toposes_ , pp.284-297 in LNM **871** Springer Heidelberg 1981.

* [[Peter Johnstone]], _Sketches of an Elephant vol. 2_ , Cambridge UP 2002. (section C4.3, pp.738-745)


[[!redirects injective objects]]

[[!redirects enough injectives]]

[[!redirects injective type]]
[[!redirects injective types]]

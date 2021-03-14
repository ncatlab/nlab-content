
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Separators
* table of contents
{: toc}

## Idea

An [[object]] $S$ (or family $\mathcal{S}$ of objects) in a [[category]] $\mathcal{C}$ is called a _separator_ or _generator_ if [[generalized elements]] with [[domain]] $S$ (or domain from $\mathcal{S}$) are sufficient to distinguish [[morphisms]] in $\mathcal{C}$.

The [[duality|dual]] notion is that of a _[[coseparator]]_.


## Caution on terminology {#Terminology}

The term 'generator' is slightly more ambiguous because of the use of 'generators' in [[generators and relations]]. That said, there is a link between these two senses provided by theorem \ref{motive} (q.v.). 


## Definitions

+-- {: .num_defn}
###### Definition

An [[object]] $S \in \mathcal{C}$ of a [[category]] $\mathcal{C}$ is called a __separator__ or a __generator__ or a __separating object__ or a __generating object__, or is said to __separate morphisms__ if:

* for every pair of [[parallel morphisms]] $f,g \colon X \to Y$ in $\mathcal{C}$, if $f\circ e = g\circ e$ for every morphism $e\colon S \to X$, then $f = g$

=--

Equivalently, we have that $S$ is a separator if, for every object $X$ in $\mathcal{C}$, morphisms $f:S\rightarrow X$ are [[jointly epimorphic family|jointly epic]]. Assuming that $\mathcal{C}$ is [[locally small|locally small category]], we have equivalently that $S$ is a separator if the [[hom functor]] $Hom(S,-) \colon \mathcal{C} \to $ [[Set]] is [[faithful functor|faithful]].


More generally:

+-- {: .num_defn}
###### Definition

A [[family]] $\mathcal{S} = (S_a)_{(a\colon A)}$ of [[objects]] of a [[category]] $\mathcal{C}$ is a __separating family__ or a __generating family__ if:

* for every pair of [[parallel morphisms]] $f,g \colon X \to Y$ in $\mathcal{C}$, if $f \circ e = g \circ e$ for every $e \colon S_a \to X$ sourced in the family, then $f = g$.
=--

Assuming again that $\mathcal{C}$ is [[locally small category|locally small]], we have equivalently that $\mathcal{S}$ is a separating family if the family of [[hom functors]] $Hom(U_a,-) \colon \mathcal{C} \to $ [[Set]] is [[jointly faithful family of functors|jointly faithful]].

Since repetition is irrelevant in a separating family, we may also speak of a _separating [[class]]_ instead of a separating family.

+-- {: .num_defn}
###### Definition

A __separating set__ is a [[size issues|small]] separating class.
=--

### In fibered categories {#fibered}

The notion of separating family can be generalized from categories to [[fibered categories]] in such a way that the [[family fibration]] of a category $\mathbf{C}$ 
has a separating family if and only if $\mathbf{C}$ has a small separating family.
+-- {: .num_defn}
###### Definition
A separating family in a [[fibered category]] $P:\mathbf{E}\to \mathbf{B}$ is an object $S\in \mathbf{E}$ such that for every parallel pair $f,g:A\to B$ in $E$ with $f\neq g$ and $P(f) = P(g)$ there exist arrows $c: X\to S$ and $h:X\to A$ (constituting a span) such that $c$ is $P$-cartesian, and $f h \neq g h$ .
=--

See Definition B2.4.1 in the [[Elephant]].

## Examples and applications

* In [[Set]], any [[inhabited set]] is a separator; in particular, the [[point]] is a separator.

*  More generally, in any [[well-pointed category]], any [[terminal object]] is a separator.  More generally still, in any represented [[concrete category]], the representing object is a separator.

* The standard example of a separator in the category of $R$-[[modules]] over a [[ring]] $R$ is any [[free module]] $R^I$ (for $I$ an [[inhabited set]]) and $R$ (which is $R^I$ for $I$ a [[point]]) in particular.  If a separator is a finitely generated [[projective object]] in the category of $R$-modules, then one sometimes says (especially in the older literature, e.g. Freyd's *Abelian Categories*) that the separator is a _progenerator_.  Progenerators are important in classical Morita theory, see [[Morita equivalence]].


* The existence of a small separating family is one of the conditions in [[Giraud's theorem]] characterizing [[Grothendieck topos]]es.

* The existence of a small (co)separating family is one of the conditions in one version of the [[adjoint functor theorem]].


## Strengthened separators

+-- {: .num_theorem #motive}
###### Motivating theorem

If $C$ is [[locally small category|locally small]] and has all small [[coproduct]]s, then a set-indexed family $(S_a)_{(a\colon A)}$  is separating  if and only if, for every $X\in C$, the canonical morphism
$$ \varepsilon_X\colon \coprod_{a\colon A, f\colon S_a \to X} S_a \longrightarrow X $$
is an [[epimorphism]].
=--

This theorem explains a likely origin of the term "generator" or "generating family". For example, in linear algebra, one says that a set of morphisms $f_a: S_a \to X$ spans or generates $X$ if the induced map $\oplus S_a \to X$ maps epimorphically onto $X$. 

More generally:

+-- {: .num_defn}
###### Definition

If $\mathcal{E}$ is a subclass of epimorphisms, we say that $(S_a)_{(a\colon A)}$ is an _$\mathcal{E}$-separator_ or __$\mathcal{E}$-generator__ if each morphism $\varepsilon_X$ (as above) is in $\mathcal{E}$.
=--

The weakest commonly-seen strengthened notion is that of __extremal separator__, i.e. separator where all maps $\varepsilon_X$ are [[extremal epimorphisms]]. The notion of extremal separator admits an 
equivalent reformulation not referencing coproducts:

+-- {: .num_prop #Extremal}
###### Proposition

If $C$ is [[locally small category|locally small]] and has all small [[coproduct]]s, then a set-indexed family $(S_i)_{(i\colon I)}$ is an extremal separator if and only if 
the functors $C(S_i,-):C\to\mathrm{Set}$ are jointly faithful and jointly [[conservative functor|conservative]].
=--

+-- {: .proof}
###### Proof

Assume first that the family $(S_i)_{(i\colon I)}$ is an extremal separator.
The functors $C(S_i,-):C\to\mathrm{Set}$ are jointly faithful for every separator.
To see that they are also jointly conservative, let $f:A\to B$ such that all
$C(S_i,f)$ are bijective. Then $\varepsilon_B$ factors through $f$ since all its
components do, which implies that $f$ is an extremal epi since $\varepsilon_B$ is one by assumption. It remains to show that $f$ is a monomorphism. For this, let $u,v:X\to A$ such that $f u = f v$. Then we have $f u h = f v h$ for all $i\in I$ and $h:S_i\to X$,
which implies $u h = v h$ since the $C(S_i,f)$ are bijective, and we conclude that $u=v$
since $(S_i)_{(i\colon I)}$ is separating.

Conversely, assume that the functors $C(S_i,-)$ are jointly faithful and jointly
conservative. Given $A\in C$, joint faithfulness implies that $\varepsilon_A$ is epic.
To see that it is extremally so, assume a factorization $\varepsilon_A = m g$ with $m$ monic. We have to show that 
$m$ is an isomorphism, and for this it is sufficient to show that all $C(S_i,m)$
are bijections. Injectivity is clear since $m$ is monic, and surjectivity follows since every $h:S_i\to A$ factors through $\varepsilon_A$.
=--

The concepts "strong separator" and "regular separator" corresponding to the 
notions of [[strong epimorphism]] and [[regular epimorphism]] do not admit such a reformulation, but the following result shows that they are equivalent to extremal separators in reasonable categories.

+-- {: .num_prop}
###### Proposition

Assume that $C$ is [[locally small category|locally small]] and has all small [[coproduct]]s. 

1. If $C$ is balanced, then every separator is extremal.

2. If $C$ has pullbacks, then every extremal separator is strong.

3. If $C$ is [[regular category|regular]], then every strong separator is regular.

The converse implications do always hold.
=--

+-- {: .proof}
###### Proof
This is a direct consequence of the facts that 

1. in a balanced category every epi is extremal,

2. in a category with pullbacks, every extremal epi is strong, and 

3. in a regular category every strong epi is regular.

=--

+-- {: .un_remark}
###### Remarks

1. Proposition \ref{Extremal} gives rise to a notion of extremal separator that makes sense independently of the existence of coproducts. In fact claim 1 of the preceding result holds in this more general setting, since every faithful functor out of a balanced category is conservative.

2. Most of the literature uses the term "strong separator" (or strong generator) for what we call an extremal separator. [Adamek and Rosicky (Section 0.6)](#AdamekRosicky) also comment on this mismatch, writing
"It would be more reasonable, but unfortunately less standard, to call [a strong generator] an extremal generator".
   However, item 2 of the preceding result shows that this discrepancy disappears and the terms coincide in presence of pullbacks (and coproducts).

3. In the Elephant, Johnstone uses "separator" in the same sense as we do, and writes "generator" for extremal separators, in the more general sense not assuming coproducts. Since he always assumes finite limits, he can use a simplified criterion only requiring joint conservativity of the hom-functors (since a conservative functor $F:C\to D$ is automatically faithful whenever $C$ has equalizers and $F$ preserves them).
=--

### Dense separators


Finally, the strongest kind of separator commonly seen is that of __dense separator__. 

+-- {: .num_defn}
###### Definition

A __dense separator__ in a category $C$ is a family $(S_i)_{(i\colon I)}$ of objects 
such that the generated full subcategory is [[dense subcategory|dense]].
=--

Every dense separator is an extremal separator, and it is also strong and regular whenever those words make sense, i.e. $C$ is locally small and has small coproducts. If $C$ furthermore has pullbacks and the coproducts are pullback-stable, then every regular separator is dense (see [Borceux I, Proposition 4.5.6](#Borceux)).
To see that the pullback-stability condition is necessary, consider the category of abelian groups. Here, the free group on one generator is a regular, but not a dense separator.

### Giraud's axioms

[[Grothendieck topos#Giraud|Giraud's axioms]] characterize Grothendieck toposes as locally small regular categories with effective equivalence relations and disjoint and pullback-stable coproducts admitting a small separator. The previously stated and cited results show that in fact every such separator is dense (the effectivity and disjointness assumptions don't play a role for this conclusion).

## Related concepts

* [[coseparator]]

## References

* {#Borceux} [[Francis Borceux]], _Handbook of Categorical Algebra I_, Cambridge University Press, 1994

* {#AdamekRosicky} [[Jiří Adámek]] and [[Jiří Rosicky]], Locally presentable and accessible categories, Cambridge University Press


[[!redirects separator]]
[[!redirects separators]]

[[!redirects separating family]]
[[!redirects separating families]]
[[!redirects generating family]]
[[!redirects generating families]]

[[!redirects separating class]]
[[!redirects separating classes]]
[[!redirects generating class]]
[[!redirects generating classes]]

[[!redirects separating set]]
[[!redirects separating sets]]
[[!redirects generating set]]
[[!redirects generating sets]]

[[!redirects strong separator]]
[[!redirects strong separators]]
[[!redirects strong generator]]
[[!redirects strong generators]]
[[!redirects strong separating set]]
[[!redirects strong separating sets]]
[[!redirects strong generating set]]
[[!redirects strong generating sets]]

[[!redirects dense separator]]
[[!redirects dense separators]]
[[!redirects dense generator]]
[[!redirects dense generators]]

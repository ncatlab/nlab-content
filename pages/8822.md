
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

* for every pair of [[parallel morphisms]] $f,g \colon X \to Y$ in $\mathcal{C}$, if $f\circ e = g\circ e$ for every morphism $e\colon S \to X$, then $f = g$.
=--

Assuming that $\mathcal{C}$ is [[locally small|locally small category]], we have equivalently that $S$ is a separator if the [[hom functor]] $Hom(S,-) \colon \mathcal{C} \to $ [[Set]] is [[faithful functor|faithful]].


More generally:

+-- {: .num_defn}
###### Definition

A [[family]] $\mathcal{S} = (S_a ;|; a\colon A)$ of [[objects]] of a [[category]] $\mathcal{C}$ is a __separating family__ or a __generating family__ if:

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

+-- {: .num_prop}
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
conservative. Given $A\in C$, joint faithfulness shows that $\varepsilon_A$ is epic.
To see that it is extremally so, assume a factorization $\varepsilon_A = mg$ with $m$ monic. We have to show that 
$m$ is an isomorphism, and for this it is sufficient to show that all $C(S_i,m)$
are bijections. Injectivity is clear since $m$ is monic, and surjectivity follows since every $h:S_i\to A$ factors through $\varepsilon_A$.
=--

+-- {: .un_remark}
###### Warning

Confusingly, some authors use "strong generator" for what we call an extremal separator. In a category with [[pullbacks]], extremal epis reduce to strong ones, and so extremal separators are necessarily strong, and the clash of terminology is resolved.
=--

Stronger still is a __regular generator__. Since regular epis are strong, regular generators are strong.

Finally, the strongest sort of generator commonly seen is a __dense generator__. Dense generators don't fit into our scheme based on classes of epimorphisms, but they do admit a nice functorial definition: a full subcategory $\mathcal{G} \subset \mathcal{C}$ is dense if and only if the functor $\mathcal{C}(i_{\mathcal{G}}, -): \mathcal{C} \to [\mathcal{G}^{\mathrm{op}}, \mathrm{Set}]$ is full and faithful, where $i_{\mathcal{G}}: \mathcal{G} \to \mathcal{C}$ is the inclusion. That is to say, $\mathcal{G}$ is a dense generator if $i_{\mathcal{G}}$ is a [[dense functor]]. In a category with coproducts, every dense generator is regular: this can be seen by reformulating denseness in terms of canonical colimits and expressing the relevant colimit as a coequalizer of two coproducts.

+-- {: .query}
[[Daniel Schaeppi]] Something seems to be wrong here: strong epimorphisms are extremal, so the notion of extremal generator is weaker than the notion of strong generator. In general, not every strong separator / strong generator is ($Set$-)dense (take the free abelian group on one separator, for example).

Tim Campion: I've attempted to fix these errors. Hopefully it's all right now.
=--


## Related concepts

* [[coseparator]]


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

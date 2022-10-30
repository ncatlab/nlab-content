
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $R$ a [[ring]], let $R$[[Mod]] be the category of $R$-[[modules]].

An **injective module** over $R$ is an [[injective object]] in $R Mod$. 

This is the dual notion of a _[[projective module]]_. 

## Properties

### Equivalent characterizations

Let $R$ be a [[commutative ring]] and  $C = R Mod$ the category of $R$-[[modules]]. We discuss [[injective modules]] over $R$ (see there for more).

+-- {: .num_theorem #BaerTheorem}
###### Theorem 
**([[Baer's criterion]])**


If the [[axiom of choice]] holds, 
then a [[module]] $Q \in R Mod$ is an [[injective module]] precisely if for $I$ any left $R$-[[ideal]] regarded as an $R$-module, any [[homomorphism]] $g : I \to Q$ in $C$ can be extended to all of $R$ along the inclusion $I \hookrightarrow R$.

=-- 

+-- {: .proof} 
###### Sketch of proof 

Let $i \colon M \hookrightarrow N$ be a [[monomorphism]] in $R Mod$, and let $f \colon M \to Q$ be a map. We must extend $f$ to a map $h \colon N \to Q$. Consider the [[poset]] whose elements are pairs $(M', f')$ where $M'$ is an intermediate [[submodule]] between $M$ and $N$ and $f' \colon M' \to Q$ is an extension of $f$, ordered by $(M', f') \leq (M'', f'')$ if $M''$ contains $M'$ and $f''$ extends $f'$. By an application of [[Zorn's lemma]], this poset has a [[maximal element]], say $(M', f')$. Suppose $M'$ is not all of $N$, and let $x \in N$ be an element not in $M'$; we show that $f'$ extends to a map $M'' = \langle x \rangle + M' \to Q$, a [[contradiction]]. 

The set $\{r \in R: r x \in M'\}$ is an ideal $I$ of $R$, and we have a module [[homomorphism]] $g \colon I \to Q$ defined by $g(r) = f'(r x)$. By [[hypothesis]], we may extend $g$ to a module map $k \colon R \to Q$. Writing a general element of $M''$ as $r x + y$ where $y \in M'$, it may be shown that 

$$f''(r x + y) = k(r) + g(y)$$ 

is well-defined and extends $f'$, as desired. 

=-- 

+-- {: .num_cor}
###### Corollary
{#DirectSumInjectives} 

Assume that the [[axiom of choice]] holds.

Let $R$ be a [[Noetherian ring]], and let $\{Q_j\}_{j \in J}$ be a collection of [[injective modules]] over $R$. Then the [[direct sum]] $Q = \bigoplus_{j \in J} Q_j$ is also injective. 

=-- 

+-- {: .proof}
###### Proof 

By [Baer's criterion](#Baer), it suffices to show that for any [[ideal]] $I$ of $R$, a module [[homomorphism]] $f \colon I \to Q$ extends to a map $R \to Q$. Since $R$ is Noetherian, $I$ is [[finitely generated module|finitely generated]] as an $R$-module, say by elements $x_1, \ldots, x_n$. Let $p_j \colon Q \to Q_j$ be the [[projection]], and put $f_j = p_j \circ f$. Then for each $x_i$, $f_j(x_i)$ is nonzero for only finitely many summands. Taking all of these summands together over all $i$, we see that $f$ factors through 

$$\prod_{j \in J'} Q_j = \bigoplus_{j \in J'} Q_j \hookrightarrow Q$$ 

for some finite $J' \subset J$. But a [[product]] of injectives is injective, hence $f$ extends to a map $R \to \prod_{j \in J'} Q_j$, which completes the proof. 

=-- 

+-- {: .num_prop}
###### Proposition

Conversely, $R$ is a [[Noetherian ring]] if [[direct sums]] of injective $R$-[[modules]] are injective. 

=--

This is due to Bass and Papp. See ([Lam, Theorem 3.46](#Lam)).



### Preservation of injectives

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

between [[abelian categories]] such that the [[left adjoint]] $L$ is an [[exact functor]], then the [[right adjoint]] preserves injective objects.

=--

+-- {: .proof}
###### Proof

Observe that an object is injective precisely if the [[hom-functor]] into it sends [[monomorphisms]] to [[epimorphisms]], and that $L$ preserves monomorphisms by assumption of exactness. With this the statement follows via adjunction isomorphism

$$
  Hom_{\mathcal{A}}(-,R(I))\simeq Hom_{\mathcal{B}}(L(-),I)
  \,.
$$

=--


### Existence of enough injectives
 {#ExistenceOfEnoughInjectives}

We discuss that in the presence of the [[axiom of choice]] at least, the category $R$[[Mod]] has _[[injective object|enough injectives]]_ in that every module is a [[submodule]] of an injective one. We first consider this for $R = \mathbb{Z}$. We do assume prop. \ref{InjectiveAbelianGroupIsDivisibleGroup}, which may be proven using [[Baer's criterion]]. 

+-- {: .num_prop #AbHasEnoughInjectives}
###### Proposition

Assuming the [[axiom of choice]],
the [[category]] $\mathbb{Z}$[[Mod]] $\simeq$ [[Ab]] has [[injective object|enough injectives]].

=--

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





## Examples

### Injective $\mathbb{Z}$-modules / abelian groups

Let $C = \mathbb{Z} Mod \simeq $ [[Ab]] be the abelian category of [[abelian groups]]. 

+-- {: .num_prop #InjectiveAbelianGroupIsDivisibleGroup}
###### Proposition

An [[abelian group]] $A$ is injective as a $\mathbb{Z}$-module precisely if it is a [[divisible group]], in that for all [[integers]] $n \in \mathbb{N}$ we have $n G = G$.

=--

Using Baer's criterion, prop. \ref{BaerTheorem}.

+-- {: .num_example}
###### Example

By prop. \ref{InjectiveAbelianGroupIsDivisibleGroup} the following [[abelian groups]] are injective in [[Ab]].

The group of [[rational numbers]] $\mathbb{Q}$ is injective in [[Ab]], as is the additive group of [[real numbers]] $\mathbb{R}$ and generally that underlying any [[field]]. The additive group underlying any [[vector space]] is injective. The [[quotient]] of any injective group by any other group is injective.

=--

+-- {: .num_example}
###### Example

**Not** injective in [[Ab]] is for instance the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ for $n \gt 1$.

=--


## Related concepts


* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * **injective module**

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]


## References

The notion of injective module was introduced in 

* {#Baer}R. Baer, _Abelian groups that are direct summands of every containing abelian group_ , Bulletin AMS **46** no. 10 (1940) pp.800-806. ([projecteuclid](http://projecteuclid.org/euclid.bams/1183503234))

(The dual notion of [[projective modules]] was considered explicitly only much later.)

A general discussion can be found in 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

The general notion of [[injective objects]] is in section 9.5, the case of injective complexes in section 14.1.

[Baer's criterion](#Baer) is discussed in many texts, for example 

* N. Jacobsen, _Basic Algebra II_, W.H. Freeman and Company, 1980. 

See also 

* T.-Y. Lam, _Lectures on modules and rings_, Graduate Texts in Mathematics 189, Springer Verlag (1999). 
{#Lam}

Section 4.2 of 

* [[Peter May]], _Notes on Tor and Ext_ ([pdf](http://www.math.uchicago.edu/~may/MISC/TorExt.pdf))
 {#May}


For [[abelian sheaves]] over the [[etale site]]:

* [[James Milne]], section 8 of _[[Lectures on Étale Cohomology]]_



[[!redirects injective modules]]

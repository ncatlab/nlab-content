
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}




## Idea

Every [[geometric morphism]] between [[toposes]] factors into a [[geometric surjection]] followed by a [[geometric embedding]]. This exhibits an [[image]] construction in the [[topos theory|topos-theoretic]] sense, and gives rise to a [[factorization system in a 2-category]] for [[Topos]].

## Statement

+-- {: .num_prop}
###### Proposition

There is a [[factorization system on a 2-category|factorization system]] on the [[2-category]] [[Topos]] whose left class is the 
[[surjective geometric morphism]]s and whose right class is the [[geometric embeddings]].  

Moreover, the factorization of a given geometric morphism $f : \mathcal{E} \to \mathcal{F}$ is, up to [[equivalence of categories|equivalence]], through the canonical surjection onto the [[topos of coalgebras]] $f^* f_* CoAlg(\mathcal{E})$ of the [[comonad]]  $f^* f_* : \mathcal{E} \to \mathcal{E}$:

$$
  \array{
     \mathcal{E} &&\stackrel{f}{\to}&& \mathcal{F}
     \\
     & {}_{\mathllap{F}}\searrow && \nearrow
     \\
     && f^* f_* CoAlg(\mathcal{E})
  }
  \,E.
$$

=--

This appears for instance as ([MacLaneMoerdijk, VII 4., theorem 6](#MacLaneMoerdijk)).

We use the following lemma

+-- {: .num_lemma #ConditionForSheafFactorization}
###### Lemma

Let $j$ be a [[Lawvere-Tierney topology]] on a [[topos]] $\mathcal{E}$ and write $i : Sh_j(\mathcal{E}) \to \mathcal{E}$ for the corresponding [[geometric embedding]]. 

Then a [[geometric morphism]] $f : \mathcal{F} \to \mathcal{E}$ factors through $i$ precisely if 

* the [[direct image]] $f_*$ takes values in $j$-sheaves;

or, equivalently

* the [[inverse image]] $f^*$ sends $j$-[[dense monomorphism]]s to [[isomorphism]]s.

=--

This appears as ([MacLaneMoerdijk, VII 4. prop. 2](#MacLaneMoerdijk)).

+-- {: .proof}
###### Proof of the lemma


We first show the first statement, that for $f$ to factor it is sufficient for $f_*$ to take values in $j$-sheaves: in that case, set

$$
  p_* := i^* f_*: \mathcal{F} \to Sh_j(\mathcal{E})
  \,.
$$

Since by assumption the [[unit of an adjunction|unit]] map $x \to i_* i^* x$ is an [[isomorphism]] on the image of $f_*$ this indeed serves to factor $f_*$:

$$
  i_* p_* \simeq i_* i^* f_* \simeq f_*
  \,.
$$

The [[left adjoint]] to $p_*$ is then 

$$
  p^* \simeq f^* i_*
  \,,
$$

because

$$
  \begin{aligned}
    \mathcal{F}(g^* E, F)
     & \simeq \mathcal{F}(f^* i_* E, F)
    \\  
    & \simeq \mathcal{E}(i_* E, f_* F)
    \\
    & \simeq \mathcal{E}(i_* E, i_* i^* f_* F)
    \\
    & \simeq Sh_j\mathcal{E} (E, i^* f_* F)
    \\
    & \simeq Sh_j(E, p_* F)
  \end{aligned}
  \,,
$$

where in the middle steps we used that $f_* F$ is a $j$-sheaf, by assumption, and that $i_*$ is full and faithful.

It is clear that $p^*$ is left exact, and so $(p^* \dashv p_*)$ is indeed a factorizing geometric morphism.

We now show that $f_*$ taking values in sheaves is equivalent to $f^*$ mapping dense monos to isos. 

Let $u : U \hookrightarrow X$ be a $j$-[[dense monomorphism]] and $A \in \mathcal{E}$ any object. Consider the induced naturality square

$$
  \array{
    \mathcal{E}(X, f_* A) &\stackrel{\simeq}{\to}& \mathcal{F}(f^* X, A)
    \\ 
    {}^{\mathllap{\mathcal{E}(u, f_* A)}}\downarrow 
     && 
     \downarrow^{\mathrlap{\mathcal{F}(f^* u, A)}}
    \\
    \mathcal{E}(U, f_* A)
      &\stackrel{\simeq}{\to}&
    \mathcal{F}(f^* U, A)
  }
$$

of the adjunction [[natural isomorphism]]. If now $f_* A$ is a $j$-sheaf and $u$ a [[dense monomorphism]], then by definition the left vertical morphism is also an isomorphism and so is the right one. By the [[Yoneda lemma]] this being an iso for all $A$ is equivalent to $f^* u$ being an iso. And conversely.

=--

+-- {: .proof}
###### Proof of the proposition

Let $f : \mathcal{F} \to \mathcal{E}$ be any [[geometric morphism]]. 

We first discuss the existence of the factorization, then its uniqueness.

To construct the factorization, we shall give a [[Lawvere-Tierney topology]] on $\mathcal{E}$ and factor $f$ through the [[geometric embedding]] of the corresponding [[sheaf topos]].

Take the closure operator $\overline{(-)} : Sub(-)_{\mathcal{E}} \to Sub(-)_{\mathcal{E}}$ to be given by sending $U \hookrightarrow X$ to the [[pullback]]

$$
  \array{
    \overline{U} &\to& f_* f^* U
    \\
    \downarrow && \downarrow
    \\
    X &\to& f_* f^* X
  }
  \,,
$$

where the bottom morphism is the $(f^* \dashv f_*)$-[[unit of an adjunction|unit]].  One checks that this is indeed a closure operator by the fact that $f^*$ preserves both pullbacks and pushouts.

Notice that this implies that for two [[subobject]]s $U_1, U_2 \hookrightarrow X$ we have

\[
  \label{ASubobjectRelation}
  (U_1 \subset \overline{U_2})
   \;\;\;
   \Leftrightarrow
   \;\;\;
  (f^* U_1 \subset f^* U_2)
\]

Write $j$ for the corresponding [[Lawvere-Tierney topology]] and 

$$
  i : Sh_j(\mathcal{E}) \to \mathcal{E}
$$

for the corresponding [[geometric embedding]]. 

By lemma \ref{ConditionForSheafFactorization} we get a factorization through $I$ if $f^*$ sends $j$-[[dense monomorphism]]s to [[isomorphism]]s. But if $U \hookrightarrow X$ is dense so that $X \subset \overline{U}$ then, by (eq:ASubobjectRelation), $f^* X \subset f^* U$ and hence $f^* X = f^* U$.

Write 

$$
  f : \mathcal{F} \stackrel{p}{\to} Sh_j(\mathcal{E}) \stackrel{i}{\to}
  \mathcal{E}
$$

for the factorization thus established. It remains to show that $p$ here is a [[geometric surjection]]. By one of the equivalent characterizations discussed there, this is the case if $p^*$ induces an injective homomorphism of subobject lattices.

So suppose that for subobjects $U_1, U_2 \subset X$ we have $p^* U_1 \simeq p^* U_2$. Observe that then also $f^* i_* U_1 \simeq f^* i_* U_2$, because 

$$
  \begin{aligned}
    f^* i_* U_1 & \simeq p^* i^* i_* U_1
    \\
    & \simeq p^* U_1
    \\
    & \simeq p^* U_2
    \\
    & \simeq p^* i^* i_* U_2
    \\
    & \simeq f^* i:* U_2
  \end{aligned}
$$ 

by the fact that $i_*$ is [[full and faithful functor|full and faithful]].  With (eq:ASubobjectRelation) it follows that also 

$$
  i_* U_1 \simeq \overline{i_* U_2}
$$

and hence

$$
  \cdots \simeq i_* U_2
$$

by the very fact that $i_*$ includes $j$-sheaves in general, hence $j$-closed subobjects in particular. Finally since $i_*$ if a [[full and faithful functor]] this means that 

$$
  U_1 \simeq U_2
  \,.
$$

So $p^*$ is indeed injective on subobjects and so $p$ is a [[geometric surjection]].

This establishes the existence of a surjection/embedding factorization. Next we discss that this is unique.

So consider two factorizations

$$
  \array{
    && \mathcal{A}
    \\
    & {}^{\mathllap{p_1}}\nearrow &\Downarrow^\simeq& \searrow^{\mathrlap{i_1}}
    \\
    \mathcal{F}
    &&\stackrel{f}{\to}&&
    \mathcal{E}
    \\
    & {}_{\mathllap{p_2}}\searrow &\downarrow^{\simeq}& \nearrow_{\mathrlap{i_2}}
    \\
    && \mathcal{B}
  }
$$

into a geometric surjection followed by a geometric embedding.

We will now argue that $i_1$ factors -- essentially uniquely -- through $i_2$ in a way that makes 

$$
  \array{
    && \mathcal{A}
    \\
    & {}^{\mathllap{p_1}}\nearrow && \searrow^{\mathrlap{i_1}}
    \\
    \mathcal{F}
    &&\downarrow^g&&
    \mathcal{E}
    \\
    & {}_{\mathllap{p_2}}\searrow && \nearrow_{\mathrlap{i_2}}
    \\
    && \mathcal{B}
  }
$$

commute up to natural isomorphisms. By the same argument for the upside-down situation we find an essentially unique middle vertical morphism $h : \mathcal{B} \to \mathcal{A}$ the other way round. Then essential uniqueness of these factorizations implies that $g \circ h \simeq Id$ and $h \circ g \simeq Id$. This means that the original two factorizations are equivalent.

To find $g$ and $h$, use again that every [[geometric embedding]] (by the discussion there) is, up to equivalence, an inclusion of $j$-sheaves for some $j$. Find such a $j$ the bottom morphism and then use again lemma \ref{ConditionForSheafFactorization} that $i_1$ factors through $i_2$ -- essentially uniquely -- precisely if $i_1^*$ sends [[dense monomorphism]]s to isomorphisms.

To see that it does, let $IU \to X$ be a dense mono and consider the naturality square

$$
  \array{
    p_2^* i_2^* U &\stackrel{\simeq}{\to}& p_1^* i_1^* U
    \\
    \downarrow && \downarrow 
    \\
    p_2^* i_2^* X &\stackrel{\simeq}{\to}& p_1^* i_1^* X    
  }
  \,.
$$

Since $i_2^*(U \to X)$ is an iso by definition, the left vertical morphism is, and thus so is the right vertical morphism. But since $p_1$ is a [[geometric surjection]] we have (by the discussion there) that $p_1^*$ is [[conservative functor|conservative]], and hence also $i_1^* U \to i_1^* X$ is an isomorphism.

Hence $i_1$ factors via some $g$ through $i_2$ and the proof is completed by the above argument.

=--

## Examples

* For $f : X \to Y$ a [[continuous function]] between [[topological space]]s and $X \to im(f) \to Y$ its ordinary [[image]] factorization through an [[embedding]], the corresponding composite of geometric morphisms of [[sheaf topos]]es 

  $$
    Sh(X) \to Sh(im(f)) \to Sh(Y)
  $$

  is a geometric surjection/geometric embedding factorization.

* For $\mathcal{E}$ any topos, $f : X \to Y$ any morphism in $\mathcal{E}$, and $X \to im(f) \to Y$ its [[image]] factorization, the corresponding composite of [[base change geometric morphisms]]

  $$
    \mathcal{E}/X  \to \mathcal{E}/im(f) \to \mathcal{E}/Y
  $$  

  is a geometric surjection/embedding factorization.

* For $f : C \to D$ any [[functor]] between [[categories]], write $C \to im(f) \to D$ for its [[essential image]] factorization. Then the induced composite <a href="http://ncatlab.org/nlab/show/geometric%20morphism#BetweenPresheafToposes">geometric morphism of presheaf toposes</a>

  $$
    [C^{op}, Set] \stackrel{}{\to} [im(f)^{op}, Set] \to 
    [D^{op}, Set]
  $$

  is a geometric surjection/embedding factorization.

See ([MacLaneMoerdijk, p. 377](#MacLaneMoerdijk)).

## Properties

### As idempotent approximation

A geometric morphism $f:\mathcal{F}\to\mathcal{E}$ induces via the adjunction $f^\ast\vdash f_\ast$ a [[monad]] on $\mathcal{E}$. Due to a general result by S. Fakir this induces an associated [[idempotent monad]] on $\mathcal{E}$ and this idempotent approximation coincides with the monad induced by $i^\ast\vdash i_\ast$ given by the inclusion $i$ from the factorization $f=i\circ q$. 

For references and further details on the idempotent approximation see at [[idempotent monad]].

### A logical description

Let $T$ be a [[geometric theory]] over a signature $\Sigma$ and $f:\mathcal{E}\to Set[T]$ a geometric morphism to its [[classifying topos]]. Then by the general properties of a classifying topos, $f$ corresponds to a certain $T$-model $M$ in $\mathcal{E}$. 

Notice that every geometric morphism $f$ between [[Grothendieck toposes]] is of this form for some geometric theory $T$ and hence corresponds to some model $M$ ! This model permits to attach a geometric theory to $f$ as well:

The **theory of M** $Th(M)$ consists of all geometric sequents $\sigma$ over $\Sigma$ such that $M\models \sigma$.

Then the following holds ([Caramello 2009](#Caramello09), p.57):

+-- {: .num_prop}
###### Proposition

The topos occurring in the middle of the surjection-embedding factorization of $f$ is precisely the classifying topos for $Th(M)$: $\mathcal{E}\twoheadrightarrow Set[Th(M)]\hookrightarrow Set[T]$.

=--


## Related entries

* [[open subtopos]]

* [[(dense,closed)-factorization]]



## References

* {#Johnstone77} [[Peter Johnstone]], _Topos Theory_ , Academic Press 1977 (Dover reprint 2014). (section 4.1, pp.103-107) 

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_, Oxford UP 2002. (section A4.2, pp.172ff)

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (section VII.4)
 {#MacLaneMoerdijk}

* [[Olivia Caramello|O. Caramello]], _Lattices of theories_ , arXiv:0905.0299v1 (2009). ([pdf](http://arxiv.org/pdf/0905.0299v1)) {#Caramello09}

[[!redirects geometric surjection/embedding factorization]]
[[!redirects geometric surjection/inclusion factorization]]
[[!redirects geometric surjection/embedding factorization system]]
[[!redirects geometric surjection/inclusion factorization system]]
[[!redirects (geometric surjection, inclusion) factorization system]]

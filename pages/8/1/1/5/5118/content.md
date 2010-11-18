
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

For $C$ and $D$ [[monoidal model categories]], a **lax monoidal Quillen adjunction**

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D
$$

is

* a [[Quillen adjunction]] $(L \dashv R)$ between the underlying [[model categories]];

* equipped with the structure of a [[lax monoidal functor]] on $R$ with respect to the underlying [[monoidal categories]]

* such that the induced structure of an [[oplax monoidal functor]] on $L$ satisfies:

  1. for all cofibrant objects $x,y \in D$ the oplax monoidal transformation

     $$
       L(x \otimes y) \to L(x) \otimes L(y)
     $$

     is a weak equivalence in $C$    

  1. for some (hence any) cofibrant [[resolution]] $q : \hat I_D \stackrel{\simeq}{\to} I_D$ of the monoidal unit object in $D$, the composite

     $$
       L(\hat I_D) \stackrel{L(q)}{\to} L(I_D) \to I_C
     $$

     is a weak equivalence in $C$.

This is called a **strong monoidal Quillen adjunction** if $L$ is a [[strong monoidal functor]]. 

If a monoidal Quillen adjunction is also a [[Quillen equivalence]] it is called a **monoidal Quillen equivalence**.

## Properties

### Recognition of monoidal Quillen adjunctions {#Recognition}

+-- {: .un_theorem}
###### Theorem

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a [[Quillen adjunction]] between [[monoidal model categories]] and let $R$ be equipped with the strcuture of a [[lax monoidal functor]].

Then the following two conditions are sufficient for $(L \dashv R)$ to be a lax monoidal Quillen adjunction:

1. for some (hence any) cofibrant [[resolution]] $q : \hat I_D \stackrel{\simeq}{\to} I_D$ of the unit object in $D$, the composite morphism

   $$
     L(\hat I_D) \stackrel{L(q)}{\to} L(I_D) \stackrel{\tilde i}{\to} I_C
   $$

   is a weak equivalence, (wher $\tilde i$ is the [[adjunct]] of $i : I_D \to R(I_C)$);

1. the unit object $I_D$ _detects weak equivalences_ in that for every weak equivalence $f : X \to Y$ between fibrant objects the morphism $D^{\Delta^{op}}(Q I_D, f)$ of [[hom-object]]s in the category of [[simplicial object]]s in $D$ is an equivalence of Kan complexes, for $Q I_D$ a cofibrant resolution in the [[Reedy model structure]] $D^{\Delta^{op}}_{Reedy}$. 

=--

This is proposition 3.16 in ([SchwedeShipley](#SchwedeShipley)).




### Lift to an adjunction on monoids {#LiftToAdjunctionOnMonoids}

We discuss how a monoidal Quillen adjunction $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ induces, under mild conditions, an adjunction $(L^{mon} \dashv R) : Mon(C) \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} Mon(D)$ on the corresponding categories of [[monoid]]s. In the following secton we discuss how this is itself a Quillen adjunction


The [[lax monoidal functor]] $R : C \to D$ induces (as described there) a functor $R : Mon(C) \to Mon(D)$ on monoids (which by slight abuse of notation we denote by the same symbol). While the left adjoint $L$ will not extend to monoids unless $R$ is a [[strong monoidal functor]] there is nevertheless an adjoint $L^{mon}$ to $R : Mon(C) \to Mon(D)$:


+-- {: .num_prop}
###### Proposition

Let $C$ be a [[monoidal category]] with colimits, write $Mon(C)$ for its category of [[monoid]]s and $U_C : Mon(C) \to C$ for the evident [[forgetful functor]]. This has a [[left adjoint]] $F_C : C \to Mon(C)$ where on an object $X \in C$ the underlying object of $F_C X$ is

$$
  U_C F_C X 
  = 
  \coprod_{n \in \mathbb{N}} X^{\otimes n}
  = 
  I_C \coprod X \coprod (X \otimes X) \coprod \cdots
$$

in $C$, with the monoidal structure given by tensor product/juxtaposition.


=--

+-- {: .proof}
###### Proof 

A morphism $f : F_C X \to A$ in $Mon(C)$ with components $f_k : X^{\otimes k} \to U_C A$ is entirely fixed by its component $\tilde f = f_1 : X \to U_C A$ on $X$, because by the homomorphism property and the special free nature of the product in $F_C X$

$$
  \array{
    X^{\times k} \otimes X^{\otimes (n-k)} &\stackrel{f_k \otimes f_{n-k}}{\to}&
    A \otimes A
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\mu_A}}
    \\
    X^{\otimes n} &\stackrel{f_{n}}{\to}& A
  }
$$

it follows that 

$$
  f_n :
  X^{\otimes n} \stackrel{f_1^{\otimes n}}{\to} A^{\otimes n} \stackrel{\mu_A}{\to} A
  \,.
$$

Conversely, every choice for $f_1$ extends to a morphism $f$ in $Mon(C)$ this way.

=--

+-- {: .num_prop #AdjunctionOnMonoids}
###### Proposition

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a pair of adjoint functors between monoidal categories where $R$ is a lax monoidal functor and $D$ has all small colimits.

Then the functor $R : Mon(C) \to Mon(D)$ has a left adjoint

$$
  L^{mon} : Mon(D) \to Mon(C)
$$

given by forming the [[coequalizer]]s

$$
  L^{mon} : B 
    \mapsto 
   \lim_{\to}
  (F_C L F_D B \stackrel{\to}{\to} F_C L B)
$$

in $Mon(C)$ of the following two morphisms

* the first one is the image under $F_C \circ L$ of the [[unit of an adjunction|adjunction counit]] $ F_D U_D B  \to B$;

* the second is the unique $C$-monoid morphism that restricts to the $C$-morphism

  $$
    L F_D B
    \simeq
   \coprod_{n \in \mathbb{N}} L( B^{\otimes n})
    \stackrel{\coprod \tilde e}{\to}
   \coprod_{n \in \mathbb{N}}
   (L B)^{\otimes n}
   \simeq
   F_C L B
  $$

  which is componentwise given by the [[lax comonoidal functor|lax comonoidal structure]] on $L$ induced by the lax monoidal structure on $R$.

=--

This is considered on p. 305 of ([SchwedeShipley](#SchwedeShipley))

+-- {: .proof}
###### Proof 

To see that $(L^{mon} \dashv R)$ first notice that a morphism of monoids

$$
  L^{mon} X \to Y
$$

is by the definition of coequalizer a morphism of monoids $f : F_C L X \to Y$ satisfying a condition. By the free property of $F_C L X$ this in turn is a morphism $f_1 : L X \to Y$ in $C$ which by $(L \dashv R)$ is a morphism $\tilde f_1 : X \to R Y$ in $C$. So we need to show that the condition satisfied by $f$ is precisely the condition that makes $\tilde f_1$ a morphism of monoids in that
 
$$
  \array{
    X \otimes X &\stackrel{\tilde f_1 \otimes \tilde f_1}{\to}& R  Y \otimes R  Y
    \\
    \downarrow && \downarrow
    \\
    && R ( Y \otimes  Y)
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\tilde f_1}{\to}& R  Y
  }
$$

commutes. We insert the definition of the [[adjunct]] $\tilde f_1$ and the [[lax natural transformation|lax naturality]] square of $R$ to get

$$
  \array{
    X \otimes X 
    &\to&
    R L X \otimes R L X 
    &\stackrel{R f_1 \otimes R f_1}{\to}& R  Y \otimes R  Y
    \\
    \downarrow && \downarrow &=& \downarrow
    \\
    && R(L X \otimes L Y) &\stackrel{R f_1}{\to}& R ( Y \otimes  Y)
    \\
    \downarrow && && \downarrow
    \\
    X & &\stackrel{\tilde f_1}{\to}&& R  Y
  }
  \,.
$$


The [[adjunct]] of the left/bottom composite is

$$
  L(X\otimes X) \to L X \stackrel{f_1}{\to} Y
$$

while the adjunct of the top/right composite is that of the diagonal, which is

$$
  L(X \otimes X) \stackrel{\tilde e}{\to} L X \otimes L X
  \stackrel{f_1 \otimes f_1}{\to} Y \otimes Y \to Y
$$

which by the definition of $f$ in terms of its components, this is 

$$
  L(X \otimes X) \stackrel{\tilde e}{\to} L X \otimes L X
  \stackrel{f_2}{\to}Y
  \,.
$$

The coequalizer property says indeed precisely that these two adjuncts are equal.

=--


+-- {: .num_lemma #LemmaOnNaturalIso}
###### Lemma

There is a [[natural isomorphism]]

$$
  L^{mon} \circ F_D
  \simeq
  F_C \circ L
  \,.
$$

=--

This is considered on p. 305 of ([SchwedeShipley](#SchwedeShipley)).


### Lift to a Quillen adjunction on monoids {#LiftToQuillenAdjunctionOnMonoids}

We now describe how the adjunction  $(L^{mon} \dashv R)$ established above becomes a [[Quillen adjunction]] for the [[transferred model structure]]s on the categories of monoids, transferred along the [[stuff, structure, property|forgetful]]/[[free functor]] adjunction 

$$
  (F_C \dashv U_C) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  C
  \,.
$$

For the purposes of the following statement, we define

+-- {: .un_def #CreatedModelStructure}
###### Definition

We say a model category structure on $Mon(C)$ is _created_ by $U_C$ if

* it is the [[transferred model structure]];

* every cofibrant object in $Mon(C)$ is a [[retract]] of a [[cell object]].

=--

+-- {: .un_theorem}
###### Theorem

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a lax monoidal Quillen adjunction between [[monoidal model categories]] with cofibrant unit obects.

If the forgetful functors $U_C$ and $U_D$ [create](#CreatedModelStructure) model structures on monoids, then the adjunction $(L^{mon} \dashv R)$ from [above](#AdjunctionOnMonoids) is a [[Quillen adjunction]]

$$
  (L^{mon} \dashv R) 
  : 
  Mon(C) \stackrel{\overset{L^{mon}}{\leftarrow}}{\underset{R}{\to}} Mon(D)
  \,,
$$

between the transferred model structures on monoids.

=--

This is theorem 3.12 in ([SchwedeShipley](#SchwedeShipley)). Its proof uses the following technical lemmas.

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a monoidal Quillen adjunction between monoidal model categories with cofibrant unit objects.

Suppose the adjunction

$$
  (L^{mon} \dashv R) 
  : 
  Mon(C) \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} Mon(D)
$$

described above exists (just as an adjunction, not yet assumed to be a Quillen adjunction).

+-- {: .num_lemma #VeryFirstTechnicalLemma}
###### Lemma

The morphism

$$
  L^{mon} I_D \to I_C
$$

induced by the oplax counit $\tilde e : L I_D \to I_C$ of the oplax monoidal functor is an [[isomorphism]] of monoids.

=--

+-- {: .proof}
###### Proof 

We have that $I_D$ and $I_C$ are the [[initial object]]s in $Mon(D)$ and $Mon(C)$, respectively.  Because $L^{mon}$ is [[left adjoint]], it preserves these initial objects, so that there is _some_ isomorphism as claimed. It is hence sufficient to show that the oplax counit induces a morphism of monoids at all, by  the universal property of the initial object it will be an isomorphism.

It is clear that

$$
  \coprod_n \mu^n {\tilde e}^{\otimes n} : F L I_D \to I_C
$$

is a morphism of monoids, because

$$
  \array{
    (L I)^{\otimes k} \otimes (L I)^{\otimes (n-k)}
    &\stackrel{\mu_I^k {\tilde e}^{\otimes k} \otimes \mu_I^{n-k}{\tilde e}^{\otimes (n-k)}}{\to}&
    I \otimes I
    \\
    \downarrow && \downarrow
    \\
    (L I)^{\otimes n}
    &\stackrel{\mu^n_I {\tilde e}^{n}}{\to}& I
  }
$$

commutes. So we have to show that this morphism
coequalizes the two morphisms in the definition  of $L^{mon} I_D$.
By the same argument as in the [above proof](#AdjunctionOnMonoids) this is equivalent to showing that 

$$
  \array{
    I_C \otimes I_C &\stackrel{e \otimes e}{\to}& 
    R I_C \otimes R I_C
    \\
    \downarrow && \downarrow
    \\
    && R (I_C \otimes I_C)
    \\
    \downarrow && \downarrow
    \\
    I_C &\stackrel{e}{\to}& R I_C
  }
$$

commutes. This follows from the unitality of the [[lax monoidal functor]] $R$.

=--

+-- {: .num_lemma #OneTechnicalLemma}
###### Lemma

For every monoid $B \in Mon(D)$ which is an $(L^\mon \dashv R)$-[[cell object]], the $(L \dashv R)$-[[adjunct]]

$$
 \chi_B :  L B \to L^{mon} B
$$

to the morphism underlying the [[unit of an adjunction|unit]] $B \to R L^{mon} B$ is a weak equivalence.

=--

This is proposition 5.1 in ([SchwedeShipley](#SchwedeShipley)).

+-- {: .proof}
###### Proof 

We first show this for $B = I_D$ the tensor unit in $D$, which in $Mon(D)$ is the [[initial object]]s:

* We claim hat the [[unit of an adjunction|adjunction unit]] $I_C \to R L^{mon} I_D \stackrel{\simeq}{\to} R(I_C)$ is the lax monoidal unit $e$ of $R$. 

  To see this, use that by the [previous lemma](#VeryFirstTechnicalLemma) the $(L \dashv R)$-[[adjunct]] of $I \to R L^{mon} I \to R I$ is $L I \to L^{mon} I \stackrel{\coprod_n \mu^n {\tilde e}^{\otimes n}}{\to} I$. Here the first morphism factors through the single power of $L I$, hence this is indeed $\tilde e : L I_D \to I_C$.

  Therefore by the axioms on monoidal Quillen adjunctions the
$(L \dashv R)$-adjunct $\chi_I$ is a weak equivalence.

We now proceed from this by induction over the cells of the [[cell object]] $B$.

So assume now that we have already shown that on some cell object $B$ the morphism $\chi_B$ is a weak equivalence. We want to deduce then that that after forming a new monoid $P$ by cell attachment, i.e. by a [[pushout]]

$$
  \array{
    F K &\to& F K'
    \\
    \downarrow && \downarrow 
    \\
    B &\to& P
  }
$$

for $K \to K'$ a cofibration in $D$, also $\chi_P : L P \to L^{mon} P $ is a weak equivalence.

Notice that since $L^{mon}$ is left adjoint also

$$
  \array{
    L^{mon} F K &\to& L^{mon} F K'
    \\
    \downarrow && \downarrow 
    \\
    L^{mon} B &\to& L^{mon} P
  }
$$

is a pushout in $Mon(C)$, and by the natural isomorphism from [the above lemma](#LemmaOnNaturalIso) so is

$$
  \array{
    F L K &\to& F L K'
    \\
    \downarrow && \downarrow 
    \\
    L^{mon} B &\to& L^{mon} P
  }
  \,.
$$



* We claim that $B$ is cofibrant and that we can without restriction assume $K$ and $K'$ to be cofibrant in $D$.

  The first statement follows from an inductive application of [SchwedeShipleyAlgebras, lemma 6.2](#SchwedeShipleyAlgebras). For the second statement notice that since $F$ is left adjoint and preserves pushouts in $D$, we have that $P$ is also the pushout of the diagram

  $$
    \left(
    \array{
      F B &\to& F( B \coprod_K K' )
      \\
      \downarrow && \downarrow 
      \\
      B &\to& P
    }
    \right)
    =
    \left(  
       \array{
          && F K &\to& F K' 
          \\
          && \downarrow && \downarrow
          \\
          F B &\to& F B
          \\
          \downarrow &&&& \downarrow
          \\
          B && \to && P
       }
    \right)
    \,.
  $$

  Since cofibrations are preserved by the Quillen left adjoint $F$ and under pushout, it follows that also $B \coprod_K K'$ is cofibrant if $K \to K'$ is a cofibration. So $B \to B \coprod_K K'$ can be used in place of $K \to K'$.

Notice that this means that our pushout square is in fact a [[homotopy pushout]] square (as discussed there). In particular a weak equivalence of these pushout diagrams will induce a weak equivalence of the pushouts, so that is what we will establish.

We now use the proof of ([SchwedeShipleyAlgebras, lemma 6.2](#SchwedeShipleyAlgebras)) for getting the following statement about the object underlying $P$

This $P$ is a [[colimit]] of a sequence of cofibrations

$$
  P \simeq \lim_{\to} ( B := P_0 \hookrightarrow P_1 \hookrightarrow P_2 \hookrightarrow \cdots )
$$

such that each morphism $P_{n-1} \hookrightarow P_n$ is a pushout in $D$ of a particular cofibration $Q_n(K,K', B) \hookrightarrow (B \otimes K')^{\otimes n} \otimes B$

By the coresponding disccussion of these pushouts under $L^{mon}$ it follows that also $L^{mon} P$ is the colimit of a sequence of cofibrations betwen objects $R_n$ that are pushouts of these particular cofibrations.

And the morphism $\chi_P$ respects all that and sends

$$
  \chi_{P_n} : L P_n \to L^{mon} R_n 
$$

at each stage of the cell attachments. So it is sufficient to show that the three components of these maps on the pushout squares are weak equivalences. Since we showed above that our pushout squares are actually [[homotopy pushout]] squares, this will imply that also $\chi_P$ is a weak equivalence.

This again works by using ([SchwedeShipleyAlgebras, lemma 6.2](#SchwedeShipleyAlgebras)).


=--


+-- {: .un_lemma #AnotherTechnicalLemma}
###### Lemma

If $U_C$ [creates](#CreatedModelStructure) the model structure on $Mon(C)$ and the unit in $C$ is cofibrant,  then a cofibrant $C$-monoid is also cofibrant as an object in $C$.

=--

This is a special case of  ([SchwedeShipleyAlgebras, lemma 6.2](#SchwedeShipleyAlgebras))

+-- {: .proof}
###### Proof 

(...)

=--


+-- {: .proof}
###### Proof of the theorem

First notice that since by assumption the model structure on $Mon(D)$ is [created](#CreatedModelStructure) by $U_D$ it follows by definition that the cofibrant $B$ is a [[retract]] of a [[cell object]] in $Mon(D)$. Then the [above lemma](#OneTechnicalLemma) asserts that

$$
  \chi_B : L B \to L^{mon} B
$$

is a weak equivalence. 


To prove the theorem, we have to show for every cofibrant $B \in Mon(D)$  and fibrant $Y \in Mon(C)$ that a morphism $B \to R Y$ is a weak equivalence in $Mon(D)$ (hence its underlying morphism in $D$) precisely if its adjunct $L^{mon} B \to Y$ is a weak equivalence in $Mon(C)$ (hence its underlying morphism in $C$).

By definition of adjunct we have that 

$$
 (B \to R Y) = ( B \to R L^{mon} B  \to R Y)
 \,.
$$

By the [second lemma above](#AnotherTechnicalLemma) we have that $B$ is cofibrant also in $C$. Therefore, since $(L \dashv R)$ is a Quillen equivalence between $C$ and $D$, the right hand is a weak equivalence precisely if its $(L \dashv R)$-adjunct

$$
  L B \stackrel{\chi_B}{\to} L^{mon} B \to Y
$$ 
 
is a weak equivalence in $D$. But since $\chi_B$ is a weak equivalence, this is the case precisely if $L^{mon}B \to Y$ is a weak equivalence.

=--


## Examples

Examples arise in the [[monoidal Dold-Kan correspondence]]. See there for details.


## Related concepts

* [[Quillen adjunction]]

* [[simplicial Quillen adjunction]]

* [[Quillen equivalence]]

* **monoidal Quillen adjunction**



## References

The notion of strong monoidal Quillen adjunction is def. 4.2.16 in 

* [[Mark Hovey]], _Model categories_

The lax monoidal version is considered as definition 3.6 of 

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}

Some of the facts mentioned above are from

* [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 
{#SchwedeShipleyAlgebras}

[[!redirects monoidal Quillen adjunctions]]

[[!redirects monoidal Quillen equivalence]]
[[!redirects monoidal Quillen equivalences]]

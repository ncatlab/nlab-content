
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}
 
## Idea

From the [[nPOV]] on [[cohomology]], the notion of Hochschild cohomology is the following.

+-- {: .standout}

Hochschild cohomology is the [[cohomology]] $\mathbf{H}(\mathcal{L}X,C)$ of [[free loop space object]]s $\mathcal{L}X$ in a [[derived stack]] [[(∞,1)-topos]] $\mathbf{H}$ with coefficients in [[quasicoherent ∞-stack|quasicoherent ∞-stacks of modules]] $C$. 

This naturally inherits an $S^1$-action from the [[free loop space object]]. The $S^1$-[[equivariant cohomology]] refinement of Hochschild cohomology is [[cyclic cohomology]].

=--

After unwinding what this means in algebraic terms, one obtains the tradional way of conceiving Hochschild cohomology.

Hochschild homology and cohomology are characteristic objects associated to  a [[bimodule]] $N$ over a [[monoid]] $A$, in a context where $A$ is really to be thought of as a [[algebra in an (infinity,1)-category|monoid in an monoidal (∞,1)-category]].

If the [[monoid]] in  question plays the role of an _algebra of functions_ on a [[space]] $X$, $A = C(X)$,
then this has geometric interpretations. Notably
  
* the _Hochschild homology_ of $A$ regarded as a bimodule over itself 
  tends to be like the algebra of 
  [[Kähler differential]]s $\Omega^\bullet_K(A)$ on $A$, and hence is something like the algebra of [[differential form]]s on $X$;
    
* the _Hochschild cohomology_ of $A$ regarded as a bimodule over itself
  tends to be like the algebra of [[derivation]]s $Der(A)$ of $A$, 
  and hence something like the [[vector field]]s on $X$.

The seminal [[Hochschild-Kostant-Rosenberg theorem]] states that under suitable [[smooth scheme|smoothness]] conditions on $A$, these statements become exactly true.    
 
Notice that differential forms are objects in [[de Rham cohomology]] but 
are still computed by the Hochschild _homology_ of $A$. 
The terminology reflects the dualization in passing from the [[space]] $X$ to the algebra of functions $A = C(X)$ on it:
it is the Hochschild _homology_ of algebra objects that relates to the
_[[cohomology]]_ of [[space]]s.

Below in section 

* [The nPOV on Hochschild cohomology](#nPOV)

we discuss a conceptual interpretation of Hochschild homology,
that will explain _why_ this is true, and what Hochschild
homology is conceptually, from the [[nPOV]] on [[cohomology]], as 
described there.

Complementary to that, in the section 

* [More traditional description of Hochschild cohomology](#TraditionalIdeas)

we describe the original definition of Hochschild cohomology and 
the evolution of its understanding approaching the [[nPOV]].

Finally in the section titled [Details](#Details) the technical details
are spelled out.
 
 
### More traditional descriptions of Hochschild cohomology {#TraditionalIdeas}
 
Originally the notion of Hochschild cohomology was introduced as the 
[[cochain cohomology]] of a certain [[cochain complex]] associated to any [[bimodule]] $N$ over some [[algebra]] $A$: its [[bar complex]], written 
 
$$
  C_\bullet(N,A) := N \otimes_{A \otimes A^{op}} \mathrm{B}_\bullet A
  \,,
$$
  
where $N$ and $A$ are regarded as $A \otimes A^{op}$-bimodules in the obvious way.

Then it was understood that this complex is the result of tensoring the $A$-bimodules $N$ with $A$ over $A \otimes A^{op}$ but using the [[derived functor]] of the [[tensor product]] functor --  the [[Tor functor]] -- in the ambient [[model structure on chain complexes]]:
 
$$
   C_\bullet(N,A) = N \otimes^D_{A\otimes A^{op}} A = Tor^\bullet_{A\otimes A^{op}}(N,A)
   \,.
$$  
 
Then still a little later, it was understood that this is just the ordinary tensor product in the [[symmetric monoidal (∞,1)-category]] of [[chain complex]]es. If this
is understood, we can just write again simply 
$$
  C_\bullet(M,A) := N \otimes_{A \otimes A^{op}} A
  \,.
$$

This, generally, is the definition of the Hochschild homology object
of any bimodule over an [[monoid in a monoidal (∞,1)-category]]. Of special interest is the case where $N = A$. In this case this object is also called the ("$(\infty,1)$-" or "derived-")**center** of $A$:
  
$$
  Z(A) := A \otimes_{A \otimes A^{op}} A
$$
 
In parallel to this formal understanding of Hochschild homology, its
conceptual meaning has been better understood: from staring at the explicit description of $C_\bullet(N,A)$ one sees that it has something to do with [[loop space object]]s: a chain in $C_n(N,A)$ is usefully thought of as  a circle with $n$ marked points. One of these points is labeled $N$, the  other are labeled $A$. The [[differential]] on $C_\bullet(N,A)$ acts by taking tensor products over $A$ separately of all neighbour pairs of
bimodules sitting on this circle, and taking the alternating sum of this
as a collection of such circles with $(n-1)$ marked points.
 
A fully geometric understanding of these was given by Ben-Zvi/Nadler/Francis in their work on [[derived stack|derived]] [[loop space object]]s and their [[geometric ∞-function theory]]. This we unify now with our [[nPOV]]-perspective on [[cohomology]] in order to give the following [[nPOV]]-perspective on Hochschild cohomology, proper. 

 
Very concretely, Hochschild homology can be computed by the Hochschild chain complex, defined by (FILL IN). Hochschild cohomology can be computed by the Hochschild cochain complex, defined by (FILL IN). One has a cup product on the Hochschild cochain complex, defined by (FILL IN). This gives a dg algebra structure on the Hochschild cochain complex. One also has a bracket, called the Gerstenhaber bracket, defined by (FILL IN). This gives a dg Lie algebra structure on the Hochschild cochain complex. This dg Lie algebra is the one which controls the [[deformation theory|deformations]] of the algebra $A$.



### The $n$POV on Hochschild cohomology {#nPOV}

Let $\mathbf{H}$ be an [[(infinity,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves]] and let $\mathbf{K}$ the $(\infty,2)$-topos of $(\infty,2)$-sheaves on a [[site]] $C$, such that the [[quasicoherent ∞-stack]]

$$
  C : C^{op} \to (\infty,1)Cat
$$

$$
  U \mapsto Stab(C_{/U})
$$ 

as described at [[schreiber:∞-vector bundle]]
does indeed satisfy [[descent]] in that it is indeed an object 
in $\mathbf{K}$.

Recall that for $X \in \mathbf{H} \subset \mathbf{K}$ any object, its [[free loop space object]] $\mathcal{L} X$ is the $(\infty,1)$-[[pullback]]

$$
  \array{
     && \mathcal{L} X
     \\
     & \swarrow && \searrow
     \\
     X &&&& X
     \\
     & {}_{\mathllap{(Id,Id)}}\searrow && \swarrow_{\mathrlap{(Id,Id)}}
     \\
     && X \times X
  }
  \,.
$$

Notice that this is usefully thought of as the [[span trace]] of the 
[[identity]] [[span]]

$$
  \mathcal{L} X 
  = 
  Tr
  \left(
    \array{
      && X
      \\
      & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
      \\
      X &&&& X
    }
  \right)
  \,.
$$

Assume that $X$ is such that on it $C$ satisfies the axioms
of [[geometric function theory]] (see [[geometric ∞-function theory]] for more details).

Then:

The **Hochschild cohomology of $X$** is the [[cohomology]] of 
the [[free loop space object]] $\mathcal{L}X$
with coefficients in $C$:

$$
  HH(X) = \mathbf{H}(\mathcal{L}X, C) =: C(\mathcal{L}X)
  \,.
$$

$$
  HH^n(X) := HH_n(C(X)) := \pi_0\Omega^n\mathbf{H}(\mathcal{L}X, C)
  \,.
$$

By the assumption that $C(-)$ is a 
[[geometric function theory|geometric function object]] on $X$ we can rewrite 

$$
  HH(X) = \mathbf{H}(\mathcal{L}X,C) =: C(\mathcal{K}X)
$$

as 

$$
  \cdots \simeq C(X) \otimes_{C(X)\otimes C(X)^{op}}
   C(X)
  \,.
$$

This is hence indeed the Hochschild homology object $HH_\bullet(A) = A \otimes_{A \otimes A^{op}} A$ 
of the algebra object $A = \infty Mod(X)$, regarded  as a bimodule over itself.

More generally, let $f : Y \to X$ be a morphism in $\mathbf{H}$ and 
consider the [[span trace]] 

$$
  \mathcal{L}_X Y :=
  Tr
  \left(
    \array{
      && Y
      \\
      & {}^{\mathllap{f}}\swarrow && \searrow^{\mathrlap{f}}
      \\
      X &&&& X
    }
  \right)
$$

which is the $(\infty,1)$-[[pullback]]

$$
  \array{
    && \mathcal{L}_X Y
    \\
    & \swarrow && \searrow
    \\
    Y &&&& X
    \\
    & {}_{\mathllap{f,f}}\searrow && \swarrow_{\mathrlap{Id,Id}}
    \\
    && X \times X
  }
  \,.
$$

Then we take the Hochschild cohomology of $Y$ relative to $f : Y \to X$
to be 

$$
  HH(Y,X) := \mathbf{K}(\mathcal{L}_X Y, C) =: \infty Mod(\mathcal{L}_X Y)
  \,.
$$

In the case that $f$ is such that $C(-) = \mathbf{K}(-,C)$ satisfies 
[[geometric function theory]]
on it, this is

$$
  \cdots = C( Y \times_{X \times X} Y)
  \simeq
  C(Y) \otimes_{C(X) \otimes C(X)^{op}} C(X)
  \,.
$$

This is indeed the Hochschild homology object of the $C(X)$-bimodule
object structure on $C(Y)$ induced from $f^*$:

$$
  \cdots =: HH_\bullet(C(Y), C(X))
  \,.
$$

### Differential forms and Hochschild (co)homology

The above identifies Hochschild homology objects of function algebras with function algebras on a [[free loop space object]]. If one adds to this the observation that for a sufficiently wel behaved ordinary space regarded as [[derived stack]] its free loop space object is essentially the formal dual of the algebra of [[Kähler differential]] forms, one recovers from a [[higher geometry]] picture the stamenet of the Hochschild-Kostant-Rosenberg theorem mentioned above. Details are in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322))

* [[Bertrand Toen]] [[Gabriele Vezzosi]], _$S^1$-Equivariant simplicial algebras and de Rham theory_ ([arXiv:0904.3256](http://arxiv.org/abs/0904.3256))

Notice that the function algebra on the derived loop space is just the differential forms as a graded algebra, without the differential. The differential itself comes from the $S^1$-action on the loop space.

> ...details later... but see the above references...



## Details {#Details}


### Function algebra on derived loop space {#FuncsOnDerivedLoopSpace}

We discuss how the Hochschild complex is the function algebra on a [[derived loop space]] object in the context of [[derived geometry]].


Let $T$ be a [[Lawvere theory]] that contains the theory of commutative $k$-algebras , regarded as an [[(∞,1)-algebraic theory]]. 

Let 

$$
  T \subset C \subset  T Alg_\infty^{op}
$$

be a [[subcanonical coverage|subcanonical]] [[small site]] that is a full 
[[sub-(∞,1)-category]] of formal duals of $\infty$-$T$-algebras, closed under [[(∞,1)-limit]]s in $T Alg_\infty^{op}$.

Let $\mathbf{H} = Sh_{(\infty,1)}(C)$ be the [[(∞,1)-sheaf (∞,1)-topos]] over $C$. 

We write $\mathcal{O}(X) \in T Alg_\infty$ for an object that under the [[(∞,1)-Yoneda embedding]] $T Alg_\infty^{op} \to \mathbf{H}$ maps to an object called $X$.

+-- {: .un_def}
###### Definition

For $\mathcal{O}(X) \in T Alg \hookrightarrow T Alg_\infty$ an ordinary $T$-algebra, we say that the [[free loop space object]] $\mathcal{L}X$ of $X$ formed in $\mathbf{H}$ is the **[[derived loop space]]** of $X$.

=--

+-- {: .un_prop}
###### Proposition

We have that $\mathcal{O}(\mathcal{L}X)$ is given by the [[(∞,1)-pushout]] in $T Alg_\infty$ 

$$
  \mathcal{O}\mathcal{L}X \simeq \mathcal{O}(X) \coprod_{\mathcal{O}(X)\otimes \mathcal{O}(X) } \mathcal{O}(X)
$$

hence the universal [[cocone]]

$$
  \array{
    \mathcal{O}\mathcal{L}X &\leftarrow&
    \mathcal{O}(X)
    \\
    \uparrow && \uparrow
    \\
    \mathcal{O}(X) &\leftarrow& \mathcal{O}(X) \otimes \mathcal{O}(X)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since [[∞-stackification]] $L : PSh_{(\infty,1)}(C) \to \mathbf{H}$ is a [[left exact (∞,1)-functor]] and hence preserves finite [[(∞,1)-limit]]s, we have that the defining pullback for $\mathcal{L}X$ may be computed in the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$. Since the [[(∞,1)-Yoneda embedding]] preserves all [[(∞,1)-limit]]s this in turn may be computed in the [[(∞,1)-site]] $C$, hence by assumption in $T Alg_\infty$. The relevant $(\infty,1)$-pullback there is the claimed $(\infty,1)$-pushout in the [[opposite (∞,1)-category]] $T Alg_\infty$. 

=--

+-- {: .un_prop}
###### Proposition

Let $X \in T Alg^{op}$, hence $C(X) \in T Alg \hookrightarrow (\infty,1)T Alg$ be a [[T-algebra]], regarded as an $(\infty,1)$-$T$-algebra. 

Let $\mathcal{L}X$ be the [[derived loop space]] object of $X$, given by the [[(∞,1)-colimit|(∞,1)-pullback]] 

$$
  \array{
    \mathcal{L}X &\to& X
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    X &\to& X \times X
  }
$$

in $T Alg_\infty^{op}$. Then  $C(\mathcal{L}X) \in T Alg_\infty$
is such that 

$$
  \pi_k( C(\mathcal{L}X)) \simeq HH_k(C(X))
  \,.
$$

=--

+-- {: .proof}
###### Proof

In the following write $\otimes$ for the [[coproduct]] in $T Alg$.

Following the discussion at [[homotopy T-algebra]] we may model $T Alg_\infty$ by the _injective_ [[model structure on simplicial presheaves]] on $T^{op}$, [[Bousfield localization of model categories|left Bousfield localized]] at the morphisms $T[k] \otimes T[l] \to T[k+l]$. This localized model structure we write $[T, sSet]_{inj,prod}$.

Since left Bousfield localization does not affect cofibrations, we may, by the general recipe described at [[homotopy pushout]] compute the [[(∞,1)-colimit]]

$$
  \array{
     C(\mathcal{L}X) &\leftarrow& C(X)
     \\
     \uparrow &\swArrow_{\simeq}& \uparrow
     \\
     C(X) &\leftarrow& C(X) \otimes C(X)
  }
$$

in $T Alg_\infty$ by an ordinary [[pushout]]

$$
  \array{
     C(\mathcal{L}X) &\leftarrow& C(X)
     \\
     \uparrow && \uparrow
     \\
     Q C(X) &\leftarrow& C(X) \otimes C(X)
  }
$$


where $Q C(X)$ is some [[resolution]] of $C(X)$ such that the bottom morphism is a cofibration. Since we are in the _injective_ model structure this just means that this morphism need to be a monomorphism. If we find $Q C(X)$ also as a strictly product-preserving functor as $C(X)$ then it being monic over the generating object implies that it is monic over every object.

So we set

$$
  Q C(X) :=
  \left(
     \cdots C(X) \otimes C(X) \otimes C(X) \stackrel{\to}{\to} C(X) \otimes C(X)
  \right)
  \,.
$$

with the evident face and degeneracy maps given by binary product operation in the algebra and insertion of units. Take the morphism 
$C(X) \otimes C(X) \to Q C(X)$ to be the inclusion of $C(X) \otimes C(X)$ as the two outer direct summands. This is clearly a monomorphism. That this is also indeed a weak equivalence in $[T,sSet]_{proj}$ and hence also in $[T,sSet]_{proj,prod}$ (since left Boufield localization just adds weak equivalences, does not remove any) is the standard statement about the acyclicity of the bar complex (for instance <a href="http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=16">page 16 here</a>).

We may now compute the pushout in $[T, sSet]$ and this will compute the desired homotopy pushout. Notice that this pushout indeed takes place just in simplicial copresheaves, not in product-preserving copresheaves! The nature of left Bousfield localization ensures that the result is nevertheless equivalent to the desired $(\infty,1)$-pushout of $\infty$-$T$-algebras.

But this ordinary pushout it manifestly the claimed one.

=--






### Hochschild cohomology and extensions {#Extensions}

+-- {: .un_def }
###### Definition

An [[exact sequence]] $0 \to N \to E \to R$ of $k$-modules where
$E \to R$ is a surjective morphism of $k$-algebras is
called a **$k$-split** extension or a **Hochschild extension** of $R$ by $E$ if the sequence is a [[split sequence]] as a sequence of $k$-[[module]]s.

Two extensions are _equivalent_ if there is an isomorphism or $k$-algebra $E \stackrel{\simeq}{\to} E'$ that makes

$$
  \array{
    N &\to& E &\to& R
    \\
    \downarrow^{\mathrlap{=}} && \downarrow && \downarrow^{\mathrlap{=}}
    \\
    N &\to& E' &\to& R
  }
$$

commute.

=--


+-- {: .un_remark }
###### Remark

Due to the $k$-splitness assumption there is an isomorphism of $k$-modules $E \simeq R \oplus N$ and this is equipped with a $k$-algebra structure such that the product on the $R$ [[direct sum]]mand is that of $R$. From this we find that the product on $E$ is of the form

$$
  (r_1, n_1) \cdot (r_2, n_2) =
  (r_1 r_2 , r_1 n_2 + r_2 n_1 + f(r_1, r_2))
  \,,
$$

where $f : R \otimes_k R \to N$ is some $k$-linear map. Since the product on $E$ is (by definition) associative, it follows that for $f$ that this satisfies for all $r_0, r_1, r_2 \in R$ the _cocycle equation_

$$
  r_0 f(r_1, r_2) - f(r_0 r_1, r_2) + f(r_0 , r_1 r_2) - f(r_0, r_1) r_2 = 0
$$

as an equation in $N$. This says that $f$ must be a Hochschild cocycle

$$
  f \in HH^2(R,N)
  \,.
$$ 

=--


Conversely, every such cocycle yields a $k$-split extension of $R$ by $N$ this way:



+-- {: .un_theorem }
###### Theorem

For $R$ a $k$-algebra and $N$ an $R$-[[bimodule]], equivalence
classes of Hochschild extensions of $R$ by $N$ are in bijection with
degree 2 Hochschild cohomology $HH^2(R,N)$.

=--

See for instance [[An Introduction to Homological Algebra|Weibel, theorem 9.3.1]].


### Hochschild cohomology and deformations {#Deformations}

As a special case of the above statement about extensions of $R$, we obtain a statement about _deformation_ of $R$.

A standard problem is to deform a $k$-algebra $R$ by introducing a new "parameter" $t$ that squares to 0 -- $t \cdot t = 0$ and a new product

$$
  r_1 \cdot_t r_2 = r_1 r_2 + t f(r_1, r_2)  
  \,.
$$

From the above we see that this is the same as finding an $k$-split extension of $R$ by itself. So in particular such extensions are given by Hochschild cocycles $f \in HH^2(R,R)$.

See for instance [Ginzburg, section 7](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf) and for more see [[deformation quantization]].


### Hochschild homology and K&#228;hler differentials {#HochschildKostantRosenberg} 

The **[[Hochschild-Kostant-Rosenberg theorem]]** states that under suitable conditions, the Hochschild homology of an algebra (with coeficients in itself) computes the wedge powers of its [[Kähler differential]]s.

+-- {: .un_prop }
###### Proposition

For a $k$-algebra $R$, its module of [[Kähler differential]]s coincides with its first Hochschild homology

$$
  \Omega(R/k) \simeq HH_1(R,R)
  \,.
$$


=--

Write $\Omega^0(R/k) := R \simeq HH_0(R,R)$.

For $n \geq 2$ Write $\Omega^n(R/k) = \wedge^n_R \Omega(R/k)$ for the $n$-fold [[exterior algebra|wedge product]] of $\Omega(R/k)$ with itself: the degree $n$-K&#228;hler-differentials.

+-- {: .num_theorem }
###### Theorem

The isomorphism $\Omega^1(R/k) \simeq H_1(R,R)$ extends to a graded ring morphism

$$
  \psi : \Omega^\bullet(R/k) \to H_\bullet(R,R)
  \,.
$$

=--

If the $k$-algebra $R$ is sufficiently well-behaved, then this morphism is an [[isomorphism]] that identifies the Hochschild homology of $R$ in degree $n$ with $\Omega^n(R/k)$ for all $n$:

+-- {: .num_theorem }
###### Theorem
**(Hochschild-Kostant-Rosenberg theorem)**



If $k$ is a [[field]] and $R$ a commutative $k$-[[algebra]] which is 

* essentially of finite type 

* smooth over $R$

then there is an [[isomorphism]] of graded $R$-algebras

$$
  \psi : \Omega^\bullet(R/k) \stackrel{\simeq}{\to}
  HH_\bullet(R,R)
  \,.
$$

Moreover, dually, there is an isomorphism of Hochschild cohomology with wedge products of derivations:

$$
  \wedge^\bullet_R Der(R,R) \simeq HH^\bullet(R,R)
$$

=--

+-- {: .proof}
###### Proof

This is reviewed for instance as theorem 9.4.7 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

or as theorem 9.1.3 in [Ginzburg](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=44).

=--



 
## References
 
The traditional story of Hochschild (co)homology is exposed for instance

in chapter 9 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

or in chapter 4 of
 
* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603))

An original paper on this is

* Tsygan and Feigin,  _Additive K-theory_ 1980-s (LNM 1289, editor Manin, pp 67-209, seminar 1984-1986 in Moscow)

 
The $(\infty,1)$-categorical picture of [[derived stack|derived]] [[free loop space object]]s and their [[geometric ∞-function theory]] is discussed in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322))

* [[Bertrand Toen]] [[Gabriele Vezzosi]], _$S^1$-Equivariant simplicial algebras and de Rham theory_ ([arXiv:0904.3256](http://arxiv.org/abs/0904.3256))


* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], 
  _[[geometric infinity-function theory|Integral transforms and Drinfeld centers in derived algebraic geometry]]_ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))
 

Generalizations of Hochschild cohomology with the circle replaced by more general spaces is surveyed in 

* [[Grégory Ginot]], _Higher order Hochschild cohomology ([pdf](http://www.institut.math.jussieu.fr/~ginot/papers/Higher-Order-Hochschild-Long.pdf))


Interesting wishlists for treatments of Hochschild cohomology are in [this](http://mathoverflow.net/questions/28472/book-on-hochschild-cohomology) MO discussion.


[[!redirects Hochschild homology]]

[[!redirects Hochschild complex]]
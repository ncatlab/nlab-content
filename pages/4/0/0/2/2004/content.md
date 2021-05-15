
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The category of [[algebras over a monad]] (also: "modules over a monad") is traditionally called its _Eilenberg--Moore category_ (EM). Dually, the EM category of a [[comonad]] is its category of coalgebras (co-modules). 

The [[subcategory]] of [[free functor|(co-)free]] (co-)algebras is traditionally called the _[[Kleisli category]]_ of the (co-)monad. 

The EM and Kleisli categories have universal properties which make sense for (co-)monads in any [[2-category]] (not necessarily [[Cat]]).


## Definition
 {#Definition}

Let $(T,\eta,\mu)$ be a [[monad]] in [[Cat]], where $T \colon C\to C$ is an [[endofunctor]] with multiplication $\mu \colon T T\to T$ and unit $\eta \colon Id_C\to T$.  


+-- {: .num_defn}
###### Definition


A (left) $T$-[[algebra for a monad|module]] (or $T$-algebra) in $C$ is a pair $(A,\nu)$ of an object $A$ in $C$ and a morphism $\nu\colon T(A)\to A$ which is a __$T$-[[action]]__, in that 

$$
  \nu\circ T(\nu)=\nu\circ\mu_{A} \colon T(T(A))\to A
$$ 

and 

$$
  \nu\circ\eta_A = id_A
  \,.
$$


A [[homomorphism]] of $T$-modules $f\colon (A,\nu^A)\to (B,\nu^B)$ is a morphism $f\colon A \to B$ in $C$ that commutes with the action, in that

$$
  f\circ\nu^A=\nu^B\circ T(f)\colon T(A)\to B
  \,.
$$ 

The composition of morphisms of $T$-modules is the composition of underlying morphisms in $C$. The resulting [[category]] $C^T$ of $T$-modules/algebras is called the __Eilenberg--Moore category__ of the monad $T$, also be written $Alg(T)$, or $T\,Alg$, etc.  

By construction, there is a [[forgetful functor]] 

$$
  U^T \colon C^T \to C
$$ 

(which may be thought of as the [[universal property|universal]] $T$-module) with a [[left adjoint]] [[free functor]] $F^T$ such that the monad $U^T F^T$ arising from the adjunction is isomorphic to $T$.

=--

More generally, for $t \colon a \to a$ is a monad in any [[2-category]] $K$, then the __Eilenberg--Moore object__ $a^t$ of $t$ is, if it exists, the universal (left) $t$-module.  That is, there is a morphism $u^t \colon a^t \to a$ and a 2-cell $t u^t \Rightarrow u^t$ that mediate a natural isomorphism $K(x, a^t) \cong LMod(x,t)$ between morphisms $x \to a^t$ and $t$-modules $(m \colon x \to a, \lambda \colon t m \Rightarrow m)$.  Not every 2-category admits Eilenberg--Moore objects.


## Properties

### Universal properties

Apart from being the universal left $T$-module, the EM category of a monad $T$ in $Cat$ has some other interesting properties.

There is a [[full subcategory]] $RAdj(C)$ of the [[slice category]] $Cat/C$ on the functors $X \to C$ that have [[left adjoints]].  For any monad $T$ on $C$ there is a full subcategory of this consisting of the adjoint pairs that compose to give $T$.  The functor $U^T \colon C^T \to C$ is the [[terminal object]] of this category.

### As a colimit completion of the Kleisli category
 {#AsColimitCompletionOfKleisliCategory}


+-- {: .num_prop}
###### Proposition

Every $T$-algebra $(A,\nu)$ is the [[coequalizer]] of the first stage of its [[bar resolution]]:

$$
  (T^2 A, \mu_{T A})
  \stackrel{\overset{\mu_A}{\longrightarrow}}{\underset{T \nu}{\longrightarrow}}
  (T A, \mu_A)
  \stackrel{\nu}{\longrightarrow}
  (A,\nu)
  \,.
$$

This is a [[reflexive coequalizer]] of $T$-algebras. Moreover, the underlying [[fork]] in $C$ is a [[split coequalizer]], hence in particular an [[absolute coequalizer]] (sometimes called the _Beck coequalizer_, due to its role in the [[Beck monadicity theorem]]). A splitting is given by  

$$
  T^2 A  \stackrel{\eta_{T A}}{\longleftarrow} T A \stackrel{\eta_A}{\longleftarrow} A
\,.
$$

=--

(e.g. [MacLane, bottom of p. 148 and exercise 4 on p. 151](#MacLane)) See also at [split coequalizer -- Beck coequalizer for algebras over a monad](split+coequalizer#BeckCoequalizerForAlgebrasOverAMonad).

In particular this says that every $T$-algebra is [[generators and relations|presented]] by free $T$-algebras. The nature of $T$-algebras as a kind of completion of free $T$-algebras under colimits is made more explicit as follows.

Write $C_T$ for the [[Kleisli category]] of $T$, the category of [[free construction|free]] $T$-algebras. Write $F_T \colon C \to C_T$ the [[free functor]].
Observe that via the inclusion $C_T \hookrightarrow C^T$ every $T$-algebra [[representable functor|represents]] a [[presheaf]] on $C_T$. Recall that the [[category of presheaves]] $[C_T^{op}, Set]$ is the [[free cocompletion]] of $C_T$.

+-- {: .num_prop}
###### Proposition

The $T$-algebras in $C$ are equivalently those presheaves on the category of free $T$-algebras whose restriction along the free functor is [[representable functor|representable]] in $C$. In other words, the Eilenberg--Moore category $C^T$ is the (1-category theoretic) [[pullback]]

$$
  \array{
    C^T & \to & [C_T^{op}, Set] \\
    \downarrow & (pb) & \downarrow \mathrlap{[F_T^{op},Set]} \\
    C & \underset{Y}{\to} & [C^{op}, Set]
  }
$$

of the [[category of presheaves]] on the [[Kleisli category]] along the [[Yoneda embedding]] $Y$ of $C$. (The top arrow is given by the nerve of the inclusion of the Kleisli category into the Eilenberg--Moore category.)

=--

This statement appears as ([Street 72, theorem 14](#Street72)). It seems to go back to ([Linton 69](#Linton69)), see ([Melli&#232;s 10, p. 4](#Mellies10)). ([Street-Walters 78](#StreetWalters78)) show that it holds in any 2-category equipped with a [[Yoneda structure]].

+-- {: .proof}
###### Sketch of proof
It is easy to see that the square commutes. To see that it is a pullback, assume that $P:C_T^{op}\to Set$ is a presheaf on the Kleisli category and $A$ is an object of $C$ such that $YA=P\circ F_T^{op}$. Then a $T$-algebra structure $\alpha:TA\to A$ on $A$ 
is given by $\alpha=P(1_{TA})(1_A)$, where $1_{TA}$ is viewed as a [[Kleisli category#in_terms_of_kleisli_morphisms|Kleisli morphism]] from $TA$ to $A$ in $C_T$.
=--

### By lax 2-limits

Just as the [[Kleisli object]] of a monad $t$ in a 2-category $K$ can be defined as the [[lax colimit]] of the [[lax functor]] $\ast \to K$ [[monad|corresponding]] to $t$, the EM object of $t$ is its [[lax limit]].


S. Lack has shown how Eilenberg--Moore objects $C^T$ can be obtained as combinations of certain simpler lax limits, when the 2-category $K$ in question is the 2-category of 2-algebras over a 2-monad $\mathbf{G}$ and lax, colax or pseudo morphisms of such: 

* [[Steve Lack]], _Limits for lax morphisms_ , Applied Categorical Structures __13__:3 (2005) , pp. 189--203(15) 

This encompasses for example the theory of (op)monoidal monads and corresponding monoidal Eilenberg--Moore categories.

If $(T,\mu,\eta)$ is a monad in a small category $A$, and $B$ is another category, then consider the functor category $[B,A]$. There is a tautological monad $[B,T]$ on $[B,A]$ defined by $[B,T](F)(b) = T(F(b))$, $b\in Ob B$, $[B,T](F)(f) = T(F(f))$, $f\in Mor B$, $\mu^{[B,T]}_F : TTF\Rightarrow TF$, $(\mu^{[B,T]}_F)_b = \mu_{Fb}$
$(\eta^{[B,T]}_F)_b = \eta_{Fb} : Fb\to TFb$. Then there is a canonical isomorphism of EM categories

$$
[B,A^T] \cong [B,A]^{[B,T]}.
$$

Namely, write the object part of a functor $G : B\to A^T$ as $(G^A,G^\rho)$, where $G^A :B\to A$ and $G^\rho(b) : TG^A(b)\to G^A(b)$ is the $T$-action of $G^A(b)$ and the morphism part simply as $f\mapsto G(f)$. Then, $G^\rho : b\mapsto G^\rho(b) : TG^A\Rightarrow G^A$ is a natural transformation because for any morphism $f:b\to b'$, $G(f) : (G^A(b),G^\rho(b))\to (G^A(b'),G^\rho(b'))$ is by the definition of $G$, a morphism of $T$-algebras. $G^\rho$ is, by the same argument, an action $[B,T](G^A)\Rightarrow G^A$. Conversely, for any $[B,T]$-module $(G^A,G^\sigma)$ for any $b\in Ob B$, $G^\sigma(b)$ will evaluate to a $T$-action on $G^A(b)$, hence $b\mapsto (G^A(b), G^\sigma(b))$ is an object part of a functor in $[B,A^T]$ with morphism part again $f\mapsto G(g)$. The correspondence for the natural transformations, $g: (G^A,G^\sigma)\Rightarrow (H^A,H^\tau)$ is similar. 

Dually, for a comonad $\Omega$ in $B$, there is a canonical comonad $[\Omega, A]$ on $[B,A]$ and an isomorphism of categories 

$$
[B^\Omega, A] \cong [B,A]^{[\Omega,A]}
$$

### Limits and colimits in EM categories

* The Eilenberg--Moore category of a monad $T$ on a category $C$ has all [[limits]] which exist in $C$, and they are [[created limit|created]] by the forgetful functor.

* In contrast, the subject of [[colimits in categories of algebras]] is less easy, but a good deal can be said.


### Local presentability
 {#LocalPresentability}

+-- {: .num_defn #AccessibleMonad}
###### Definition

An _[[accessible monad]]_ is a [[monad]] on an [[accessible category]] whose underlying [[functor]] is an [[accessible functor]].

=--

+-- {: .num_prop}
###### Proposition

The Eilenberg--Moore category of a $\kappa$-accessible monad, def. \ref{AccessibleMonad}, is a  $\kappa$-[[accessible category]]. If in addition the category on which the monad acts is a $\kappa$-[[locally presentable category]] then so is the EM-category.


=--

([Adamek-Rosicky, 2.78](#AdamekRosicky))

Moreover, let $C$ be a [[topos]]. Then

* if a [[monad]] $T : C \to C$ has a [[right adjoint]] then $T Alg(C)= C^T$ is itself a topos;

* if a [[comonad]] $T : C \to C$ is [[exact functor|left exact]], then $T CoAlg(C) = C_T$ is itself a topos.

See at _[[topos of algebras over a monad]]_ for details.

## Examples

+-- {: .num_example}
###### Examples

Given a [[reflective subcategory]] $\mathcal{C} \stackrel{\overset{L}{\leftarrow}}{\underset{\hookrightarrow}{i}} \mathcal{D}$ then the Eilenberg--Moore category of the induced [[idempotent monad]] $i\circ L$ on $\mathcal{D}$ recovers the subcategory $\mathcal{C}$.

=--

For instance ([Borceux, vol 2, cor. 4.2.4](#Borceux)).



## Related concepts

* [[(∞,1)-category of algebras over an (∞,1)-monad]]

## References

General discussion is in 

* {#Street72} [[Ross Street]], _The formal theory of monads_, Journal of Pure and Applied Algebra 2, 1972 

* [[Fred Linton]], _An outline of functorial semantics_, in [[LNM 80]], 1969

* {#Linton69} [[Fred Linton]], _Relative functorial semantics: adjointness results_, Lecture Notes in Mathematics, vol. 99, 1969

* {#StreetWalters78} [[Ross Street]], [[Bob Walters]], _Yoneda structures_, J. Algebra __50__, 1978

* {#MacLane} [[Saunders MacLane]], _[[Categories for the Working Mathematician]]_

Local presentability of EM-categories is discussed on p. 123, 124 of

* [[Ji?í Adámek]], [[Ji?í Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}

The following paper of Melli&#232;s compares the representability condition of ([Linton 69](#Linton69)) with the [[Segal condition]] that distinguishes those [[simplicial sets]] that are the [[nerves]] of categories.

* {#Mellies10} [[Paul-André Melliès]], _Segal condition meets computational effects_, LICS 2010 ([pdf](http://www.pps.jussieu.fr/~mellies/papers/segal-lics-2010.pdf))

The example of [[idempotent monads]] is discussed also in

* [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_, vol.2, p. 196.
 {#Borceux}

Discussion for [[(infinity,1)-monads]] realized in the context of [[quasi-categories]] is around def. 6.1.7 of

* [[Emily Riehl]], [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))
 {#RiehlVerity13}

[[!redirects Eilenberg--Moore categories]]
[[!redirects Eilenberg–Moore category]]
[[!redirects Eilenberg--Moore category]]
[[!redirects Eilenberg--Moore category]]
[[!redirects Eilenberg--Moore object]]
[[!redirects Eilenberg--Moore object]]
[[!redirects Eilenberg--Moore object]]
[[!redirects Alg(T)]]
[[!redirects T-Alg]]
[[!redirects T-alg]]
[[!redirects T Alg]]
[[!redirects T alg]]

[[!redirects Beck coequalizer]]
[[!redirects Beck coequalizers]]
[[!redirects Beck coequaliser]]
[[!redirects Beck coequalisers]]

[[!redirects Beck equalizer]]
[[!redirects Beck equalizers]]
[[!redirects Beck equaliser]]
[[!redirects Beck equalisers]]

[[!redirects category of algebras over a monad]]
[[!redirects category of algebras for a monad]]

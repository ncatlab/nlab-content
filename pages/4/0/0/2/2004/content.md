
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
### Eilenberg--Moore object

More generally, for $t \colon a \to a$ is a monad in any [[2-category]] $K$, then the __Eilenberg--Moore object__ $a^t$ of $t$ is, if it exists, the universal (left) $t$-module.  That is, there is a "forgetful" 1-cell $u^t \colon a^t \to a$ and a 2-cell $\beta \colon t u^t \Rightarrow u^t$ that mediate a natural isomorphism $K(x, a^t) \cong LMod(x,t)$ between morphisms $h \colon x \to a^t$ and $t$-modules $(m \colon x \to a, \lambda \colon t m \Rightarrow m)$.  Not every 2-category admits Eilenberg--Moore objects.

\begin{center}
\begin{tikzcd}
x
\arrow[rrr, "m", bend left=60, "" {name=A, xshift=6ex, below} ]
\arrow[rr, "m", bend left ]
\arrow[r, dashed, "h"']
&a^t
\arrow[rr, "u^t"', bend right=80, "" {name=B, above} ]
\arrow[r, "u^t"']
&a
\arrow[Rightarrow, "\lambda", shorten >= 0.8ex, shorten <=0.4ex, to=A]
\arrow[Rightarrow, "\beta"', shorten >= 0.4ex, shorten <=0.4ex,  to=B]
\arrow[r, "t"']
& a
\end{tikzcd}
\end{center}

### (Non)example

Let [[Rel|REL]] be the (locally posetal) 2-category of sets and relations. A monad on a set $X$ is just an endorelation $R$ satisfying $id_X\subseteq R$ (reflexivity) and $R\circ R \subseteq R$ (transitivity) i.e. a [[preorder]] on $X$. When $R$ arises from an adjunction it is necessarily of the form $R=F\circ F^{op}$ implying $R=R^{op}$ (symmetry) since adjunctions in $REL$ consist of functional relations as the left adjoint with their opposite relation as right adjoint. In other words, only [[equivalence relation|equivalence relations]] admit Eilenberg--Moore objects which then consist of the set $X^R$ of equivalence classes with "free algebra functor" $F^R$ relating $x\in X$ to its equivalence class $[x]\in X^R$.

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

\begin{center}
 \begin{tikzcd}
 \mathcal C^T
 \arrow[d, ""']
 \arrow[r, ""]
\arrow[dr, phantom,  , very near start, "\lrcorner"]
 & {[\mathcal C_T^{op}, \mathbf{Set}]}
 \arrow[d, "{[F_T^{op}, \mathbf{Set}]}"]
 \\
 \mathcal C
 \arrow[r, "Y"']
 &
 {[\mathcal C^{op}, \mathbf{Set}]}
  \end{tikzcd}
\end{center}

of the [[category of presheaves]] on the [[Kleisli category]] along the [[Yoneda embedding]] $Y$ of $C$. (The top arrow is given by a functor isomorphic to the nerve of the inclusion of the Kleisli category into the Eilenberg--Moore category.)

=--

This statement appears as [(Linton 69, Observation 1.1)](#Linton69) (cf. [(Street 72, Theorem 14)](#Street72)). [(Street-Walters 78)](#StreetWalters78) establish a generalisation for a 2-category equipped with a [[Yoneda structure]]. [Arkor–McDermott '24](#AM24) establish a generalisation to a [[virtual equipment]], which also captures [[relative monads]] with [[dense functor|dense]] roots.

+-- {: .proof}
###### Sketch of proof
It is easy to see that the square commutes. To see that it is a pullback, assume that $P:C_T^{op}\to Set$ is a presheaf on the Kleisli category and $A$ is an object of $C$ such that $YA=P\circ F_T^{op}$. Then a $T$-algebra structure $\alpha:TA\to A$ on $A$ 
is given by $\alpha=P(1_{TA})(1_A)$, where $1_{TA}$ is viewed as a [[Kleisli category#in_terms_of_kleisli_morphisms|Kleisli morphism]] from $TA$ to $A$ in $C_T$.
=--

### By lax 2-limits

Just as the [[Kleisli object]] of a monad $t$ in a 2-category $K$ can be defined as the [[lax colimit]] of the [[lax functor]] $\ast \to K$ [[monad|corresponding]] to $t$, the EM object of $t$ is its [[lax limit]].


[[Steve Lack]] has shown how Eilenberg--Moore objects $C^T$ can be obtained as combinations of certain simpler lax limits, when the 2-category $K$ in question is the 2-category of 2-algebras over a 2-monad $\mathbf{G}$ and lax, colax or pseudo morphisms of such: 

* [[Steve Lack]], _Limits for lax morphisms_, Applied Categorical Structures __13__:3 (2005) , pp. 189--203(15) 

This encompasses for example the theory of (op)monoidal monads and corresponding monoidal Eilenberg--Moore categories.

If $(T,\mu,\eta)$ is a monad in a small category $A$, and $B$ is another category, then consider the functor category $[B,A]$. There is a tautological monad $[B,T]$ on $[B,A]$ defined by $[B,T](F)(b) = T(F(b))$, $b\in Ob B$, $[B,T](F)(f) = T(F(f))$, $f\in Mor B$, $\mu^{[B,T]}_F : TTF\Rightarrow TF$, $(\mu^{[B,T]}_F)_b = \mu_{Fb}$
$(\eta^{[B,T]}_F)_b = \eta_{Fb} : Fb\to TFb$. Then there is a canonical isomorphism of EM categories

$$
[B,A^T] \cong [B,A]^{[B,T]}.
$$

Namely, write the object part of a functor $G : B\to A^T$ as $(G^A,G^\rho)$, where $G^A :B\to A$ and $G^\rho(b) : TG^A(b)\to G^A(b)$ is the $T$-action of $G^A(b)$ and the morphism part simply as $f\mapsto G(f)$. Then, $G^\rho : b\mapsto G^\rho(b) : TG^A\Rightarrow G^A$ is a natural transformation because for any morphism $f:b\to b'$, $G(f) : (G^A(b),G^\rho(b))\to (G^A(b'),G^\rho(b'))$ is by the definition of $G$, a morphism of $T$-algebras. $G^\rho$ is, by the same argument, an action $[B,T](G^A)\Rightarrow G^A$. Conversely, for any $[B,T]$-module $(G^A,G^\sigma)$ for any $b\in Ob B$, $G^\sigma(b)$ will evaluate to a $T$-action on $G^A(b)$, hence $b\mapsto (G^A(b), G^\sigma(b))$ is an object part of a functor in $[B,A^T]$ with morphism part again $f\mapsto G(g)$. The correspondence for the natural transformations, $g: (G^A,G^\sigma)\Rightarrow (H^A,H^\tau)$ is similar. 

Dually, for a comonad $\Omega$ in $B$, there is a canonical comonad $[A, \Omega]$ on $[A, B]$ and an isomorphism of categories 

$$
[A, B^\Omega] \cong [A, B]^{[A, \Omega]}
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
* [[Eilenberg-Moore category]], [[Kleisli category]]
* [[Eilenberg-Moore object]], [[Kleisli object]]
* [[module over a monad]]


## References

Original reference: 

* [[Samuel Eilenberg]], [[John Moore]], _Adjoint functors and triples_, Illinois J. Math. **9** 3 (1965) 381-398 &lbrack;[doi:10.1215/ijm/1256068141](https://doi.org/10.1215/ijm/1256068141)&rbrack;

General discussion:

* [[Fred Linton]], §7 in: *An outline of functorial semantics*, in *[[Seminar on Triples and Categorical Homology Theory]]*, Lecture Notes in Mathematics **80**, Springer (1969) 7-52 &lbrack;[doi:10.1007/BFb0083080](https://doi.org/10.1007/BFb0083080)&rbrack;

* {#Linton69} [[Fred Linton]], _Relative functorial semantics: adjointness results_, Lecture Notes in Mathematics, **99** (1969)

* {#Pumplün70} [[Dieter Pumplün]], *Eine Bemerkung über Monaden und adjungierte Funktoren*, Mathematische Annalen **185** (1970) 329-337 &lbrack;[eudml:161964](https://eudml.org/doc/161964), [[Pumpluen-Monaden.pdf:file]]&rbrack;

* [[Saunders MacLane]], §VI.2 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**  Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Street72} [[Ross Street]], *The formal theory of monads*, Journal of Pure and Applied Algebra **2** 2 (1972) 149-168 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90019-9">doi:10.1016/0022-4049(72)90019-9</a>&rbrack;

* [[Michael Barr]], [[Charles Wells]], §3.2 of: *[[Toposes, Triples, and Theories]]*, Grundlehren der math. Wissenschaften **278**, Springer (1983) &lbrack;[TAC:12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)&rbrack;


* {#StreetWalters78} [[Ross Street]], [[Bob Walters]], _Yoneda structures_, J. Algebra __50__, 1978

* {#AM24} [[Nathanael Arkor]], [[Dylan McDermott]], _The pullback theorem for relative monads_ (2024) &lbrack;[arXiv:2404.01281](https://arxiv.org/abs/2404.01281)&rbrack;


* [[Stephen Lack]], [[Ross Street]], *The formal theory of monads II*, Journal of Pure and Applied Algebra
**175** 1–3 (2002) 243-265 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00137-8">doi:10.1016/S0022-4049(02)00137-8</a>&rbrack;


On [[locally presentable category|local presentability]] of EM-categories:

* {#AdamekRosicky} [[Jiří Adámek]], [[Jiří Rosický]], p. 123, 124 of: _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 

The following paper of Melli&#232;s compares the representability condition of ([Linton 69](#Linton69)) with the [[Segal condition]] that distinguishes those [[simplicial sets]] that are the [[nerves]] of categories.

* {#Mellies10} [[Paul-André Melliès]], _Segal condition meets computational effects_, LICS 2010 ([pdf](http://www.pps.jussieu.fr/~mellies/papers/segal-lics-2010.pdf))

The example of [[idempotent monads]] is discussed also in

* [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_, vol.2, p. 196.
 {#Borceux}

Discussion of the [[universal property]] as the final adjoint decomposition of the monad:

* [[Anthony Voutas]], *The basic theory of monads and their connection to universal algebra*, (2012) &lbrack;[pdf](https://voutasaur.us/monad-algebra.pdf), [[Voutas-Monads.pdf:file]]&rbrack;

Discussion for [[(infinity,1)-monads]] realized in the context of [[quasi-categories]] is around def. 6.1.7 of

* [[Emily Riehl]], [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))
 {#RiehlVerity13}

An analogue of the pullback theorem for [[lax algebras]] (there confusingly called "pseudoagebras") of a [[2-monad]] is given in:

* [[Albert Burroni]]. _Structures pseudo-algébriques (1ère partie)_. Cahiers de topologie et géométrie différentielle catégoriques 16.4 (1975): 343-393. ([pdf](http://www.numdam.org/item/CTGDC_1975__16_4_343_0.pdf))

[[!redirects Eilenberg--Moore categories]]
[[!redirects Eilenberg–Moore category]]
[[!redirects Eilenberg--Moore category]]
[[!redirects Eilenberg-Moore categories]]
[[!redirects Eilenberg--Moore object]]
[[!redirects Eilenberg--Moore objects]]
[[!redirects Eilenberg-Moore object]]
[[!redirects Eilenberg-Moore objects]]
[[!redirects Eilenberg–Moore object]]
[[!redirects Eilenberg–Moore objects]]
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

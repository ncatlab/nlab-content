

> There are two different concepts called _Weil algebra_. This entry is about the notion of Weil algebra in [[Lie theory]]. For the notion in [[infinitesimal object|infinitesimal]] geometry see [[infinitesimally thickened point]]/[[local Artin algebra]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of _Weil algebra_ is ordinarily defined for a [[Lie algebra]] $\mathfrak{g}$. It may be understood as the [[Chevalley-Eilenberg algebra]] of the tangent [[Lie 2-algebra]] $T \mathfrak{g}$ or $inn(\mathfrak{g})$ of $\mathfrak{g}$, generalizing the notion of [[tangent Lie algebroid]] $T X$ from a 0-[[truncated]] Lie algebroid $X$ (a [[smooth manifold]]) to the one-object [[Lie algebroid]] $\mathfrak{g}$.

Generally, for every [[Lie-∞-algebroid]] $\mathfrak{a}$ one may define the corresponding tangent Lie-$\infty$-algebroid $T \mathfrak{a}$, whose Chevalley-Eilenberg algebra may be called the Weil algebra of $\mathfrak{a}$:

$$
  W(\mathfrak{a})
  =
  CE(T \mathfrak{a})
  \,.
$$



### Weil algebra of a Lie algebra 

Let $\mathfrak{g}$ be a finite-dimensional [[Lie algebra]]. The **Weil algebra** $W(\mathfrak{g})$ of $\mathfrak{g}$ is

* the graded [[Grassmann algebra]] generated from the dual [[vector space]] $\mathfrak{g}^*$ together with another copy of $\mathfrak{g}^*$ shifted in degree

  $$
    W(\mathfrak{g}) 
    \coloneqq 
    \wedge^\bullet 
   (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])
  $$

* equipped with a [[derivation]] $d : W(\mathfrak{g}) \to W(\mathfrak{g})$ that makes this a [[dg-algebra]], defined by the fact that on $\mathfrak{g}^*$ it acts as the differential of the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ plus the degree shift morphism $\mathfrak{g}^* \to \mathfrak{g}^*$.

This Weil algebra has trivial [[chain homology and cohomology|cohomology]] everywhere (except in degree 0 of course) and sits in a sequence

$$
  CE(\mathfrak{g}) \leftarrow W(\mathfrak{g})
  \leftarrow inv(\mathfrak{g})
$$

with the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ and its algebra of [[invariant polynomial]]s on $\mathfrak{g}$. This may be understood as a model for the sequence of algebras of differential forms on the [[generalized universal bundle|universal G-bundle]]

$$
  G \to \mathcal{E}G \to \mathcal{B}G
  \,.
$$

As such, the Weil algebra plays a crucial role in the study of the [[Lie algebra cohomology]] of $\mathfrak{g}$.


## Definition

We first consider Weil algebras of [[L-∞ algebras]], then more generally of [[L-∞ algebroid]]s.

We use the notation and grading conventions that are described in detail at [[Chevalley-Eilenberg algebra]].


### For $L_\infty$-algebras

#### Plain Weil algebra

Let $\mathfrak{g}$  be an [[L-∞ algebra]] of [[finite type]]. By our grading conventions this means that the [[graded vector space]] $\mathfrak{g}^*$ obtained by degreewise dualization is in non-negative degree, and $\wedge^1 \mathfrak{g}^* = \mathfrak{g}^*[1]$ is its shift up into positive degree.

A quick abstract way to characterize the Weil algebra of $\mathfrak{g}$ is as follows. Notice that there is a [[free functor]]/[[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) 
  \colon 
  dgAlg 
  \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\longrightarrow}}
  Vect[\mathbb{Z}]
$$

between the [[category]] [[dgAlg]] of [[dg-algebras]] and the category of $\mathbb{Z}$-graded [[vector space]]s (all over some fixed [[field]]). Notice that a free object is unique _up to [[isomorphism]]_ .

\begin{definition}\label{PlainWeilAlgebraOfLInfinityAlgebra}
**(plain Weil algebra of $L_\infty$-algebra)**
\linebreak
The **Weil algebra** $W(\mathfrak{g})$ of an $L_\infty$-algebra is the unique representative of the [[free functor|free]] [[dg-algebra]] on $\wedge^1 \mathfrak{g}^*$ for which the projection of graded vector spaces $\wedge^1(\mathfrak{g}^* \oplus \mathfrak{g}^*[1]) \to \wedge^1 \mathfrak{g}^*$ extends to a [[dg-algebra]] [[homomorphism]] $W(\mathfrak{g}) \to CE(\mathfrak{g})$

\end{definition}

We discuss below in the [Properties](#Properties) section that this is equivalent to the following component-wise definition

+-- {: .num_defn #WeilForLInfinitityAlgebra}
###### Definition

The **Weil algebra** $W(\mathfrak{g})$ is the [[semi-free dga]] whose underlying graded-commutative algebra is the [[exterior algebra]]

$$
  \wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])
$$

on $\mathfrak{g}^*$ and a shifted copy of $\mathfrak{g}^*$,
and whose [[differential]] is the sum

$$
  d_{W(\mathfrak{g})} = d_{CE(\mathfrak{g})} + \mathbf{d}
$$

of two graded [[derivations]] of degree +1 defined by

* $\mathbf{d}$ acts by degree shift $\mathfrak{g}^* \to \mathfrak{g}^*[1]$ on elements in $\mathfrak{g}^*$ and by 0 on elements of $\mathfrak{g}^*[1]$;

* $d_{CE(\mathfrak{g})}$ acts on unshifted elements in $\mathfrak{g}^*$ as the differential of the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ and is extended uniquely to shifted generators by graded-commutativity 
 
  $$
    [d_{CE(\mathfrak{g})}, \mathbf{d}] = 0
  $$

  with $\mathbf{d}$:

  $$
    d_{CE(\mathfrak{g})} \mathbf{d} \omega 
    \coloneqq
    - \mathbf{d} d_{CE(\mathfrak{g})} \omega
  $$

  for all $\omega \in \wedge^1 \mathfrak{g}^*$.

=--

#### Adjusted Weil algebras
 {#AdjustedWeilAlgebras}

For some purposes of [[schreiber:L-infinity algebra connections|$L_\infty$-algebra valued connection]], the [above](#WeilForLInfinitityAlgebra) definition of Weil algebra of an $L_\infty$-algebra is not quite appropriate. While Def. \ref{WeilForLInfinitityAlgebra} gives the Weil algebra up to compatible [[isomorphism]], in applications there is in fact the freedom to choose it up to compatible [[quasi-isomorphism]], and this freedom allows to find better representatives.

For more on this see at *[[adjusted Weil algebra]]*.



### For $L_\infty$-algebroids

Where the [[Chevalley-Eilenberg algebra]] of an [[L-∞ algebra]] has in degree 0 the ground field, that of an [[L-∞ algebroid]] has more generally an [[algebra over a Lawvere theory|algebra over]] a [[Lawvere theory]]. For [[L-∞ algebroid]]s over [[smooth manifold]]s this is the algebra of [[smooth function]]s on a manifolds, regarded as a [[smooth algebra]] ($C^\infty$-ring).

So let $T$ be a [[Fermat theory]]. Write $T Alg$ for the corresponding [[category]] of [[algebra over a Lawvere theory|algebra]]. There is a [[free functor]]/[[forgetful functor]] [[adjunction]]


$$
  (F \dashv U) :  
   T Alg 
    \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} 
  CRing
$$

to the category [[CRing]] of commutative [[Ring]]s.

We need the facts that

* a [[module]] over a $T$-algebra $A$ is uniquely specified by its underlying module over $U(A)$;

* the universal [[derivation]] on a $T$-algebra $A$ is the  [[de Rham differential]] 

  $$
    d_{dR} : A \to \Omega^1(A)
  $$

 with values in the $A$-module of $T$-[[Kähler differential]]s. 

See the corresponding entries for more details. The second point means that for $v : A \to N$ any $T$-[[derivation]] on $A$, there is a unique $A$-[[module]] [[homomorphism]]

$$
  \Omega^\bullet(A) \to N
$$

such that the diagram

$$
  \array{
    && \Omega^\bullet(A)
    \\
    & {}^{\mathllap{d_{dR}}}\nearrow & \downarrow^{\mathrlap{v}}
    \\
    A &\stackrel{v}{\to}& N
  }
$$

commutes. 

Let now $\mathfrak{a}$ be an [[L-∞ algebroid]] with [[Chevalley-Eilenberg algebra]] considered as the following data;

1. a graded commutative [[semifree dga]] $CE(\mathfrak{a})$ over the ground field;

1. the structure of a $T$-[[algebra over a Lawvere theory|algebra]] on the [[associative algebra]] $A \coloneqq CE(\mathfrak{a})_0$ (over the ground field)

   such that $d_{CE(\mathfrak{a})} : CE(\mathfrak{a})_0 \to CE(\mathfrak{a})_1$ is a [[derivation]] of $T$-algebra modules.

By [[semifree dga|semi-freeness]] there exists a $\mathbb{N}$-[[graded vector space]] $(\mathfrak{a}^*)^\bullet$ and an [[isomorphism]]

$$
  CE(\mathfrak{a})
   \simeq
  (\wedge^\bullet_{A} (\mathfrak{a}^*), d_{CE(\mathfrak{a})})
  \,.
$$


+-- {: .num_defn}
###### Definition

The **Weil algebra** $W(\mathfrak{a})$ of the $L_\infty$-algebroid $\mathfrak{a}$ is the Chevalley-Eilenberg algebra of the $L_\infty$-algebroid defined as follows

* the $T$-algebra $A$ in degree 0 is the same as that of $\mathfrak{A}$;

* the underlying graded algebra is the [[exterior algebra]] on $\mathfrak{a}^*$ and a shifted copy $\mathfrak{a}^*[1]$ as well as one copy of the [[Kähler differential]] module $\Omega^1$ in lowest degree (though of as the shifted copy of $A$ itself)

  $$
    \wedge^\bullet (\Omega^1(A) \oplus  (\mathfrak{a}^*) \oplus \mathfrak{a}^*[1])
    \,.
  $$

* the [[differential]] is the sum 

  $$
    d_{W(\mathfrak{a})} = d_{CE(\mathfrak{a})} + \mathbf{d}
  $$

  of two degree +1 graded derivations, where $d_{CE(\mathfrak{a})}$ and $\mathbf{a}$ are defined on $\wedge^1 \mathfrak{a}^* \oplus \mathfrak{a}^*[1]$ as [above](#WeilForLInfinitityAlgebra) for $L_\infty$-algebras and on $A$ itself $d_{CE(\mathfrak{a})}$ vanishes and $\mathbf{d}$ acts as the universal derivation

  $$
    \mathbf{d}|_A = d_{\mathrm{dR}} : A \to \Omega^1(A)
    \,.
  $$

=--



## Properties 
  {#Properties}

### Free property
 {#FreeProperty}

The main point of the definition is that the differential restricted to the original (unshifted) generators is the original differential plus the shift:

$$
  d_{W(\mathfrak{a})} |_{\mathfrak{a}^*} = 
   d_{CE(\mathfrak{a})} + \mathbf{d}
  \,.
$$

By solving the condition $d_{W(\mathfrak{a})} \circ d_{W(\mathfrak{a})} = 0$ and using that $d_{CE(\mathfrak{a})} d_{CE(\mathfrak{a})} = 0$ this already fixes uniquely the differential $d_{W(\mathfrak{a})}$. To see this we only need to show that the value of $d_{W(\mathfrak{a})}(x)$ on a generator $x=\sigma(t) \in \mathfrak{a}^*[1]$ is completely determined by $d_{W(\mathfrak{a})}\vert_{\wedge^\bullet\mathfrak{a}^*}$. One computes:

$$
  \begin{aligned}
    0 & =
    d_{W(\mathfrak{a})}(d_{W(\mathfrak{a})} t)
    \\
    & = 
    d_{W(\mathfrak{a})}(d_{CE(\mathfrak{a})}t + \sigma t)
    \\
    & = \sigma d_{CE(\mathfrak{a})} t + d_{W(\mathfrak{a}) } x
  \end{aligned}
$$

and hence

$$
  d_{W(\mathfrak{a})} x = - \sigma d_{CE(\mathfrak{a})} \sigma^{-1} (x)
  \,.
$$

This implies the following universal [[free functor|freeness property]]:

+-- {: .num_prop}
###### Proposition

Let $\mathfrak{g}$ be an $L_\infty$-algebra. Morphisms of $dg$-algebras $W(\mathfrak{g}) \to A$ are in natural bijection to morphisms of [[graded vector space]]s $\mathfrak{g}^* \to A$.

=--

+-- {: .proof}
###### Proof

Forgetting the differential, $W(\mathfrak{g})$ is the free graded-commutative algebra generated by (a shifted copy of) $\mathfrak{g}^*$ and $\mathfrak{g}^*[1]$. Therefore,
$$
Hom_{dgca}(W(\mathfrak{g}),A)\subseteq Hom_{gca}(W(\mathfrak{g}),A)=Hom_{grVect}(\mathfrak{g}^*,A)\oplus Hom_{grVect}( \mathfrak{g}^*[1],A).
$$
Projecting down to $Hom_{grVect}(\mathfrak{g}^*,A)$, one obtains a natural map
$$
Hom_{dgca}(W(\mathfrak{g}),A)\to Hom_{grVect}(\mathfrak{g}^*,A),
$$
which is a bijection. 

To prove injectivity, we just have to show that the restriction of a dgca morphism $f:W(\mathfrak{g})\to A$ to $\mathfrak{g}^*$ determines the restriction of $f$ to $\mathfrak{g}^*[1]$. One has, for any $x=\sigma(t)\in \mathfrak{g}^*[1]$,
$$
\begin{aligned}
f(x)&=f(\sigma(t))=f(d_{W(\mathfrak{g})}t-d_{CE(\mathfrak{g})}t)\\
&=d_A f(t)- f(d_{CE(\mathfrak{g})}t).
\end{aligned}
$$
Since $d_{CE(\mathfrak{g})}(t)$ lies in the sub-gca of $W(\mathfrak{g})$ generated by $\mathfrak{g}^*$, the element $f(d_{CE(\mathfrak{g})}(t))$, and therefore $f(x)$, is determined by $f\vert_{\mathfrak{g}^*}$. 

Next we show surjectivity, i.e. that every morphism of graded vector spaces $\phi:\mathfrak{g}^*\to A$ can be extended to a dgca morphism $f:W(\mathfrak{g})\to A$. Denote by $f_0: \wedge^\bullet \mathfrak{g}^*\to A$ the extension of $\phi$ to a graded commutative algebra morphism, and let $\psi:\mathfrak{g}^*[1]\to A$ be the graded vector space morphism defined by
$$
\psi(x)=d_A \phi(t)-f_0d_{CE(\mathfrak{g})}(t),
$$
for any $x=\sigma(t)\in \mathfrak{g}^*[1]$.
The graded vector space morphism $\phi+\psi:\mathfrak{g}^*\oplus\mathfrak{g}^*[1]\to A$ extends to a commutative graded algebra $f:W(\mathfrak{g})\to A$, whose restriction to $\mathfrak{g}^*$ is $\phi$. We want to show that $f$ is actually a dgca morphism. We only need to test commutativity with the differentials on generators $t\in \mathfrak{g}^*$ and $x=\sigma(t)\in \mathfrak{g}^*[1]$. We have
$$
d_A f(t)=d_A\phi(t)=\psi(\sigma(t))+f_0d_{CE(\mathfrak{g})}(t)=f(\sigma(t))+
f d_{CE(\mathfrak{g})}(t)=f d_{W(\mathfrak{g})}(t),
$$
which in particular implies that $d_A f\vert_{\wedge^\bullet \mathfrak{g}^*}=f d_{W(\mathfrak{g})}\vert_{\wedge^\bullet \mathfrak{g}^*}$,
and
$$
d_A f(x)= d_A \psi(x) = -d_A f_0d_{CE(\mathfrak{g})}(t)=-d_A f (d_{CE(\mathfrak{g})}(t)).
$$
Since $d_{CE(\mathfrak{g})}(t)\in \wedge^\bullet \mathfrak{g}^*$, we obtain
$$
d_A f(x)= -f d_{W(\mathfrak{g})} (d_{CE(\mathfrak{g})}(t))=
-f d_{W(\mathfrak{g})}(d_{W(\mathfrak{g})}(t)-x)=f d_{W(\mathfrak{g})}(x).
$$

=--

+-- {: .num_example}
###### Example

For $A=CE(\mathfrak{g})$ the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$, the inclusion $\mathfrak{g}^*\hookrightarrow CE(\mathfrak{g})$ induces a canonical surjective dgca morphism $W(\mathfrak{g})\to CE(\mathfrak{g})$. This is the identity on the unshifted generators, and 0 on the shifted generators.

=--


+-- {: .num_example}
###### Example


For $A = \Omega^\bullet(X)$ the [[de Rham complex]] of a [[smooth manifold]] $X$, we have that 

$$
  Hom_{dgAlg}(W(\mathfrak{g}), \Omega^\bullet(X))
  = 
  (\Omega^\bullet(X) \otimes \mathfrak{g})^1
$$

is the collection of total degree 1 [[differential form]]s with values in the $\infty$-Lie algebra $\mathfrak{g}$.

A morphism of 

$$
  (A, F_A) : W(\mathfrak{g}) \to \Omega^\bullet(X)
$$

sends the unshifted generators $t^a$ to differential forms $A^a$, which one thinks of as local connection forms, and sends the shifted generators $\sigma t^a$ to their [[curvature]]. The respect for the differential on the shifted generators is the [[Bianchi identity]] on these curvatures.

A morphism $W(\mathfrak{g}) \to \Omega^\bullet(X)$ encodes a collection of _flat_ $L_\infty$-algebra valued forms precisely if it factors by the canonical morphism $W(\mathfrak{g}) \to CE(\mathfrak{g})$ from above through the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$.

=--

The freeness property of the Weil algebra can be made more explicit by exhibiting a concrete [[isomorphism]] to the free dg-algebra on $\mathfrak{g}^*$.

+-- {: .num_defn}
###### Definition

The _canonical free dg-algebra_ on $\mathfrak{g}^*$ is

$$
  F(\mathfrak{g}) \coloneqq \wedge^\bullet( \mathfrak{g}^* \oplus \mathfrak{g}^*[1], d_F )
$$

where the differential $d_f$ is on the unshifted generators $t \in \mathfrak{g}^*$ the shift isomorphism $\sigma : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ extended as a derivation and vanishes on the shifted generators 

$$
  d_F : t \mapsto \sigma(t)
  \,,
$$

$$
  d_F : \sigma(t) \mapsto 0
  \,.
$$

=--

Or in other words, if $\bar \mathfrak{g}$ is the $\infty$-Lie algebra whose underlying graded vector space is that of $\mathfrak{g}$, but all whose brackets vanish, then 

$$
  F(\mathfrak{g}) = W(\bar \mathfrak{g})
  \,.
$$

Notice the evident

+-- {: .num_lemma}
###### Observation

The [[cochain cohomology]] of $F(\mathfrak{g})$ vanishes in positive degree.

=--


To see this, let $K \coloneqq \sigma^{-1} : F(\mathfrak{g}) \to F(\mathfrak{g})$ be the degree down-shift isomorphism $\mathfrak{g}^*[1] \to \mathfrak{g}^*$ extended as a graded derivation of degree -1, then 

$$
  [d_{F(\mathfrak{g})}, K] = Id : F(\mathfrak{g}) \to F(\mathfrak{g})
$$

and hence for any $\omega \in F(\mathfrak{g})$ such that $d_{F(\mathfrak{g})} \omega = 0$ we have $\omega = d_{F(\mathfrak{g})} K \omega$.



+-- {: .num_prop}
###### Lemma


Given $\mathfrak{g}$, there is an [[isomorphism]] of [[dg-algebra]]s 

$$
  f : F(\mathfrak{g}) \to W(\mathfrak{g})
$$

given by

$$
  f : t \mapsto t
$$

$$
  f : \sigma(t) \mapsto d_{W(\mathfrak{g})}  t  = d_{CE(\mathfrak{g})} t + \sigma(t)
  \,.
$$

=--


+-- {: .proof}
###### Proof

It is clear that $f$ is a dg-algebra homomorphism. The inverse dg-algebra morphism is given on generators by

$$
  f^{-1} : t \mapsto t
$$

$$
  f^{-1} : \sigma(t) \mapsto \sigma(t) - d_{CE(\mathfrak{g})}(t)
  \,.
$$
Note that the isomorphism $f$ is precisely the dgca isomorphism induced between $W(\overline\mathfrak{g})$ and  $W(\mathfrak{g})$ by the identity of $\mathfrak{g}^*$ as a graded vector spaces morphism $\overline{\mathfrak{g}}^*\to\mathfrak{g}^*$.
=--



+-- {: .nun_cor}
###### Corollary


The [[cochain cohomology]] of the Weil algebra of an $L_\infty$-algebra is trivial.

=--

+-- {: .num_remark}
###### Remark


This means that [[homotopy theory|homotopy-theoretically]] the Weil algebra is the point. Dually, the $\infty$-Lie algebra $inn(\mathfrak{g})$ is a model for the point. In fact, one can see that $inn(\mathfrak{g})$ is the [[universal principal ∞-bundle]] over $\mathfrak{g}$ in the canonical [[model category|model]] for the [[(∞,1)-topos]] [[SynthDiff∞Grpd]]. In fact, it is a [[groupal model for universal principal ∞-bundles]]. This is discussed at [[∞-Lie algebra cohomology]].

=--

### Characterization in the smooth $\infty$-topos
 {#CharacterizationInSmoothTopos}

The Weil algebra of a Lie algebra is naturally identified with the
de Rham algebra of differential forms on the "universal $G$-principal bundle with connection" in its stacky incarnation ([Freed-Hopkins 13](#FreedHopkins13)):

Write $\mathbf{B}G_{conn}\simeq \mathbf{\Omega}(-,\mathfrak{g})//G$ for the universal [[moduli stack]] of $G$-[[principal connections]] (as discussed there), a [[smooth groupoid]]. The quotient projection may be regarded as the universal $G$-connection:

$$
  \array{
     && \mathbf{\Omega}_{flat}(-,\mathfrak{g})
     \\
     && \downarrow
     \\
     \mathbf{E}G_{conn} &\coloneqq & \mathbf{\Omega}(-,\mathfrak{g}) 
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}G_{conn} &\coloneqq &\mathbf{\Omega}(-,\mathfrak{g})//G
  }
$$

(After forgetting the connection/form data this is just the [[universal principal bundle]] $\mathbf{E}G \to \mathbf{B}G$)

The differential $k$-forms on a [[smooth groupoid]] $X$ are just homs $X \to \mathbf{\Omega}^k(-)$ into the sheaf of $k$-forms. (See at [[geometry of physics -- differential forms]]). These $\Omega^k(X)$ inherit the de Rham differential and hence form the de Rham complex of the stack. (Notice that this is very different from the hom of $X$ into a shift of the full de Rham complex regarded as a sheaf of complexes. The latter is instead a model for the real [[ordinary cohomology]] of $X$, see at _[[smooth infinity-groupoid -- structures]]_ for more on this).

{#FreedHopkinsResult} One finds ([Freed-Hopkins 13](#FreedHopkins13)) that the de Rham complex, in this sense, of $\mathbf{E}G_{conn}$ is the Weil algebra:

$$
  \Omega^\bullet(\mathbf{E}G_{conn})
  \coloneqq
  \Omega^\bullet( \mathbf{\Omega}(-,\mathfrak{g}) )
  \simeq 
  W(\mathfrak{g})
  \,.
$$


[[!include Weil algebra abstractly -- table]]

Turning this around, this motivates to algebraically _define_ the [[connection on a principal ∞-bundle]], [via Lie integration](connection+on+a+smooth+principal+infinity-bundle#ByLieIntegration), as discussed there.

### Relation to Cartan model for equivariant de Rham cohomology

The Weil algebra may be identified with the 
[[Cartan model]] for [[equivariant de Rham cohomology]] for the special 
case of the Lie group $G$ acting on itself by right multiplication. Concersely, the [[Cartan models]] form a generalization of the Weil algebra. See at _[equivariant de Rham cohomology -- Cartan model](equivariant+de+Rham+cohomology#TheCartanModel)_ for more.

## As the CE-algebra of the $L_\infty$-algebra of inner derivations {#AsInnerDer}

By the discussion at [[∞-Lie algebra]] and [[Chevalley-Eilenberg algebra]], we may _identify_ the [[full subcategory]] of the [[opposite category]] [[dgAlg]] on commutative [[semi-free dga]]s in non-negative degree with that of [[∞-Lie algebra]]s/[[∞-Lie algebroid]]s.

That means that the Weil algebra $W(\mathfrak{g})$ of some [[L-∞ algebra]] $\mathfrak{g}$ is the Chevalley-Eilenberg algebra of _another_ $\infty$-Lie algebra. 

+-- {: .num_defn}
###### Definition

For any $\infty$-Lie algebra $\mathfrak{g}$ write $inn(\mathfrak{g})$ for the $\infty$-Lie algebra whose CE-algebra is $W(\mathfrak{g})$:

$$
  CE(inn(\mathfrak{g})) 
  \coloneqq 
  W(\mathfrak{g})
  \,.
$$

=--

In the following we discuss these _inner automorphism $\infty$-Lie algebras_ in more detail. (See section 6 of ([SSSI](#SSSI))).

### For an ordinary Lie algebra


+-- {: .num_lemma}
###### Observation

For $\mathfrak{g}$ an ordinary [[Lie algebra]] the [[inner derivation Lie 2-algebra]] is the [[strict Lie 2-algebra]] given by the [[dg-Lie algebra]]

$$
  inn(\mathfrak{g}) = ( \mathfrak{g} \stackrel{d}{\to} \mathfrak{g}, [-,-])
$$

whose

* elements in degree -1 are the elements $x \in \mathfrak{g}$, thought of as inner degree-(-1) [[derivation]]s

  $\iota_x : CE(\mathfrak{g}) \to CE(\mathfrak{g})$

  given by contraction with $x$;

* elements in degree 0 are the derivations of degree 0 that are of the form

  $ \mathcal{L}_X 
    \coloneqq 
    [d_{CE(\mathfrak{g})}, \iota_x] 
    \colon 
    CE(\mathfrak{g}) \to CE(\mathfrak{g})$;

* the differential $d = [d_{CE}, -] : \mathfrak{g} \to \mathfrak{g}$ is the commutator of derivations with the differential $d_{CE(\mathfrak{g})}$;

* the bracket is the graded commutator of derivations.

=--

Equivalently this is identified with the [[differential crossed module]] $(\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g})$ with the action being the [[adjoint action]] of $\mathfrak{g}$ on itself.

One checks that for all $x, y \in \mathfrak{g}$ we have in $inn(\mathfrak{g})$ the brackets

* $[\iota_x, \iota_y] = 0$

* $[\mathcal{L}_x, \iota_y] = \iota_{[x,y]}$

* $[\mathcal{L}_x, \mathcal{L}_y] = \mathcal{L}_{[x,y]}$

and of course

* $ \mathcal{L}_x = [d, \iota_x] $.

These identities are known as [[Cartan calculus]]. In this context $\mathcal{L}_x$ is called a [[Lie derivative]].

In this sense one may understand $inn(\mathfrak{g})$ for general $\infty$-Lie algebras $\mathfrak{g}$ as providing an $\infty$-version of [[Cartan calculus]].


## Relation to other concepts

### $\infty$-Lie algebra valued differential forms {#LieAlgValuedForms}

For $\mathfrak{g}$ an [[∞-Lie algebra]],  $X$ a [[smooth manifold]], an 
[[∞-Lie algebra valued differential form]] is a morphism

$$
  \Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : A
$$

of [[dg-algebra]]s, from the Weil algebra into the [[de Rham complex]] of $X$.

The image of the unshifted generators $A : \wedge^1 \mathfrak{g}^* \to \Omega^\bullet(X)$ are the forms themselves, the image of the shifted generators $F_A : \wedge^1 \mathfrak{g}^*[1]$ are the corresponding [[curvature]]s. The respect for the differential on the shifted generators are the [[Bianchi identity]] on the curvatures.

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
  \,.
$$


### Invariant polynomials and Chern-Simons elements

A [[cocycle]] in the [[∞-Lie algebra cohomology]] of the [[∞-Lie algebra]] $\mathfrak{g}$ is a closed element in the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$.

An [[invariant polynomial]] $\langle -\rangle$ on $\mathfrak{g}$ is a closed element in the Weil algebra $\langle -\rangle \in W(\mathfrak{g})$, subject to the additional condition that it its entirely in the shifted copy of $\mathfrak{g}$, $\langle - \rangle \in \wedge^\bullet (\mathfrak{g}^*[1])$.

$$
  \langle -\rangle  \in \wedge^\bullet( \mathfrak{g}^*[1] )
$$


$$
  d_{W(\mathfrak{g})} \langle -\rangle = 0
  \,.
$$

For $x \in \mathfrak{g}$ an element of the $\infty$-Lie algebra, let

$$
  \iota_x : W(\mathfrak{g}) \to W(\mathfrak{g})
$$

the evident operation of contraction with $x$

$$
  \iota_x : t \mapsto t(x)
$$

$$
  \iota_x : \sigma(t) \mapsto 0
$$

extended as a graded derivation. Then the [[Lie derivative]]

$$
  \mathcal{L}_x 
   \coloneqq ad_x 
   \coloneqq 
   [d_{W(\mathfrak{g})}, \iota_x] 
   \colon 
   W(\mathfrak{g}) \to W(\mathfrak{g})
$$

encodes the coadjoint action of $\mathfrak{g}$ on $\mathfrak{g}^*$. By the above definition of an [[invariant polynomial]] $\langle - \rangle$, we have 

$$
  \iota_x \langle - \rangle = 0
$$

and

$$
  d_{W(\mathfrak{g})} \langle - \rangle = 0
$$

and hence

$$
  ad_x \langle -\rangle  = 0
  \,.
$$

Since the cohomology of $W(\mathfrak{g})$ is trivial, there is necessarily for each invariant polynomial an element $cs_{\langle -\rangle}$ such that

$$
  d_{W(\mathfrak{g})} cs_{\langle -\rangle} = 
  \langle -\rangle
  \,.
$$

This is the [[Chern-Simons element]] of the invariant polynomial. Notice, crucially, that this is ingeneral _not_ restricted to the shifted part $\wedge^\bullet (\mathfrak{g}^*[1])$ Its restriction

$$
  \mu_{\langle -\rangle} 
  \coloneqq 
  cs_{\langle - \rangle}|_{\wedge^\bullet \mathfrak{g}^*}
$$

to the unshifted copy, hence to the [[Chevalley-Eilenberg algebra]], is the cocycle that is in transgression with $\langle - \rangle$.

For 

$$
  (A,F_A) \colon W(\mathfrak{g}) \to \Omega^\bullet(X)
$$

a collection of $\mathfrak{g}$-valued differential forms (as [above](LieAlgValuedForms)) and $\langle -\rangle  : CE(b^{n-1}\mathbb{R}) \to W(\mathfrak{g})$ an [[invariant polynomial]], the composite

$$
  \langle F_A\rangle
  :
  CE(b^{n-1}\mathbb{R})
  \stackrel{\langle - \rangle}{\to}
  W(\mathfrak{g})
  \stackrel{(A,F_A)}{\to}
  \Omega^\bullet(X)
$$

is the corresponding [[curvature characteristic form]], a closed $n$-form on $X$. For $(\langle - \rangle, cs) : W(b^{n-1}) \to W(\mathfrak{g})$ the corresponding [[Chern-Simons element]] we have that $cs(A,F_A)$ is the corresponding [[Chern-Simons form]] on $X$.


## Examples

### Weil algebra of a Lie algebra {#WeilofLieAlg}

Let $\mathfrak{g}$ be a finite dimensional [[Lie algebra]]. This Lie algebra regarded as a [[Lie algebroid]] has as base manifold the point, $X_0 = pt$. Its algebra of functions is accordingly the ground field, and the algebra $\wedge^\bullet_{C^\infty(X_0)} \mathfrak{g}^*$ is just a [[Grassmann algebra]].

The [[Chevalley-Eilenberg algebra]] is

$$
  CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{g}^*, d_{\mathfrak{g}})
  \,,
$$

where the differential acts on the elements of $\mathfrak{g}^*$ in degree 1 by the linear dual of the Lie bracket.

$$
  d \mathfrak{g}|_{\mathfrak{g}^*} = [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^*
  \,.
$$

The corresponding Weil algebra is obtained by adding another copy of $\mathfrak{g}^*$ in degree 2

$$
  W(\mathfrak{g}) = (\wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1]), d_{W(\mathfrak{g})})
$$

where with $\sigma : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ the degree shift isomorphism, the differential acts as

$$
  d_{W(\mathfrak{g})}|_{\mathfrak{g}^*}
  : 
  [-,-]^* + \sigma
$$

$$
  d_{W(\mathfrak{g})}|_{\mathfrak{g}^*[1]}
  : 
  \sigma \circ d_{CE(\mathfrak{g})} \circ \sigma^{-1}
  \,.
$$

For illustration, we spell this out in a basis.

Let $\{t_a\}_a$ be a basis for the underlying vector space of $\mathfrak{g}$ and let $\{C^a{}_{b c}\}$ be the corresponding structure constants of the Lie bracket

$$
  [t_b, t_c] = C^a{}_{b c} t_a 
  \,.
$$

Then the Chevalley-Eilenberg algebra is generated on generators $\{t^a\}$ of degree 1, on which the differential acts as

$$
  d_{CE(\mathfrak{g})} : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,.
$$

The Weil algebra in turn is generated from these generators $\{t^a\}$ in degree 1 and generators $\{r^a\}$ in degree 2, with differential given by

$$
  d_{W(\mathfrak{g})} : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a
$$

$$
  d_{W(\mathfrak{g})} : r^a \mapsto C^a{}_{b c} t^b \wedge r^c 
  \,.
$$

### Weil algebra of a 0-Lie algebroid



A 0-[[truncated]] Lie algebroid is one for which the chain complex of modules over the $T$-algebra in degree 0 vanishes:

$$
  CE(\mathfrak{a}) = (\wedge^\bullet_A (\mathfrak{a}^*), d_{CE(\mathfrak{a})})
  = (A, d = 0)
  \,.
$$

For instance for $T$=[[CartSp]] the theory of [[smooth algebra]]s, any [[smooth manifold]] $X$ regarded as an 
[[L-∞ algebroid]] is a 0-Lie algebroid with $CE(X) = C^\infty(X)$ the [[smooth algebra]] of [[smooth function]]s on $X$.


+-- {: .num_prop}
###### Observation

The Weil algebra of a 0-Lie algebroid $X$ is the [[Kähler differential|Kähler]] [[de Rham complex]] of $A = CE(X)$:

$$
  W(\mathfrak{a}) = 
  (\Omega^\bullet(A), d_{dR})
  \,.
$$

=--

This Weil algebra is the Chevalley-Eilenberg algebra of the
[[tangent Lie algebroid]] $T X$ of $X$, which is the [[de Rham algebra]]
$\Omega^\bullet(X)$ of $X$:

$$
  W(X) = CE(T X) = (\Omega^\bullet(X), d_{dR})
  \,.
$$


## Related concepts

* [[∞-Lie algebra cohomology]]

* [[Chevalley-Eilenberg algebra]]

* **Weil algebra**

* [[invariant polynomial]]

* [[Sullivan model of free loop space]]


## References

Among the original references on Weil algebras for ordinary Lie algebras is 

* [[Henri Cartan]], _Cohomologie r&#233;elle d'un espace fibr&#233; principal diffrentielle_ I, II, S&#233;minaire Henri Cartan,
1949/50, pp. 19-01 &#8211; 19-10 and 20-01 &#8211; 20-11, CBRM, (1950).

and

* {#Cartan50} [[Henri Cartan]], *Notions d'alg&#233;bre diff&#233;rentielle; application aux groupes de Lie et aux vari&#233;t&#233;s ou op&#232;re un groupe de Lie* , Colloque de topologie (espaces fibrs), Bruxelles, (1950), pp. 15&#8211;27.


This also explains the use of the Weil algebra in the calculation of the [[equivariant cohomology|equivariant]] [[de Rham cohomology]] of manifolds acted on by a compact group. These papers are reprinted, explained and put in a modern context in the book

In monographs: 

* {#GHV} [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], chapter VI, vol III of:  _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)
 

Some remarks on the notation there as compared to ours: our $d_W$ is their $\delta_W$ on p. 226 (vol III). Their $\delta_E$ is our $d_{CE}$. Their $\delta_\theta$ is our $d_\rho$ ($\theta$/$\rho$ denoting the representation)..

In the context of [[equivariant de Rham cohomology]]:

* {#AtiyahBott84} [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology 23, 1 (1984) (<a href="https://doi.org/10.1016/0040-9383(84)90021-1">doi:10.1016/0040-9383(84)90021-1</a>, [pdf](https://www.math.stonybrook.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))

* {#Kalkman93} [[Jaap Kalkman]], _BRST model applied to symplectic geometry_, Ph.D. Thesis, Utrecht, 1993 ([arXiv:hep-th/9308132](https://arxiv.org/abs/hep-th/9308132), [cds:9308132](http://cds.cern.ch/record/568522), [euclid:1104252784](http://projecteuclid.org/euclid.cmp/1104252784))

and with an eye towards [[supersymmetry]]:

* {#Miettinen96} Mauri Miettinen, _Weil Algebras and Supersymmetry_ ([arXiv:hep-th/9612209](https://arxiv.org/abs/hep-th/9612209), [cds:317377](http://cds.cern.ch/record/317377), [spire:427720](http://inspirehep.net/record/427720))

* {#GuilleminSternberg99} [[Victor Guillemin]], [[Shlomo Sternberg]], _Supersymmetry and equivariant de Rham theory_, Springer, (1999) ([doi:10.1007/978-3-662-03992-2](https://link.springer.com/book/10.1007/978-3-662-03992-2))

The (obvious but conceptually important) observation that [[Lie algebra-valued 1-forms]] regarded as morphisms of graded vector spaces $\Omega^\bullet(X) \leftarrow \wedge^1 \mathfrak{g}^* : A$ are equivalently morphisms of dg-algebras out of the Weil algebra $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : A$ and that one may think of as the identity $W(\mathfrak{g}) \leftarrow W(\mathfrak{g}) : Id$ as the _universal $\mathfrak{g}$-connection_ appears in early articles for instance highlighted on p. 15 of

* Franz W. Kamber; Philippe Tondeur, _Semisimplicial Weil algebras and characteristic classes for foliated bundles in Cech cohomology_ , Differential geometry (Proc. Sympos. Pure Math., Vol. XXVII, Stanford Univ., Stanford, Calif., 1973), Part 1, pp. 283--294. Amer. Math. Soc., Providence, R.I., (1975). 


A survey of Weil algebras for Lie algebras is also available at

* [[eom|Encyclopedia of Mathematics]]: [Weil algebra of a Lie algebra](http://eom.springer.de/W/w130050.htm)

Weil algebra for [[L-infinity algebra]]s and their role in defining [[invariant polynomial]]s and [[Chern-Simons element]]s on $\infty$-Lie algebras from [[infinity-Lie algebra cohomology|L-infinity algebra cocycle]] are considered in

* {#SSSI} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], *[[schreiber:L-infinity algebra connections|$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport]]*, in *Quantum Field Theory*, Birkhäuser (2009) 303-424 &lbrack;[arXiv:0801.3480](https://arxiv.org/abs/0801.3480), [doi:10.1007/978-3-7643-8736-5_17](https://doi.org/10.1007/978-3-7643-8736-5_17)&rbrack;

The abstract characterization is due to

* {#FreedHopkins13} [[Daniel Freed]], [[Michael Hopkins]], _Chern-Weil forms and abstract homotopy theory_, Bull. Amer. Math. Soc. 50 (2013), 431-468 ([arXiv:1301.5959](http://arxiv.org/abs/1301.5959))

Further discussion of Weil algebras for the [[string Lie 2-algebra]]:

* {#Schmidt19} [[Lennart Schmidt]], _Twisted Weil Algebras for the String Lie 2-Algebra_, in [[Christian Saemann]], [[Urs Schreiber]], [[Martin Wolf]] (eds.) _[Higher Structures in M-Theory](http://www.maths.dur.ac.uk/lms/109/index.html)_, [Durham Symposium](http://www.maths.dur.ac.uk/lms/) 2018, Fortschritte der Physik 2019 ([arXiv:1903.02873](https://arxiv.org/abs/1903.02873))


[[!redirects Weil algebras]]